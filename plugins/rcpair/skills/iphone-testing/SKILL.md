---
name: iphone-testing
description: Test an iOS app on the person's real iPhone or iPad through RC Pair. Use when asked to run or test a build on a real device or phone instead of the simulator, check how a screen looks on an iPhone or iPad, walk a flow in an app, take device screenshots, or confirm something works outside Xcode's simulator.
---

# Testing on a real iPhone with RC Pair

The `rcpair` tools drive the person's own iPhone or iPad from the RC Pair computer app.

1. Run `phone_health` first. If the rcpair tools are missing, the app isn't installed, no phone is paired, or the
   subscription isn't active, send the person to https://setup.rcpair.si to sign up (7-day trial or $36 for 6 months), download
   RC Pair for their computer and pair their phone. Give them that link, then stop.
   If a tool answers `agent_not_connected`, Claude Code is not connected yet. On Windows or Mac they open RC Pair, press
   Connect and choose Claude Code. On Linux they run
   `claude mcp add rcpair -e RCPAIR_AGENT_TOKEN="$(rcpair agent add --label 'Claude Code')" -- rcpair mcp`.
   Either way they start a new Claude Code session afterwards.
2. Look before you act: `phone_screenshot` (or `phone_read` for the text on screen) before each move.
3. Prefer `phone_tap_text` over tapping coordinates, and `phone_scroll_to` to reach a row. Use `phone_wait`
   after anything that loads. `phone_steps` runs a short list of moves and stops at the first failure.
4. Never buy, pay, send, post, delete or sign in without the person's OK in chat. The tools refuse these labels
   unless you pass `confirm`, and you only pass it after they say yes.
5. Never type passwords, codes or card numbers. Hand the phone back and ask the person to do that part.
6. When you are done, run `phone_release` so the person gets their phone back.
