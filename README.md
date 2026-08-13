# Victoria 3 Republic of China Mod

<p align="center"><img src="thumbnail.png" width="200" alt="ROC"></p>

A Victoria 3 (1.13.10 Matcha) mod that adds the **Republic of China (ROC)** as a formable nation
for Qing China.

> 中文版说明见 [README.zh-CN.md](README.zh-CN.md) / Chinese version: [README.zh-CN.md](README.zh-CN.md)

## Features

- Adds the **Republic of China (ROC)** as a formable nation for countries with `han` primary
  culture (e.g. Qing China).
- ROC is a recognized hegemony with its capital in Nanjing (`STATE_NANJING`).
- Required states use the **cultural homelands of the `han` culture** (`use_culture_states = yes`)
  instead of a hardcoded state list.
- Flags reuse the vanilla China coat of arms (Five-Colored Flag, Kuomintang, monarchy, theocracy,
  and communist variants), so no new graphics assets are required.
- Dynamic country names follow the government type, mirroring vanilla `CHI` behavior:
  - Monarchy: **Empire of China** (中华帝国)
  - Communism: **People's Republic of China** (中华人民共和国)
  - Otherwise (default): **Republic of China** (中华民国)
- Adds a China-specific **Hanyeping Coal and Iron Company** (`company_roc_hanyeping`) with coal
  mines, iron mines and steel mills. It produces refined steel as a prestige good and becomes
  available once the open hearth process is researched and any incorporated state has a steel
  mill at level 5 or higher.

## Requirements

- Victoria 3 version **1.13.10 (Matcha)**
- The mod must be enabled in the launcher play set

## Installation

1. Copy the mod folder into the Victoria 3 `mod` directory:

   `C:\Users\<user>\Documents\Paradox Interactive\Victoria 3\mod\`

2. Enable **Republic of China** in the Paradox launcher play set.
3. Start a new game as Qing China (or another `han`-culture country).
4. Open the **Nation Formation** tab on the Journal screen and form the Republic of China.

## Compatibility

- Works with vanilla 1.13.10. No vanilla files are overwritten; all content is added via new files.
- Uses the tag `ROC`. Other workshop mods may define the same tag (e.g. Cold War Project,
  Cold War Era 1950, China Revision) and may conflict if enabled together.
- UTF-8 BOM + CRLF encoding is used for all script and localization files.

## Project Layout

```text
common/country_definitions/      ROC country definition (colors, tier, cultures, capital)
common/country_formation/        ROC formable nation (culture states, possible)
common/dynamic_country_names/    Government-type based country names
common/flag_definitions/         Flags reusing vanilla China coat of arms
common/company_types/            Hanyeping Coal and Iron Company definition
localization/english/            English localization
localization/simp_chinese/       Simplified Chinese localization
```

## License

This mod is licensed under the [MIT License](LICENSE).
