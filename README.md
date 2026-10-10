# HeesooServer resource pack

Minecraft Java 26.2 server pack for personal, non-commercial use.

[Download the pack](https://raw.githubusercontent.com/heebbuk/heesoo-server-resourcepack/main/Heesoo-26.2-resources.zip)

SHA-1: `e53c97b8fa7d246ac083000cf7e4da579b8dd950`

Use this download URL and SHA-1 in `server.properties` (`resource-pack` and `resource-pack-sha1`). Minecraft asks the player to accept server resource packs before downloading. The server owner can require acceptance with `require-resource-pack=true`.

HeesooServer 2.4.11 displays a six-card Korean/English main menu through the `heesoo:menu` bitmap font. Its replaceable artwork is `assets/heesoo/textures/gui/main_menu.png` (1536 × 1024; retain this exact size). The font slices it into 24 cells of 256 × 256 pixels, respecting Minecraft's font atlas limit, and composes the full 162 × 108 GUI without modifying the artwork. The matching invisible GUI item model is `heesoo:gui/empty`. This menu uses no new CustomModelData IDs. Existing weapon and Dragon resources are retained.

The 36-slot (9 by 4) finance menu uses `heesoo:finance` and `assets/heesoo/textures/gui/finance_menu.png` (2172 × 724; retain the exact dimensions). Three cards — 저축 / SAVINGS, 주식 / STOCK and 기부 / DONATE — occupy nine clickable slots each. Its font uses atlas-safe source cells and 54-pixel card boundaries. The plugin draws the header 금융 메뉴 separately. Slots 27–35 form a full-width blue 뒤로가기 / BACK button that returns to the main menu. Its `heesoo:back` font reads the middle row of `assets/heesoo/textures/gui/back_menu.png` (2172 × 724, three stacked 9:1 banners) as nine 241 × 241 source cells, composing a single 162 × 18 bottom-row banner. All three original finance cards retain their exact 3 by 3 click areas. No new CustomModelData IDs are required.

The 36-slot growth menu uses `heesoo:growth` and `assets/heesoo/textures/gui/growth_menu.png` (2172 × 724), with three 3×3 cards: 숙련도허브 / SKILL HUB, 수리 / REPAIR, 무기강화 / UPGRADE. Every card slot opens its existing server feature, including the implemented 1–20 equipment enhancement system. Slots 27–35 reuse the blue BACK banner.

The 54-slot shop menu uses `heesoo:shop` and `assets/heesoo/textures/gui/shop_menu.png` (2160 × 1200). Top cards occupy SHOP 5×3 and SPECIAL SHOP 4×3; lower cards occupy FISH MARKET 4×2 and SELL 5×2. Slots 45–53 use `heesoo:back_shop`, which reuses the original BACK image at the sixth row. Every card slot opens the existing shop or sale window. Keep PNG dimensions and card boundaries when replacing artwork. Growth/shop source font cells are 181×120 / 120×120, within the font atlas limit. GUI backgrounds require no new CustomModelData. Growth and shop artwork was generated for this server from the owner-provided design references; shop card placement was corrected with the owner’s approval. Validation: 38 unit tests and 300 isolated Paper menu checks passed; final rendering still needs a Minecraft client check.

Original assets: [Blades of Majestica by Eftann Senpai and Zerotekz](https://www.planetminecraft.com/texture-pack/blades-of-majestica-3d-weapon-pack/) and [Impossible Dragon by McMakistein and collaborators](https://mcmakistein.com/creations/impossible_enderdragon). The archive includes the original Dragon license and full credits. Artwork, models and audio remain their creators' work; no ownership is claimed.

Technical adapters add native item model dispatch for Minecraft 26.2. Obsolete 1.21 core shader overrides are omitted, so shader-only glow and screen overlays are unavailable. Sacred Tree Blade uses the creator's retained 2D texture. In-game client rendering has not been verified automatically; check the card artwork and click alignment in a Minecraft client after accepting the pack.

This repository contains resource files only. No server worlds, player information, configuration secrets or databases are published.

## HeesooServer 2.5.0

The shop's top-right card now opens SPECIAL SHOP (특별상점). The original SHOP, FISH MARKET and SELL images are byte-for-byte retained. New special-menu artwork is `assets/heesoo/textures/gui/special_menu.png` (2160×720), with XP SHOP on the left five columns and WEAPON SHOP on the right four columns. New experience-menu artwork is `assets/heesoo/textures/gui/experience_menu.png` (2160×960), six 3×2 cards in a 54-slot inventory; the final row reuses BACK. Both new bitmap fonts use 120×120 source cells.

Default text uses Nanum Gothic Bold; supplementary fonts `heesoo:regular` and `heesoo:extra_bold` use Regular and ExtraBold. Fonts are bundled under the SIL Open Font License, included as `NanumGothic-OFL.txt`. Variation selectors VS15/VS16 have zero advance. No additional CustomModelData IDs are introduced.

Validation: 53 unit tests, 294 isolated Paper checks, all 71 font-provider definitions parsed by the actual Minecraft 26.2 client codec. 1,849 existing resource files remain unchanged. Client screenshot and 2–4-player balance playtesting still require a live session.

Font size adjustment: Nanum Gothic Bold, Regular and ExtraBold each use size 10 (previously 11). Card artwork, bitmap GUI fonts and all other pack files remain unchanged.

## HeesooServer 2.5.1

Eight native Minecraft 26.2 equipment definitions hide worn humanoid armor (leather, chainmail, copper, iron, gold, diamond, netherite, turtle shell), including trim and enchantment effects. Inventory icons, defense values, elytra and existing animal armor mappings are preserved. All existing ZIP entries remain byte-for-byte unchanged; Nanum Gothic fonts remain size 10. No new bitmap assets or CustomModelData IDs are required. Equipment definitions were validated with the actual Minecraft 26.2 codec.

## HeesooServer 2.5.2

Three native Mythical Staff item models (nongko), Wither's Wrath music/trophy resources (ImHer0), and the expanded special shop back row. Existing GUI artwork, Nanum Gothic size 10, armor visibility and weapon models remain preserved. Existing sounds are retained with new Wither events added. Attribution and compatibility changes: ATTRIBUTIONS-2.5.2.md inside the ZIP.

## HeesooServer 2.6.0

Cooking laboratory GUI, fourteen food icons, four held platter models and forty fish icons. Existing 1,900 resources remain unchanged.

2.6.0 resource fix: register the shared food/fish texture in the Minecraft 26.2 item atlas.

Staff texture fix: register the five existing staff textures in Minecraft 26.2 item atlas. All other ZIP entries are unchanged. Native item/model codecs pass (3 item definitions, 9 models); actual client screenshot check remains pending.

## Content patch: shared panels and fishing gauge

HeesooServer menus now use a restrained blue-gray panel family, native item buttons, Nanum Gothic typography and a single back button. The earlier illustrated card assets remain in the archive but are no longer the active menu layout. Six atlas-safe panel textures live at assets/heesoo/textures/gui/panel_1.png through panel_6.png; slot interiors are transparent so they cannot cover item icons. External InfiniteShops and EMF chest menus use the same panel font through their existing holders. The fishing title gauge uses heesoo:fishing_gauge. Staff gameplay/datapack was removed; retained models only preserve appearance of old items. No new CustomModelData IDs. Minecraft client visual inspection remains required.
