# clawdbot-ops

A Claude Code skill for starting, stopping, diagnosing, and troubleshooting [Clawdbot](https://github.com/openclaw) (OpenClaw/Moltbot).

## Installation

```bash
# Clone to your Claude Code skills directory
git clone https://github.com/hqwuzhaoyi/clawdbot-ops ~/.claude/skills/clawdbot-ops
```

## Usage

In Claude Code, type `/clawdbot-ops` to invoke this skill.

## Quick Commands

| Action | Command |
|--------|---------|
| Start gateway | `clawdbot gateway start` |
| Start as daemon | `clawdbot gateway start --daemon` |
| Stop gateway | `clawdbot gateway stop` |
| Check status | `clawdbot gateway status` |
| Health check | `clawdbot doctor` |
| Auto-fix issues | `clawdbot doctor --fix` |
| View logs | `clawdbot logs --follow` |
| Open dashboard | `clawdbot dashboard` |

## What's Included

- **Gateway Management**: Start, stop, and monitor the Clawdbot gateway
- **Health Checks**: Diagnose issues with `clawdbot doctor`
- **Common Fixes**: Solutions for port conflicts, zombie processes, config corruption
- **Emergency Recovery**: Steps to recover from broken states
- **Config Locations**: Quick reference for all config files

## Config Paths

| Path | Purpose |
|------|---------|
| `~/.clawdbot/clawdbot.json` | Main config |
| `~/.clawdbot/clawdbot.json.bak` | Config backup |
| `~/.clawdbot/logs/` | Log files |
| `~/.clawdbot/credentials/` | API keys & tokens |

## Emergency Recovery

If everything is broken:

```bash
pkill -9 -f clawdbot
clawdbot reset
clawdbot onboard
```

## License

MIT
