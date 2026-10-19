# FINDINGS — getboring/didymus-os   (save as repo-docs-review/sheets/getboring__didymus-os.md)
- reviewed_sha: 874faa799c6d98706d693b3eaf37794e994b4701
- main_moved: no
- default_branch: main / reviewed_at (ET): 2026-10-19 06:17 ET / reviewer (agent id): bc-914db389-61da-57f9-815f-14fa74ec805a
- status: DORMANT  evidence: INFERENCE. FACT: the GitHub repo is not archived — https://github.com/getboring/didymus-os . FACT: `Boring-Works/didymus-os` does not resolve — https://github.com/Boring-Works/didymus-os . FACT: head commit `874faa799c6d98706d693b3eaf37794e994b4701` is dated 2026-09-06 19:48:53 -0400, 43 days before 2026-10-19. FACT: one merged pull request and no issues — https://github.com/getboring/didymus-os/pull/1 . No doc line says the work is paused or will resume. LIVE needs a deploy and a commit in the last 90 days. ACTIVE needs a commit in the last 30 days. PAUSED needs an intent-to-resume signal in the 30–180 day window. That signal is absent, so the status is DORMANT.
- live since: not deployed — FACT: deployments list is empty — https://api.github.com/repos/getboring/didymus-os/deployments . FACT: Pages returns 404 — https://api.github.com/repos/getboring/didymus-os/pages . FACT: QUOTE «this tree has never been installed.» — hosts/didymus-lab/configuration.nix:40 @874faa799c6d98706d693b3eaf37794e994b4701. No wrangler config and no deploy workflow are in the tree at reviewed_sha.
- what it is (one sentence, from code not docs): A Nix flake that builds two NixOS configurations (didymus-lab and qemu-lab), an opt-in ISO, a QEMU VM script, and a NixOS VM test that boots the lab modules and checks a twin-init oneshot plus files under /etc/didymus.
- live where: none

## Docs claim (quote, file:line)

- FACT: QUOTE «# Didymus OS» — README.md:1 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «**A twin of NixOS.**» — README.md:3 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| **Twin generations** | Every rebuild produces a verifiable pair (primary + twin) with signed receipts |» — README.md:21 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| **Stable twin / Experimental twin** | Two concurrent profiles you can switch between without losing the other |» — README.md:22 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| **Receipts** | Ed25519-signed, content-addressed records of what changed (ScopeBlind-ready) |» — README.md:23 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «**v0.1 — Scaffolding** (September 2026)» — README.md:29 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «Flake + modules + lab host + QEMU twin + NixOS VM test + cloud CI.» — README.md:30 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «A physical machine is not required to evaluate, build, or boot a generation.» — README.md:31 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nix eval .#nixosConfigurations.qemu-lab.config.system.build.toplevel.drvPath» — README.md:43 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nix build .#checks.x86_64-linux.didymus-lab -L» — README.md:47 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nix build .#qemu-vm» — README.md:50 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «From a phone: push to `main` or open a PR. GitHub Actions and Garnix do steps 1–3.» — README.md:54 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| `nixosConfigurations.didymus-lab` | Physical lab twin | labelled `didymus-root` / `didymus-boot` |» — README.md:63 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| `nixosConfigurations.qemu-lab` | Same software, QEMU | virtio, auto-format |» — README.md:64 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| `checks.x86_64-linux.didymus-lab` | Headless NixOS VM test | none (test driver) |» — README.md:65 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| `packages.qemu-vm` | Interactive `run-didymus-qemu-vm` | none on the host |» — README.md:66 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «| `packages.iso` | Live installer ISO | opt-in, not a CI gate |» — README.md:67 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «├── flake.lock                # Pinned nixos-26.05» — README.md:74 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «├── profiles/                 # Ready-to-use profiles (desktop, server, agent, etc.)» — README.md:83 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «Every meaningful change leaves a receipt.» — README.md:93 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- [x] Cloud CI (GitHub Actions + Garnix)» — README.md:99 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- [ ] Twin generation manager (systemd + CLI)» — README.md:100 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- [ ] Signed receipts (Ed25519 + content-addressed)» — README.md:101 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- [ ] `didymus` CLI (`switch`, `twin`, `receipts`, `verify`)» — README.md:102 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- [ ] Minimal desktop + server profiles» — README.md:103 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- [ ] ISO builder» — README.md:104 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «AGPL-3.0-or-later» — README.md:110 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «https://getboring.io · https://codyboring.com» — README.md:117 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «`didymus-lab` (physical) is the same software as `qemu-lab`.» — docs/TESTING.md:18 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «bootable in QEMU: it expects disks labelled `didymus-root` and `didymus-boot`.» — docs/TESTING.md:19 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «It builds everything in `garnix.yaml` (eval, VM» — docs/TESTING.md:31 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «test, QEMU closure).» — docs/TESTING.md:32 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «as `getboring/boring-agent-appliance`.» — docs/TESTING.md:34 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- hostname `didymus-lab`, version `0.1.0-scaffold`» — docs/TESTING.md:46 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- `didymus-twin-init.service` ran and stayed active» — docs/TESTING.md:48 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- `/var/lib/didymus/receipts/.initialized` exists and names `stable-experimental`» — docs/TESTING.md:49 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «2. **Receipts** — signed, content-addressed records of what changed.» — docs/philosophy.md:11 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- **ScopeBlind** — receipts are designed to be compatible with Ed25519 / Cedar policy verification» — docs/philosophy.md:39 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «v0.1 Imagine drafts — twin mark, wordmark, boot splash, boot animation.» — branding/README.md:3 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: no CLAUDE.md, AGENTS.md, PLAN*, ROADMAP*, THE-PLAN*, or .boring/project.json is in `git ls-tree` at reviewed_sha. OBSERVATION: the markdown files are README.md, docs/TESTING.md, docs/philosophy.md, and branding/README.md.

