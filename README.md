# 宏观日历解读

`laogu-macro`

宏观日历解读 skill：加载即生成本周宏观事件日历中文解读（议息会议、PMI、CPI、就业数据，时间注北京时间）+ 影响链条解读 + 跟踪点。

## 一键安装

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-macro`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-macro.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-macro/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-macro/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-macro/`（项目级用 `.trae/skills/laogu-macro/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，定时能力由宿主平台提供）
- `references/sources.md` — 数据源：财经日历搜索模板、来源优先级、北京时间换算规则

## 输出结构

- 本周宏观日历：日期+北京时间+事件+来源（A股休市日单独标注）
- 重点事件影响链条：直接影响 → 传导路径 → 对A股/汇率/大宗的二级影响
- 跟踪点：公布时间与市场关注焦点
- 一句话提示：本周最值得盯的 1-2 个事件（不预测涨跌）

## 定时建议

- 每周一开盘前推送（如 8:30）
- 可与 `laogu-morning` 联动：早报中的"宏观事件日历"子项直接引用本周解读

## 使用注意

- 宏观日历无统一公开 API，以网页搜索财经媒体日历为主力路径，事件时间需两个以上来源交叉
- 长假休市安排每年以官方公告为准，不凭记忆写日期

---
## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。
