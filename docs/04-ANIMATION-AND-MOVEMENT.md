# Animation, movement, ball control, and physics

## Design architecture

Treat movement as compatible action pieces: stance, setup, transfer, plant, exit, gather, finish, landing, recovery. Each piece has a purpose and a defined connection to the next. Style changes can alter silhouette and rhythm while retaining compatible contact points.

The complete game needs both authored character animation and responsive simulation. The simulation decides location, possession, contacts, timing, eligibility, and results. Animation makes those decisions visible. Avoid competing systems that each move the same player or ball independently.

## The action record

For each move, eventually define:

- Entry and exit ball hand; live dribble or gathered ball.
- Entry and exit speed, facing, body orientation, and balance.
- Support foot, foot plants, airborne intervals, and legal gather state.
- Intended displacement and permitted steering.
- Ball release, floor contact, hand contact, and catch markers.
- Commitment, branch, cancel, and recovery windows.
- Stamina cost and stat eligibility.
- Stat-driven dribble-speed range, phase-specific retiming bounds, and valid faster/slower transition contacts.
- Ball exposure and defender-contact opportunities.
- Collision response, blocked-path response, and out-of-bounds behavior.
- Sound and haptic event markers.
- Camera permissions; camera choices cannot alter gameplay data.
- Short, tall, left-handed, right-handed, and mirrored-quality requirements.

These fields are a production contract, not implemented software.

## Ball ownership

| Phase | Proposed authority | Reason |
|---|---|---|
| Controlled dribble | Authored ball path synchronized to hands and floor | Reliable visible contact and readable rhythm |
| Hand-to-hand transfer | Shared action timeline plus targeted hand correction | Avoid a ball teleport during blends |
| Gather / held ball | Defined hand attachment with bounded correction | Stable grip while the body plants |
| Pass / released shot | Ball-flight simulation | Genuine trajectory and interception/block opportunities |
| Dunk | Authored approach and hand path until release, with contact checks | Preserve ball-rim alignment without guaranteed success |
| Deflection / loose ball | Free ball simulation | Consistent bounces and recoveries |

Use one authoritative ball object. Transition between modes while preserving position and velocity. An animation event must not spawn a second ball. When interrupted, restore ownership explicitly.

## Locomotion and feet

Responsive normal movement should control acceleration, braking, turning, and collisions. Authored movement can supply the desired displacement for specific plants and gathers, but the movement controller must still constrain it to valid space. If the desired path is blocked, choose a compatible contact or recovery result rather than sliding through a defender.

Blend locomotion based on speed and direction. Use foot locking and limited hand/foot correction to remove small discrepancies. Large corrections hide a mismatched clip; replace the clip or transition rather than stretching limbs visibly. Mirror only where footwork and ball-hand semantics remain correct.

## Chain continuity

Transitions are a separate production workload. A crossover clip can look excellent alone and still fail when entered from a retreat with the wrong support foot. For each supported pair, verify foot contact, ball hand, speed, balance, and gesture responsiveness.

Prioritize branch points that preserve a live dribble. Once the ball is gathered, use shot, pivot, pass, or legal finish branches. Do not give every animation an unrestricted cancel.

## Defender and contact

The defender observes current and recent visible movement, ball exposure, distance, angle, and velocity. Their stance and commitment should appear before the attacker receives a clear advantage. A reversal against a committed defender can produce a hip turn, lost step, stumble, or rare fall according to physical context.

A dramatic fall is a reaction outcome, not a direct player command. The normal reward for a good move is usable space. Reach attempts, cutoffs, body bumps, recovery steps, trailing contests, vertical contests, deflections, and blocks all need animation coverage.

Evaluate contests with distance, angle, reach, hand position, and timing. Being nearby behind the shooter should not count exactly like a hand in the release path. Record why an attempt failed so the feedback can explain it.

## Gathers and finishes

Build gather and finish as separate compatible components, with explicit hand, foot, travel, and timing conditions. A side-step gather may branch to an outside-hand layup or a power finish only when reach and remaining motion allow it. A contact reaction can redirect or deny a finish without snapping to an unrelated pose.

Dunk coverage includes takeoff, ball extension, hand/rim contact, release, hang if permitted, landing, balance recovery, and miss/blocked alternatives. Alley-oops add a pass trajectory, catch window, airborne or grounded catch, hand acquisition, and failed-catch recovery. The camera does not supply these behaviors.

Airborne dunk-to-layup conversion is an explicit owner requirement. Build a pose-aware route graph with valid entry envelopes, finite transition durations, and reachable releases; document 20 defines the proposal. The catalogue's Euro-step and post actions are excluded research records.

Character motion also includes breathing, blinking, gaze, weight shifts, and original face variation. Garments need pose compression and responsive settling, with real cloth physics evaluated as necessary. Static wrinkle shading alone is insufficient. Document 19 defines the visual floor and fabric review cases.

## Shots and results

Choose an assisted-shot model for early design: direction aims at the intended basket, while timing quality, distance, balance, stamina, and contest influence release error. Then simulate the resulting flight and rim/backboard interactions. Do not play a visually clean shot through a blocked hand path because a timing score says perfect.

Alternatively, a more authored make/miss trajectory can improve consistency, but the team must choose one authoritative result system. Never let a make-probability roll and independent physics disagree about whether the basket counted.

Use robust swept collision or equivalent fast-ball handling, simple court colliders, and a clear scoring trigger requiring the ball to pass downward through the basket. Net simulation can be visual. Full cloth, deformable bodies, finger-level collisions, and unrestricted ragdolls are not prerequisites.

## Asset production

Create a consistent humanoid rig, body scale, hand poses, ball size, floor height, and basket scale. Capture or keyframe original performances. Record clean isolated moves and the important transitions, using the same performer and neutral entry/exit poses where practical.

Video-based motion capture may provide a body-motion draft; ball tracking, fingers, hand contact, foot plants, and occluded limbs still need deliberate review. Do not assume generated video is an exportable, reliable game animation. Never feed unlicensed footage into an animation-generation workflow merely because it was publicly watchable.

Approve each animation in isolation, in a chain, against contact, and from both camera settings. Preserve source files, performer permissions, asset licences, and export settings for our own production assets.

## Performance design targets

Target 120 frames per second on compatible iPhones and a stable 60-frame supported baseline, subject to sustained device testing. These are aspirations, not benchmarks. No lower-rate device tier is committed. Use timestamps rather than frame counts for player input, simulation events, and skill checks. See document 14 for visual scaling and thermal evaluation.

Start with a small visible cast, baked lighting where suitable, limited dynamic shadows, modest materials, pooled effects, and simple collision shapes. Measure input-to-visible-response separately from animation duration. Long locked animations can feel slow even at a high frame rate.