## Code shows (entrypoints, routes, schema, deploy config, CI; file:line)

- FACT: QUOTE «description = "Didymus OS — a twin of NixOS. Declarative, verifiable, boring on purpose.";» — flake.nix:2 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «# Current stable. 24.11 is EOL; this matches getboring/boring-agent-appliance.» — flake.nix:5 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nixpkgs.url = "github:NixOS/nixpkgs/nixos-26.05";» — flake.nix:6 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «"rev": "fcb8fcd6bf2d0adecae5bd491afaaaf8311b758d"» — flake.lock:9 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «"ref": "nixos-26.05"» — flake.lock:14 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./modules/didymus.nix» — flake.nix:17 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./modules/boring.nix» — flake.nix:18 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./modules/twin.nix» — flake.nix:19 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «devShells.${system}.default = pkgs.mkShell {» — flake.nix:31 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «name = "didymus-os";» — flake.nix:32 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «didymus-lab = mkHost [» — flake.nix:50 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./hosts/didymus-lab/configuration.nix» — flake.nix:51 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./hosts/didymus-lab/hardware.nix» — flake.nix:52 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «qemu-lab = mkHost [» — flake.nix:56 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./hosts/didymus-lab/configuration.nix» — flake.nix:57 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./hosts/qemu-lab/default.nix» — flake.nix:58 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «packages.${system} = {» — flake.nix:62 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «default = self.nixosConfigurations.didymus-lab.config.system.build.toplevel;» — flake.nix:63 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «qemu-vm = self.nixosConfigurations.qemu-lab.config.system.build.vm;» — flake.nix:64 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «# ISO is opt-in: large, and not part of `nix flake check`.» — flake.nix:65 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «iso =» — flake.nix:66 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «./iso/iso.nix» — flake.nix:68 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «checks.${system}.didymus-lab = pkgs.testers.runNixOSTest {» — flake.nix:74 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «imports = didymusModules ++ [ ./hosts/didymus-lab/configuration.nix ];» — flake.nix:80 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.wait_for_unit("multi-user.target")» — flake.nix:88 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.wait_for_unit("didymus-twin-init.service")» — flake.nix:89 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.wait_for_unit("sshd.service")» — flake.nix:90 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «version = machine.succeed("cat /etc/didymus/version").strip()» — flake.nix:93 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «assert version == "0.1.0-scaffold", version» — flake.nix:94 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «hostname = machine.succeed("hostname").strip()» — flake.nix:95 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «assert hostname == "didymus-lab", hostname» — flake.nix:96 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.succeed("test -f /etc/didymus/README")» — flake.nix:97 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.succeed("test -f /etc/didymus/TWIN.md")» — flake.nix:98 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.succeed("test -f /etc/didymus/TIRED-TEST.md")» — flake.nix:99 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.succeed("test -f /var/lib/didymus/receipts/.initialized")» — flake.nix:103 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «assert "stable-experimental" in init, init» — flake.nix:105 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «machine.succeed("systemctl is-active didymus-twin-init.service")» — flake.nix:108 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «default = "0.1.0-scaffold";» — modules/didymus.nix:20 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «default = "didymus";» — modules/didymus.nix:26 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «twinMode = mkOption {» — modules/didymus.nix:30 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «type = types.enum [ "stable-experimental" "primary-mirror" "disabled" ];» — modules/didymus.nix:31 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «default = "stable-experimental";» — modules/didymus.nix:32 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «system.nixos.label = "didymus-${cfg.version}";» — modules/didymus.nix:51 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «the didymus CLI (coming soon).» — modules/didymus.nix:58 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «# Placeholder twin service (will become real later)» — modules/twin.nix:48 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «systemd.services.didymus-twin-init = {» — modules/twin.nix:49 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «Type = "oneshot";» — modules/twin.nix:54 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «RemainAfterExit = true;» — modules/twin.nix:55 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «mkdir -p ${twinCfg.receiptDir}» — modules/twin.nix:59 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «if [ ! -f ${twinCfg.receiptDir}/.initialized ]; then» — modules/twin.nix:60 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «Mode: ${cfg.twinMode}» — modules/twin.nix:63 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «environment.etc."didymus/TWIN.md".text = ''» — modules/twin.nix:73 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «Receipts will eventually be:» — modules/twin.nix:87 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- content-addressed» — modules/twin.nix:88 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- Ed25519 signed (ScopeBlind-compatible)» — modules/twin.nix:89 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «For now use standard nixos-rebuild; the twin layer is scaffolding only.» — modules/twin.nix:98 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «# environment.systemPackages = [ pkgs.didymus-cli ];» — modules/twin.nix:102 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «default = "/var/lib/didymus/receipts";» — modules/twin.nix:28 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «PasswordAuthentication = mkDefault false;» — modules/boring.nix:35 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «PermitRootLogin = mkDefault "prohibit-password";» — modules/boring.nix:36 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «version = "0.1.0-scaffold";» — hosts/didymus-lab/configuration.nix:10 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «hostname = "didymus-lab";» — hosts/didymus-lab/configuration.nix:11 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «users.users.cody = {» — hosts/didymus-lab/configuration.nix:18 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «"wheel"» — hosts/didymus-lab/configuration.nix:22 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «initialPassword» — hosts/didymus-lab/configuration.nix:26 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «CHANGE ME — scaffolding only» — hosts/didymus-lab/configuration.nix:26 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «system.stateVersion = "26.05";» — hosts/didymus-lab/configuration.nix:41 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «device = "/dev/disk/by-label/didymus-root";» — hosts/didymus-lab/hardware.nix:9 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «device = "/dev/disk/by-label/didymus-boot";» — hosts/didymus-lab/hardware.nix:13 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «# Same software as didymus-lab, no physical disks.» — hosts/qemu-lab/default.nix:2 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «imports = [ "${modulesPath}/profiles/qemu-guest.nix" ];» — hosts/qemu-lab/default.nix:14 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «networking.hostName = lib.mkForce "didymus-qemu";» — hosts/qemu-lab/default.nix:16 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «device = "/dev/disk/by-label/nixos";» — hosts/qemu-lab/default.nix:22 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «autoFormat = true;» — hosts/qemu-lab/default.nix:24 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «services.getty.autologinUser = "cody";» — hosts/qemu-lab/default.nix:28 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: locked nixpkgs qemu-guest.nix line 2 is `virtio).` and line 11 is `"virtio_blk"` — https://github.com/NixOS/nixpkgs/blob/fcb8fcd6bf2d0adecae5bd491afaaaf8311b758d/nixos/modules/profiles/qemu-guest.nix
- FACT: QUOTE «hostname = "didymus-iso";» — iso/iso.nix:10 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «volumeID = "DIDYMUS_OS";» — iso/iso.nix:16 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «# profiles/server.nix — minimal durable server profile» — profiles/server.nix:1 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «services.xserver.enable = false;» — profiles/server.nix:5 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: no other Nix file imports profiles/server.nix. The flake module list is only the three paths at flake.nix:17, flake.nix:18, and flake.nix:19.
- FACT: QUOTE «echo "This script is a placeholder."» — scripts/init-repo.sh:6 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- checks.x86_64-linux.*» — garnix.yaml:8 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- devShells.x86_64-linux.default» — garnix.yaml:9 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- packages.x86_64-linux.default» — garnix.yaml:10 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- packages.x86_64-linux.qemu-vm» — garnix.yaml:11 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- nixosConfigurations.didymus-lab» — garnix.yaml:12 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- nixosConfigurations.qemu-lab» — garnix.yaml:13 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «- packages.x86_64-linux.iso» — garnix.yaml:15 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «name: CI» — .github/workflows/ci.yml:1 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «on:» — .github/workflows/ci.yml:3 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «push:» — .github/workflows/ci.yml:4 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «branches: [main]» — .github/workflows/ci.yml:5 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «pull_request:» — .github/workflows/ci.yml:6 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «workflow_dispatch:» — .github/workflows/ci.yml:7 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «eval:» — .github/workflows/ci.yml:17 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «name: Eval hosts (no KVM)» — .github/workflows/ci.yml:18 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «uses: DeterminateSystems/determinate-nix-action@61cbfe2efc2d4e7a8a6d56967c3c1058e846c858 # v3» — .github/workflows/ci.yml:25 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nix eval .#nixosConfigurations.didymus-lab.config.system.build.toplevel.drvPath» — .github/workflows/ci.yml:33 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nix eval .#nixosConfigurations.qemu-lab.config.system.build.toplevel.drvPath» — .github/workflows/ci.yml:34 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «nix:» — .github/workflows/ci.yml:36 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «name: NixOS VM test and QEMU closure» — .github/workflows/ci.yml:37 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «needs: eval» — .github/workflows/ci.yml:39 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «run: test -e /dev/kvm» — .github/workflows/ci.yml:51 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «run: nix flake check -L --show-trace» — .github/workflows/ci.yml:54 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «run: nix build .#qemu-vm -L» — .github/workflows/ci.yml:57 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: QUOTE «GNU AFFERO GENERAL PUBLIC LICENSE» — LICENSE:1 @874faa799c6d98706d693b3eaf37794e994b4701
- FACT: branding image files are in branding/ and no Nix file references branding/, logo-mark, or boot-splash (search of the tree at reviewed_sha).
- OBSERVATION: the tree has no package.json, Makefile, Worker name, Pages project, or database name.

