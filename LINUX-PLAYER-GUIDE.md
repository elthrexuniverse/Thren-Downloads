# Thren Linux test client

This native x86-64 Linux client is for the friend's **Linux Mint 21.3 Cinnamon** computer. It is an experimental cross-built candidate: Linux launch, graphics, input and internet play still require testing on that computer. Mint Cinnamon is not a separately qualified Unity platform. No Wine, Unity Editor, Windows runtime installer or developer tools are required to try this package.

## Install and join

1. Download `Thren-Client-Linux-0.4.0-private-alpha.10-linux.1.tar.gz` from the public Thren-Downloads release. Extract the entire archive to a new folder in your home directory. Keep all files together; do not overwrite an existing installation.
2. Open that folder in a terminal and run `./Launch-Thren.sh`. The archive preserves executable permissions. If your extraction tool removes them, run `chmod +x Launch-Thren.sh Thren.x86_64` once, then launch again. Do not run the game as root.
3. Open Private Multiplayer. Enter the host's address (`hostname:port` or `IPv4:port`), your display name, and **your own personal access code** supplied privately by the host. Select Join Server. A remote host's address is not `127.0.0.1`.
4. This client uses protocol **15**, compatibility **thren-private-alpha-1**, and is intended to join the existing Windows **0.4.0-private-alpha.10** server. Its source revision is separately recorded in `build-info.json`. The server does not need a Linux-specific build.
5. Leave through the game menu. After relaunching, paste the same personal code again to return to the same character and belongings. Linux does **not save access codes**; there is no plaintext fallback. Keep your code privately or ask the host to rotate access for your existing identity. Changing your display name does not create a different character.

The scope of this package is joining a Windows host/server. Solo and Linux player-hosting are not yet qualified. The Windows-only separate-server launcher is not a Linux server distribution. Existing saves and protocol are unchanged; no account or save migration is required.

## If it fails

- If the game does not open, run it from a terminal and retain the printed error and `~/.config/unity3d/DefaultCompany/Thren/Player.log` before another launch. Record your Mint version, graphics card/driver and whether you use X11 or Wayland. Do not install arbitrary DLLs or disable security settings.
- If graphics fail, a diagnostic launch with `./Launch-Thren.sh -force-glcore` selects OpenGL. This is a troubleshooting option, not a verified fix for every driver.
- Timeout/unreachable: verify the host's public/private-network address and configured TCP port (usually 27019). There is no automatic relay; the host must arrange reachable networking. This package makes no firewall/router changes.
- Invalid/revoked code: ask the host to check access. Never use someone else's code; it owns their character.
- Already connected: close your old session and allow the server's disconnect timeout before reconnecting. A version error requires a compatible package.
- Recovery error: preserve the existing identity and ask the host to recover the complete world. Do not create replacement characters to hide a recovery failure.

Logs may contain names and addresses. Review them before sharing. Never include access codes, private server identity files, saves or backups in public bug reports.

## First Linux acceptance test

Record exact client/server build labels. Launch on Mint without Unity installed; join with a personal code; verify terrain, mouse/camera, WASD, jump, Tab inventory, Q crafting and Esc; mine and transfer a small stack; leave/relaunch/rejoin and verify identity and inventory; repeat after a safe server restart. Then play with the Windows client connected concurrently. Record failures rather than treating cross-compilation or local Windows tests as Linux/internet proof.

Known prior gameplay defect remains: occupants can cross an intact falling cabin after ship fuel exhaustion. Avoid using valuable worlds for this test; this candidate is not a fully qualified alpha. Other camera, normal UI, human and external-network acceptance gaps remain open.

Platform references: [Mint 21.3 Cinnamon](https://www.linuxmint.com/rel_virginia_cinnamon.php), [Unity 6000.3 requirements](https://docs.unity.com/en-us/engine/6000.3/manual/get-started/install-and-upgrade/getting-started-installing-unity/system-requirements).
