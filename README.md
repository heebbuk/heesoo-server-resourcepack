# HeesooServer resource pack

Minecraft Java 26.2 server pack for personal, non-commercial use.

[Download the pack](https://raw.githubusercontent.com/heebbuk/heesoo-server-resourcepack/6d6ee81e35812bbd808a78d495a06ae4eec99e6c/Heesoo-26.2-resources.zip)

SHA-1: `1d42c1f6aad2adab83d2d965972b9b196da01891`

Use this download URL and SHA-1 in `server.properties` (`resource-pack` and `resource-pack-sha1`). Minecraft asks the player to accept server resource packs before downloading. The server owner can require acceptance with `require-resource-pack=true`.

HeesooServer 2.4.2 adds a six-card Korean/English main menu through the `heesoo:menu` bitmap font. Its replaceable artwork is `assets/heesoo/textures/gui/main_menu.png` (1536 × 1024; keep a 3:2 aspect ratio). The matching invisible GUI item model is `heesoo:gui/empty`. This menu uses no new CustomModelData IDs. Existing weapon and Dragon resources are retained.

Original assets: [Blades of Majestica by Eftann Senpai and Zerotekz](https://www.planetminecraft.com/texture-pack/blades-of-majestica-3d-weapon-pack/) and [Impossible Dragon by McMakistein and collaborators](https://mcmakistein.com/creations/impossible_enderdragon). The archive includes the original Dragon license and full credits. Artwork, models and audio remain their creators' work; no ownership is claimed.

Technical adapters add native item model dispatch for Minecraft 26.2. Obsolete 1.21 core shader overrides are omitted, so shader-only glow and screen overlays are unavailable. Sacred Tree Blade uses the creator's retained 2D texture. In-game client rendering has not been verified automatically; check the card artwork and click alignment in a Minecraft client after accepting the pack.

This repository contains resource files only. No server worlds, player information, configuration secrets or databases are published.
