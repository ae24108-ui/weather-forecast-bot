# weather-forecast-bot
> n8nで作成

## 🚩概要

- LINEから送られたメッセージを解析し、都市・日時を抽出して OpenWeatherMapで天気予報を返す n8n ワークフローです。

- 簡単なLINEbotを開発しようと思い製作しました。

---

## 📃ファイル構成

- 'weather-forecast-bot.json' : n8nでエクスポートしたワークフロー
- '.env.example' :環境変数のテンプレート（APIキーやトークンは含まない）
- 以下省略

---

## 🎳実行方法（クラウド版n8n用）

1. リポジトリを clone

```bash
git clone https://github.com/ae24108-ui/weather-forecast-bot.git
cd weather-forecast-bot
```

---

2. 環境変数の設定

- '.env.example'をコピーして'.env'を作成

```bash
# Windows PowerShell
Copy-Item .env.example .env

# Linux/macOS
cp .env.example .env
```

- '.env'に各自のAPIキーやトークンを設定

```env
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxx
OPENWEATHERMAP_API_KEY=yyyyyyyyyyyyyyyy
LINE_CHANNEL_ACCESS_TOKEN=zzzzzzzzzzzz
N8N_ENCRYPTION_KEY=32文字のランダム文字列
```

---

3. n8n の起動

```bash
n8n start
```

---

4. ワークフローのimport

- n8n UI で workflow-weather-forecast.json をインポート

- ローカルで webhook を使う場合は、Cloudflare トンネルや localtunnel などで外部公開が必要です

- 公式クラウド版 n8n を使う場合は webhook URL は常時アクセス可能

---   

5. 動作確認

- LINEにメッセージを送って応答が返るか確認
- ワークフロー内のノードや環境変数を調整可能


