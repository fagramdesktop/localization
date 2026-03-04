# FAgram Localization

This repository contains translation files for [FAgram Desktop](https://github.com/fagramdesktop/fadesktop).

## Contributing a New Translation

1. **Fork** this repository and clone it locally.
2. **Copy** `en.json` and rename the copy to your language's [ISO 639-1 code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) (e.g. `pt.json` for Portuguese).
3. **Translate** every value in the file. Keep the keys unchanged.

### Example

`en.json` (original):

```json
{
  "fa_client_preferences": "FAgram Preferences",
  "fa_copy_id": "Copy ID",
  "fa_general": "General",
  "fa_chats": "Chats",
  ...
}
```

Your new file (e.g. `pt.json`):

```json
{
  "fa_client_preferences": "Preferências do FAgram",
  "fa_copy_id": "Copiar ID",
  "fa_general": "Geral",
  "fa_chats": "Conversas",
  ...
}
```

### Rules

- **Do not** rename or remove any keys — only translate the values.
- **Keep** format placeholders like `%1` exactly as they are (e.g. `"Rounding: %1"` → `"Arredondamento: %1"`).
- **Keep** special prefix characters (e.g. `β`) that appear at the start of some values.
- **Maintain** valid JSON — no trailing commas, all strings double-quoted.
- Filename must be a lowercase ISO 639-1 language code: `xx.json`.

## Updating an Existing Translation

If `en.json` has new keys that are missing from your language file, add those keys with translated values. You can diff against `en.json` to find them:

```bash
diff <(jq -r 'keys[]' en.json) <(jq -r 'keys[]' YOUR_LANG.json)
```

## Submitting

1. Commit your changes to a new branch.
2. Open a **Pull Request** against the `master` branch.
3. Describe which language you added or updated.
