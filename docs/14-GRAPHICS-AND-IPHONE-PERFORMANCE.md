# Graphics and iPhone performance

## Owner direction

Target the best graphics that can be delivered reliably, with high-quality 3D players and the highest practical iPhone frame rate. Explore layered two-dimensional scenery behind the hoop to create realistic depth. Reliability and responsiveness belong in the visual target from the start.

**Art direction confirmed:** the world is arranged in three-dimensional space. Players, ball, and nearby interactive objects use three-dimensional models enhanced through lighting and material quality. Distant scenery uses high-quality illustrated/painted layers, with an art treatment suited to each location. Camera movement produces depth through their relative positions. Select parts of the character, such as hair, loose clothing, and jewelry, have secondary motion. This mixed treatment is an intentional visual identity, not merely a temporary placeholder for full 3D scenery.

## Lighting the character against a painted world

Use a clear key light to describe anatomy and fabric, a restrained fill to retain readable shadow detail, and selective edge light where the background would swallow the silhouette. These are artistic roles, not a requirement for three expensive dynamic lights per player. Coordinate painted light direction, color temperature, softness, and time of day with the 3D subject.

Material response should distinguish skin, textured rubber, fabric, leather-like shoe panels, and metal jewelry. The ball needs readable texture and believable highlights while rotating. Keep contact shadows beneath feet and ball and plausible shadowing around the basket. Avoid lighting that makes the player appear pasted onto the illustration.

Use a common color palette, contrast hierarchy, and level of visual detail across the 3D and illustrated layers. Paint distant detail selectively rather than covering every surface with sharp edges that compete with the player. The court can be physically 3D while using an illustrated material treatment consistent with the scenery.

## Secondary motion budget

Use a few carefully constrained moving elements: hair tips, chain pendants, jacket hems, and selected loose fabric. Prefer authored motion or limited bone-based response before full cloth or strand simulation. Their movement must follow acceleration and landing without intersecting the face, ball, or hands. Offer lower-cost variants through device profiles while preserving the character's silhouette.

## Layered art requirements

Author near, middle, and far scenic layers separately with overscan beyond the visible frame. Fill the regions that become exposed when camera height or framing changes; do not leave holes behind a foreground silhouette. Use shallow geometry or a bent plane when one perfectly flat card cannot support the required perspective. Depth-tested layers must occlude in a consistent order and share the court's world-space camera.

Start with baked scene lighting and fixed time-of-day variants for the illustrated scenery. A fully dynamic day/night cycle would require additional art or shading work to keep the painted and 3D illumination coherent. No dynamic weather or day/night cycle is committed.

Use texture atlases, mipmaps, appropriate compression, restrained transparency, and only the texture detail that the frame can reveal. Illustrated backgrounds reduce some geometry and lighting work, but may increase texture memory and transparent overdraw. Compare actual scenes before claiming a processing saving.

## Proposed hybrid scene

| Layer | Representation | Why |
|---|---|---|
| Players, ball, rim, backboard, net | True 3D with appropriate animation | Moving silhouettes, contact, and close finishing views must remain convincing |
| Playable floor, near sidelines, basket support | 3D geometry with authored materials and baked/static lighting where useful | Foot contact, bounce location, shadows, and perspective are critical |
| Nearby wall, padding, fence, bleachers | Simple 3D forms with detailed textures | Camera height changes and dunk views reveal depth and occlusion |
| Far stands, distant architecture, trees, skyline | Layered image planes, simplified geometry, or a distant backdrop | Suggest detail and depth where the camera reveals little parallax |
| Atmosphere and lighting accents | Restrained particles, gradients, baked illumination | Mood without obscuring the ball or timing cues |

This is often called a hybrid 2.5D environment, but the basketball action remains 3D. It is a design choice to validate, not a guarantee that every flat layer is faster than geometry. Large overlapping transparent layers can be expensive too.

Depth comes from perspective, correct relative scale, light direction, contrast, occlusion, and modest parallax as the camera changes. Do not simply move every background layer at an arbitrary speed. Place scenery consistently in the same scene and constrain camera motion to views the art supports.

## Camera consequences

The primary rear portrait view is especially suitable for a detailed backdrop behind the hoop. Adjustable height and the closer finishing camera expose the upper surfaces and sides of objects. Build the near basket area in 3D and use distant flat layers only where their thinness cannot be seen.

Approve a bounded camera envelope before final environment art: lowest/highest main height, widest/tightest framing, and finishing-view positions. Test left and right drives, baseline finishes, and player occlusion at every extreme. Do not promise a free orbit camera with scenery authored for one view.

If a finish cut reveals an unsupported view, revise that camera or replace the offending layer with geometry. Both wide and cinematic settings must represent the same court and defender positions. Photo/replay camera freedom would be a separate asset scope decision.

## Frame-rate target

Propose a **120 fps performance target on compatible high-refresh iPhones**, with a stable **60 fps supported baseline** where hardware or sustained conditions require it. Display support is a ceiling, not proof that the game can render at that rate. System power and thermal conditions may reduce the available cadence; the application must remain correct when the rate changes.

At 120 fps each frame has about 8.33 milliseconds; at 60 fps it has about 16.67 milliseconds. CPU and GPU work need separate measurement, and shared-resource contention matters. Do not add every profiler category together as though all work occurs serially. Preserve headroom for camera cuts, extra characters, effects, and warmer devices.

The latest supported device list must be checked when implementation begins. No iPhone has run this game, and no measured frame-rate or thermal claim is being made here. Android parity, minimum devices, and launch-platform priority remain to be defined.

## Where to spend visual detail

Prioritize body motion, hands and ball alignment, foot plants, face/hair silhouettes, apparel fit, skin and fabric response, readable lighting, and local contact shadows. The player and ball deserve more of the budget than a distant crowd face. Crisp timing UI should remain full-resolution even if scene resolution scales.

Use authored/baked environment light where suitable, a restrained number of dynamic lights, character-focused shadows, controlled material variety, and detail levels for distant people and props. Evaluate floor reflections carefully; a polished gym need not use expensive full-scene reflections. Evaluate hair and jewelry overdraw as closely as polygon counts.

Avoid setting a universal triangle count before profiling the actual rigs, materials, camera, and number of characters. A 3v3 return-lob scene with apparel and shadows is a more meaningful stress case than a lone bare character on an empty floor.

## Proposed settings and scaling order

Offer Auto, Performance, and Quality if testing justifies them. Auto selects a sustainable device profile. Performance prioritizes high refresh and input response. Quality improves appearance within an honest frame-rate target. Do not expose twenty technical sliders on a phone.

Reduce distant decoration, shadow cost, reflections, effects, and scene resolution before degrading critical ball/hand alignment or timing UI. Keep motion blur subtle or off in gameplay so hand changes stay readable. Use stable scaling decisions instead of rapidly oscillating quality every few seconds.

Input timestamps, skill-check windows, shot clock, animation events, and simulation outcomes must use elapsed time rather than frame counts. Rendering at 120 fps cannot make a move twice as fast or give a shorter shot clock. A later technical design must specify simulation stepping and interpolation independently from presentation refresh.

## Later acceptance work

Measure sustained play rather than a cold launch. Test a defined 20–30 minute session with six players, return lobs, the cinematic cut, the most demanding supported outfit, haptics, and career environments. Record frame-time distribution, long stalls, input-to-visible response, memory, thermal changes, and battery conditions. Compare both camera settings and low-power behavior.

Set a minimum supported device only after this work. If reliable 120 fps and the desired detail conflict, present the measured tradeoff; do not promise both by removing the word reliable from the requirement.
