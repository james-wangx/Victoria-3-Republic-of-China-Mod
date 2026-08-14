# 维多利亚3 中华民国 Mod

<p align="center"><img src="thumbnail.png" width="200" alt="ROC"></p>

一个为 **维多利亚3（1.13.10 Matcha）** 制作、为清朝中国新增 **中华民国（ROC）** 成立国家的 Mod。

> English version: [README.md](README.md)

## 功能

- 为拥有 `han` 主流文化的国家（如大清）新增 **中华民国（ROC）** 成立国家。
- 中华民国为得到承认的霸权国家，首都在南京（`STATE_NANJING`）。
- 所需领土使用 **`han` 文化的文化故土**（`use_culture_states = yes`），无需硬编码州列表。
- 旗帜复用原版中国的盾徽（五色旗、国民党旗、君主制、神权制与共产制变体），无需新增图形资源。
- 国名随政府类型动态变化，与原版 `CHI` 行为一致：
  - 君主制：**中华帝国**
  - 共产主义：**中华人民共和国**
  - 其他（默认）：**中华民国**
- 新增中国专属的 **汉冶萍公司**（`company_roc_hanyeping`），建筑为煤矿、铁矿与炼钢厂；名贵商品为精炼钢；研究“平炉炼钢法”后，苏州为已整合地区且炼钢厂达到 5 级即可成立。
- 替换原版 **汉阳兵工厂**：科技条件改为“栓动式步枪”，增益为陆军进攻 +10%、防御 +10%，名贵商品为“汉阳造步枪”。
- 替换原版 **江南织造局**：棉花种植园改为基础建筑，染料作物种植园为扩展建筑，增益改为纺织厂 +10%、丝绸种植园 +10%。
- 新增中国专属的 **泰康食品公司**（`company_roc_taikang_foods`）：建筑为食品厂，扩展行业为渔业码头，名贵商品为精加工食品，增益为食品厂 +10%、贸易优势 +10%；研究“罐装机”科技后，山东或苏州的已整合地区食品厂达到 5 级即可成立。
- 新增中国专属的 **延长石油公司**（`company_roc_yanchang_petroleum`）：建筑为油田，增益为油田吞吐量 +20%；陕西为已整合地区且油田达到 5 级即可成立。

## 需求

- 维多利亚3 **1.13.10（Matcha）** 版本
- 需要在启动器中启用本 Mod

## 安装

1. 将 Mod 文件夹复制到维多利亚3的 `mod` 目录：

   `C:\Users\<用户名>\Documents\Paradox Interactive\Victoria 3\mod\`

2. 在 Paradox 启动器的播放集中启用 **Republic of China**。
3. 以大清（或其他 `han` 文化国家）开始新游戏。
4. 打开日志界面（Journal）中的 **成立国家** 标签页，成立中华民国。

## 兼容性

- 兼容原版 1.13.10；不覆盖任何原版文件，所有内容均通过新文件添加。
- 使用 `ROC` 标签。其他 Workshop Mod 可能定义相同标签（例如 Cold War Project、
  Cold War Era 1950、China Revision），同时启用时可能冲突。
- 所有脚本与本地化文件均使用 UTF-8 BOM + CRLF 编码。

## 项目结构

```text
common/country_definitions/       ROC 国家定义（颜色、等级、文化、首都）
common/country_formation/         ROC 成立国家（文化故土、possible 条件）
common/dynamic_country_names/     按政府类型变化的国名
common/flag_definitions/          复用原版中国盾徽的旗帜
common/company_types/             汉冶萍公司定义（煤矿、铁矿、炼钢厂）
common/prestige_goods/            汉阳造步枪名贵商品
localization/english/             英文本地化
localization/simp_chinese/        简体中文本地化
```

## 许可

本 Mod 采用 [MIT 许可证](LICENSE)。
