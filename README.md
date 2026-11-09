# RC Pair for Claude Code

Let Claude test on your real iPhone or iPad. It sees the screen, taps, types, scrolls and reads text. No Mac needed.

## Install

1. Sign up at https://setup.rcpair.si. It downloads RC Pair for your computer (Windows, Mac or
   Linux) and walks you through pairing your iPhone. Start with a 7-day trial, then $12 a month, or $36 for your first 6 months during launch.
2. Connect Claude Code to RC Pair:
   - Windows or Mac: open RC Pair, press Connect and choose Claude Code.
   - Linux: run
     ```
     claude mcp add rcpair -e RCPAIR_AGENT_TOKEN="$(rcpair agent add --label 'Claude Code')" -- rcpair mcp
     ```
3. Add this plugin in Claude Code:

```
/plugin marketplace add rcpair/claude-plugin
/plugin install rcpair@rcpair
```

Start a new Claude Code session and ask Claude to try your app on your phone.

You stay in charge: approve each agent on your phone, and stop it any time.
