# Alien Swarm - Reactive Drop - Servers (Gandalf's, ASRD Germany)

## Description

This repository contains information about the Alien Swarm - Reactive Drop servers, and in specific ASRD Germany which also known as Gandalf's.

## Issues

If you have issues with the servers, or if you want any changes, feel free to create an issue or discussion in this project:

- [Issues](https://github.com/mithrand0/servers/issues)
- [Discussions](https://github.com/mithrand0/servers/discussions)


## Config

The configuration used on all servers is:

|name|value|reason|
|---|---|---|
sv_minrate,sv_maxrate|30000-120000|above ~120k, people have additional lag if they cannot handle it|
|sv_mincmdrate,sv_maxcmdrate|60-60|minimum value is enforced to prevent stuttering for clients who turned interp off|
|sv_minupdaterate,sv_maxupdaterate|20-60|
|asw_instant_restart|0|set to off to prevent issues with some maps and challenges|
|rd_slowmo|0|disabled, because some clients experience lag, possibly due misconfiguration|
|rd_override_fps_max|0|set to 0 to unlock maximum framerate for lowest possible processing latency (~900)|
|net_maxcleartime|0.001|creates choke at default setting|
|net_splitrate|2|to prevent choke when a large amount of aliens is spawned at once|
|net_splitpacket_maxrate|120000|same as sv_maxrate|
|sv_client_min_interp_ratio|0|let clients pick their own interp ratio, even if it is adviced never to set to 0|
|sv_client_predict|1|force client prediction|


## Hardware

All servers run in a datacenter on a dedicated server with AMD server hardware, connected by redundant fiber uplink.

## Updates

The game servers restart every two hours. During a restart, it checks for any Alien Swarm updates, those are applied before the server is started. In addition, all servers restart after the last player left.

The Windows update maintenance window is set to start at 06:00 UTC. During this time, the server itself might force restart or have small lags.

## Ramdisk

Logs, saves and any transient data is stored on ramdisk, and copied over after the server restarts.

## Spectators

The spectator slots on all servers are disabled. The reason is some people are actively abusing this feature. Alien Swarm is about playing games together, not join a lobby and idle for hours, while lagging a server.

In the future, the servers will support Source TV for spectators as soon as it is available.

## Reporting

All servers gather data regarding custom clients and cheats used. This data is forwarded to Valve for analysis using:

- [Valve Anti-Cheat (VAC) and Game Bans](https://partner.steamgames.com/doc/features/anticheat)
