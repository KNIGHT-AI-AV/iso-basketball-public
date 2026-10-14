# Cameras, visual direction, and locations

## Main reference: owner-supplied gym reel

**Observed on September 26, 2026:** the public reel became accessible in a browser after the initial text retrieval failed. Its video element reported 1080 × 1920 and approximately 15.83 seconds. Several playback frames were inspected; there is no frame-by-frame motion annotation or audio analysis in this dossier.

The reel is 1080 × 1920 at 60 fps. It was kept as a private research reference and is not published with this dossier; see the [reference note](../research-references/README.md). It is excluded from game assets and public release material; it is not an animation extraction source or production asset. The same applies to the dunk-camera photograph and the character-quality examples.

The view is behind the player, aimed toward a centered basket. The full body and shoes are visible while the player works around a cylindrical obstacle. There is useful lateral space around the body and a substantial visible approach to the basket. Court lines provide depth cues. The inspected framing stays broadly anchored to the court as the player approaches the hoop, making the player smaller with distance.

**Preserve:** full-body silhouette, readable foot plants, visible floor, clear depth toward the hoop, space on both sides, and the intimate feeling of watching someone work out in a gym.

**Do not infer:** an exact physical camera height, focal length, lens field of view, tracking rig, or world-space distance. A rendered frame alone does not uniquely establish them. No precise camera calibration has been completed.

## Default gameplay camera proposal

Start with a court-anchored rear view inspired by the supplied composition. Allow restrained tracking inside a framing boundary when the attacker or defender would otherwise leave view. Avoid a close shoulder camera that hides the ball or feet.

The owner's preferred distance should lead the visual calibration. Matching this reference matters more than fitting a generic third-person camera preset.

| Control | Requirement |
|---|---|
| Height | Small bounded adjustment; retarget the view to preserve the hoop and full-body framing |
| Distance | Begin locked to the approved reference composition; consider a narrow range only after testing |
| Follow strength | Designer setting first; compare anchored and restrained follow behavior |
| Camera motion | Reduced-motion option; no unnecessary shake during dribbling |
| Handed layout | Mirror interface zones without flipping the basketball court or reversing world direction |
| Offensive/defensive role | Keep the same basket-facing direction; no automatic role-based camera flip |
| Aspect ratio | 9:16 reference; adapt to taller phones and safe areas without stretching the scene |

Reference-led composition tests, not approved measurements:

- At the starting spot, try a player height around 35–45% of the gameplay viewport.
- Keep both feet above the dense touch-control area.
- Keep the basket, defender, and likely drive lane visible together.
- Move the interface or compress empty background before cropping hands or feet.
- Test the same framing at both wings, the baseline, and the paint.

## Dunk reference: owner-supplied photograph

**Observed:** a rear view of an airborne player with the whole body visible, the ball extended out on one side, bent legs visible below the torso, and the rim just above the player's head. The view looks toward the backboard and includes floor and background space. This is a screenshot containing a photograph; the surrounding social interface is not part of the proposed game composition.

**Candidate direction, not final approval:** a lower and closer rear view, slightly offset to the ball side when necessary. Preserve the extension of the arm, the legs, and the relationship between body and rim. The image establishes a composition, not a camera-motion path or a verified dunk sequence.

The original reference media remains separate from game assets. Our court, uniforms, banners, athlete, and audio should be original or appropriately licensed.

## Two-stage camera sequence

| Stage | Camera behavior | Input behavior |
|---|---|---|
| Read and create | Reference-style rear view | Dribble and movement gestures |
| Finish intent | Keep the main view while the player chooses to attack the rim | Confirm finish intent and route |
| Gather | Begin a short, predictable move toward the finishing composition | Close the dribble phase; prepare a fresh finish gesture |
| Airborne finish | Lower, closer rear composition; hands and rim visible | Dunk gesture or layup timing |
| Rim result | Keep contact readable; avoid crossing the player-rim axis | Do not accept a new possession command |
| Landing / reset | Return smoothly, or cut after the ball is dead | Restore the normal control layout |

A dunk camera must not become an invulnerability cutscene. The defender remains in the simulation and can contest within the permitted rules. Never move the player to fit the camera.

Default proposal: real-time finishing. Optional assisted practice can slow the entire simulation, including defender, ball, animation, and clock. Do not slow only the attacker or silently provide extra competitive time. Decide whether such assistance is available in scored modes after testing.

**Owner-confirmed setting:** offer Cinematic Finishes and Wide Throughout. Both use identical gestures, gesture windows, shot checks, defender behavior, clock rules, and haptics. Wide Throughout keeps the main wide composition for the entire possession, including dunks. Camera mode is presentation only. Show the same finishing cue in either view. Changing modes must never make a dunk easier or add time.

For pull-up jumpers in Cinematic Finishes, test a modest camera tightening after the gather instead of a major angle change. A hard cut during release timing may conceal the cue. Reduced motion can disable camera movement independently.

## Location system

The owner wants different locations. Every location should preserve the approved basketball scale, collision behavior, visibility, and camera clearance. Atmosphere can vary without changing the input rules.

| Candidate | Visual identity | Main design risk |
|---|---|---|
| Quiet school gym | Wood floor, restrained banners, warm overhead lights | Reflections or banners competing with the ball |
| Outdoor neighborhood court | Worn paint, fence, surrounding greenery | Fence and foliage hiding the defender silhouette |
| Rooftop evening court | Distant skyline, warm sky, perimeter lights | Bloom and bright backgrounds reducing ball contrast |
| Warehouse practice space | Concrete, tall windows, strong material contrast | Excessive darkness around feet |
| Seaside court | Open horizon, soft daylight, wind ambience | Overbright floor and horizon distracting from the rim |
| Night park | Pools of light, quiet surroundings | Maintaining consistent visibility on low settings |

Suggested first location: an original quiet gym. Subsequent courts should reuse a common basket, dimensions, spawn logic, camera-clearance volume, and lighting test procedure. Weather, slippery floors, crowds, destructible objects, and changing ball bounce are separate features, not automatic consequences of a new location.

## Art and sound brief

Use the owner's confirmed mixed art direction: carefully lit 3D people, ball, and near-court geometry, with high-quality painted/illustrated scenery placed at different depths in the same 3D scene. Select hair, jewelry, and clothing elements move with the body. Lighting, materials, contact shadows, and shared color treatment should connect the two styles. Camera movement creates parallax across the background layers. See document 14 for production and performance implications.

Prioritize ball bounces, hand contact, shoe squeaks, foot plants, net, rim, and a restrained clock sound. Their timing should follow real action events. Music must leave those cues audible and require separate rights. Do not inherit music from a visual reference.

## Next visual documents

Prepare an original six-frame storyboard: size-up, defender commitment, drive, braking/pull-up branch, dunk gather, finish/landing. Then prepare a camera comparison sheet using the same original body pose and court for every candidate. Store image-derived estimates as estimates until approved against a viewable mockup.
