# Shooting, upgrades, and haptics

## Skill check

Owner direction: a readable timed check with failed, okay, and perfect regions. The basketball work before the shot changes its difficulty. Use an original interface and visual identity.

Proposal: a compact sweep meter near the lower-center control area, clear of the player's body. A moving indicator enters a broad okay zone containing a smaller perfect zone. Start with a predictable direction and speed. Differentiate zones with shape/labels as well as color. Show early, late, okay, or perfect after evaluation.

The first Shot tap commits shot intent and starts the gather. A second tap evaluates the sweep. Do not add an unrelated swiping requirement to a basic jumper. An alternative hold-and-release mapping can be compared later; it is not the owner-confirmed default.

## What changes the window

| Factor | Intended effect | Guardrail |
|---|---|---|
| Shot upgrade | Modestly increases comfortable range and timing tolerance | No guaranteed basket through an actual block |
| Defender separation | Reduces shot pressure when sufficient space was created | Distance and recovery reach matter, not a hidden combo multiplier |
| Defender imbalance | Slows recovery or contest through visible physical state | Does not magically improve the shooter's own balance |
| Shooter balance | Stable feet improve tolerance; awkward stops reduce it | Readable gather/lean shows the cost |
| Stamina | Low reserve narrows tolerance and limits explosive actions | No purchasable in-possession rescue required |
| Range and shot type | Beyond comfortable range or difficult stepbacks are less forgiving | Display expectations before committing where possible |
| Late defense | May physically block or alter an exposed release | Do not secretly move the perfect zone after the input |

Compute a preview during setup, then freeze timing-zone geometry when the active sweep starts. Continue simulating defense: a later hand on the ball can still block a perfectly timed release. This separates a stable input test from an ongoing basketball contest. A label such as "Perfect timing — blocked" is more truthful than promising every perfect tap scores.

The release error determines an assisted shot trajectory together with distance, balance, and contest. Do not roll an unexplained second random miss after advertising an uncontested perfect release. If randomness is later introduced, describe and evaluate it openly. Outcome selection and ball flight must agree visually.

Illustrative starting windows for a basic jumper, measured as total input duration within each zone:

| Situation | Okay zone including perfect | Perfect zone |
|---|---:|---:|
| Open, balanced, comfortable range | 240 ms | 80 ms |
| Mild contest or imperfect stop | 180 ms | 50 ms |
| Heavy pressure or low stamina | 120 ms | 30 ms |

These are invented tuning examples, not measured values or commitments. They must be assessed against phone input latency and motor accessibility. Do not stack every penalty without a floor. Offer an appropriately labeled timing-assistance setting in noncompetitive play.

## Dunk and alley-oop checks

A valid finish first needs a viable approach, reachable ball/rim, legal gather, sufficient lift, and usable space. Finishing stats affect available attempts and execution tolerance. A high rating does not teleport a missed lob into the hand.

Use the finish stroke to choose an eligible style. Evaluate its completion or release against a visible timing band. That is the dunk skill check; avoid an additional independent tap unless playtests justify it. For an alley-oop, show the same check during the catch-to-finish sequence, with advance cueing during ball flight. One finish check covers that sequence.

Passing accuracy affects lob placement. The receiver's finishing, stamina, approach, and defensive pressure affect the catch/finish envelope. Okay can produce a plain safe finish; perfect can produce the selected clean finish when feasible; fail can produce a bobble, missed connection, or miss matched to the actual failure. Never award an impossible basket just to complete the cinematic.

A fresh airborne tap can switch a selected dunk toward a feasible layup. The change of intent must not reset the clock or erase a failed timing result. Whether the tap itself evaluates layup timing remains open; do not silently introduce an extra skill prompt. See document 20.

Cinematic and wide settings share timing windows, touch ownership, defensive interaction, and results. Default proposal is real-time gameplay. Optional slow motion needs a separate decision and must not quietly extend the shot clock or grant one camera setting easier inputs.

## Seven upgrade categories

