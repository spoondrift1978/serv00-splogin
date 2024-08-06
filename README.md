## serv00自动化批量保号，并且发送消息到Telegram

利用github Action以及python脚本实现

🙏🙏🙏点个Star！！Star！！Star！！

### 将代码fork到你的仓库并运行的操作步骤

#### 1. Fork 仓库

    - 点击页面右上角的 "Fork" 按钮，将仓库 fork 到你的 GitHub 账户下。

#### 2. 设置 GitHub Secrets

1. **创建 Telegram Bot**
    - 在 Telegram 中找到 `@BotFather`，创建一个新 Bot，并获取 API Token。
    - 在 Telegram 中找到 @IDBot，获取电报ID。

2. **配置 GitHub Secrets**
    - 转到你 fork 的仓库页面。
    - 点击 `Settings`，然后在左侧菜单中选择 `Secrets`。
    - 添加以下 Secrets：
        - `ACCOUNTS_JSON`: 包含账号信息的 JSON 数据。例如：
        - 
          ```json
          [
            {"username": "serv00的账号", "password": "serv00的密码", "panel": "panel6.serv00.com"},
            {"username": "ct8的账号", "password": "ct8的密码", "panel": "panel.ct8.pl"},
            {"username": "user2", "password": "password2", "panel": "panel6.serv00.com"}
          ]
          ```
        - `TELEGRAM_BOT_TOKEN`: 你的 Telegram Bot 的 API Token。
        - `TELEGRAM_CHAT_ID`: 你的 Telegram Chat ID。

3. 启动 GitHub Actions

    - 在你的 fork 仓库中，进入 `Actions` 页面。
    - 如果 Actions 没有自动启用，点击 `Enable GitHub Actions` 按钮以激活它。
    - 如果需要手动触发，可以在 Actions 页面手动运行工作流。

