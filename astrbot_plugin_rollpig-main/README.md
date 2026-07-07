<div align="center">

![astrbot_plugin_rollpig](https://raw.githubusercontent.com/MegSopern/astrbot_plugin_rollpig/main/logo.png)

# astrbot_plugin_rollpig
_✨ [astrbot](https://github.com/AstrBotDevs/AstrBot) 今日小猪 ✨_ 

[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![AstrBot](https://img.shields.io/badge/AstrBot-3.4%2B-orange.svg)](https://github.com/Soulter/AstrBot)

</div>

## 🌟 项目介绍
每日用户可随机抽取专属“今日小猪”，并生成配图展示名称、描述和性格。无需繁琐配置，支持自定义猪猪库和素材。自动缓存结果，每日刷新，避免重复。适合群聊互动或签到，增添聊天趣味。在astrbot的原插件上，自己加了几十张图，并添加了同一张图的不同文案的随机选择。
## 📦 安装：

```bash
# 克隆仓库到插件目录
cd /AstrBot/data/plugins
git clone https://github.com/Loki-lover/copied-qqbot

# 控制台重启AstrBot
```

## 🐷 使用 🐷

**今日小猪** - 抽取今天属于你的小猪类型 🐖

- 每个用户每天只能抽取一次 🐽  
- 重复抽取不会改变结果 🐷  
- 每天 0 点自动重置 🐖

---

## 🐖 新增小猪 🐖

插件资源路径：

```
astrbot_plugin_rollpig/resource
```

- **pig.json** 小猪信息，例如：

```json
[
    {
        "id": "pig",
        "name": "猪",
        "description": "普通小猪",
        "analysis": "你性格温和，喜欢简单的生活，容易满足。在别人眼中可能有些慵懒，但你知道如何享受生活的美好。"
    },
    {
        "id": "pig",
        "name": "猪",
        "variants": [
            {
                "description": "普通小猪",
                "analysis": "你性格温和，喜欢简单的生活，容易满足。"
            },
            {
                "description": "快乐小猪",
                "analysis": "你很会享受当下，总能发现生活里轻松可爱的一面。"
            }
        ]
    }
]
```

- **image/** 小猪图片  
    - 图片命名需和信息中的 `id` 一致  
    - 支持图片类型：`["png", "jpg", "jpeg", "webp", "gif"]`
    - 同一张图片需要多个文案时，推荐在同一个 `id` 下使用 `variants` 数组；抽中时会随机选择其中一组文案，并在当天缓存中固定

---

### 🐽 目录结构示例 🐽

```
astrbot_plugin_rollpig/
├─ main.py               # 插件主逻辑（AstrBot插件核心）
└─ resource/
    ├─ pig.json          # 小猪信息数据
    └─ image/
        └─ pig.png       # 小猪图片（与id对应）
```

---

## 🐖 注意事项 🐖

- 新增小猪时只需在 `pig.json` 添加对象，并将对应图片放到 `image/` 文件夹即可 🐷  
- 图片自动按 id 匹配，无需在 JSON 中写图片后缀 🐖  

## 🎖️ 致谢
[![GitHub](https://img.shields.io/badge/作者-MegSopern-pink)](https://github.com/MegSopern)
- 本插件基于[nonebot-plugin-rollpig](https://github.com/Bearlele/nonebot-plugin-rollpig)的核心逻辑进行改造。
- 欢迎前往原仓库为作者的辛苦付出点亮 ⭐ Star 支持！
- 此外，作为我在astrbot这边搬运的插件，因为[astrbot_plugin_rollpig](https://github.com/MegSopern/astrbot_plugin_rollpig)也有大半年没有加入新的小猪了，我就自己请人画，并自己在网上搬运可爱好玩的小猪添加到仓库中。


## 📜 许可证

本项目采用 [MIT 许可证](LICENSE) 开源，详情请查阅许可证文件

![Star History Chart](https://api.star-history.com/svg?repos=MegSopern/astrbot_plugin_rollpig&type)
