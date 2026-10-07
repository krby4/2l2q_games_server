# Game Server Requests

This repository is used to request new game servers, mods, modpacks, and configuration changes for the game servers I host.

Please submit requests through **GitHub Issues** so that requests can be tracked, discussed, and documented.

## Currently Supported Games

These games already have working server configurations and can be hosted without needing to build a new deployment from scratch:

- **Minecraft**
  - Vanilla
  - Modded servers / modpacks
  - Specific server implementations can be requested if needed
- **Satisfactory**
- **Windrose**
- **Valheim**
- **Palworld**

Other games may be possible if they provide a usable dedicated server. Submit an issue and I can look into whether the server can reasonably be hosted.

Availability of a game does not necessarily mean that it can be running at the same time as every other game server. Port conflicts, resource usage, maintenance, and actual demand may affect what is running.

---

# Requesting a New Game Server

Create an issue for the game and include as much of the following information as possible.

## Required Information

- **Game name**
- **Link to the game**
  - Steam page or official website is preferred.
- **Who wants to play**
  - Rough number of expected players.
- **When you expect to play**
  - Regularly, occasionally, one-time event, etc.
- **Does the game have a dedicated server?**
  - If you know, provide a link to the dedicated server documentation.
- **Desired version**
  - Stable/release version unless there is a reason to use something else.

## Helpful Information

If you already know any of this, include it:

- Linux dedicated server support
- Docker image/project for the server
- Required TCP/UDP ports
- Expected RAM requirements
- Expected disk usage
- SteamCMD App ID
- Server configuration documentation
- Whether the server requires an account, token, license, or API key
- Whether the server supports automatic updates
- Any special networking requirements

You do **not** need to research all of this before making a request. A game name and some information about how you want to use the server is enough to start the discussion.

---

# Requesting Mods or Modpacks

For an existing server, create an issue containing:

- **Game**
- **Mod/modpack name**
- **Link to the mod**
  - Steam Workshop, CurseForge, Modrinth, Nexus, GitHub, etc.
- **Requested version**
- **Why you want it**
- **Whether all players need the mod installed locally**
- **Any known dependencies**
- **Any known incompatibilities with existing mods**
- **Whether adding the mod requires starting a new world/save**

For a modpack, provide the exact pack and version rather than only the modpack name.

Example:

> **Game:** Minecraft  
> **Modpack:** All the Mods 10  
> **Version:** 4.2.1  
> **Link:** `<link>`  
> **Players:** 4-6  
> **Notes:** New world is fine.

---

# Changes to Existing Servers

Issues can also be submitted for things such as:

- Adding/removing mods
- Changing server settings
- Increasing player limits
- Changing difficulty
- Updating versions
- Installing a new map/world
- Resetting a world
- Changing scheduled restarts
- Adding plugins
- Investigating performance problems

For anything destructive such as a world reset, clearly state that a reset is being requested.

---

# What Happens After a Request

For a new game, I will generally check:

1. Whether a dedicated server exists.
2. Whether it runs reasonably on Linux or in Docker.
3. CPU, RAM, and storage requirements.
4. Required TCP/UDP ports and whether they conflict with an existing server.
5. Persistent data/save requirements.
6. Backup requirements.
7. Update procedure.
8. Authentication/licensing requirements.
9. Whether the service can be cleanly started, stopped, rebuilt, and maintained.

If it looks reasonable to host, the issue can then be used to track deployment.

---

# A Few Rules

- Do not include passwords, API keys, server tokens, or other secrets in an issue.
- Link directly to mods/download pages instead of uploading random binaries.
- Mods should come from a reasonably trustworthy source.
- Server stability takes priority over adding a mod immediately.
- Existing save data will be backed up before significant changes when practical.
- A request is not a guarantee that a game or mod can be hosted.

The goal is to keep game-server changes documented instead of relying on messages such as:

> "Hey, can you install this thing?"