# ISO: Basketball — research and design dossier

September 26, 2026 · Research revision 1 · Application name approved

**Purpose:** describe a portrait basketball game about creating separation through expressive swipe dribbling, then finishing the possession. This package is research and design documentation. No game development has started.

## Owner direction

- Application name: **ISO: Basketball**. Short form: **ISO**. Original repository name: `iso-basketball`.
- Phone upright. Compose around a 9:16 reference while supporting taller phone screens.
- Target the best reliable iPhone graphics and responsiveness. Explore 3D action with layered distant scenery, a 120 fps target on compatible devices, and a sustainable fallback established by testing.
- Confirmed mixed art direction: carefully lit 3D people and ball, selective hair/clothing/jewelry motion, and high-quality illustrated scenery layered in the same 3D space to create camera parallax.
- Surpass the two supplied character screenshots: distinct faces, blinking, gaze, breathing, idles, and believable moving fabric. Evaluate actual cloth physics where needed rather than relying on painted wrinkles alone.
- The supplied gym reel is the primary reference for the main camera, distance, full-body visibility, and surrounding space.
- The supplied video and three photos were kept as private research references and are not published; see the [reference note](../research-references/README.md). They stay out of game builds and public releases.
- Chain ball-handling moves to beat a defender, drive, pull up, or stop for a stepback.
- Exclude Euro steps and post offense. A fresh airborne tap after dunk selection can request a natural pose-aware layup conversion; eligibility and timing details are specified separately.
- Play defense through hold/drag movement and swipe contests, with the same camera direction and no role-based flip. Future one-on-one PvP is part of the vision, with scope and cost still to evaluate.
- Practice against a cone or obstacle; play against a defender in competitive modes.
- A shot clock creates urgency. Passing to a teammate with different abilities is part of the broader concept, while isolation remains the focus.
- Dunking may have a second gesture phase and a closer camera. The supplied dunk photograph is a candidate reference for that view.
- Offer different locations. Allow camera-height adjustment without losing the reference composition.
- Include cinematic finishing and wide-camera-throughout settings with identical controls and gameplay timing.
- Provide haptics for dribbles and dunk impact.
- Double-tap the left or right teammate area to pass. Control switches to the receiver. An upper-left or upper-right diagonal-down gesture selects a return alley-oop play involving that side.
- Include character creation and a broad wardrobe: haircuts, tattoos, jewelry, shirts, jackets, pants, original shoes, barefoot, and shirtless appearance options.
- Start in a plain white tank top and gray joggers with no tattoos. Tattoos are intended as expensive cosmetic items. Dribble speed is stat-driven, with Handle as the proposed simple upgrade category.
- Progress from fictional high school to fictional college to a fictional professional league. Plan 20 high schools and 20 colleges; league naming needs clearance.
- Practice grows from a home court to college facilities to a mansion court. Keep teammate development and customization simple inside this hub.
- Include understandable stat upgrades, including accuracy and stamina. Jump shots use a timed fail/okay/perfect skill check influenced by the basketball situation.
- Microtransactions are definite. No ads, including rewarded ads. A two-currency economy with optional premium-to-earned conversion is being explored; prices and conversion rates are not approved.
- Research movement and animation coverage broadly before selecting a small future playable scope.
- Saved documents use original requirements and basketball terminology, without naming the restricted basketball reference product, copying its control tables, or including citations. Other public apps are identified only in the owner-requested feasibility comparison.

## Read in this order

