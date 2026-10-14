# Owner decisions and dependent design work

This register distinguishes explicit direction from supporting design choices. New owner requirements should propagate across related systems rather than being appended to one isolated feature list. A derived proposal is not automatically an owner-approved implementation detail.

| Owner direction | Required implications | Supporting proposal / open issue | Main documents |
|---|---|---|---|
| Application name: ISO: Basketball; put the research on GitHub | Use exact display name and `iso-basketball` repository name; owner KNIGHT-AI-AV; include the full written dossier and catalogues | Brand availability is unverified | 06, repository README |
| Upload reference video and photos with cleaned names and metadata | Neutral filenames; strip identifying embedded metadata; remove social-account header/caption from the dunk screenshot; preserve originals outside Git | Sanitized copies were kept privately for research, are not published, and remain excluded from game builds and public releases | 02, 09, reference library |
| Research and documents only | No engine project, game code, purchased assets, deployment, or live store changes | Later experiments require a separate development instruction | 07, 08, 09 |
| Portrait with reference-led full-body camera | Touch-safe framing, visible feet, screen-shape adaptation | One-thumb vs two-thumb still open | 02, 03 |
| Same camera direction on defense | Keep basket orientation, label controlled player, distinguish body-relative backstep from screen direction | Defensive touch-region map requires storyboard review | 02, 17 |
| Cinematic finish or wide throughout | Same gestures, skill windows, clock, defense, haptics | Camera cuts must not hide active defensive input | 02, 10, 17 |
| Swipe-chain dribbles | Legal hand/foot state, action buffers, transitions, contact and failure coverage | Start with a small reliable vocabulary | 03, 04, 05 |
| Dribble speed is stat-driven | Retiming, ball path, exposure, stamina per second, opponent response, sound/haptics, future network validation | Group speed under Handle; bound every move's duration | 04, 10, 17 |
| Double-tap pass to either wing; switch control | Two side teammates, assigned defenders, catch-based ownership, readable indicators | Team isolation is distinct from strict one-on-one | 01, 03 |
| Diagonal-down side gesture for return alley-oop | Passer/receiver roles, cut, lob flight, catch window, finish check, failed connections | Compare one-command give-and-go vs pass-first invocation | 03, 10 |
| Playable defense and possible ankle breaks | Offense AI, defensive control, physical commitment, fair recovery, animation coverage | Seven stat categories with Defense added | 10, 17 |
| Eventual live one-on-one PvP | Authority, prediction, event order, reconnect, match results, latency testing, operations estimates | Provider and paid-stat fairness remain open | 17 |
| Fail/okay/perfect shooting and dunk checks | Visible timing cue, input timestamp, animation alignment, outcome feedback | Freeze shot zones at sweep start; separate late physical blocks | 10 |
| Stamina and upgrades | Meaningful previews, bounded penalties, recovery, teammate upgrades | Seven simple categories; ten levels as a testable proposal | 10 |
| Haptics on dribbles/dunks | Actual contact events, synchronized retiming, strength/off, device fallback | Avoid heavy vibration on every bounce | 10 |
| No ads; definite microtransactions | Purchase ledger, entitlements, transparent shop, durable progress | Premium-to-coins conversion would be paid progression | 11 |
| Many appearance items and original shoes | Compatible rig/layers, asset variants, wardrobe preview, ownership, performance | A few shoe meshes with many authored colorways | 13 |
| Starter white tank + gray joggers + no tattoos | Default outfit assets and thumbnails, body-fit testing, no tattoo granted by default | Basic original starter shoes recommended; not yet specified | 13 |
| Expensive tattoos; possible premium barefoot/shirtless | Cosmetic pricing tiers and clear access paths | Exact prices/earnability unapproved; no stat advantage | 11, 13 |
| High school → college → professional career | Forty working school identities, shared venue kits, tier pacing | School counts are content plans, not first-playable scope | 12, school CSV |
| Home → campus → mansion practice | Reuse hub actions; casual outfits; easy teammate training | No scheduling or attendance management | 12, 13 |
| Lit 3D action + layered illustrated scenery | Shared light palette, depth/occlusion, camera envelope, texture budget | Nearby objects may need shallow or full geometry | 14 |
| Best reliable iPhone graphics and frame rate | Sustained performance, input latency, thermal scaling, wardrobe stress test | 120 fps target on capable devices; 60 fps baseline proposal | 14 |
| Broad animation coverage research | Catalogue plus actual variant/transition acceptance criteria | No claim of exhaustive basketball or production coverage | 04, 05, CSVs |
| Commercially ambitious but simple | Prioritize repeatable possession quality, usable wardrobe, retention and distribution evidence | No revenue guarantee or unannounced-AI assumption | 15, 16 |

## Change propagation procedure

Latest additions: surpass the supplied character-quality examples with distinct faces and living motion; treat fabric compression/settling as a visible requirement and evaluate actual cloth physics; exclude Euro steps and post offense; route a fresh airborne tap from dunk selection into a pose-compatible layup. These affect the move atlas, gesture states, timing checks, transition coverage, wardrobe deformation, device budget, and future online validation. See documents 19 and 20.

For each new direction, check controls; player/AI rules; states and failure paths; animation and ball authority; stats/stamina; camera; sound/haptics; customization; progression/economy; accessibility; device performance; future online authority; and acceptance criteria. Only affected areas need updates. Do not invent unrelated systems merely to fill every column.

Keep the simple player-facing action whenever possible and place necessary detail in the underlying specification. For example, "Handle makes dribbles faster" is a simple upgrade promise backed by controlled retiming, contact markers, bounded transitions, and fair defensive response.
