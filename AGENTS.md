# Victoria 3 Republic of China Mod

## Rules

- All documentation and code comments must be written in English.

## References

- Official modding documentation (Paradox Wiki): https://vic3.paradoxwikis.com/Modding
- Game files (base game directory, same structure as the mod folder):
  `C:\Program Files (x86)\Steam\steamapps\common\Victoria 3\game`
- Installed mods directory (Steam Workshop content):
  `C:\Program Files (x86)\Steam\steamapps\workshop\content\529340`
- Current game version: 1.13.10 (Matcha)

## Maintenance

- When the game updates, re-sync every state definition overridden in
  `map_data/state_regions/99_roc_east_asia.txt` with the matching vanilla state in
  `game/map_data/state_regions/11_east_asia.txt` or `15_russia.txt` (provinces, arable
  land, resources, city/port/farm/mine/wood, IDs, etc.), keeping only the mod-specific
  additions such as the `state_trait_roc_*` entries in the `traits` block.

## Installed mods

Each subfolder under the workshop content directory is named by workshop id; the `name` field in
`<id>\.metadata\metadata.json` is the mod name (UTF-8 encoded).

| Workshop ID | Name |
| --- | --- |
| 2880069248 | 牛奶汉化 |
| 2881762225 | Dense Market Details |
| 2881990033 | Divergences CN |
| 2882576273 | Daoyu Cheat - Achievement Available Cheat Tool |
| 2884578451 | 民国行政区划 & 地图细节修正 |
| 2889925770 | [1.13] Morgenroete - Dawn of Flavor |
| 2895083666 | Marble Emperor |
| 2898469548 | Formable Nations: Plus [1.13] |
| 2927730563 | Age Of Ming |
| 2941771030 | Cold War Project |
| 2981574864 | Western Clothes: Redux |
| 2988303719 | Cold War Era (1950) |
| 3032185644 | More Unique Companies |
| 3033142209 | Real England |
| 3043932826 | Super Power |
| 3086429193 | 牛奶汉化之公司扩展 |
| 3087374456 | Panama-Suez Canal Company |
| 3118003368 | Divergences of Darkness |
| 3119303385 | qunxings' Factory Expansion |
| 3188040563 | More Wonders 更多奇观 |
| 3199730217 | Hail, Columbia! - United States Flavor Pack |
| 3219394272 | Victorian Century |
| 3227982912 | Kuromi's AI |
| 3249824317 | Cold War Era (1946) |
| 3279083349 | [1.7.5]China Revision-v1.4 |
| 3287619434 | More principle groups |
| 3301469448 | Pharmaceuticals and Hospitals |
| 3338630543 | Mandate of Heaven |
| 3346844497 | Interwar 1910-1960 |
| 3385002128 | [1.13] Community Mod Framework |
| 3402206104 | More Formables |
| 3442069606 | Westernized Uniforms |
| 3459869359 | Explorable Real-World Resources |
| 3472248460 | [1.13] Tech & Res |
| 3527702083 | Improved Company List |
| 3532981672 | Earth United Nations |
| 3535929411 | Project Utopia - Extended Timeline - Technical Preview |
| 3537967277 | 乌托邦计划 - 扩展时间线 - 技术预览 (中文汉化) |
| 3543487941 | Coat of Arms for Powerblocs |
| 3577586767 | Assimilation & Homeland |
| 3581945635 | Uboy.UI-Companies_filter |
| 3614842384 | Age of Discovery 1444 [1.11] (All Languages) |
| 3631994291 | More Wonder/Unique Building Update |
| 3637985014 | 中国史实/想象公司拓展 |
| 3660310561 | Sacré Bleu |
| 3687643380 | Swap Decentralized |
| 3717461054 | Cheat Menu Pro |
| 3725477773 | UNIPOLAR |
