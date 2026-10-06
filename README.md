# HeesooServer resource pack

Minecraft Java 26.2 server pack for personal, non-commercial use.

[Download the pack](https://raw.githubusercontent.com/heebbuk/heesoo-server-resourcepack/a99f0bc23dabd9d4d077cc1ccd9ae7eab7a70601/Heesoo-26.2-resources.zip)

SHA-1: `bfdf1808036db8589cb8b6f4bcf10d16f0fe0d12`

Use this download URL and SHA-1 in `server.properties` (`resource-pack` and `resource-pack-sha1`). Minecraft asks the player to accept server resource packs before downloading. The server owner can require acceptance with `require-resource-pack=true`.

HeesooServer 2.4.3 displays a six-card Korean/English main menu through the `heesoo:menu` bitmap font. Its replaceable artwork is `assets/heesoo/textures/gui/main_menu.png` (1536 × 1024; retain this exact size). The font slices it into 24 cells of 256 × 256 pixels, respecting Minecraft's font atlas limit, and composes the full 162 × 108 GUI without modifying the artwork. The matching invisible GUI item model is `heesoo:gui/empty`. This menu uses no new CustomModelData IDs. Existing weapon and Dragon resources are retained.

Original assets: [Blades of Majestica by Eftann Senpai and Zerotekz](https://www.planetminecraft.com/texture-pack/blades-of-majestica-3d-weapon-pack/) and [Impossible Dragon by McMakistein and collaborators](https://mcmakistein.com/creations/impossible_enderdragon). The archive includes the original Dragon license and full credits. Artwork, models and audio remain their creators' work; no ownership is claimed.

Technical adapters add native item model dispatch for Minecraft 26.2. Obsolete 1.21 core shader overrides are omitted, so shader-only glow and screen overlays are unavailable. Sacred Tree Blade uses the creator's retained 2D texture. In-game client rendering has not been verified automatically; check the card artwork and click alignment in a Minecraft client after accepting the pack.

This repository contains resource files only. No server worlds, player information, configuration secrets or databases are published.
