# CUBOMetre

Public issue tracker, release notes, and architecture overview for [cubometre.online](https://cubometre.online), the multiplayer platform built for the [Steve Blocks](https://www.youtube.com/@SteveBlocks012) community.

[![Portal](https://img.shields.io/badge/platform-cubometre.online-334155?style=flat-square&labelColor=1e293b)](https://cubometre.online)
[![Discord](https://img.shields.io/badge/discord-Steve%20Blocks-334155?style=flat-square&labelColor=1e293b)](https://discord.gg/JNA8TwBtBe)
[![Core Mod](https://img.shields.io/badge/mod-CUBOMod-334155?style=flat-square&labelColor=1e293b)](https://github.com/Aurbey/CUBOMod)
[![Issues](https://img.shields.io/github/issues/Aurbey/CUBOMetre?style=flat-square&color=334155&labelColor=1e293b)](https://github.com/Aurbey/CUBOMetre/issues)

### Context

CUBOMetre is a private, 24/7 multiplayer gaming platform engineered on dedicated bare-metal hardware for the [Steve Blocks](https://www.youtube.com/@SteveBlocks012) community. It pairs high-performance Minecraft Fabric architecture with custom economy mechanics, live web telemetry, and community automation.

This repository is the public coordination hub for player feedback, bug reports, and ecosystem documentation while proprietary server configurations and world data remain private.

### Architecture

- **Edge Routing & Ingress:** Traffic enters via HAProxy with PROXY protocol forwarding into a Velocity proxy cluster. This conceals backend server nodes while preserving client IPs for moderation and rate limiting.
- **Game Engine & Modding:** Vanilla-client Fabric backend powered by [CUBOMod](https://github.com/Aurbey/CUBOMod), running custom banking, leveling, and server-side mechanics with zero client mod requirements.
- **Live-Ops & Web:** Production portal at [cubometre.online](https://cubometre.online) with an interactive 3D world map (BlueMap) and real-time player telemetry.
- **Bot Bridge & Automation:** Bidirectional Python bridge integrating Discord with in-game chat, transaction audits, and custom stat card rendering.
- **Disaster Recovery:** Daily automated deduplicated backups via BorgBackup sent to remote encrypted storage.

### Community & Feedback

Report bugs, server latency issues, or feature proposals in [GitHub Issues](https://github.com/Aurbey/CUBOMetre/issues). Include your in-game username, coordinates (if applicable), and reproduction steps.

---
Maintained by [Denis (Aurbey)](https://github.com/Aurbey).
