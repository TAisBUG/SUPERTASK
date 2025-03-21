# SillyTavern-SuperObjective

## 此扩展目前处于测试阶段，可能存在错误或其他异常。如果您发现任何问题，请提交 issue。

## 这是什么？

这是对原始 SillyTavern [Objective](https://docs.sillytavern.app/extensions/objective/) 扩展的重大扩展和部分重写。

SuperObjective 扩展允许您为 AI 在聊天过程中设定一个目标。这个目标会被分解成逐步的任务，可以组织成层级结构。任务可以分支，子任务可以自动或手动创建，让您能够创建复杂的任务树。

这与静态提示不同，它添加了顺序和节奏性的指令，让 AI 无需用户干预就能遵循，创造更真实的 AI 自主追求目标的体验。

## 前提条件

在开始之前，请确保满足以下条件：

- **使用扩展面板中的"管理扩展"按钮卸载原有的 Objectives 扩展。**
- 使用以下链接安装 ST-SuperObjective 扩展：https://github.com/ForgottenGlory/ST-SuperObjective.git，通过扩展面板中的"安装扩展"按钮安装。

## 常见用例

您的想象力就是极限！您可以给 AI 任何目标，它会规划如何实现。示例包括：
- 规划如何屠龙
- 设计营销活动
- 创建详细的故事大纲
- 制定商业策略
- 构建虚构世界

## 开始使用

1. 打开扩展菜单并选择 SuperObjective
2. 在顶部文本框中输入目标
3. 点击"自动生成任务"让 AI 创建任务列表
4. 观察 AI 自动完成各项任务

## 主要功能

### 任务生成和管理

- **自动生成任务**：根据您的目标创建完整的任务列表
- **生成更多任务**：添加额外任务而不需要重新开始
- **任务层级**：创建任务之间的父子关系
- **手动任务创建**：在任何位置添加自己的任务
- **任务编辑**：随时修改任务描述
- **任务移动**：使用拖放功能重新排序任务
- **任务删除**：使用删除按钮移除任务

### 任务进度可视化

- 进度条一目了然地显示完成百分比
- 显示已完成任务与总任务数
- 随着任务完成动态更新
- 通过绿色进度条提供视觉反馈

### 任务完成跟踪

- 在可配置的时间间隔自动检查任务完成情况
- 通过复选框手动完成任务
- 通过扩展菜单手动检查任务
- 当所有子任务完成时，父任务自动完成

### 任务角色配置

- **任务角色选择**：选择任务如何注入到提示中（助手、用户或系统消息）
- 适用于聊天完成和文本完成 API

### 任务持续时间功能

- **任务持续时间**：设置任务可以自动完成前的最小消息数
- 视觉反馈显示持续时间要求的进度（黄色表示持续时间进行中，绿色表示持续时间已过）
- 无论持续时间设置如何，手动完成任务始终可用

### 最近完成的任务

- 维护可配置的最近完成任务列表
- 任务标记完成时自动添加
- 控制提示中包含多少已完成任务
- 在专门的弹出窗口中查看已完成任务，具有增强的 UI
- 不再需要时清除任务
- 启用/禁用在提示中包含已完成任务

### 即将到来的任务

- 自动识别和跟踪当前任务之后的任务
- 优先考虑与当前任务在同一父容器中的任务
- 控制提示中包含多少即将到来的任务
- 在专门的弹出窗口中查看即将到来的任务，具有增强的 UI
- 不再需要时清除任务
- 启用/禁用在提示中包含即将到来的任务

### 任务、模板和提示导入/导出

- **任务模板**：保存和加载可重用的任务结构
- **导出任务**：将当前任务保存到 JSON 文件
- **导入任务**：从之前导出的文件加载任务
- **模板管理**：预览、重命名和删除模板
- **提示集导出/导入**：使用自定义文件名导出和导入自定义提示集

### 统计和历史

- 使用时间戳跟踪任务完成情况
- 查看已完成任务和目标的统计信息
- 所有聊天的全局统计
- 当前会话的聊天特定统计
- 查看最近完成的任务，包含描述和日期

## 配置

### 基本设置

- **在聊天中的位置**：控制任务在 AI 上下文中出现的显著程度
- **任务检查频率**：AI 检查任务是否完成的频率（默认为 3，0 表示禁用）
- **将滑动计入任务检查**：是否将消息滑动计入任务检查计数器的递减（默认禁用）
- **任务注入频率**：控制任务信息注入 AI 上下文的频率（默认为 1，表示每条消息）
- **隐藏任务**：隐藏任务列表以获得更神秘的体验

### 高级设置

- **自定义提示**：编辑用于任务生成和检查的提示
- **保存/加载提示**：保存您的自定义提示以供将来使用

## 使用技巧

### 当前任务选择

当前任务始终是第一个列出的未完成任务。任何任务更新都会触发对当前任务应该是什么的检查。任务按深度优先选择，意味着所有子任务会按顺序首先被选择，然后继续向下列表。

### 分支任务

点击分支任务按钮将当前任务设置为目标，您可以生成或手动创建子任务。您可以继续将任何子任务转换为目标以创建更深的层级。

### 任务持续时间

点击任务上的时钟图标设置任务可以自动完成前必须经过的最小消息数。这对于需要延长对话的任务很有用。

### 任务角色选择

使用每个任务上的下拉菜单确定它如何注入到提示中 - 作为助手、用户或系统消息。这适用于聊天完成和文本完成 API。

### 隐藏任务

如果您想保持对 AI 正在尝试完成的任务不知情，请勾选隐藏任务框以隐藏任务列表。为了最大程度的神秘感，在点击自动生成任务之前执行此操作！

### 任务上下文感知

通过最近完成和即将到来的任务功能，AI 保持对过去成就和未来目标的感知，创造更连贯和以目标为导向的对话体验。

## 警告

任务检查在单独的 API 请求中进行。将任务检查频率设置为 1 将使您对 LLM 服务的 API 调用翻倍。如果您使用付费服务，请谨慎使用此设置。 