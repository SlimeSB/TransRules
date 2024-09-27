密涅瓦的猫头鹰要等黄昏到来才会起飞。从这一点看，规范或指南的制定一定是落后于语言的发展的，就像数年前大家更常用“Mod”而今天更常用“模组”。此指南也并非硬性要求，有经验的译者可以自行取舍。  
本文按 CC0 许可证发布，示例及第三方内容保留其原始条款。

## 1.普适原则

- 不得脱离原文。
    - 翻译前最好游玩一遍，熟悉物品、机制、操作后再进行翻译，以免错译。
    - 一般不要丢掉形容词、副词、从句。
    - 适度润色是允许的。
    - **确定**原文有误时可以按实际情况翻译，记得将这一错误反馈给模组作者。
- 译文应符合中文表达习惯
    - 日期时间、货币、度量衡等应一并转换至中文语言习惯。可直接写转换后的数据，也可以括注。
    - 定语从句或被动语态应调整至中文语序。  
        例：`The Red Cedar Tree is a large tree that has magical properties.`（[Totemic](https://www.curseforge.com/minecraft/mc-mods/totemic)）  
        译：`高大无比的红柏树有着魔法的属性。`
- 根据使用场景灵活变通
    - 绝大多数情况直译即可，不必过度发挥。
    - 详见 [## 变通手段](#5变通手段)
- 注意翻译记忆（TM）和术语库
    - 物品、方块、生物是重中之重，务必确保每次引用相同的名称。
    - 模组中多次出现的句式应当有统一的翻译。
    - 模组中多次出现的形容词、副词一般情况下也应统一。
- 因精力有限、能力不足或其他原因，不得不提交半成品翻译时，应删去未翻译的内容。
    - 需要保留原文的内容不应删去。
- 对旧版翻译，非严重错误不建议改动。
- 语言文件一般编码为 `UTF-8 without BOM` 即 UTF-8，在保存时需要注意。
- 模组作者非英语母语者，且有其母语语言文件时，建议以其母语作为源语言进行翻译。如果不熟悉也可以从英语翻译，遇到难以理解的内容时请务必检查母语内容。
- 模组作者的要求与本指南冲突时，以模组作者要求为准。

## 2.格式规范

### 代码保留

- 格式占位符形如 `%s` `%d`，或以 `%` 围起来的字符串（如 `%msg%`）。这些占位符应保留在译文中，它们会在游戏中被替换为对应的文本。
    - 格式占位符可以通过添加位置标识的方式调换前后顺序，以适应翻译的需要。
        - 原文：`Summoned %s with difficulty %d`
        - 译文：`召唤了难度为%2$d的%1$s`
    - 如果不确定最终效果，请打开游戏进行测试。
    - 注意不要误用全角百分号 `％`。
- [格式化代码](https://zh.minecraft.wiki/w/格式化代码)形如 `§0` `§r` ，又称颜色代码。一般使用 `§0` 或者 `&0` 恢复默认颜色，`§r` 或者 `&r` 恢复默认格式。遇到时请保留，并将其放到对应文本两侧。
- 命令如 `/say` `/effect` 以及明文参数请保留不要翻译，而解释性参数则需要翻译
    - 原文：`/time (add|query|set) <time>`（Minecraft，Mojang）
    - 译文：`/time (add|query|set) <时间>`
- 在某些模组的手册中会使用 `<br>`、`\n` 等作为换行符，遇到时请保留。
- 在遇到 tellraw JSON 字符串的时候，请**仅**翻译 `"text"` 项的值，对于其它的键和值均不翻译，请保留
    - 原文：`{"text":" has shared a ","color":"blue"}`（[Botania](https://github.com/Vazkii/Botania)，Vazkii）
    - 译文：`{"text":"分享了一本","color":"blue"}`
- 少数 Mod 使用 XML 格式的语言文件，对于这种文件请保留以 `<` 和 `>` 开头结尾的标签
- 若语言文件所使用的格式上述未提及，请参照对应文件格式进行翻译，若不清楚请查找相应信息或询问其他有经验的译者

### 排版

- 标点符号应与原版Minecraft统一，并使用规范的中文全角标点。
    - 夹用英文时，仅在完整的英文句子中使用英文标点。
    - 方括号 `[]` 建议按原版直接使用 `[]`
    - 进度描述、暂停菜单选项中的省略号可以只用半个 `…`
- 英文字母、阿拉伯数字等非中文字符，与中文字符之间**不应添加空格**分开。
    - 阿拉伯数字与英文单位之间也**不必添加空格**
    - Patchouli 手册中的文本中仍需在中文与非中文字符之间**添加空格**
    - 中文字符与标点符号之间**不必添加空格**。按句翻译时记得删去每句之间的空格。
    - 有特殊规定的术语、专有名词除外。
    - 因排版需要的除外。
- 其他另有格式要求之处除外。

## 3.特殊词汇（第一段未完成）

- 翻译过程中遇到出现频率高的词语，需判断是否要保持术语一致性
    - 对于原版中出现的术语请根据 Minecraft Wiki 上的 [标准译名](https://zh.minecraft.wiki/w/Minecraft_Wiki:%E8%AF%91%E5%90%8D%E6%A0%87%E5%87%86%E5%8C%96) 按照对应 Minecraft 版本进行翻译。
    - 对于其他术语，应当保持前后翻译一致，附属模组与主模组翻译一致。必要时可建立术语库方便管理。
    - 一般来说，术语之间是互斥的。若A已译作A1，那么B则不能译作A1.
    - 一般来说，模组要遵循原版的术语，附属模组、联动模组要遵循主模组的术语。
    - 两个互不相干的模组往往不必保持术语一致，但另有要求的除外。

- 人名/生物名/商标名/曲名
    - 有通用翻译的外文人名或商标，则进行翻译
        - 如翻译牛顿、阿基米德等
    - 出现神话或故事中出现的人物或怪物名请首先搜索流行译名，如果找不到的话则音译
        - 原文：`Baykok`（[Totemic](https://github.com/TeamTotemic/Totemic)，TeamTotemic）
        - 译文：`贝柯克`
    - 指 Mod 社区的某个人物，或贡献列表中的人物，或者已有商标、唱片、歌曲等无中文翻译的则保留不翻译
        - 如 `Vazbee`（[Magic Bees](https://github.com/MagicBees/MagicBees)，MysteriousAges, Arkandos, mezz, et al.）
        - 原文：`Patreon Pie`（[Pam's HarvestCraft](https://github.com/MatrexsVigil/harvestcraft)，MatrexsVigil）
        - 译文：`Patreon派`
    - 对于其它的名字，保留原文不翻译
- 若在现实中有对应的事物存在，但游戏中的表现与该实际事物不相关，应合理变通以区分二者。
- 一些可供参考的资料：
    - [模组翻译参考词典](https://dict.mcmod.cn/)
    - [我的世界中英术语库](https://github.com/CFPAOrg/Glossary)
    - [模组译名标准化列表](https://github.com/Krasjet/Mod-Translation-Styleguide/blob/master/glossary.md)（**部分已过时**）
    - [CFPA汉化仓库](https://github.com/CFPAOrg/Minecraft-Mod-Language-Package) 主页下的各类可用资源
- 如果没有找到，请自行拟定翻译，如果实在无法想出翻译，则暂时保留不译。

### 固定译法

- 一些提示性语句有固定的表达方式
    - 原文：`and %s more...` (Minecraft, Mojang, shulkerBox)
    - 译文：`还有%s项未显示…`
- [字幕](https://zh.minecraft.wiki/w/%E5%AD%97%E5%B9%95)（Subtitle）一般是翻译键中带有 `subtitles` 或 `sound` 的条目。
    - 若字幕原文为主谓结构，则应译作 `主体：声音` 的格式。
        - 原文：`Bee buzzes`（Minecraft，Mojang）
        - 译文：`蜜蜂：嗡嗡`
    - 若原文没有主语，视情况翻译。
        - 原文：`Rowing`（Minecraft，Mojang）
        - 译文：`划船`
- 能量单位、体积单位等（如：FE、RF、MB）请保留不翻译，但出现全称时（如：Forge Energy）需要翻译。
- 键盘功能键​​（如 Shift、Ctrl 等）请不要翻译，并将首字母大写。
- 游戏动作（如 Sneak、Interact、Reload）需要翻译，且不要翻译成对应的按键，因为这些键位是可以更改的。
    - `Sneak + Right Click` -> `潜行右击`
- 鼠标操作（如 Right Click、Click）需要翻译，注意不要译作“左键”（Left Mouse Button）、“右键”，应译作“右键点击”、“右击”等，可以参考原版的翻译。

### 模组名

- 确定模组名的翻译前请至少将整个模组通玩一遍，熟悉模组的特性与整体风格。
- 模组名翻译发挥空间很大，言之有理且大众喜闻乐见即可。
- 简明的模组名称不需要别出心裁重新起名。
    - `Forestry` -> `林业`
    - `Logistics Pipes` -> `物流管道`
    - `Chisel` -> `凿子`
- 已广为人知的模组应采熟知译名。
    - `IndustrialCraft2` -> `工业时代2`
    - `Twilight Forest` -> `暮色森林`
- 国创模组不在翻译业务范围内，但中译英时也可参考本指南原则。
- 机械动力附属模组常以 `Create: ...` 的格式起名，建议采用 `主模组：子模组`  的格式翻译。
    - `Create: Steam 'n' Rails` -> `机械动力：汽鸣铁道`
    - 其他附属模组名也可参考该格式。
- 部分模组存在多个`ItemGroup`，建议统一采用 `模组名丨分栏名` 格式翻译，中间的竖线为汉字 `丨(gǔn)(shù)`
    - `Forestry Apiculture` -> `林业丨养蜂`
- 以生造词或含义广泛的词为模组名时，如果想不出合适的翻译可以先保留原文，等待玩家社区的意见发酵。之后译者可选择数个符合要求的名称开展投票确定最终译名。
    - `Minecraft` -> `我的世界`

## 4.语言风格（未完成）

- 译文应与原文风格一致，按灵活程度分为以下几类。
    - 一般场景
        - 如实翻译，减少发挥
        - 示例占位
    - 梗/meme
        - 若其中文版广为人知，直接使用其中文表达方式。
        - 若晦涩或鲜为人知，根据使用场景替换另一意思差不多的中文梗。
        - 示例占位
    - 幽默恶搞
        - 适度发挥，能传达幽默感即可。
        - 示例占位
    - 诗歌
        - 讲究对仗遣词造句，需兼顾格式与内容。鼓励扩充，谨慎删减。
        - 示例占位
- 神秘/密契主义、宗教相关以及其他特定风格内容，根据各模组风格具体讨论。
- 如果你想进行恶搞性质的“同人创作”，可以前往 [梗体中文资源包](https://github.com/Teahouse-Studios/mcwzh-meme-resourcepack) 。注意遵守该项目的贡献方针。

<!-- - 对于语言的正式程度，请参见词条原文
    - 如果原文非常正式，那么请不要玩梗或卖萌
        - 原文：`This pair of enchanted boots have been stuffed full of magic to ease the journey of any traveler.<BR>They allow you to move faster than normal. They also allow you to jump higher and fall further.`（[Thaumcraft 5](https://github.com/Azanor/thaumcraft-5)，Azanor，节选）
        - 译文：`这双富含神秘的魔力工艺技巧的靴子能让任何旅行者的旅途变得更轻松愉快。<BR>它能够让你移动得比平常更加迅速，并且能够直接掠过较高的台子。它也能够让你跳得更高，落得更远。`
    - 如果原文本身就在玩梗，或者语气非常轻松，那么也不需要使用非常正式的语言
        - 原文：`NANI SORE!? BOTANIA IS OUTDATED!?`（[Botania](https://github.com/Vazkii/Botania)，Vazkii）
        - 译文：`(つд⊂)なにそれ！？植物魔法版本落后了！？`
- 如果原文使用了拉丁化的日语，可以将其书写为对应中文的[空耳](https://zh.moegirl.org.cn/index.php?title=%E7%A9%BA%E8%80%B3)，或者直接保留为罗马音
- 如果原文使用了游戏电影等中的梗，请首先参考原出处的中文翻译，如果是日语而没有统一的翻译，则改写为日语原文（在此情况下请保持翻译与否的统一）
    - 原文：`You notice Botania has updated. It fills you with determination.`（[Botania](https://github.com/Vazkii/Botania)，Vazkii，梗出自于Undertale）
    - 译文：`你注意到植物魔法已经更新了。这使你充满了决心。`
- 如果你自己做了一版卖萌形式或者玩梗形式的汉化文件，请不要发送到作者那里作为默认的汉化文件，仅流传在第三方就行了
- **切勿在语言文件中玩不适宜的烂梗**（尤其是带有较大负面影响的） -->

<span id="5变通手段"></span>

## 5.变通手段（未完成）

- **分切（Cutting）**：拆分长句或复杂结构以适应目标语表达习惯。例如，将汉语流水句拆分为多个英语短句。
- **转换（Conversing）**：调整词性（如名词转动词）或句式（如主动转被动）以符合译入语语法规范。
- **转移（Transposing）**：改变语序或逻辑关系，如将汉语的因果倒置调整为英语的因果顺叙。
- **引申（Extending）**：扩展词义以传达隐含意义，如将文化负载词（如“江湖”）通过加注或释义表达。
- **替代（Substituting）**：用目标语中功能对等的表达替换源语特有概念，如用“the Forbidden City”代指“故宫”。
- **还原（Restituting）**：恢复原文因语言差异被省略的语义成分，如补充汉语无主句的主语。
- **阐释或注释（Interpretation）**：通过脚注或括号补充文化背景信息。
- **融合（Blending）**：糅合源语与目标语的文化元素，如将“粽子”译为“sticky rice dumplings wrapped in bamboo leaves”。
- **音译（Transliterating）**：保留专有名词的音译（如“Taoism”对应“道教”），辅以注释说明。
- **增补（Adding）与省略（Omitting）**：根据目标语读者需求增删冗余信息，如省略汉语重复修辞，增补英语必要的逻辑连接词。
- **重构（Recasting）**：完全重写原文结构以传递等效效果，常见于诗歌或广告翻译。

## 6.署名

除非作者在语言文件中专门提供了翻译者署名的地方，否则不应在任何位置添加翻译者署名，特别是作者要求签署 CLA 的情况。你的贡献将会在 Contribution 或其他合适的地方彰显。

## 7.工具推荐

- [ParaTranz](https://paratranz.cn/) 可以实现大部分 CAT（计算机辅助翻译）功能，并且支持多人协作。  
- Tryanks 编写的适用于 Minecraft 1.16+ 版本的 Minecraft [模组翻译器](https://github.com/CFPATools/Minecraft-Mods-Translator)（**已归档**）
- Snownee 编写的一个[在线网页工具](https://snownee.github.io/l10n-tools/update.html)
- crafteverywhere 之前写的一个[文本更新检测工具](https://github.com/crafteverywhere/Craft_Minecraft_Mod_Localization/blob/master/lang_checker.py)（运行需要 Python 3+ 环境）
- GitHub [语言文件关键字查询](https://github.com/Krasjet/Mod-Translation-Styleguide/blob/master/tools/GithubKeywordQuery.py)（需要 Python 3.4+ 环境）
- GWYOG 的 [LocalizationAssistant](https://github.com/GWYOG/LocalizationAssistant)（运行需要 Java 运行环境，**已过时**）
- 3TUSK 的[文本自动更新工具](https://github.com/3TUSK/TemporaryLocalization/blob/1.9/Tool_Update.lua)（运行需要 Lua 5.3+ 运行环境，**已过时**）

## 8.参考资料

- [Minecraft Mod简体中文翻译规范与指南](https://github.com/Krasjet/Mod-Translation-Styleguide)（喵呜机）
- [Minecraft 模组简体中文翻译规范与指南](旧版链接)（CFPAOrg）
- [中文文案排版指北](https://github.com/mzlogin/chinese-copywriting-guidelines)
- CY∕T 154-2017 中文出版物夹用英文的编辑规范
- ZYF 001-2016 本地化翻译和文档排版质量评估规范
- GBT 19682-2005 翻译服务译文质量要求
