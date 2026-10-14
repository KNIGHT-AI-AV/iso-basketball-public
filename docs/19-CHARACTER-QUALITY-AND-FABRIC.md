# Character quality floor, lifelike motion, and fabric

## Owner-supplied quality references

Two supplied character screenshots establish a minimum comparison level to surpass, not models or designs to reproduce. The owner dislikes the generic/repetitive facial impression and wants more appealing, individual basketball characters. These static images do not establish source mesh counts, engine settings, actual roster variety, animation quality, or device performance.

The main basketball reel is the movement and fabric reference. It was reviewed privately at 1080 × 1920 and 60 fps and is not published. Sampled stills show clothing in different body poses; evaluating movement requires the temporal sequence. No conclusion about another game's cloth implementation can be drawn from a screenshot.

## Required quality improvements

| Area | Acceptance direction | Avoid |
|---|---|---|
| Facial identity | Different head shapes, jawlines, noses, eyes, brows, lips, and proportions | One head with only skin tone and hair swapped |
| Eyes | Believable eyelids, gaze, restrained highlights, blink variation | Fixed wide stare or synchronized blinking |
| Skin | Coherent color, material roughness, soft form lighting, readable detail | Uniform plastic shine or flickering fine detail |
| Hair | Distinct silhouette, credible scalp connection, selective motion | A rigid block or excessive transparent strands |
| Body | Athletic proportions and clean elbows/shoulders/knees | Collapsed joints or stretched anatomy |
| Clothes | Correct fit and thickness; folds responding to pose and movement | Texture glued onto a rigid body; arbitrary waving |
| Shoes and bare feet | Credible shape, planted soles, correct scale | Floating feet or invisible-shoe barefoot presentation |
| Lighting | Form-defining light integrated with painted scenery | Lighting used to disguise poor anatomy |

Lighting improves a sound model; it does not create missing anatomy or distinct faces. Start with a clean main mesh/rig and a small roster of distinguishable heads with compatible expression controls. The number of presets and supported body shapes is not approved yet.

## Characters should look alive

Provide subtle breathing, weight shifts, hand relaxation, blinking, eye/head attention toward ball or opponent, and fatigue recovery. Vary phase and timing so a lineup does not move together. Idles should be restrained and blend into accepted input quickly.

Separate identity shapes from expression changes. Eyelids and basic expression shapes must work across supported faces. Gaze follows visible targets without extreme neck/eye snaps. Blinking and breathing do not imply a dialogue or full lip-sync system.

Breathing must not dislodge an attached ball. Hand-contact constraints take priority when necessary. Face animation and cosmetic secondary motion do not alter gameplay hitboxes or ball authority.

## Fabric is a first-class motion requirement

Owner emphasis: capture the actual movement of the tank top and joggers, including folds, drag, bounce, compression, and settling. Evaluate real cloth physics where needed. Merely adding a wrinkle texture does not meet this requirement.

For the starter white tank, inspect shoulder pull, armhole shape, waist compression, hem delay, torso twist, and separation from the abdomen. For gray joggers, inspect hip folds, knee bending, thigh/calf movement, ankle cuffs, and settling after stops or landings. Define fabric weight and fit in each original asset brief.

## Candidate methods

| Method | Contribution | Limitation |
|---|---|---|
| Skinned garment with corrective shapes | Predictable folds during crouch, bend, twist | Limited delayed settling after arbitrary movement |
| Pose-driven wrinkle normal/material maps | Fine shading that responds to posture | No silhouette change or loose hem movement |
| Limited secondary bones/springs | Low-cost lag in selected hems and accessories | Limited general contact/drape behavior |
| Constrained cloth simulation | Reactive drape, acceleration response, settling, configured collisions | Requires stability, collision, and device-cost work |
| Authored simulation cache | Repeatable high-quality fabric in a fixed presentation | Cannot independently support arbitrary gameplay branches |

Recommended investigation: corrective garment fit plus simulated or spring-driven loose regions, compared against a more fully simulated version of the same garment. Choose using moving footage and sustained device measurements. Neither physics nor authored motion is automatically the better result.

Constrain attachment regions and allow freedom where fabric moves. Configure collision proxies around torso and limbs and review the solver's actual limits. Hands and basketball remain controlled by gameplay/animation; decorative cloth cannot become an unstable source of ball outcomes. Fast movement, contact, pose transitions, and camera cuts require review.

Lower-cost profiles may simplify distant secondary motion or cloth complexity but must retain the approved main-character quality floor. If a device cannot support the required look and response, evaluate excluding it after measurement rather than promising universal support.

## Planned acceptance session

Use the same original character, camera, light, and outfit to compare candidates at gameplay and close-view sizes. Review idle/breathing, deep crossover, torso twist, sprint-stop, stepback, gather, airborne layup conversion, dunk, landing, and recovery.

Show at least three distinct original faces with common hair and lighting to test actual facial identity. Then evaluate different hair and skin tones. Inspect blinking and gaze in motion rather than only a posed render.

Compare fabric at normal speed and slowed playback, watching seams, hems, knees, and shoulders. Record penetration, unstable oscillation, frozen folds, texture stretching, and discontinuities between actions. Repeat at low/high Handle because changed dribble speed changes acceleration and fabric response.

Test the most demanding supported outfit in six-character play as well as one-on-one. A wardrobe close-up does not prove gameplay performance. No model, cloth prototype, or phone-rendered quality proof exists yet.

## Production implications

Budget distinct face design, eyelid/expression shapes, eye materials, breathing/idles, garment corrections, wrinkle materials, cloth/secondary-motion setup, and compatibility testing. AI can assist drafting and cleanup; visual direction and actual motion review remain required.
