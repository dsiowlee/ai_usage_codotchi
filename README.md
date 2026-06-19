# Codotchi

A Tamagotchi-style virtual pet that lives inside your AI coding assistant.
Raises your pet in the terminal alongside your coding session and tracks your
daily API usage cost.

Available for **OpenCode** and **Claude Code**.

---

## OpenCode

### Features

| Feature | Description |
|---------|-------------|
| **Tick loop** | Pet advances every 6 s via a background timer |
| **Event hooks** | Reacts to file edits (coding reward), session idle, and server connect |
| **`/codotchi` slash command** | 10+ actions: status, feed, snack, play, pat, sleep, wake, clean, medicine, new_game |
| **ASCII art renderer** | 30 frames (6 stages × 5 moods), ANSI-coloured speech bubbles, status bars |
| **Daily cost tracking** | Pet speech bubble colour reflects today's OpenCode API spend |

### Installation

Download `opencode-codotchi-2.10.2.zip` from the
[Releases page](https://github.com/dsiowlee/ai_usage_codotchi/releases),
extract it, then run the installer:

**Windows (PowerShell):**

```powershell
Expand-Archive opencode-codotchi-2.10.2.zip
cd opencode-codotchi-2.10.2
node bin/install.js --install
```

**macOS / Linux:**

```bash
unzip opencode-codotchi-2.10.2.zip
cd opencode-codotchi-2.10.2
node bin/install.js --install
```

Node.js is the only prerequisite. No npm publish or repository clone required.

After running the installer, open any project in OpenCode. Your codotchi will
greet you in a speech bubble on first startup.

### Actions

```text
/codotchi              — show status
/codotchi feed         — give a meal
/codotchi snack        — give a snack
/codotchi play         — play with your pet
/codotchi pat          — gently pat your pet
/codotchi sleep        — put your pet to sleep
/codotchi wake         — wake your pet up
/codotchi clean        — clean up droppings
/codotchi medicine     — give medicine to cure sickness
/codotchi new_game name=<name> petType=<type>  — start a fresh pet
```

Pet types: `codeling` (default), `bytebug`, `pixelpup`, `shellscript`

---

## Claude Code

### Features

| Feature | Description |
|---------|-------------|
| **Statusline pet** | Multiline ANSI ASCII art renders in the statusline, refreshes every 10 seconds |
| **Coding rewards** | Every file write/edit boosts your pet's happiness and discipline |
| **Session hooks** | Pet greets you on session start and says farewell when the session stops |
| **`/codotchi` slash command** | Care actions available directly in Claude Code |
| **Daily cost tracking** | Pet speech bubble colour reflects today's Claude API spend |

### Installation

Download `claude-codotchi-2.10.2.zip` from the
[Releases page](https://github.com/dsiowlee/ai_usage_codotchi/releases),
extract it, then run the installer script to get the exact commands for your
machine:

**Windows (PowerShell):**

```powershell
Expand-Archive claude-codotchi-2.10.2.zip
cd claude-codotchi-2.10.2
.\install.ps1
```

**macOS / Linux:**

```bash
unzip claude-codotchi-2.10.2.zip
cd claude-codotchi-2.10.2
chmod +x install.sh && ./install.sh
```

The script prints the two `/plugin` commands to paste into a Claude Code
session:

```
/plugin marketplace add <path-to-extracted-folder>
/plugin install claude-codotchi
```

See `INSTALL.md` inside the zip for full installation details.

### Actions

| Action | Description |
|--------|-------------|
| `/codotchi` or `/codotchi status` | Show the pet's ASCII art and full stats |
| `/codotchi feed` | Give a meal (max 3 per wake cycle) |
| `/codotchi pat` | Pat the pet |
| `/codotchi sleep` | Put the pet to sleep |
| `/codotchi wake` | Wake the pet up |
| `/codotchi clean` | Remove droppings |
| `/codotchi medicine` | Give medicine (3 doses to cure sickness) |
| `/codotchi on` | Enable ASCII art in statusline |
| `/codotchi off` | Disable ASCII art |
| `/codotchi rename <name>` | Rename your pet |
| `/codotchi warnthreshold <amount>` | Set warning spend threshold (default: $30) |
| `/codotchi shoutthreshold <amount>` | Set shout spend threshold (default: $50) |

---

## Daily cost tracking

The pet's speech bubble colour reflects how much you've spent on API calls today:

| Spend | Colour | Tone |
|-------|--------|------|
| Below warn threshold | Green | Cheerful |
| Warn → shout threshold | Yellow | Concerned |
| Above shout threshold | Red | ALL CAPS alarm |

Default thresholds: **$30 warn / $50 shout**. Configurable per plugin.

---

## Current release: v2.10.2

- `opencode-codotchi-2.10.2.zip` — OpenCode plugin
- `claude-codotchi-2.10.2.zip` — Claude Code plugin
