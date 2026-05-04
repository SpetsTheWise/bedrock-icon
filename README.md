# bedrock-icons

Steam Inventory Service icon assets for **rocks.exe / BEDROCK** (Steam app id `4685210`).

This repository contains **only PNG icon files** used by the game's Steam Inventory item definitions. No game source, no logic, no balance data — just the visible icon art for cases, keys and reward items.

## Layout

```
small/   96 × 96   px PNGs   (Steam inventory thumbnail size)
large/   360 × 360 px PNGs   (Steam item preview size)
```

Each icon is named `<itemdefid>_<item_id>.png`, where `<itemdefid>` matches the corresponding itemdefid in the game's Steam Inventory Service definitions.

## Itemdef coverage

| Range       | Count | Purpose                       |
|-------------|-------|-------------------------------|
| `1000`      | 1     | Standard Key                  |
| `2001-2010` | 10    | Cases                         |
| `3001-3095` | 50    | Reward items (10 × 5 rarities) |

Hidden generators (5xxx) are not represented here — they never surface to the player.

## URL pattern

Icons are served via raw GitHub URLs:

```
https://raw.githubusercontent.com/<owner>/<repo>/main/small/<itemdefid>_<item_id>.png
https://raw.githubusercontent.com/<owner>/<repo>/main/large/<itemdefid>_<item_id>.png
```

These URLs are referenced from the game's `rocks_steam_itemdefs_master.json` via the `icon_url` and `icon_url_large` fields. Steam fetches and caches its own copy on first publish.
