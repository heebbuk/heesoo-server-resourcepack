# HeesooServer resource pack

Minecraft Java 26.2 server pack for personal, non-commercial use.

[Download the pack](https://raw.githubusercontent.com/heebbuk/heesoo-server-resourcepack/1655fc762858f3d7d6419238dc642f27570add3e/Heesoo-26.2-resources.zip)

SHA-1: `3e120e042dc1658adab2eff8b3f3c55e53d3ff21`

Use this download URL and SHA-1 in `server.properties` (`resource-pack` and `resource-pack-sha1`). Minecraft asks the player to accept server resource packs before downloading. The server owner can require acceptance with `require-resource-pack=true`.

HeesooServer 2.4.11 displays a six-card Korean/English main menu through the `heesoo:menu` bitmap font. Its replaceable artwork is `assets/heesoo/textures/gui/main_menu.png` (1536 × 1024; retain this exact size). The font slices it into 24 cells of 256 × 256 pixels, respecting Minecraft's font atlas limit, and composes the full 162 × 108 GUI without modifying the artwork. The matching invisible GUI item model is `heesoo:gui/empty`. This menu uses no new CustomModelData IDs. Existing weapon and Dragon resources are retained.

The 36-slot (9 by 4) finance menu uses `heesoo:finance` and `assets/heesoo/textures/gui/finance_menu.png` (2172 × 724; retain the exact dimensions). Three cards — 저축 / SAVINGS, 주식 / STOCK and 기부 / DONATE — occupy nine clickable slots each. Its font uses atlas-safe source cells and 54-pixel card boundaries. The plugin draws the header 금융 메뉴 separately. Slots 27–35 form a full-width blue 뒤로가기 / BACK button that returns to the main menu. Its `heesoo:back` font reads the middle row of `assets/heesoo/textures/gui/back_menu.png` (2172 × 724, three stacked 9:1 banners) as nine 241 × 241 source cells, composing a single 162 × 18 bottom-row banner. All three original finance cards retain their exact 3 by 3 click areas. No new CustomModelData IDs are required.

The 36-slot growth menu uses `heesoo:growth` and `assets/heesoo/textures/gui/growth_menu.png` (2172 × 724), with three 3×3 cards: 숙련도허브 / SKILL HUB, 수리 / REPAIR, 무기강화 / UPGRADE. Every card slot opens its existing server feature, including the implemented 1–20 equipment enhancement system. Slots 27–35 reuse the blue BACK banner.

The 54-slot shop menu uses `heesoo:shop` and `assets/heesoo/textures/gui/shop_menu.png` (2160 × 1200). Top cards occupy SHOP 5×3 and WEAPON SHOP 4×3; lower cards occupy FISH MARKET 4×2 and SELL 5×2. Slots 45–53 use `heesoo:back_shop`, which reuses the original BACK image at the sixth row. Every card slot opens the existing shop or sale window. Keep PNG dimensions and card boundaries when replacing artwork. Growth/shop source font cells are 181×120 / 120×120, within the font atlas limit. GUI backgrounds require no new CustomModelData. Growth and shop artwork was generated for this server from the owner-provided design references; shop card placement was corrected with the owner’s approval. Validation: 38 unit tests and 300 isolated Paper menu checks passed; final rendering still needs a Minecraft client check.

Original assets: [Blades of Majestica by Eftann Senpai and Zerotekz](https://www.planetminecraft.com/texture-pack/blades-of-majestica-3d-weapon-pack/) and [Impossible Dragon by McMakistein and collaborators](https://mcmakistein.com/creations/impossible_enderdragon). The archive includes the original Dragon license and full credits. Artwork, models and audio remain their creators' work; no ownership is claimed.

Technical adapters add native item model dispatch for Minecraft 26.2. Obsolete 1.21 core shader overrides are omitted, so shader-only glow and screen overlays are unavailable. Sacred Tree Blade uses the creator's retained 2D texture. In-game client rendering has not been verified automatically; check the card artwork and click alignment in a Minecraft client after accepting the pack.

This repository contains resource files only. No server worlds, player information, configuration secrets or databases are published.