| Document | What it answers |
|---|---|
| [01 — Vision and scope](01-VISION-AND-SCOPE.md) | What is the game, its modes, roster, progression, and wider product scope? |
| [02 — Cameras and locations](02-CAMERAS-AND-LOCATIONS.md) | What do the two supplied references establish? How should portrait framing work? |
| [03 — Gesture and possession design](03-GESTURES-AND-POSSESSIONS.md) | How do swipes, movement, shooting, dunks, passing, and the clock coexist? |
| [04 — Animation and movement](04-ANIMATION-AND-MOVEMENT.md) | How do hands, feet, ball, contacts, transitions, and physics stay coherent? |
| [05 — Move atlas and coverage](05-MOVE-ATLAS.md) | How is the catalogue organized, and what does animation completeness mean? |
| [06 — Naming](06-NAMING.md) | What is the approved application name, and what remains unresolved for league and school identities? |
| [07 — Tools and production](07-TOOLS-AND-PRODUCTION.md) | Which tools, roles, assets, and workflows would be needed later? |
| [08 — Future MVP and evaluation](08-FUTURE-MVP-AND-EVALUATION.md) | What would we build first if development is authorized, and how would we judge it? |
| [09 — Research gaps and content rights](09-RESEARCH-GAPS-AND-RIGHTS.md) | What is known, proposed, unverified, or still dependent on rights and specialist review? |
| [10 — Shooting, upgrades, and haptics](10-SHOOTING-UPGRADES-AND-HAPTICS.md) | How do shot timing, created space, balance, stamina, upgrades, and tactile feedback fit together? |
| [11 — Economy and no-ad monetization](11-ECONOMY-AND-MONETIZATION.md) | How can two currencies support purchases without frustrating players? |
| [12 — Career and fictional world](12-CAREER-AND-WORLD.md) | How do schools, colleges, the professional league, and practice hubs fit together? |
| [13 — Character creation and wardrobe](13-CHARACTERS-AND-WARDROBE.md) | How do original cosmetics, shoes, outfits, and practice customization stay manageable? |
| [14 — Graphics and iPhone performance](14-GRAPHICS-AND-IPHONE-PERFORMANCE.md) | How do 3D characters, layered backgrounds, lighting, and high refresh fit together? |
| [15 — Feasibility and business assessment](15-FEASIBILITY-AND-BUSINESS-ASSESSMENT.md) | Is the idea credible, what have smaller teams shipped, where can AI help, and what creates financial risk? |
| [16 — Additional features and priorities](16-ADDITIONAL-FEATURES-AND-PRIORITIES.md) | Which small additions improve the core, and which larger systems should wait? |
| [17 — Defense and future PvP](17-DEFENSE-AND-FUTURE-PVP.md) | How do defensive gestures, balance, unchanged camera direction, and eventual live one-on-one fit? |
| [18 — Decisions and dependencies](18-DECISIONS-AND-DEPENDENCIES.md) | How do owner requirements propagate into the related systems while proposals remain distinguishable? |
| [19 — Character quality and fabric](19-CHARACTER-QUALITY-AND-FABRIC.md) | What quality floor, facial variety, living motion, and garment behavior must production satisfy? |
| [20 — Airborne finish routing](20-AIRBORNE-FINISH-ROUTING.md) | How can an airborne tap change a chosen dunk into a natural layup without pose snapping? |
| [Move catalogue](data/move-catalogue.csv) | Filterable inventory of candidate basketball actions and their intended role. |
| [Animation coverage](data/animation-coverage.csv) | Required animation families, variations, and completion criteria. |
| [Fictional schools](data/schools.csv) | Forty original working school concepts, subject to name clearance. |

## Status language

**Owner direction** means the owner explicitly requested it. **Observed** means visible in the supplied reference. **Proposal** means our design recommendation. **Needs validation** means a definition, physical behavior, gesture, cost, or asset has not been established through testing or specialist review.

The catalogue is a broad first-pass inventory, not a claim that every basketball move or every animation has been identified. A named action is not a finished clip. A clip is not a working transition. No recognition accuracy, frame rate, build, animation quality, or device acceptance has been measured.

## Current recommendation

Use **ISO: Basketball** as the application name and **ISO** as the short form. Design around a patient, full-body court view and an earned closer finishing view. Plan a modular movement vocabulary: individual actions should combine through compatible hand, foot, speed, and balance states.

The next useful design artifact is an original six-frame possession storyboard anchored to the two supplied references. The next research priority is reviewing the catalogue with a basketball movement specialist and turning each selected family into a precise animation brief. Neither task requires starting game development.
