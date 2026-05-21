# Lark Agent Skills

飞书 / Lark AI Agent Skills — 23 个面向 [lark-cli](https://github.com/larksuite/lark-cli) 的 agent skill，让 AI 助手能够通过自然语言操作飞书资源。

## 快速开始

### 前置条件

1. 安装 OpenCode：参考 [opencode.ai](https://opencode.ai)
2. 安装 lark-cli：`npm install -g @larksuite/lark-cli`
3. 安装 skills：

```bash
opencode skills install --from github:7emotions/lark-skills
```

### 首次配置

```bash
# 初始化飞书应用配置
lark-cli config init --new
```

按提示在浏览器中完成授权后即可使用。

## Skills 目录

### 基础设施

| Skill | 说明 |
|-------|------|
| [lark-shared](lark-shared/SKILL.md) | 🔧 共享基础：配置初始化、认证登录、身份切换、权限管理 |
| [lark-openapi-explorer](lark-openapi-explorer/SKILL.md) | 🔍 OpenAPI 探索：查找并调用未经 CLI 封装的原生飞书 API |
| [lark-skill-maker](lark-skill-maker/SKILL.md) | 🛠️ 自定义 Skill 创建：将飞书 API 操作封装成可复用 Skill |

### 即时通讯

| Skill | 说明 |
|-------|------|
| [lark-im](lark-im/SKILL.md) | 💬 即时通讯：收发消息、管理群聊、上传下载文件、表情回复 |

### 协作文档

| Skill | 说明 |
|-------|------|
| [lark-doc](lark-doc/SKILL.md) | 📄 云文档：创建/编辑飞书文档，Markdown 导入，图片管理 |
| [lark-sheets](lark-sheets/SKILL.md) | 📊 电子表格：创建表格、读写数据、筛选视图、样式设置 |
| [lark-slides](lark-slides/SKILL.md) | 📽️ 幻灯片：创建演示文稿、管理 PPT 页面 |
| [lark-base](lark-base/SKILL.md) | 🗃️ 多维表格：建表、字段管理、记录读写、视图配置、工作流 |
| [lark-wiki](lark-wiki/SKILL.md) | 📚 知识库：管理知识空间、成员和文档节点 |

### 文件与空间

| Skill | 说明 |
|-------|------|
| [lark-drive](lark-drive/SKILL.md) | ☁️ 云空间：上传下载、文件夹管理、权限设置、格式导入 |

### 日历与会议

| Skill | 说明 |
|-------|------|
| [lark-calendar](lark-calendar/SKILL.md) | 📅 日历：日程管理、参会人邀请、忙闲查询、会议室预定 |
| [lark-vc](lark-vc/SKILL.md) | 🎥 视频会议：查询会议记录、获取 AI 纪要（总结/待办/章节） |
| [lark-minutes](lark-minutes/SKILL.md) | 🎙️ 妙记：查询妙记列表、下载音视频、获取 AI 产物 |

### 流程与管理

| Skill | 说明 |
|-------|------|
| [lark-approval](lark-approval/SKILL.md) | ✅ 审批：审批实例管理、审批任务处理 |
| [lark-task](lark-task/SKILL.md) | ✅ 任务：创建待办、管理清单、分配协作成员 |
| [lark-okr](lark-okr/SKILL.md) | 🎯 OKR：目标与关键结果管理 |

### 人员与通讯

| Skill | 说明 |
|-------|------|
| [lark-contact](lark-contact/SKILL.md) | 👤 通讯录：查询组织架构、搜索员工、获取用户信息 |
| [lark-mail](lark-mail/SKILL.md) | ✉️ 邮箱：起草、发送、回复、转发邮件，管理文件夹和标签 |

### 其他

| Skill | 说明 |
|-------|------|
| [lark-attendance](lark-attendance/SKILL.md) | 🕐 考勤：查询打卡记录 |
| [lark-event](lark-event/SKILL.md) | 🔔 事件订阅：WebSocket 实时监听飞书事件 |
| [lark-whiteboard](lark-whiteboard/SKILL.md) | 🎨 画板：查看/编辑画板，PlantUML/Mermaid 可视化 |

### 工作流

| Skill | 说明 |
|-------|------|
| [lark-workflow-meeting-summary](lark-workflow-meeting-summary/SKILL.md) | 📋 会议纪要整理：汇总指定时间范围的会议纪要并生成报告 |
| [lark-workflow-standup-report](lark-workflow-standup-report/SKILL.md) | 📋 日程待办摘要：生成当日日程与未完成任务摘要 |

## 使用示例

安装后，通过自然语言与 AI 助手交互：

```
"帮我查一下明天下午有哪些会议"
"在飞书创建一个项目周报文档"
"给我的团队群发一条消息说明天九点开会"
"把这周的会议纪要整理成周报"
"查一下张三的联系方式"
```

## 目录结构

每个 skill 遵循标准结构：

```
lark-xxx/
├── SKILL.md              # Skill 主文件（元数据 + 指令）
├── references/           # 参考文档（API 工作流、最佳实践）
│   ├── lark-xxx-xxx.md
│   └── ...
└── scripts/              # 辅助脚本（如有）
```

## 许可

Private — 7emotions
