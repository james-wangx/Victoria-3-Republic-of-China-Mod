# Victoria 3 Republic of China Mod

<p align="center"><img src="thumbnail.png" width="200" alt="ROC"></p>

<p align="center">
  <img src="https://img.shields.io/badge/Game-Victoria%203-blue" alt="Game">
  <img src="https://img.shields.io/badge/Game%20Version-1.13.10%20Matcha-blue" alt="Game Version">
  <img src="https://img.shields.io/badge/Mod%20Version-1.13.10-blueviolet" alt="Mod Version">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License">
  <img src="https://img.shields.io/badge/Language-English%20%7C%20ZH--CN-lightgrey" alt="Language">
</p>

A Victoria 3 (1.13.10 Matcha) mod that adds the **Republic of China (ROC)** as a formable nation
for Qing China, together with China-specific companies, regional state traits and unique
buildings.

**Tags:** Formable Nation · Companies · State Traits · Unique Buildings

> 中文版说明见 [README.zh-CN.md](README.zh-CN.md) / Chinese version: [README.zh-CN.md](README.zh-CN.md)

## Features

### Formable nation: Republic of China (ROC)

| Item | Value |
| --- | --- |
| Tag | `ROC` |
| Country type | Recognized |
| Tier | Hegemony |
| Primary culture | `han` |
| Capital | Nanjing (`STATE_NANJING`) |
| Map color | `{ 23 61 115 }` (blue) |
| Required states | Cultural homelands of the `han` culture (`use_culture_states = yes`) |
| Required states fraction | 60% (`required_states_fraction = 0.6`) |
| Formation conditions (`possible`) | Primary culture is `han`; `ROC` does not exist yet; government is a republic (Presidential or Parliamentary Republic); voting franchise is enabled |
| AI will do | Always |

On formation, the country's capital is moved to Nanjing (`STATE_NANJING`) and its market
capital is moved to Suzhou (`STATE_SUZHOU`).

The country name changes with the government type, mirroring vanilla `CHI` behavior:

| Government type | Country name |
| --- | --- |
| Monarchy | Empire of China (中华帝国) |
| Communist | People's Republic of China (中华人民共和国) |
| Republic (default) | Republic of China (中华民国) |

Flags reuse the vanilla China coat of arms (Five-Colored Flag for republics, Kuomintang flag for
dictatorships, Han imperial flag for monarchies, plus theocracy and communist variants), so no
new graphics assets are required.

### Game start setup

Tibet (the Lhasa and Ngari states) starts directly as part of Qing China as
unincorporated territory instead of a Qing subject; the vanilla Qing-Tibet
vassal pact is removed at game start.

### Companies

Ten China-specific companies, five of which replace vanilla companies (`TRY_REPLACE`). All
companies require an incorporated state (`is_incorporated = yes`) and the stated building at
level 5 or higher in their headquarters state.