| Player-facing category | Internal effects to tune | What it does not buy |
|---|---|---|
| Handle | Dribble speed, ball protection, demanding transition tolerance, weak-hand control | Automatic defender stumbles |
| Shot | Timing tolerance and comfortable shooting range | Immunity to blocks |
| Finish | Reachable finishing repertoire, catch/touch tolerance, controlled contact finishes | Impossible takeoffs |
| Footwork | First step, braking, lateral control, balance recovery | Instant direction changes without momentum |
| Stamina | Capacity and recovery between explosive actions | A compulsory energy timer that prevents play |
| Passing | Delivery consistency and usable lob envelope | Passes through bodies |
| Defense | Controlled contests, reach execution, recovery tolerance after commitment | Forced steals or automatic immunity to being beaten |

Proposal: a short level scale, initially ten steps per category, with diminishing improvements and a visible preview before spending Coins. This is simpler than exposing every internal rating. Teammates use the same screen and categories. Defense is the seventh category added for playable defense. It works with Footwork and Stamina rather than duplicating all movement upgrades. Computer discipline parameters remain internal.

Stamina drains mainly from explosive attacks, repeated hard changes, contact, and jumps. Patient dribbling and short pauses offer partial recovery; a new possession restores a defined amount. Reaching low stamina reduces explosive options rather than disabling the entire game. Communicate fatigue through a meter and believable body response.

## Stat-driven dribble speed

Owner direction: dribble speed depends on a stat. Recommended simple presentation is a visible sub-effect of Handle rather than a separate eighth upgrade category. Explain the benefit as faster controlled hand changes and better transition pace, while Footwork still governs travel acceleration and braking.

Each move needs a minimum/maximum believable duration, phase-specific timing, stamina cost, and a compatible exit. Apply the Handle effect within those bounds. Do not uniformly speed up a whole body clip until feet slide or a bounce skips the floor. Shorter dribble cycles may need adjusted ball paths and hand poses; ground contact, sound, and haptics must remain synchronized.

Faster handling changes how long the ball is exposed and when a defender can respond. Keep meaningful counterplay rather than giving maximum Handle instant moves. Skillful timing, choice, and spacing still matter. Fatigue can reduce the available pace smoothly without changing gesture recognition thresholds unpredictably.

Do not demand physically faster finger drawing simply because a character is upgraded. Recognition maps intended gestures; the action system executes them at the character's eligible pace. Buffer/branch rules must account for the new durations. Compare low/high Handle in the same scenario and inspect contacts, stamina per second, opponent recovery, and frame-rate independence.

Style cosmetics do not secretly modify these durations. Competitive normalization, if adopted, includes dribble speed as well as shooting and defense. In future online play the match authority validates duration from the match's ratings; the client cannot claim an instantaneous transfer.

The practice hub offers "Train" and "Upgrade" from the same simple character/teammate selection. Teammates can appear automatically in a short background practice scene. No required attendance, calendar, transport, or separate energy system is proposed.

## Haptic vocabulary

| Event | Proposed feel | Trigger |
|---|---|---|
| Routine dribble | Light, short pulse; reduced intensity for rapid bounces | Actual ball-floor contact event |
| Strong change of pace | Optional slightly firmer accent | Accepted plant/ball event, avoiding a duplicate pulse |
| Dunk | Short pronounced impact, followed by restrained landing pulse if useful | Rim/ball impact and actual landing |
| Lob catch | Light catch confirmation | Ball secured, not merely requested |
| Shot feedback | Distinct short confirmation | Evaluated result, not advance perfect-zone information |
| Error/denial | Small neutral cue plus visible feedback | Invalid action or expired opportunity |

Avoid constant heavy vibration and long rumbling for every move. Expose Off, Light, and Standard strength choices; respect device/system capabilities and interruptions. Phones without fine haptics receive visual/audio equivalents. Haptics cannot supply a secret early timing cue unavailable to players with vibration disabled.

Later testing must cover whether tactile bounce timing stays aligned under frame drops and whether repeated vibration becomes tiring. Researching the platform APIs does not verify the feel on a physical phone.
