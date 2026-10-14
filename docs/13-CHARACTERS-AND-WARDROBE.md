# Character creation and wardrobe

## Owner direction

Substantial character creation and many purchasable appearance assets are part of the concept. Requested categories are haircuts, tattoos, jewelry, shirts, jackets, pants, and especially shoes. Barefoot and shirtless options are included. Casual looks belong in practice and eligible non-team games, while team games use uniforms.

The owner suggested that barefoot and shirtless options could be expensive. Their exact pricing, earned unlock path, and rarity remain proposals; neither should grant gameplay advantages.

**Confirmed starter outfit:** plain white tank top, gray joggers, and no tattoos. Use an original character and original garment construction. Starter shoes are not specified; propose a free original basic low-top so the default look is complete. Tattoos are intended as expensive/premium expression items; exact currency prices and earned access remain open. Skin tone, face, hair, and body should still be chosen through character creation rather than copied from a reference character.

## A simple player flow

Create player → choose appearance → save a casual look → play. The practice hub has one Style screen with categories and an immediate on-character preview. Selecting an owned item equips it; selecting an unowned item previews its clear price and unlock method. Save a small set of outfits rather than managing an inventory grid with dozens of currencies.

Separate character identity, gameplay build, and clothing. A shoe or haircut does not rewrite the player's stats. If body proportions affect reach or movement, expose that effect when choosing the build and constrain later cosmetic edits appropriately. The supported body range and gender presentation options require a dedicated design decision before estimating assets.

## Content slots and production implications

| Category | Proposed structure | Main production work |
|---|---|---|
| Face and skin | Curated face presets, skin tones, limited adjustable features | Consistent lighting, facial rig/expressions where visible |
| Hair | Original short, braided, loc, curl, fade, and longer style families | Scalp fit, silhouette, deformation, efficient materials |
| Tattoos | Original selectable designs in predefined placements | Skin UV fit, placement preview, wardrobe masking |
| Jewelry | Ear, neck, wrist options | Attachment points, restrained movement, clipping rules |
| Tops | Shirts, sleeveless tops, hoodies, jackets, shirtless | Layer compatibility, shoulder and torso deformation |
| Bottoms | Shorts, fitted pants, relaxed pants | Crouch/knee deformation and shoe overlap |
| Footwear | Original low, mid, high, knit, and court-classic silhouettes | Foot rig, sole contact, scale, materials, both feet |
| Barefoot | Dedicated bare-foot presentation | Foot/toe mesh, ground contact, animation fit; not an invisible shoe hack |
| Team uniform | School/team kit overrides | Original marks, number treatment, compatible base fit |

These are proposed content families, not a launch promise for every category variation. User-uploaded tattoo images are not included in the initial concept; a curated library keeps ownership, moderation, and UI simpler.

## Shoes: many looks from a manageable foundation

Start with approximately five original base silhouettes as a planning hypothesis: streamlined low-top, padded mid-top, supportive high-top, lightweight knit court shoe, and a simple court classic. Give each its own shape language and fictional branding. Avoid copying a recognizable commercial shoe and changing its colors.

Use controlled color/material channels for upper, panels, laces, sole, and accents. Five silhouettes with twelve authored colorways each produce sixty sellable appearance variants, but still require review for contrast, materials, thumbnails, naming, and in-game fit. Sixty variants are not sixty independently modeled shoes.

Concept images can help choose a design. A usable game shoe still needs a clean 3D mesh, UVs, textures, deformation/attachment, contact checks, and suitable detail levels. Generated images or models require human cleanup and ownership review before production use.

## Layer and compatibility rules

Use a small fixed wardrobe layer order. A jacket can automatically hide an incompatible shirt region; pants and shoes choose compatible cuffs. Store the rule with the asset so the player does not troubleshoot clipping. Avoid simulating every chain, shoelace, and jacket fold in real time.

Every asset brief records supported bodies, layers hidden, attachment points, materials, texture limits, detail levels, and permitted modes. Review an outfit in idle, deep dribble crouch, crossover, full extension, dunk, landing, and camera close-up. Review tattoos with both covered and exposed skin.

## Content scale without menu complexity

Keep the number of equip slots modest while expanding their contents over time. Organize by type, owned status, and a few collections; provide a clear search/filter only when the catalogue size justifies it. No maintenance fee, durability loss, or clothing stat system is proposed.

Use a capsule wardrobe for the future vertical slice: representative hair, one tattoo placement, one jewelry attachment, a few tops/bottoms, several shoes, barefoot, and shirtless. Prove fit and performance before commissioning hundreds of items.

Premium collections can fund continued content. The goal is desirable expression, not making the default player deliberately unattractive. Prices and release cadence depend on production cost and measured player demand, not a promise that volume alone creates revenue.
