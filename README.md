# Alfred

Public butler soul for a Hermes desktop bot. No API keys, no client files.

Private profile data stays in `adrozdenko/hermes-data`. Do not copy `config.yaml`, `.env`, `auth.json`, or `credentials/` from there into this repo.

## Stand him up

On the machine where Hermes is installed:

```bash
git clone https://github.com/adrozdenko/alfred.git
cd alfred
```

If `~/.hermes/profiles/alfred` does not exist:

```bash
hermes profile create alfred --clone --description "Особистий дворецький пана Ігоря — розклад, клієнти, Kramp. Не технічний помічник."
```

Then:

```bash
cp SOUL.md ~/.hermes/profiles/alfred/SOUL.md
hermes -p alfred config set terminal.cwd ~/.hermes/profiles/alfred
```

Write `~/.hermes/profiles/alfred/profile.yaml`:

```yaml
description: Особистий дворецький пана Ігоря — розклад, клієнти, Kramp. Не технічний помічник.
description_auto: false
display_name: Альфред
ui_meta:
  hermes-bots:
    title: Альфред
    description: Особистий дворецький пана Ігоря — розклад, клієнти, Kramp. Не технічний помічник.
    created: 0
    imageKind: shape
    pinned: false
_ui_meta_revisions:
  hermes-bots: 1
```

Set `created` to the current unix time in milliseconds. Open **Bots**. Do not copy `auth.json`.
