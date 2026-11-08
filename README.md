# Thren downloads

Windows client/server and experimental Linux client downloads for friends-and-family testing. **This repository contains packaged builds and instructions, not the game's source code.**

## Download the test build

**[Open the download page — 0.4.0-private-alpha.10](https://github.com/elthrexuniverse/Thren-Downloads/releases/tag/v0.4.0-private-alpha.10)**

- **[Download Windows client ZIP](https://github.com/elthrexuniverse/Thren-Downloads/releases/download/v0.4.0-private-alpha.10/Thren-Client-0.4.0-private-alpha.10.zip)** — for Windows players.
- **[Download Windows dedicated-server ZIP](https://github.com/elthrexuniverse/Thren-Downloads/releases/download/v0.4.0-private-alpha.10/Thren-Server-0.4.0-private-alpha.10.zip)** — for the person running an independent server.
- **[Download experimental Linux client](https://github.com/elthrexuniverse/Thren-Downloads/releases/download/v0.4.0-private-alpha.10/Thren-Client-Linux-0.4.0-private-alpha.10-linux.1.tar.gz)** — Mint 21.3 Cinnamon target; [Linux launch instructions](LINUX-PLAYER-GUIDE.md).
- **[Read the testing guide](TESTING-GUIDE.md)** — setup, known issues and what to test.

Extract the complete ZIP into a new folder. Launch `Thren.exe` for the client. The server package includes `Server.cmd` and `PRIVATE-SERVER-GUIDE.md`. Unity Editor and development tools are not required. Use matching versions. GitHub's automatic **Source code** archives contain only this downloads repository's documents, not the playable game.

## Unfinished test candidate

This is **not a release-qualified alpha**. Fuel exhaustion can make standing crew pass through a falling ship's roof; keep ships fueled during this initial test. Separate-computer, real-internet and clean-Windows qualification remains unperformed. Other camera/UI/performance checks remain open. Use disposable test worlds and the supported backup workflow.

Downloads are public, but multiplayer worlds require a personal access code from the host. Never publish those codes, credentials, world data or backups here. Hosting requires the network owner's configuration; this repository does not provide a public game server or matchmaking.

Windows build source: `5fc251e4dc37029c0ad127575a41ae7b29e1c1b1`. Archive checksums and provenance are attached to the release. Publication makes the existing candidate available for testing; it does not claim that the outstanding checks passed.

## Experimental Linux client

The Linux `.10-linux.1` client is built from `8fa0d5db38ee4edbeb08fa09a97a37e40f4476cf` with a session-only access-code fix; it is intended to join the existing Windows `.10` server (protocol 15). Windows archives remain unchanged. Linux execution, graphics, input and internet connectivity have **not** been tested here. Extract the complete tar.gz and run `./Launch-Thren.sh`; paste your personal access code on each launch. See [Linux guide](LINUX-PLAYER-GUIDE.md).
