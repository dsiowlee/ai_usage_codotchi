# Codotchi

A Tamagotchi-style virtual pet that lives inside your AI coding assistant.
Raises your pet in the terminal alongside your coding session and tracks your
daily API usage cost.

Available for **OpenCode** and **Claude Code**.

--

## OpenCode

<img width="736" height="184" alt="image" src="https://github.com/user-attachments/assets/bd3a4e64-2988-460d-bbb7-e4d96b3c9a08" />


### Features

| Feature | Description |
|---------|-------------|
| **`/codotchi` slash command** | Control your pet directly from OpenCode |
| **ASCII art renderer** | ANSI-coloured speech bubbles, messages whilst you code |
| **Daily cost tracking** | Pet speech bubble colour reflects today's OpenCode API spend |

### Installation

Download `opencode-codotchi-2.11.0.zip` from the
[Releases page](https://github.com/dsiowlee/ai_usage_codotchi/releases),
extract it, then run the installer:

**Windows (PowerShell):**

```powershell
Expand-Archive opencode-codotchi-2.11.0.zip
cd opencode-codotchi-2.11.0
node bin/install.js --install
```

**macOS / Linux:**

```bash
unzip opencode-codotchi-2.11.0.zip
cd opencode-codotchi-2.11.0
node bin/install.js --install
```

Node.js is the only prerequisite. No npm publish or repository clone required.

After running the installer, open any project in OpenCode. Your codotchi will
greet you in a speech bubble on first startup.

---

## Claude Code

### Features

| Feature | Description |
|---------|-------------|
| **Statusline pet** | Multiline ANSI ASCII art renders in the statusline, refreshes every 10 seconds |
| **`/codotchi` slash command** | Control your pet directly from Claude Code |
| **Daily cost tracking** | Pet speech bubble colour reflects today's Claude API spend |

### Installation

Download `claude-codotchi-2.11.0.zip` from the
[Releases page](https://github.com/dsiowlee/ai_usage_codotchi/releases),
extract it, then run the installer script to get the exact commands for your
machine:

**Windows (PowerShell):**

```powershell
Expand-Archive claude-codotchi-2.11.0.zip
cd claude-codotchi-2.11.0
.\install.ps1
```

**macOS / Linux:**

```bash
unzip claude-codotchi-2.11.0.zip
cd claude-codotchi-2.11.0
chmod +x install.sh && ./install.sh
```

The script prints the two `/plugin` commands to paste into a Claude Code
session:

```
/plugin marketplace add <path-to-extracted-folder>
/plugin install claude-codotchi
```

See `INSTALL.md` inside the zip for full installation details.

---

## Daily cost tracking

The pet's speech bubble colour reflects how much you've spent on API calls today:

| Spend | Colour | Tone |
|-------|--------|------|
| Below warn threshold | Green | Cheerful |
| Warn → shout threshold | Yellow | Concerned |
| Above shout threshold | Red | ALL CAPS alarm |

Default thresholds: **$30 warn / $50 shout**. Configurable via `/codotchi warnthreshold` and `/codotchi shoutthreshold`.

---

## Current release: v2.11.0

- `opencode-codotchi-2.11.0.zip` — OpenCode plugin
- `claude-codotchi-2.11.0.zip` — Claude Code plugin
