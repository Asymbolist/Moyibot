🤖 墨逸QQ机器人 (MoyiBot)

一款基于 Python NoneBot2 框架开发，功能丰富、易于管理的智能QQ机器人助手。它拥有精美的Win11风格图形化管理界面，集成了AI对话、娱乐互动、媒体处理等核心功能，致力于为用户提供安全、有趣、高效的群组与私聊自动化体验。

---

🚀 快速开始

环境要求

在开始使用前，请确保你的系统满足以下条件：

· 操作系统: Windows 10 / 11, macOS, 或 Linux
· Python: 3.8 或更高版本，并且必须确保在安装时勾选了“Add Python to PATH”选项。
· 网络: 能够正常访问互联网。
· QQ账号: 一个用于登录机器人的QQ小号（出于安全考虑，强烈建议不要使用主号）。

使用说明

第一步：获取与安装

1. 克隆或下载项目到你的本地电脑。
2. 安装核心依赖：打开命令行工具（CMD/PowerShell/Terminal），进入项目根目录 MoyiBot/，运行以下命令：
   ```bash
   pip install -r requirements.txt
   ```

第二步：一键配置与启动

1. 进入项目根目录 MoyiBot/。
2. 运行 启动管理面板.bat（Windows）或 python bot_gui.py（macOS/Linux）。
3. 首次启动会打开墨逸机器人管理面板，这是一个符合Win11设计风格的图形化配置界面。

第三步：配置机器人
在管理面板中，你需要完成以下基本配置：

· 基础设置：填写你的主人QQ号。
· AI API配置（可选）：如需使用AI对话(/ai)和翻译功能，在此处填写你的DeepSeek或豆包等服务的API密钥。
· 功能管理：根据需要启用或禁用各项功能模块。

第四步：连接QQ
墨逸机器人需要通过go-cqhttp 连接QQ官方服务器。你已将此连接器放置在项目中，请按以下步骤操作：

1. 在项目根目录下，运行 go-cqhttp 可执行文件。
2. 首次运行时，在命令行中选择 0（正向WebSocket）。
3. 程序将提示你扫码登录之前准备好的QQ小号。

第五步：开始使用

1. 在管理面板中点击“启动机器人”。
2. 现在，你的机器人已经上线！你可以在QQ群或私聊中尝试以下命令：
   · /帮助 - 获取完整的命令列表和使用指南。
   · /关于 - 查看机器人版本和制作者信息。
   · /点歌 歌曲名 - 体验完整的免责条款流程后，获取音乐。

📁 项目结构与核心文件

了解项目结构能帮助你更好地进行二次开发或故障排查。

```
MoyiBot/
├── 📁 assets/               # 静态资源目录 (Logo、字体、水印)
├── 📁 plugins/              # 机器人功能插件目录
│   ├── __init__.py
│   ├── basic_commands.py    # 基础命令：关于、帮助、签到、笑话等
│   ├── music_player.py      # **点歌功能**：含免责条款与MP3下载
│   ├── ai_chat.py           # AI对话与总结功能
│   ├── image_tools.py       # 表情包生成与图片处理
│   └── weather_tools.py     # 天气查询
├── 📁 logs/                 # 运行日志目录（自动生成）
├── 📁 temp/                 # 临时文件目录（自动生成）
├── 🐍 bot.py                # 机器人主程序入口
├── 🐍 bot_gui.py            # Win11风格图形化管理面板
├── 🐍 config_manager.py     # 配置读写模块
├── 🔧 pyproject.toml        # NoneBot2项目配置文件
├── 🌐 .env                  # 环境变量配置文件（需配置主人QQ）
├── 📄 requirements.txt      # Python依赖包列表
├── 🤖 go-cqhttp*            # QQ协议连接器（已内置）
├── 🚀 启动管理面板.bat      # Windows一键启动脚本
└── 📋 创建桌面快捷方式.vbs  # 用于创建桌面快捷方式
```

核心功能亮点

· 安全合规的点歌系统：创新的免责条款确认流程，下载并发送MP3文件，规避版权与格式转换风险。
· 一体化管理面板：所有配置（API密钥、功能开关、权限）均可通过图形界面完成，无需手动编辑配置文件。
· 模块化插件设计：每个功能独立为插件，结构清晰，方便你扩展自己的功能。
· 完善的错误处理：关键功能（如点歌）发生错误时，会自动生成带错误ID的详细日志文件，便于反馈和调试。

📜 许可证 (License)

本项目采用 GNU General Public License v3.0 (GPL-3.0) 开源许可证进行分发。

这意味着你可以自由地：

· 运行此软件，无论出于何种目的。
· 学习和修改源代码。
· 再分发软件的副本或修改后的版本。

但需要遵守该许可证的核心条款，例如：如果你分发修改后的版本，必须保持开源并采用相同的GPL-3.0许可证。

你可以在项目的 LICENSE 文件中查看完整的许可证文本。根据GPL-3.0的要求，许可证核心声明如下：

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

🤝 贡献指南

我们非常欢迎和感谢任何形式的贡献，这包括但不限于：报告Bug、提议新功能、改进文档、提交代码修复。

贡献流程

1. Fork 项目仓库：点击GitHub页面右上角的 Fork 按钮，创建你账户下的副本。
2. 克隆到本地：将你Fork的仓库克隆到本地进行开发。
3. 创建功能分支：基于 main 分支创建一个新的分支，例如 git checkout -b fix/typo-in-readme。
4. 进行修改并提交：完成你的修改后，提交到你的功能分支。
5. 发起 Pull Request (PR)：在你的仓库页面发起PR，详细描述你所做的更改及其原因。
6. 讨论与审查：项目维护者会与你一起审查和讨论代码，在修改完善后将其合并。

报告问题或建议新功能
我们使用GitHub的Issues 来跟踪Bug和功能请求。在提交Issue前，请先搜索是否已有类似问题。提交时，请提供清晰的信息：

· Bug报告：描述问题、复现步骤、预期与实际结果，以及相关的日志文件（位于logs/目录下）。
· 功能请求：清晰地描述新功能的场景和预期效果。

代码与文档风格

· 代码：请尽量遵循项目中已有的Python代码风格（如PEP 8）。
· 文档：如果你修改了功能，请同步更新本说明文件或相关代码注释。

❤️ 致谢

墨逸机器人的诞生离不开众多优秀开源项目与社区的支持，在此向他们表示由衷的感谢：

· NoneBot2 框架团队：提供了强大、优雅的机器人开发框架。
· go-cqhttp 项目组：实现了与QQ客户端稳定可靠的连接，是项目运行的基石。
· 所有测试用户与贡献者：感谢你们的反馈、建议和每一行代码，是你们让这个项目变得更好。

---

最后的提示：请务必遵守QQ平台的使用规范，合理使用机器人功能。享受墨逸带来的乐趣吧！如果你觉得这个项目对你有帮助，欢迎在GitHub上留下一个Star⭐，这是对我们最大的鼓励！

如果你在配置或使用中遇到任何问题，请先查阅logs/文件夹下的日志，或通过GitHub Issues向我们反馈。
