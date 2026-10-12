# Multi-Claude (side project)

With Phumipat Jiranarongwat, who started the project and is the main author.

## What it is

A desktop app for running several Claude Code sessions side by side, in tabs, each in its own project folder.

The main selling point is hot-swapping accounts. You can switch to a different account at any time, even in the middle of a session, and carry on working.

It also signs in to other coding agents, such as Codex and Antigravity, and you can use them in coding sessions too (terminal view only). Phumipat's coworkers use it day to day. He built it for Windows. I wanted it on my Mac, so I took on the macOS version.

## My part

- Build and maintain the macOS version. Each time a new upstream release comes out, I port it over, test it and ship a new macOS build through the app's update feed.
- Suggested features, for example bringing Gemini into the app next to Claude. I built the Gemini sign-in on macOS.
- Do the final security and bug review before releases. I run it with Claude Code review skills (OWASP checks included), and it has caught bugs that earlier checks missed. Those were fixed before release.

## Stack

Electron, TypeScript, React, Vite, Node.js, Vitest.

## Problems worth mentioning

**Gemini sign-in did nothing.** Clicking sign in showed no window and no error. I added a small flow log to see each step, and it showed the app was reading a leftover debug-port file from an old browser profile, so it talked to a browser that no longer existed. Deleting the stale file before launch, and waiting for the old browser to really exit, fixed it.

**Pop-out windows opening behind the app.** A tab popped out into its own window opened underneath the main window, so it looked like nothing happened. Windows now open offset from the main one and are brought to the front. If the window fails, the tab stays where it was instead of disappearing.

**The "+" new-tab button stopped working.** Closing the active tab left no tab active, and "+" needed an active tab to know which folder to open. The next tab now becomes active, and "+" falls back to the last one used.

**Wrong context size for new models.** New models showed a 200k context window because they weren't in a hard-coded list. The app now reads limits from the model catalog instead.

## Result

macOS builds released through the update feed, with about 4,100 automated tests passing.
