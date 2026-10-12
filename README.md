# 白教堂来信 · 五警探与杰克

Foundry VTT v12 模组，当前版本 **0.1.0-dev.1 Pre-release**。五名普通玩家分别控制五名警探，指定 GM 扮演杰克并在线裁决。

## 安装

在 Foundry Setup 的“附加模组 → 安装模组”粘贴以下 Manifest URL：

```text
https://raw.githubusercontent.com/litchicalpis/whitechapel/main/module.json
```

[发布页与安装包](https://github.com/litchicalpis/whitechapel/releases/tag/v0.1.0-dev.1)

也可下载 `whitechapel-0.1.0-dev.1.zip`，将其中的 `whitechapel` 解压到 `Data/modules/`，重启 Foundry 并在测试 World 中启用。不要使用 GitHub 自动生成的 Source code ZIP；仓库默认分支仅托管 README 和清单，完整运行代码、可编辑地图数据、文档及来源许可证在安装 ZIP 内。

进入世界默认不自动打开；使用 `Shift+W`、Token 工具栏放大镜或模组设置入口打开。“进入世界时打开白教堂”为客户端偏好，已有显式选择不会被默认值覆盖。

## 已实现

- 修订版基础规则：准备、四夜追逐、调查与逮捕、马车、小巷、第三夜双案发和胜负判定。
- 195 个编号地点、234 个路口、591 条道路的可缩放矢量棋盘；不含官方棋盘扫描图。
- GM 全量信息默认折叠，自动保存、备份恢复、席位重绑及旧案件归档。
- 杰克视角日志过滤未知信息，可复制地图、规则和局面给 AI；返回动作须校验并经 GM 确认，不自动调用外部 AI 服务。

## 验证边界

51 项 Node 自动化测试与 16 项真实浏览器检查通过。浏览器使用模拟 Foundry 文档、用户与通信接口，**不是实际 FVTT v12 服务器验收**，因此标记 Pre-release，清单不填写 `compatibility.verified`。请先在测试 World 或现有世界副本使用，升级前备份。

保密采用可信牌桌模式，不提供对管理员或恶意客户端的严格隔离；杰克输入包含自身秘密，不应发送给警方。首版不包含 Dear Boss 或可选规则。

地图由社区数据转换并交叉核验，不是出版社认证。随包 `DATA-SOURCES.md` 记录来源与差异，`data/` 保留 LGPL-3.0、GPL-3.0 和 MIT 来源许可、原始记录及独立数据；不改变第三方数据的许可证。使用说明和完整验证边界见随包 `README.md`、`VALIDATION.md`。
