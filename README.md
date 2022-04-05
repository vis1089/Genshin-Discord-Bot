# 原神Discord Bot


## 簡介
使用Discord機器人快速查詢原神內資訊，不需開啟Hoyolab App，包含：
- 即時便箋，包含樹脂、洞天寶錢、探索派遣...等
- 查詢深境螺旋紀錄
- 查詢旅行者札記
- Hoyolab每日簽到
- Hoyolab使用兌換碼

## 範例
![](https://i.imgur.com/N4O4LJI.png)

## 安裝與使用

### 網頁端
1. 到 [Discord Developer](https://discord.com/developers/applications "Discord Developer") 登入Discord帳號

![](https://i.imgur.com/dbDHEM3.png)

2. 點選「New Application」建立應用，輸入想要的名稱後按「Create」

![](https://i.imgur.com/BcJcSnU.png)

3. 在 Bot 頁面，按「Add Bot」新增機器人

![](https://i.imgur.com/lsIgGCi.png)

4. 在 OAuth2/URL Generator，分別勾選「Bot」「Send Messages」「Manage Messages」，最底下產生的 URL 連結就是機器人的邀請連結，開啟連結將機器人邀請至自己的伺服器

![](https://i.imgur.com/08fcHs0.png)

5. 回到 Bot 頁面，按「Reset Token」來取得並複製機器人的 Token，等等會用到

![](https://i.imgur.com/BfzjewI.png)


### 本地端
1. 下載並安裝Python 3: https://www.python.org/downloads/
2. 在專案資料夾 (Genshin-Discord-Bot) 內，用文字編輯器開啟 `config.example.json` 檔案，把剛才取得的 Token 貼在 `bot_token` 欄位，並將檔案另存為 `config.json`
3. 在專案資料夾內開啟 cmd 或 powershell，輸入底下命令安裝相關套件：
```
pip3 install -r requirements.txt
```
4. 開始運行機器人
```
python .\main.py
```

## 配置檔案說明 (config.json)
```python
{
    "bot_token": "ABCDEFG",  # 機器人Token，需從 Discord 網頁取得
    "bot_prefix": "%",       # 機器人指令前綴
    "bot_cooldown": "3"      # 機器人對同一使用者接收指令的冷卻時間 (單位：秒)
}
```

## 結尾
構想啟發自: https://github.com/Xm798/Genshin-Dailynote-Helper

API使用自: https://github.com/thesadru/genshin.py
