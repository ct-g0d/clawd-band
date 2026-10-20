# clawd-band

A live band above Claude Code's prompt, for the desktop app.

- **Desk clock**: HH:MM in a backlit LCD.
- **5H / 7D**: your 5-hour and 7-day plan limits, as bars.
- **SESSION / CTX**: what the session has cost, over a context bar split by category the way `/context` splits it.
- **HIT / TOK/S**: how much of the last request came from the prompt cache, and how fast the reply streamed.
- **CACHE**: minutes left on the prompt cache. From 10 minutes it frosts over, and at 0 it freezes.
- **STATUS**: what Claude is doing right now (Thinking, Replying, Editing, Running, Planning…), with the turn's time ticking underneath.

It also adds **`/keepwarm`**, which re-sends the conversation once so the prompt cache stays warm for another hour, with a little fire on the CACHE chip. Once the cache has already gone cold it declines, because your next message rebuilds the cache anyway.

The figures that only a reply can tell (the limits, the cache countdown, HIT and TOK/S) are kept between restarts, so a resumed chat opens with them instead of blanks.

## Install

At the prompt of a terminal session:

```
/plugin install clawd-band --marketplace charleschenantong-maker/clawd-band
```

Answer `y` to add the marketplace, then pick a scope. From a shell:

```bash
claude plugin install clawd-band --marketplace charleschenantong-maker/clawd-band
```

## Font and Clawd

The band was built around the Claude app's own font and its Clawd mascot animation. Both belong to Anthropic, so neither ships here: the band draws in your system's sans and leaves Clawd out. A setup step that builds both from your own install of the Claude app is planned.
