# Tools and production plan

Research recommendation only. No engine has been selected, installed, licensed, or used to build this game. Costs, license eligibility, and platform requirements must be checked again when procurement or development starts.

## Engine candidates

| Candidate | Fit for this concept | Main tradeoff | Recommendation |
|---|---|---|---|
| Unity with Universal Render Pipeline | Mobile rendering, touch input, skeletal animation, rig constraints, broad tooling | Commercial license eligibility and package compatibility need review; animation still requires substantial original work | Leading candidate for a later technical evaluation |
| Godot | Open engine, flexible input and rendering, straightforward ownership of project code | This particular animation-heavy 3D mobile pipeline needs an early device proof and team experience | Serious alternative if the team prefers open tooling |
| Unreal Engine | Strong character animation and cinematic tools | Portrait mobile performance, content size, and production complexity require careful constraints | Consider when the team already has expertise and the visual target justifies it |

Do not select an engine from a rendered desktop demo alone. Later, compare a small original character, a ball-hand constraint, a planted foot transition, portrait UI, and a sustained device run. That comparison is future development work, not part of this research package.

## Design and asset tools

| Need | Proposed tool or approach | Deliverable |
|---|---|---|
| Flows and portrait UI | Figma | Screen layouts, touch regions, career hub, wardrobe, timing check storyboard |
| Design records | Markdown and CSV in this folder | Decisions, move atlas, asset briefs, scope tracking |
| Characters, shoes, courts, animation cleanup | Blender | Original meshes, UVs, rigs, authored motion, exportable assets |
| Motion reference | Commissioned athlete recordings with written rights | Multi-angle basketball actions and timing notes |
| Optional capture acceleration | Evaluate a motion-capture service such as Rokoko | Starting body motion requiring cleanup; not reliable finished ball/hand contact by itself |
| Generic placeholder motion | Licensed library assets, with license-specific review | Temporary non-signature locomotion; do not assume basketball techniques exist |
| Audio and video assembly | DaVinci Resolve / Fairlight or a suitable audio editor | Original/licensed ball bounces, sneakers, rim contacts, reference cuts |
| Concept exploration | Optional image-generation tools using authorized inputs | Wardrobe, original shoe silhouettes, court mood studies; images are not rigged game assets |
| Device profiling | Engine profiler plus platform tooling | Input latency, frame time, memory, thermal behavior, haptic reliability |

Do not feed third-party game footage or the supplied social posts into a capture or generation service without permission for that use. Observation and access do not establish an asset-production license. Use the references to describe the desired composition; create or license production material separately.

## Art direction proposal

Owner direction is the highest reliable visual quality and iPhone responsiveness. A proposed execution is realistic 3D characters and basketball action with carefully layered distant scenery. The exact degree of stylization remains open. Prioritize convincing weight, materials, and light while protecting ball visibility, hand contrast, feet, and court lines. See document 14 for the hybrid environment and high-refresh plan.

Build reusable gym, outdoor court, and arena kits. School identity changes through colors, original insignia, wall graphics, lighting, equipment, and crowd treatment. A roster of forty schools should not automatically become forty unrelated architecture projects.

Use a small common character skeleton with controlled body proportion ranges. Evaluate clothing layers, tattoo placement, footwear, and bare feet against that skeleton. All apparel must survive dribbling, deep crouches, gathers, jumps, and landings. Accessories and jackets need a low-cost movement solution; full cloth simulation is not a default requirement.

## Animation production path

1. Select a move family and document legal entry/exit states.
2. Have a movement reviewer check its mechanics and terminology.
3. Record or commission authorized reference from useful angles.
4. Author or clean body motion; establish foot plants and ball events.
5. Connect hand, ball, root, and foot constraints; specify every release and reattachment.
6. Validate mirrored and dominant-hand variations individually.
7. Later test transitions, interruptions, contacts, body sizes, clothes, and both cameras on actual phones.

Every deliverable needs ownership/license metadata, source files, export settings, scale, rig version, and review status. A purchased clip is not automatically compatible with our skeleton or move system. An AI-generated video is not an animation graph, a clean rig, or guaranteed usable motion.

## Roles and dependencies

Essential competencies: basketball movement direction; gesture and gameplay design; technical animation; character and environment art; mobile engineering; UI/UX; audio/haptics; QA and accessibility. A person may cover multiple roles, but the responsibilities do not disappear.

Commerce later adds purchase integration, a durable currency ledger, support/refund handling, and economy tuning. Online multiplayer would add an independent networking and operations burden. Original names and commercially distributed content require appropriate rights review.

The current machine is Windows. An eventual iOS release needs access to the supported Apple build/signing workflow and real iPhones; an existing account, Mac, or build service has not been audited for this project. Android needs physical device coverage as well. Do not purchase resources based on this document alone.

## Planning order rather than a promised schedule

Research and storyboards → phone control experiment → animation connectivity proof → one complete offensive possession → playable defense against authored and AI attacks → team passing and return lob → small career/wardrobe slice → economy and store integration → device and release validation. Future PvP requires its own authority/networking evaluation; preserve suitable action/event boundaries from the start.

Avoid a calendar commitment before estimating the selected animation cases and assessing the team's reusable assets. Animation authoring, transition cleanup, outfit fitting, and device iteration are likely major costs. A tiny interaction prototype and a commercially shippable content-rich game are different budget items.
