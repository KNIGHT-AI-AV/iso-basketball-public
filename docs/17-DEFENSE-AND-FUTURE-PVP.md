# Playable defense and future one-on-one PvP

## Confirmed direction

The player can defend as well as attack. Keep the same court-facing camera direction; do not flip or rotate behind the defender when control changes. Use hold/drag movement and directional swipe actions, including an upward swipe/hold for a block attempt. Defensive ability and physical commitment affect whether the defender gets beaten or loses balance. Human and computer-controlled players should follow the same basketball constraints.

Live one-on-one isolation PvP is an intended future mode. Its architecture, launch timing, provider, and budget are not selected. The present work remains research and documentation only.

## Camera and directional language

The basket remains toward the upper part of the main screen in both roles. On defense, the controlled defender is usually between the nearer attacker and the basket, facing the ball handler. Keep both full bodies visible where the existing camera permits. Mark the controlled player with a restrained ground indicator and a role label when the possession starts.

Do not label screen-down as "toward the basket" in this fixed camera if the basket is screen-up. The owner's examples establish a desired family of gestures, not a calibrated direction map. Recommended movement is screen-relative: dragging toward the visible basket moves toward it, and dragging toward the attacker closes space. The character automatically faces the ball; moving backward in the defender's body coordinates may therefore be screen-up. Final arrows must be checked on the storyboard.

No camera flip is necessary to play both roles. A cinematic finishing cut is separate from a role flip, but it must preserve the defender's active input and visible chance to contest. For the first defensive control evaluation, use wide throughout; test an optional finishing cut only after proving that it does not hide a block cue.

## Proposed small defensive vocabulary

| Input | Intent | Constraint |
|---|---|---|
| Touch, hold, and drag within the movement area | Slide, close space, retreat, or move diagonally while facing ball | Bounded acceleration and braking; not a dash every frame |
| Short committed left/right swipe | Quick lateral recovery step | Real plant and stamina cost; cannot instantly reverse repeatedly |
| Backward diagonal movement | Drop-step recovery toward rim protection | Screen direction and body-relative movement are distinct |
| Upward swipe then hold in a block region | Begin one timed jump contest; maintain hand extension through that jump | Holding never suspends the character in the air or repeatedly jumps |
| Release block hold | Complete the current legal contest and recovery | Does not cancel gravity or erase the commitment |
| Optional dedicated reach action | Try to steal an exposed ball | Later addition; missed reach gives attacker an opening |

The exact block region is a proposal, chosen to avoid confusing upward movement with upward blocking. Compare a compact visible block target with a stationary-start gesture mode. A moving touch must not become a block simply because its path points up. Reserve touch ownership at initiation and require a fresh action after landing before another jump.

One-thumb use can accept that a committed block temporarily ends manual sliding while momentum continues. A compact two-thumb layout can permit simultaneous positioning and contest preparation. Do not claim these layouts are equivalent before testing. The owner has chosen portrait, not a thumb count.

Passive close positioning can apply an ordinary hand-up contest. A jump block is the higher-commitment response. Early jumps can be beaten by a pump fake; late jumps may miss the release. Actual reach and ball contact determine a block, not a successful animation request alone.

## Ankle breaks and recovery

Track defensive velocity, facing, support foot, chosen movement, distance to the attacker, stamina, and the attacker's committed change of direction. A defender leaning or accelerating one way must take time to brake and push the other way. Greater mismatch can produce an overstep, stumble, or rare fall if the physical state warrants it.

Defensive upgrades improve recovery tolerance and contest control; Footwork governs movement/braking and Stamina limits repeated explosive responses. Attacking skill helps execute a convincing and controlled move, but no rating should automatically force an otherwise well-positioned human defender to fall.

Use graded outcomes: slight wrong step → lost half-step → crossed feet → stumble → exceptional full fall. The reaction should follow visible cause, and control should return at a defined recovery point. Avoid long helpless cutscenes. The computer cannot inspect an unfinished swipe or read future input; the human is not punished by a hidden scripted loss.

## Offline scope first

Add Defense Practice against a small set of scripted attack patterns, then computer attack choices drawn from the same valid move graph. Offer alternating offense/defense possessions in a local AI duel. End each attempt on the existing result rules; reset to the same hoop between possessions rather than requiring a full-court camera transition.

This requires an attacking decision system as well as the existing defensive one. Reusing the same legal-action graph can reduce duplication, but the offense AI must still choose space, moves, shots, and passes plausibly. Defense is not complete merely because a player can slide a defender model.

## Future PvP scope

Begin with two human players, one ball, one basket, and alternating possessions. Keep team passing/return-lob play separate from strict one-on-one. A future team mode could add AI teammates, but it should be labeled differently and estimated separately.

Recommended initial online features: private invite, short match, explicit turn/possession ownership, readiness, disconnect/reconnect rules, result confirmation, and quick rematch. Public matchmaking/ranks, spectating, chat, tournaments, and larger teams can follow separately.

No per-player gameplay pause or slow motion during an online possession. Local camera preference may differ, but the authoritative clock and action deadlines cannot. Block, ball contact, shot release, and scoring need a common ordering independent of each display's refresh rate.

## Infrastructure and cost reasoning

Managed matchmaking/relay services offer entry-level usage allowances and usage-based plans. That makes small experiments possible without owning a large server fleet. Those services do not write or validate responsive basketball networking for us.

Evaluate a trusted authoritative match simulation for ranked competition, with local prediction and reconciliation where needed. Player-hosted or distributed-authority prototypes can have lower initial infrastructure requirements but create trust, host advantage, connection, and departure tradeoffs. A relay forwards data; it does not automatically make player-reported outcomes trustworthy. Provider topology recommendations vary and must be evaluated for this game's timing and anti-cheat requirements.

Do not select a networking library solely because it synchronizes positions in a tutorial. Test change-of-direction, steals, blocks, gathers, and late-clock releases under latency, jitter, loss, disconnects, and device throttling. Animation/physics rewinds need a concrete design; deterministic replay cannot be assumed from an ordinary physics engine.

Estimate operations from peak and average concurrent users, average match length, regional demand, bandwidth per player, server work per match, storage, monitoring, and support. Total downloads are not concurrent users. A small two-player test and a worldwide competitive service have different costs. Engineering and quality assurance may be larger early costs than hosting.

## Design decisions worth preserving now

Use explicit action states, stable event timestamps, clear ball authority, bounded transitions, and data-driven attributes in the future implementation. These help both local correctness and later networking. Do not build servers now or claim that multiplayer can simply be attached at the end without revisiting timing and authority.

Competitive paid-stat treatment remains unresolved. If premium currency can accelerate upgrades, normalized PvP ratings are recommended; cosmetic outfits should never alter hitboxes or timing opportunities invisibly.
