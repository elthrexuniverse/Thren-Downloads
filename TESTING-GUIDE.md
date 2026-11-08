# Thren — friends-and-family test build

> Linux Mint testers: use the separate `.10-linux.1` tar.gz and [Linux guide](LINUX-PLAYER-GUIDE.md). It is intended for this Windows `.10` host; native Linux execution remains unverified. Windows instructions below apply to Windows packages.

Version **0.4.0-private-alpha.10**, Windows x64. This is an unfinished test candidate, not a release-qualified game. The downloads are public; each multiplayer world still requires the host's private access code.

## Players

1. Download **Thren-Client-0.4.0-private-alpha.10.zip** from this release's Assets. Do not choose GitHub's automatic “Source code” ZIP or tarball: those contain this downloads repository's documentation, not the game.
2. Extract the entire ZIP into a new folder. Do not run from inside the ZIP or copy only the executable.
3. Read `START-HERE.md`, then launch `Thren.exe`. Unity Editor and development tools are not needed. If Microsoft's x64 Visual C++ runtime is missing, the package includes the signed prerequisite under `Prerequisites`; follow the included instructions. The game itself is not code-signed. Do not disable Windows protections.
4. Get the server address and **your own personal access code** privately from your host. Open Private Multiplayer, enter those details and join. Every player and the server must use the same `.10` release.
5. Use the same personal code or saved connection when returning. Sharing another player's code opens their identity; a display name is not an account.

## Dedicated-server host

Download **Thren-Server-0.4.0-private-alpha.10.zip**, extract it fully into a separate new folder and read `PRIVATE-SERVER-GUIDE.md`. Create a disposable new test world for this candidate; keep existing worlds and backups separate.

The guide covers configuration, independent world initialization, issuing each player a code, starting/stopping, backups, recovery and diagnostics. The default listener is local-only (`127.0.0.1`). Internet hosting needs an appropriate listening address and a reachable **TCP port, default 27019**, configured by the network owner. The package does not alter your firewall/router. Some connections using carrier-grade NAT cannot accept direct incoming connections. No automatic relay or public matchmaking is supplied.

Player-hosted sessions use the game's existing hosting and private-access menus. Host and dedicated worlds use the same authoritative persistence model. Read the guide before moving or restoring a world between modes.

Never upload server data, world saves, backups, invitations, operator tokens or saved credentials to this public repository. Send each access code only to its intended player.

## Known problems and testing limits

- **Fuel exhaustion can cause standing crew to pass through the roof of a falling ship.** Keep ships fueled for this first test. Exhaustion is a confirmed unresolved active-player collision defect; it is not fixed by this build's camera changes.
- Separate physical computers, real internet connections and clean Windows installations have **not yet been qualified**. Local multiplayer and simulated delay do not prove those environments work.
- Some camera, normal-menu, resolution/scaling, load and long-session checks remain open. This is not an unaided-human usability or performance certification.
- Cabin pressure/life support is not simulated. Airtight geometry does not establish breathable-cabin survival; the existing survival hazard is tied to the survey area.
- Logout/rejoin position and seat behavior has incomplete qualification. Preserve disposable test progress with the supported backups; do not assume this candidate is suitable for an irreplaceable world.
- Solo and multiplayer hotbar shortcuts remain separate, although inventories and ownership persist. Reassign shortcuts by dragging as needed.

## Useful first test

Record Windows/hardware, actual computers and network paths, hosting mode, setup difficulties and elapsed time. Try independent launch, fresh server initialization, two authorized players joining, gathering/crafting, crew permissions and known-quantity cargo transfers, fueled ship operation, a normal leave/rejoin, safe server shutdown/restart and return to the same belongings. Preserve failures rather than replacing the world to hide them.

Read `EXTERNAL-ACCEPTANCE.md` in the package for the broader checklist. Full qualification remains larger than a short two-person smoke test. Avoid destructive failure tests on original player worlds.

For a bug, privately send your host the version, time, reproduction steps, expected/actual result and screenshots without access codes. Review diagnostics before sharing; ordinary reports should not contain private saves or credentials.

## Build identity and existing evidence

Executable source: `5fc251e4dc37029c0ad127575a41ae7b29e1c1b1`; Unity 6000.3.26f1; non-development Windows Release; protocol 15; compatibility `thren-private-alpha-1`.

Existing evidence includes 851 EditMode and four PlayMode passes (including opt-ins), 15 packaged native-server checks, bounded local rendered flight and measured delayed encrypted traffic, and earned-state continuity across dedicated, solo and hosted copies. These do not override the known failing fuel-loss case or establish external/human acceptance.

The original client/server archives are unchanged. Verify them using `SHA256SUMS.txt`, `release-manifest.json` and the manifests inside each package. This public repository distributes binaries and documentation only; source development remains separate.