| Company | Type | Headquarters | Core buildings | Extensions | Prestige goods | Requirements | Prosperity modifier |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Hanyeping Company | New | Suzhou | Coal mine, iron mine, steel mill | Railway | Refined steel | Open Hearth Process; Suzhou steel mill ≥ 5 | +10% steel mill throughput; +10% railway throughput |
| Hanyang Arsenal | Replaces vanilla | Eastern Hubei | Arms industry, explosives factory, munition plant | Artillery foundry | Hanyang Rifle, high-grade explosives | Bolt-Action Rifles; Eastern Hubei arms industry ≥ 5 | +10% army offense; +10% army defense |
| Jiangnan Weaving Bureaus | Replaces vanilla | Suzhou / Zhejiang / Nanjing | Silk plantation, textile mill, cotton plantation | Dye plantation | Suzhou silk | SoI DLC; South China interest; silk plantation or textile mill ≥ 5 | +10% textile mill throughput; +10% silk plantation throughput |
| Taikang Food Company | New | Shandong / Suzhou | Food industry | Fishing wharf | Gourmet groceries | Canneries; Shandong or Suzhou food industry ≥ 5 | +10% food industry throughput; +10% trade advantage |
| Yanchang Petroleum Company | New | Xi'an | Oil rig | Power plant | — | Xi'an oil rig ≥ 5 | +20% oil extraction throughput |
| Shanghai Electric Company | New | Suzhou | Power plant, railway | Electrics industry | — | Suzhou power plant ≥ 5 | +10% power plant throughput; +10% railway throughput |
| Shanghai Machine Paper Mill | New | Suzhou | Paper mill | Logging camp | Craft paper | Mechanical Tools; Suzhou paper mill ≥ 5 | +10% paper mill throughput; +10% bureaucracy |
| China Merchants' Steam Navigation Company | New | Suzhou | Trade center, port | Shipyard | Swift merchant marine | Suzhou trade center ≥ 5 and port ≥ 5 | +10% trade advantage; +10% port throughput |
| Jiangnan Arsenal | New | Suzhou | Motor industry, tooling workshop | Automotive industry | Jiangnan engines, precision tools | Suzhou motor industry ≥ 5 | +10% capital ship construction efficiency; +10% motor industry throughput |
| Foochow Arsenal | Replaces vanilla | Fujian | Shipyard | Motor industry | — | Ironclads and Gantry Cranes; Fujian shipyard ≥ 5 | +10% supply ship construction efficiency; +10% shipyard throughput |

The custom prestige goods (Hanyang Rifle, Jiangnan Engines) require the *Sphere of Influence*
DLC (`mp1_content`); the other prestige goods reuse vanilla ones.

All companies produce every listed prestige good as soon as they are prosperous
(`prestige_goods_trigger = { always = yes }`), so companies with multiple prestige goods
(Hanyang Arsenal, Jiangnan Arsenal) produce all of them.

### State traits

Twenty state traits: nineteen ROC-specific traits plus a rebalanced vanilla Yellow River trait
(infrastructure bonus kept, market access price impact removed). Traits are grouped by category.

| Trait | Category | Applied to (states) | Effects |
| --- | --- | --- | --- |
| Yellow River (rebalanced) | River | Hebei, Shandong, Shanxi, Inner Mongolia, Henan | +15 infrastructure |
| Beijing–Hangzhou Grand Canal | River | Beijing, Hebei, Shandong, Northern Anhui, Jiangsu, Nanjing, Suzhou, Zhejiang | +15 infrastructure; −5% market access price impact |
| Heilongjiang River | River | Northern Heilongjiang, Southern Heilongjiang, Northern Jilin, Southern Jilin | +15 infrastructure |
| Mongolian Plateau Deposits | Mining | Uliastai, Urga | +10% coal mine throughput; +10% iron mine throughput |
| Anshan–Benxi Iron | Mining | Shengjing | +10% iron mine throughput |
| Fushun Coal | Mining | Shengjing | +10% coal mine throughput |
| Datong Coal | Mining | Shanxi | +10% coal mine throughput |
| Pingxiang Coal | Mining | Jiangxi | +10% coal mine throughput |
| Daye Iron | Mining | Eastern Hubei | +10% iron mine throughput |
| Panzhihua Iron | Mining | Sichuan | +10% iron mine throughput |
| Yumen Oilfield | Mining | Gansu | +10% oil extraction throughput |
| Daqing Oilfield | Mining | Southern Heilongjiang | +20% oil extraction throughput |
| Karamay Oilfield | Mining | Dzungaria | +10% oil extraction throughput |
| Bayan Obo Iron | Mining | Inner Mongolia | +20% iron mine throughput |
| Kailuan Coal | Mining | Hebei | +10% coal mine throughput |
| Shenfu–Dongsheng Coalfield | Mining | Xi'an | +20% coal mine throughput |
| Northeast Black Soil | Agriculture | Southern Heilongjiang, Southern Jilin | +20% agriculture throughput; +20% plantation throughput |
| Jiangnan Land of Fish and Rice | Agriculture | Jiangsu, Nanjing, Suzhou, Zhejiang | +20% agriculture throughput; +20% plantation throughput |
| North China Plain | Agriculture | Beijing, Hebei, Shandong, Northern Anhui, Henan | +10% agriculture throughput; +10% plantation throughput |
| Shanghai Port | Port | Suzhou | +30% trade capacity; −10% market access price impact; +20% shipyard throughput; +20% port throughput |

