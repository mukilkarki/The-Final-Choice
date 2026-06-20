# The Final Choice

**The Final Choice** is a single-file cinematic interactive story game built with only HTML, CSS, and JavaScript.

It follows an emotional healing journey through:

- The storm
- Someone staying
- Healing chapters
- A memory montage
- A heartbeat confession
- The final choice
- A Yes ending
- A No ending
- A handwritten letter from him
- Credits

## How to play

Open `index.html` in a modern browser and follow the story. Complete all healing chapters, watch the confession, then choose **YES** or **NO**.

## Features

- Single self-contained `index.html`
- No frameworks
- Generated Web Audio music
- Hidden always-on music at full volume after browser audio unlock
- Scene-specific music moods
- Heartbeat confession cues
- Falling tear particles
- Memory montage
- Expanded Yes and No endings
- Handwritten letter scene
- Mobile-responsive layout
- Smooth cinematic transitions
- Gmail choice forwarding through a free FormSubmit setup

## Music behavior

The game attempts to start music automatically. Modern browsers usually block audio until the first player interaction, so the music starts as soon as the browser allows it, typically on the first tap/click/key press.

There are no visible music controls. Music plays at full volume.

## Send choices to Gmail

The game includes code to send the player's **YES** or **NO** answer to a Gmail inbox using FormSubmit.

See [`CHOICE_EMAIL_SETUP.md`](CHOICE_EMAIL_SETUP.md) for setup instructions.

## Development

Because this is a static game, no build step is required.

Recommended checks after editing:

```bash
git diff --check
node --check /tmp/tfc.js
```

To run the JavaScript syntax check, extract the inline script first:

```bash
python3 - <<'PY'
from pathlib import Path
s = Path('index.html').read_text()
Path('/tmp/tfc.js').write_text(s[s.index('<script>') + 8:s.index('</script>')])
PY
node --check /tmp/tfc.js
```

## Files

- `index.html` — the complete game
- `CHOICE_EMAIL_SETUP.md` — Gmail/FormSubmit setup guide
- `README.md` — game overview and development notes
