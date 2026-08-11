# AUCTRIX Anti-Novel AI Writing

版本：1.2.1-revised  
创作者：**VIRÉCHO**

AUCTRIX 系列剧本清洗 Skill。用于清理影视剧本、短剧、AI 漫剧、分镜前置文本中的小说化描写、模板化 AI 表达、主体歧义和无效表演标注。

本修订版把“信息保真”置于“影视化”之前：清洗时不得凭空增加人物、道具、动作、环境、因果或剧情结果。原文缺少足够画面依据时，保留必要信息并标记确认，不用虚构细节强行转换。

## 作者与 AUCTRIX 定位

本 Skill 由 **VIRÉCHO** 创作，可独立安装、单独调用，作为完整的剧本去小说化与去 AI 腔清洗工具使用。

同时，本 Skill 也是 VIRÉCHO 未来剧本 Agent **AUCTRIX** 的基础能力模块之一，计划在 AUCTRIX 工作流中承担剧本清洗、信息保真、主体明确和生成前置整理。无论独立使用还是由 AUCTRIX 调用，都遵守同一原则：清洗不是改戏，明确不等于加料。

## 适用任务

- 去小说味、去 AI 味、剧本清洗
- 明确动作主体和人物指代
- 清理模板化动作、表情与台词括号
- 在不改戏的前提下整理分镜或 AI 图像／视频前置文本

它不是剧情重写器，也不会自动增加爽点、感情线、钩子或镜头设计。

## 1.2.1-revised 主要修订

- 修复示例“禁止新增剧情，却凭空新增道具和事件”的矛盾
- 将硬性“不许变长”改为“以精简为目标，允许为消除歧义少量增字”
- 区分剧本清洗、生成前置和严格压缩三种模式
- 补充普通对白的去 AI 腔规则，同时保护人物声线和潜台词
- 规定无法无损可视化时使用 `【需确认：……】`，不得猜写
- 精简核心 Skill，并明确参考文件的读取条件
- 增加 `agents/openai.yaml` 界面元数据
- 增加创作者 VIRÉCHO 署名及未来剧本 Agent AUCTRIX 的项目定位

## 安装

将以下内层文件夹复制到 Codex Skills 目录：

```text
auctrix-anti-novel-ai-writing/
```

不要把最外层发布目录整体当作 Skill 安装，否则 `SKILL.md` 的层级可能不正确。

## 结构

```text
AUCTRIX-anti-novel-ai-writing/
├── README.md
├── LICENSE
└── auctrix-anti-novel-ai-writing/
    ├── SKILL.md
    ├── LICENSE
    ├── agents/
    │   └── openai.yaml
    └── references/
        ├── anti-ai-patterns.md
        ├── before-after-examples.md
        └── dialogue-cleaning.md
```

## License

MIT
