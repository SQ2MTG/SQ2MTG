# HomeLab Monitor — source attribution and current reference

## Repository relationship

`SQ2MTG/homelab-monitor` is a public fork of `SikamikanikoBG/homelab-monitor`. The upstream README is therefore the primary source for current behavior; this page records the functionality visible in the fork's current README/Compose configuration.

## Function

HomeLab Monitor is a self-hosted homelab and AI/GPU dashboard covering host health, GPU metrics, power/cost tracking, containers, systemd services, disks, network activity, uptime checks, experiments and local model benchmarking.

It supports multi-machine collection over SSH without installing a persistent agent on remote hosts. The README documents Linux, Raspberry Pi and Windows/PowerShell host support.

## AI and model monitoring

The current README documents an AI Benchmark Lab for measuring prompt/generation tokens per second, model load time, VRAM/RAM split and the largest context fitting fully in VRAM. Model-server integrations include Ollama, vLLM, llama.cpp and A1111 among a larger set of recognized servers.

## Interfaces

The dashboard defaults to port `9800`. A built-in read-only MCP server uses port `9810` and exposes homelab information to MCP clients. A standard `/metrics` endpoint is also documented.

History is persisted in `./data/gpu.db` using SQLite.

## Container architecture and privileges

The documented Compose configuration uses host networking, host PID and cgroup namespaces, `SYS_PTRACE`, an unconfined AppArmor profile, host/root filesystem access and Docker/systemd integration. This is intentionally broad host access for monitoring and service attribution.

The upstream README explicitly warns that the dashboard has no login/authentication and is intended for a trusted LAN. It should therefore remain behind LAN/VPN/firewall controls and not be exposed directly to the public Internet.

## Hardening options

The documented configuration includes options to disable MCP, disable self-update and disable service controls, plus a read-only Compose variant. These options should be preferred where write/control functionality is not required.

## Source

Repository: SQ2MTG/homelab-monitor; upstream: SikamikanikoBG/homelab-monitor
