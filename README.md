# qq-bridge-plugins

SnowLuma（小鲸鱼）QQ 桥接项目的 DSH 插件集合。这两个插件是 qq-bridge 的组成部分，发布到这里是为了：

1. 让 [dsh-plugin-updates](https://github.com/InariNGT-Ofiicial/dsh-plugin-updates) 更新引擎能检查它们的 GitHub 源；
2. 让它们进入小鲸鱼插件库（`market/index.json`，format 1 市场索引）。

## 插件

| 目录 | 说明 |
|---|---|
| `qq-mode-console` | QQ 桥接模式控制台：在 DSH settings 里暴露 `qq-mode` 命名空间（chat / closed-agent / reserved / reserved2 / simulation 模式 + ownerQQ），桥接进程通过 DSH settings API 读写。 |
| `qq-agent-presets` | qq-bridge 的 DSH agent preset bundle：把 qq-chat / qq-chat-v2(-xjy) 作为 `@deepseek-ai/dsh-agent-preset` 行插入 profile，并携带预设共用的 qq-tool-restrict 安全守卫。 |

## 安装

跟随 qq-bridge 仓库一起使用时（推荐，本地 link）：

```powershell
dsh plugin add link:./plugins/qq-mode-console
dsh plugin add link:./plugins/qq-agent-presets
```

或通过小鲸鱼插件库（DSH「发现」页 / 桥接控制台「插件库」页）安装——安装参数由 format-1 市场索引自动生成（git 源固定到发布提交）。

## 许可

MIT。人格卡（角色人设）不包含在本仓库中，由 qq-bridge 在运行时注入。
