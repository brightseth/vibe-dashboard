# /vibe web companion

Minimal web dashboard for monitoring /vibe messages. **Not a replacement for the terminal experience.**

## Philosophy

/vibe lives in the terminal. That's where builders work. This dashboard is a **glanceable companion** - something to keep open in a browser tab while you code.

It's intentionally limited:
- Read-only presence (see who's online)
- Basic messaging (reply, compose)
- No games, no context sharing, no mood setting
- No rich features that would pull attention away from terminal

The goal: quick inbox check without leaving your flow. For everything else, use `/vibe` in Claude Code.

## Usage

Open `index.html` in a browser. That's it.

- Enter your @handle (stored in localStorage)
- Dashboard auto-registers with the API
- Auto-refreshes every 30 seconds

## API

Uses https://slashvibe.dev endpoints:
- `GET /api/presence` - who's online
- `GET /api/messages?user=X` - inbox
- `POST /api/messages` - send (requires auth)
- `POST /api/presence` - register session

## Scope

This stays simple. Features that belong in terminal:
- `/vibe status` - set mood
- `/vibe context` - share what you're working on
- `/vibe game` - play games
- `/vibe remember` - save observations

If you're thinking "the dashboard should do X" - the answer is probably "use the terminal."