### Unique buildings

Six unique (monument) buildings tied to the Republic of China era. They use the
`bg_monuments` building group, cannot be expanded or downsized, and require a republican
government. Existing vanilla icons and backgrounds are reused, no new art required.

| Building | Location (state) | Effects | Requirements |
| --- | --- | --- | --- |
| Presidential Palace | Nanjing | +100 authority; +50 prestige; 800 clerk / 200 bureaucrat jobs; +20% government administration throughput | Han primary culture; Republic government (Presidential / Parliamentary); Steel-Frame Buildings technology |
| Whampoa Military Academy | Guangdong | +20% general rank impact; +20% daily organization gain; +50 training rate; 100 officer / 100 clerk / 1,800 soldier jobs | Han primary culture; Republic government (Presidential / Parliamentary); General Staff technology |
| Shanghai Stock Exchange | Suzhou (Shanghai) | +50 prestige; +10% capitalist / aristocrat investment pool contribution efficiency; 800 clerk / 100 capitalist / 100 aristocrat jobs | Han primary culture; Republic government (Presidential / Parliamentary); Mutual Funds technology; requires Interventionism or Laissez-Faire law |
| Academia Sinica | Nanjing | +1,000 academic jobs; +10% tech spread; +10% innovation; +20 max innovation investment | Han primary culture; Republic government (Presidential / Parliamentary); Dialectics technology |
| National Assembly Hall | Nanjing | +100 authority; +10 legitimacy from votes; -10% legitimacy penalty from ideological incoherence; 200 bureaucrat / 800 clerk jobs | Han primary culture; Republic government (Presidential / Parliamentary); Steel-Frame Buildings technology |
| Central Bank | Suzhou (Shanghai) | +200 bureaucrat / 800 clerk jobs; +100 authority; +10% minting; -5% loan interest rate; +5% max trade advantage from capacity | Han primary culture; Republic government (Presidential / Parliamentary); Central Banking technology |

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
- Redefines the vanilla `on_country_formed` on_action (the full 1.13.10 chain is included).
  Other mods that also define it (e.g. Community Mod Framework, Cold War Project) override
  each other by load order; only the last-loaded mod's version runs.
- UTF-8 BOM + CRLF encoding is used for all script and localization files.

## Project Layout

```text
common/country_definitions/      ROC country definition (colors, tier, cultures, capital)
common/country_formation/        ROC formable nation (culture states, possible)
common/dynamic_country_names/    Government-type based country names
common/history/states/           Tibet (Lhasa/Ngari) as unincorporated Qing territory
common/history/diplomacy/        Remove the vanilla Qing-Tibet vassal pact
common/on_actions/               Vanilla on_country_formed chain + ROC capital/market moves
common/flag_definitions/         Flags reusing vanilla China coat of arms
common/company_types/            ROC company definitions
common/prestige_goods/           Custom ROC prestige goods
common/state_traits/             Rebalanced Yellow River trait + ROC state traits
common/buildings/                ROC unique building definitions
common/production_methods/       ROC unique building production methods
common/production_method_groups/ ROC unique building PM groups
map_data/state_regions/          Overridden East Asian states with ROC traits attached
localization/english/            English localization
localization/simp_chinese/       Simplified Chinese localization
```

## License

This mod is licensed under the [MIT License](LICENSE).