## Workflows | file | jobs | triggers | runs by event (success/failure/other, `gh run list --workflow <file> --limit 200`) | first and last run (ET) |

| file | jobs | triggers | runs by event | first and last run (ET) |
| --- | --- | --- | --- | --- |
| .github/workflows/ci.yml | FACT: job id `eval` — QUOTE «eval:» — .github/workflows/ci.yml:17 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «name: Eval hosts (no KVM)» — .github/workflows/ci.yml:18. FACT: job id `nix` — QUOTE «nix:» — .github/workflows/ci.yml:36. QUOTE «name: NixOS VM test and QEMU closure» — .github/workflows/ci.yml:37. | FACT: QUOTE «on:» — .github/workflows/ci.yml:3. QUOTE «push:» — .github/workflows/ci.yml:4. QUOTE «branches: [main]» — .github/workflows/ci.yml:5. QUOTE «pull_request:» — .github/workflows/ci.yml:6. QUOTE «workflow_dispatch:» — .github/workflows/ci.yml:7. | FACT: `gh run list -R getboring/didymus-os --workflow ci.yml --limit 200 --json event,conclusion,createdAt` returned 2 runs. FACT: actions/runs total_count is 2 — https://api.github.com/repos/getboring/didymus-os/actions/runs?per_page=100 . push: success 0, failure 1, other 0. pull_request: success 0, failure 1, other 0. workflow_dispatch: 0 runs in that list. Totals: success 0, failure 2, other 0. FACT: in both runs, job eval conclusion is failure and job nix conclusion is skipped. The push eval annotation is QUOTE «The job was not started because your account is locked due to a billing issue.» — https://github.com/getboring/didymus-os/actions/runs/34067931825/job/101579889345 . The pull_request eval job annotation is the same sentence — https://github.com/getboring/didymus-os/actions/runs/34067928145/job/101579879392 . | First: pull_request 2026-09-06T23:48:50Z = 2026-09-06 19:48:50 ET, conclusion failure — https://github.com/getboring/didymus-os/actions/runs/34067928145 . Last: push 2026-09-06T23:48:55Z = 2026-09-06 19:48:55 ET, conclusion failure — https://github.com/getboring/didymus-os/actions/runs/34067931825 . |

