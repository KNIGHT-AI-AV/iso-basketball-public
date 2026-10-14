# Airborne dunk-to-layup routing

## Owner direction and exclusions

**No Euro steps. No post offense.** The broad research catalogue retains excluded examples only as explicitly marked records. They are not playable commitments. Ordinary live-dribble spins, legal non-post pivots, stops, and stepbacks are not automatically excluded by this decision.

After choosing a dunk through directional hold or swipe, the player can make a fresh tap once airborne to switch into a layup. The transition must fit the current pose and ball position and lead toward one of a small set of main layup finishes. No snapping to the beginning of an unrelated clip.

Public descriptions of adaptive airborne finishing establish a behavior to study, not the proprietary internals producing it. The following is an independent proposal, with no claim to reproduce another implementation.

## Player-facing sequence

1. Drive and start an eligible dunk gather.
2. Use the finish direction/gesture to select a dunk.
3. Once airborne, make a fresh tap in the finish region to request a layup conversion.
4. Select a feasible transition/release from the actual pose, ball side, rim position, and defender.
5. Resolve contact, release, flight, result, and landing.

One tap means one conversion request. It cannot trigger a pass, jumper, repeated hand changes, or a second takeoff. For a held dunk input, release ends the hold; a subsequent fresh tap requests conversion. A multi-touch alternative can be studied later without requiring it.

Conversion is available while the ball remains controlled and before irreversible release/rim events. Use a subtle opportunity cue. A late input cannot rewrite a score, completed dunk, or lost ball.

## Pose-aware selection

Read ball hand/location; arm and shoulder pose; torso rotation; root position and velocity; jump phase and remaining flight; rim side/distance; defender contacts; stamina/Finish; and clock deadline.

Each candidate route records valid entry envelopes, release hand, ball path, time required, compatible facing, body clearance, release point, and recovery. Reject incompatible routes first. Rank feasible routes by continuity, reachable release, clearance, and user intent. A name-based or rating-only sort is insufficient.

Use a limited library of transition clips with bounded pose/hand adjustment. Reuse finishing segments through compatible bridges. Pose matching and blending can reduce seams but do not automatically preserve ball contact or collision; authored rules and tested cases still matter.

| Current condition | Candidate destination | Needed bridge |
|---|---|---|
| High ball in outside hand; same-side rim access | High outside-hand or glass release | Reduce dunk extension into wrist release |
| Low outside ball; rising/near apex | Scoop/underhand | Continue low-to-high path without hand teleport |
| Ball held near chest in two hands | Protected short finish to available hand | Controlled two-hand-to-one-hand transfer |
| Travel underneath rim; far side reachable | Reverse layup | Preserve rotation/clearance and finite flight |
| Ball drawn away from a contest | Adjusted/double-clutch finish | Re-extend within remaining airtime |
| Little usable flight remains | Closest feasible short release or failed attempt | Preserve physical state; do not restart a clip |

These are route categories, not universal recipes. Every eligible dunk family must specify reachable destinations at each conversion phase. A complex airborne transfer may have a smaller conversion window than a basic dunk.

## Coverage contract

For each supported dunk test early/middle/late airborne conversion; both hands; approach sides; supported gathers/bodies; stamina; open/contacted states; both cameras; and low/high Handle-related approach timing. Test a block before and after the tap.

Every advertised conversion state needs a route or truthful failure outcome. "Always a way back" means complete handling of reachable states, not guaranteed success from an impossible position. Shorten an eligible window or author another bridge when necessary. Never add airtime, teleport the ball, or cancel gravity to force a finish.

## Timing-check interaction

The owner confirmed a conversion tap; whether it also evaluates layup timing is not explicitly settled. Recommended simple design: the tap requests the route, while the attempt retains its existing timing-quality context and adds situation-based layup evaluation. Avoid a surprise third precision prompt during a tiny remaining flight.

Compare evaluating the conversion tap itself against a layup opportunity in a storyboard. Either design must prevent conversion becoming a guaranteed escape from a failed dunk check. Reach, contact, balance, and Finish still matter. Explain the result clearly.

## Shared-system requirements

The clock continues; release after expiry is not rescued by the earlier dunk command. Both cameras share the conversion window. Haptics follow actual contacts. The defender can contest throughout; conversion is not invulnerability.

Future online play validates requested action and timestamp against authoritative possession/jump state and resolves one result. Cosmetic cloth and face animation follow the route without changing gameplay. Test garment continuity during abrupt shoulder/torso changes.
