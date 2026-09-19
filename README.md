# cmd.safzan.dev

A single static page pairing Command Code's marketing claims about `taste-1` with the code that
ships in `command-code@1.58.0`. Every claim on the page links to its source: archived vendor
pages on web.archive.org, and the published npm artifact on unpkg.

The page states the SHA-256 of the file examined so a reader can confirm they are looking at the
same bytes:

    curl -s https://unpkg.com/command-code@1.58.0/dist/cli.mjs | shasum -a 256
    aab2bec800371953112d18472bb7383992ef264cca22558bdcda77e7d0dc0f14

## Files

- `index.html` — the page, no build step
- `og.html` — source for the social card
- `og.png` — rendered at 1200x630 from `og.html`

Regenerate the card with headless Chrome:

    "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
      --headless --disable-gpu --hide-scrollbars --window-size=1200,630 \
      --screenshot="$PWD/og.png" "file://$PWD/og.html"

Corrections welcome. If a grep contradicts something on the page, open an issue.