Only .github/workflows/ci.yml is under .github/workflows/ at reviewed_sha.

## Features | feature | state | evidence |

| feature | state | evidence |
| --- | --- | --- |
| Flake, three modules, devShell name didymus-os | DONE | FACT: QUOTE «./modules/didymus.nix» — flake.nix:17 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «name = "didymus-os";» — flake.nix:32. The VM test script asserts version, hostname, /etc/didymus files, the receipt init file, and sshd — flake.nix:93, flake.nix:96, flake.nix:97, flake.nix:103, flake.nix:105, flake.nix:90. |
| nixosConfigurations.didymus-lab | PARTIAL | FACT: QUOTE «didymus-lab = mkHost [» — flake.nix:50 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «this tree has never been installed.» — hosts/didymus-lab/configuration.nix:40. The VM test import line does not include hardware.nix — QUOTE «imports = didymusModules ++ [ ./hosts/didymus-lab/configuration.nix ];» — flake.nix:80. |
| qemu-lab and qemu-vm | PARTIAL | FACT: QUOTE «qemu-lab = mkHost [» — flake.nix:56 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «qemu-vm = self.nixosConfigurations.qemu-lab.config.system.build.vm;» — flake.nix:64. No test script runs the VM bin. CI job nix, which runs QUOTE «run: nix build .#qemu-vm -L» — .github/workflows/ci.yml:57, was skipped — https://github.com/getboring/didymus-os/actions/runs/34067931825 |
| NixOS VM test checks.x86_64-linux.didymus-lab | PARTIAL | FACT: the test script is flake.nix:88 through flake.nix:108 @874faa799c6d98706d693b3eaf37794e994b4701. FACT: the only CI runs skipped that job before it started — https://github.com/getboring/didymus-os/actions/runs/34067931825 . The script is in the tree. There is no recorded pass. |
| Twin init oneshot | PARTIAL | FACT: QUOTE «# Placeholder twin service (will become real later)» — modules/twin.nix:48 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «if [ ! -f ${twinCfg.receiptDir}/.initialized ]; then» — modules/twin.nix:60. |
| Signed content-addressed receipts | NOT STARTED | FACT: QUOTE «Receipts will eventually be:» — modules/twin.nix:87 @874faa799c6d98706d693b3eaf37794e994b4701. The oneshot writes a plaintext file. No signing code is in the tree. |
| didymus CLI | NOT STARTED | FACT: QUOTE «the didymus CLI (coming soon).» — modules/didymus.nix:58 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «# environment.systemPackages = [ pkgs.didymus-cli ];» — modules/twin.nix:102. |
| Stable/experimental switch | NOT STARTED | FACT: QUOTE «type = types.enum [ "stable-experimental" "primary-mirror" "disabled" ];» — modules/didymus.nix:31 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «For now use standard nixos-rebuild; the twin layer is scaffolding only.» — modules/twin.nix:98. |
| Server profile | PARTIAL | FACT: QUOTE «# profiles/server.nix — minimal durable server profile» — profiles/server.nix:1 @874faa799c6d98706d693b3eaf37794e994b4701. It is not in the flake module list at flake.nix:17-19. |
| Desktop profile | NOT STARTED | FACT: QUOTE «├── profiles/                 # Ready-to-use profiles (desktop, server, agent, etc.)» — README.md:83 @874faa799c6d98706d693b3eaf37794e994b4701. No desktop profile file is in the tree. |
| Agent profile | NOT STARTED | FACT: same README.md:83 quote. No agent profile file is in the tree. |
| ISO builder | PARTIAL | FACT: QUOTE «iso =» — flake.nix:66 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «./iso/iso.nix» — flake.nix:68. QUOTE «- packages.x86_64-linux.iso» — garnix.yaml:15. No ISO test. |
| GitHub Actions workflow | PARTIAL | FACT: .github/workflows/ci.yml exists. Both recorded runs failed before jobs started — https://github.com/getboring/didymus-os/actions/runs/34067931825 |
| Garnix config file | PARTIAL | FACT: garnix.yaml:8 through garnix.yaml:15 @874faa799c6d98706d693b3eaf37794e994b4701. FACT: commit status total_count is 0 — https://api.github.com/repos/getboring/didymus-os/commits/874faa799c6d98706d693b3eaf37794e994b4701/status . UNKNOWN: whether the Garnix GitHub App is installed or built this SHA outside GitHub statuses. |
| ScopeBlind / Ed25519 integration | NOT STARTED | FACT: QUOTE «- Ed25519 signed (ScopeBlind-compatible)» — modules/twin.nix:89 @874faa799c6d98706d693b3eaf37794e994b4701 |
| scripts/init-repo.sh | PARTIAL | FACT: QUOTE «echo "This script is a placeholder."» — scripts/init-repo.sh:6 @874faa799c6d98706d693b3eaf37794e994b4701 |
| Branding assets | UNDOCUMENTED | FACT: branding/README.md:3 and the image files exist. No Nix file references them. |

## Drift | doc says | code shows | severity | cite |

| doc says | code shows | severity | cite |
| --- | --- | --- | --- |
| QUOTE «Every rebuild produces a verifiable pair (primary + twin) with signed receipts» — README.md:21 | A oneshot writes a plaintext init file only when that file is missing. QUOTE «Receipts will eventually be:» — modules/twin.nix:87. QUOTE «For now use standard nixos-rebuild; the twin layer is scaffolding only.» — modules/twin.nix:98. | HIGH | README.md:21 @874faa799c6d98706d693b3eaf37794e994b4701; modules/twin.nix:60; modules/twin.nix:87; modules/twin.nix:98 |
| QUOTE «Two concurrent profiles you can switch between without losing the other» — README.md:22 | twinMode is a string option. QUOTE «default = "stable-experimental";» — modules/didymus.nix:32. No switch command. QUOTE «the twin layer is scaffolding only.» — modules/twin.nix:98. | HIGH | README.md:22; modules/didymus.nix:31; modules/twin.nix:98 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «Ed25519-signed, content-addressed records of what changed (ScopeBlind-ready)» — README.md:23 | QUOTE «default = "/var/lib/didymus/receipts";» — modules/twin.nix:28. Signing text is future tense at modules/twin.nix:87. | HIGH | README.md:23; modules/twin.nix:28; modules/twin.nix:87 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «GitHub Actions and Garnix do steps 1–3.» — README.md:54 | Actions: 2 runs, both failure; eval not started; nix skipped. Commit statuses for reviewed_sha: total_count 0. | HIGH | README.md:54 @874faa799c6d98706d693b3eaf37794e994b4701; https://github.com/getboring/didymus-os/actions/runs/34067931825 ; https://api.github.com/repos/getboring/didymus-os/commits/874faa799c6d98706d693b3eaf37794e994b4701/status |
| QUOTE «Ready-to-use profiles (desktop, server, agent, etc.)» — README.md:83 | Only profiles/server.nix, and it is not imported. No desktop or agent profile file. | HIGH | README.md:83; profiles/server.nix:1; flake.nix:17 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «Every meaningful change leaves a receipt.» — README.md:93 | The oneshot writes the init file once if it is absent — modules/twin.nix:60. | LOW | README.md:93; modules/twin.nix:60 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «Same software, QEMU» — README.md:64 | Shared modules plus configuration.nix, then QEMU overrides. QUOTE «networking.hostName = lib.mkForce "didymus-qemu";» — hosts/qemu-lab/default.nix:16. QUOTE «autoFormat = true;» — hosts/qemu-lab/default.nix:24. virtio matches locked qemu-guest.nix line 2. | LOW | README.md:64; hosts/qemu-lab/default.nix:16; hosts/qemu-lab/default.nix:24 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «`didymus-lab` (physical) is the same software as `qemu-lab`.» — docs/TESTING.md:18 | Same shared modules and configuration.nix. qemu-lab adds hosts/qemu-lab/default.nix and does not import hardware.nix — flake.nix:52 versus flake.nix:58. | LOW | docs/TESTING.md:18; flake.nix:52; flake.nix:58 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «(eval, VM» — docs/TESTING.md:31 and QUOTE «test, QEMU closure)» — docs/TESTING.md:32 | garnix.yaml includes checks, the devShell, packages.default, qemu-vm, and both nixosConfigurations, and excludes the ISO. There is no include key named eval. | LOW | docs/TESTING.md:31; garnix.yaml:8; garnix.yaml:15 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «- [ ] ISO builder» — README.md:104 | packages.iso is defined. QUOTE «iso =» — flake.nix:66. The hosts table already says opt-in, not a CI gate — README.md:67. | LOW | README.md:104; README.md:67; flake.nix:66 @874faa799c6d98706d693b3eaf37794e994b4701 |
| QUOTE «2. **Receipts** — signed, content-addressed records of what changed.» — docs/philosophy.md:11 | Same plaintext init file. QUOTE «Receipts will eventually be:» — modules/twin.nix:87. | LOW | docs/philosophy.md:11; modules/twin.nix:87 @874faa799c6d98706d693b3eaf37794e994b4701 |

Rows that match and are not drift: disk labels didymus-root and didymus-boot (hosts/didymus-lab/hardware.nix:9, hosts/didymus-lab/hardware.nix:13); VM-test hostname and version (flake.nix:94, flake.nix:96); nixos-26.05 pin (flake.lock:14); AGPL-3.0-or-later (LICENSE:1); ISO described as opt-in and not a CI gate (garnix.yaml:15, flake.nix:65).

## Confusing names | where | name | conflicts with |

| where | name | conflicts with |
| --- | --- | --- |
| GitHub repo | didymus-os | QUOTE «# Didymus OS» — README.md:1; QUOTE «volumeID = "DIDYMUS_OS";» — iso/iso.nix:16 @874faa799c6d98706d693b3eaf37794e994b4701 |
| flake devShell | QUOTE «name = "didymus-os";» — flake.nix:32 | option default QUOTE «default = "didymus";» — modules/didymus.nix:26 |
| lab host | QUOTE «hostname = "didymus-lab";» — hosts/didymus-lab/configuration.nix:11 | QUOTE «networking.hostName = lib.mkForce "didymus-qemu";» — hosts/qemu-lab/default.nix:16; QUOTE «hostname = "didymus-iso";» — iso/iso.nix:10 |
| NixOS label | QUOTE «system.nixos.label = "didymus-${cfg.version}";» — modules/didymus.nix:51 | README QUOTE «**v0.1 — Scaffolding**» — README.md:29 versus code QUOTE «default = "0.1.0-scaffold";» — modules/didymus.nix:20 |
| VM check attribute | QUOTE «checks.${system}.didymus-lab = pkgs.testers.runNixOSTest {» — flake.nix:74 | the check import does not include hosts/qemu-lab/default.nix or hardware.nix — flake.nix:80 |
| QEMU disk label | QUOTE «device = "/dev/disk/by-label/nixos";» — hosts/qemu-lab/default.nix:22 | physical labels at hosts/didymus-lab/hardware.nix:9 and hosts/didymus-lab/hardware.nix:13 |
| package, Worker, database, product domain | none in the tree | footer QUOTE «https://getboring.io · https://codyboring.com» — README.md:117 is not a Didymus hostname |

## Possible overlap (record only, no verdict)

- ScopeBlind: QUOTE «- Ed25519 signed (ScopeBlind-compatible)» — modules/twin.nix:89 @874faa799c6d98706d693b3eaf37794e994b4701. QUOTE «- **ScopeBlind** — receipts are designed to be compatible with Ed25519 / Cedar policy verification» — docs/philosophy.md:39. Public repo getboring/scopeblind-gateway description says active development continues at ScopeBlind/scopeblind-gateway — https://github.com/getboring/scopeblind-gateway
- getboring/boring-agent-appliance: QUOTE «this matches getboring/boring-agent-appliance.» — flake.nix:5. QUOTE «as `getboring/boring-agent-appliance`.» — docs/TESTING.md:34. `gh repo view getboring/boring-agent-appliance` does not resolve a repository. UNKNOWN whether a private repo matches the Determinate Nix pin — QUOTE «uses: DeterminateSystems/determinate-nix-action@61cbfe2efc2d4e7a8a6d56967c3c1058e846c858 # v3» — .github/workflows/ci.yml:25.
- NixOS: this flake is a NixOS configuration on nixos-26.05 — flake.nix:6, flake.lock:14. QUOTE «**A twin of NixOS.**» — README.md:3.
- Boring-Works: Boring-Works/didymus-os does not resolve. No mirror recorded.

## UNKNOWN / questions

- UNKNOWN: whether the Garnix GitHub App is installed, and whether Garnix built reviewed_sha anywhere other than GitHub commit statuses (total_count 0 on https://api.github.com/repos/getboring/didymus-os/commits/874faa799c6d98706d693b3eaf37794e994b4701/status).
- UNKNOWN: whether getboring/boring-agent-appliance exists and uses the same Determinate Nix action pin. The public name does not resolve.
- UNKNOWN: whether `nix build .#checks.x86_64-linux.didymus-lab` or `nix build .#qemu-vm` succeeds. The CI job that runs `nix flake check` and `nix build .#qemu-vm` was skipped — https://github.com/getboring/didymus-os/actions/runs/34067931825
- UNKNOWN: no custom-domain go-live date. live since is not deployed from the empty deployments list, the Pages 404, and hosts/didymus-lab/configuration.nix:40.

## Self-check
- [x] Re-opened every cited file:line at reviewed_sha; each quote is word-for-word on that line (list any fixed). Fixed in this sheet before commit: receipt assert is flake.nix:105; init-file test is flake.nix:103; QEMU disk device is hosts/qemu-lab/default.nix:22; README.md:83 begins with ├── profiles/; twinMode default is modules/didymus.nix:32.
- [x] Every HIGH drift row is a wrong current-state claim about product, deploy or data; history gaps are LOW.
- [x] Every workflow file under .github/workflows/ is in the Workflows table.
- [x] No SUPERSEDED-BY / DUPLICATE-OF / DEAD / CANONICAL verdicts; no recommendations outside Naming suggestions.
## Naming suggestions (ideas only, no action)

- didymus-os / Didymus OS / DIDYMUS_OS / didymus / didymus-lab / didymus-qemu / didymus-iso / didymus-0.1.0-scaffold
- v0.1 / 0.1.0-scaffold
- check name didymus-lab / host name qemu-lab / host name didymus-lab
- disk label nixos / disk labels didymus-root and didymus-boot
- repo getboring/didymus-os; no package name, Worker name, or database name
