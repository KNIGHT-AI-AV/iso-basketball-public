# Vision and complete product scope

## The promise

Scope exclusions confirmed by the owner: Euro steps and post offense. Airborne conversion from a chosen dunk to a natural layup is included; see document 20.

**Read the defender. Make them commit. Get your bucket.**

A portrait mobile basketball game where the player's skill is expressed through changes of pace, ball-hand changes, deceptive body movement, shot selection, and finishing. A good possession should look intentional when watched without the interface.

The core pleasure is the connection between a thumb gesture and a believable basketball action. The second pleasure is earning a clear shot or a spectacular finish through the setup. Merely playing a flashy animation should not guarantee either separation or points.

## A representative possession

The player sizes up outside the arc. A hesitation draws the defender upright. A crossover attacks the newly exposed side. The defender trails, then recovers toward the rim. The player can continue for a layup, commit to a dunk if there is room, stop for a midrange jumper, retreat into a stepback, or pass to change the matchup. The clock continues throughout.

The outcome explains what happened: an open make, an early release, a smothered attempt, a clean block, a lost handle, or a shot-clock violation. Restart should be quick enough to encourage trying a different answer.

## Pillars

| Pillar | Requirement |
|---|---|
| Visible basketball | Show feet, hand changes, body lean, the defender, and usable court space. |
| Expressive control | Small reusable gestures produce different legal actions depending on hand and movement state. |
| Earned separation | The defender has momentum, readable commitments, and a recovery cost. |
| Connected finishes | The gather and finish follow naturally from the approach and available space. |
| Fast replayability | A possession is brief; the next attempt is easy to start. |
| Personal style | Fictional players differ in movement, reach, abilities, and visual personality. |

## Mode architecture

| Mode | Experience | Proposed stage |
|---|---|---|
| Open Gym | Free ball handling; optional clock; cone or cylindrical training obstacle; move hints | First playable |
| Isolation Run | One offensive player versus one defender; short possession sequences | First playable |
| Defense Practice | Control the defender against authored attacks, then an attacking AI; same court-facing camera | Core control validation after the offensive baseline |
| Finish Practice | Begin at a selected approach and rehearse gather, dunk, layup, or pull-up | First playable training tool |
| Team Isolation | Ball handler plus left and right teammates, each with a matchup; passing changes the active isolation | Future MVP extension |
| Challenge Ladder | Local authored situations: late clock, weak hand, patient defender, limited space | Early expanded release |
| Style Session | Longer free practice, advanced tricks, replay and photo presentation | Later |
| Ghost Challenge | Compare a saved attempt or reproducible challenge with another player | Later; scoring and validation work |
| Live One-on-One | Two humans alternate attacking and defending the same basket without a camera flip | Owner-requested future direction; networking phase and budget open |

These are scope proposals, not announced features. The catalogue may include actions for later modes without committing to implementing them.

## Keeping passing compatible with isolation

The owner-confirmed team concept has a ball handler and teammates on both edges. Each attacker has an assigned defender; active play remains a spread isolation. Double-tapping the left or right teammate area passes to that side. Control switches to the receiver after a successful catch and preserves the current clock. The passer relocates unless selected for a return alley-oop. Three attackers and three defenders require more animation, framing, and decision logic than one-on-one; they belong in a later scope step.

The receiver's actual position determines whether there is a catch-and-shoot, a closeout to attack, or another set isolation. Defenders never teleport during the pass. Do not impose a universal one-pass limit: a return alley-oop requires a second delivery. Limit off-ball decision complexity instead; passing still costs time and risks interception.

A less costly alternative is choosing the next attacker only between possessions, but that does not fulfill the owner's live passing idea. Keep the distinction explicit when estimating work.

## Characters and stats

Start with original archetypes rather than licensed athletes. Suggested early identities: a quick handle specialist, a balanced wing, and a strong finisher. Body shape and reach should matter without making a single build dominate.

| Attribute | Intended influence |
|---|---|
| Handle | Ball protection and difficulty of maintaining control in demanding transitions |
| First step | Acceleration after a convincing setup |
| Braking | How quickly the player can stop and recover balance |
| Midrange / long range | Comfortable shooting zones and timing tolerance |
| Touch | Layup and soft-finish tolerance |
| Lift / reach | Which finishes are physically available |
| Strength / balance | Response to legal body contact |
| Stamina | Repeated explosive actions and recovery |
| Passing | Delivery speed and accuracy under pressure |
| Defensive movement / discipline / contest | Opponent positioning, bait susceptibility, recovery, and shot pressure |

These are internal tuning dimensions. Present seven understandable upgrade categories to the player: Handle, Shot, Finish, Footwork, Stamina, Passing, and Defense. The seventh incorporates the owner's playable-defense addition. See document 10 for the mapping. Character creation and appearance options are in document 13. Separate cosmetic style from gameplay advantages. Ratings and animation eligibility will be tuned for this game's scale; no imported player ratings or package thresholds.

## Defender identities

- **Chaser:** closes space quickly and can overrun a well-timed retreat.
- **Anchor:** protects the rim, allowing more pull-up opportunities.
- **Reader:** delays commitment and is harder to fool with the same sequence.
- **Reacher:** attacks exposed dribbles but creates openings after missed reaches.

Use a small shared set of physical limits, reaction delays, and decision weights. Difficulty should change these parameters within believable bounds. The defender cannot read unfinished touch gestures or the player's future queued action.

## Scoring and progression

Keep points and style separate. Two- and three-point scoring is the proposed default; a street scoring variant can be introduced separately. A fancy miss remains a miss. A style score can reward varied, purposeful moves, well-timed changes of pace, and clean finishes, but repetitive dribbling should not outweigh a made basket.

First-session progression should teach a crossover, an attack, a stop, and a finish. Longer progression includes simple stat upgrades and can unlock original outfits, balls, courts, cosmetic movement styles, and more demanding challenges. Microtransactions are confirmed; advertising is excluded. Earned coins fund progression. A premium currency is proposed for cosmetics and optional conversion into coins. The conversion creates paid progression if those coins buy stats; that consequence must remain explicit. See the economy document for recommended limits. Prices, rates, and the competitive treatment of upgrades remain open.

## Whole-product work beyond the court

Career advances through fictional high school, college, and professional basketball. The world catalogue contains 20 working high school concepts and 20 working college concepts; this does not mean forty bespoke courts are required for the first release. Practice is a simple career-scaled home base, with wardrobe and teammate upgrades available without managing training attendance. See documents 12 and 13.

Eventually account for onboarding, move instruction, settings, pause/resume, accessible controls, saves, roster selection, challenge selection, audio mixing, localization, device performance, crash handling, store presentation, privacy disclosures, support, content rights, and updates. Multiplayer would add servers, synchronization, matchmaking, cheating controls, moderation, and ongoing operations.

The eventual first playable can function offline with local progress. A commercial release with paid currency requires purchase verification, durable entitlements, and a currency ledger; it is a separate expansion of technical scope. Advertising is ruled out. Live one-on-one is an owner-requested future direction; its timing and architecture remain open, as do other social features. These systems are not prerequisites for researching the core idea.
