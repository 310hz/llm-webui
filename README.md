# LLM WebUI

自分用のLLM webインターフェース。

- [Open WebUI](https://github.com/open-webui/open-webui): webインターフェース
- [Ollama](https://ollama.com/): ローカルLLM管理

## 使い方

| コマンド | 内容 |
| --- | --- |
| `just start` | 起動 |
| `just stop` | 停止 |
| `just restart` | 再起動 |
| `just update` | イメージを pull して再起動 |
| `just logs` | ログ表示 |

サーバーを起動すると以下のURLに各種ページが立ち上がる:

- Open WebUI: http://localhost:50011

`OPENAI_API_BASE_URL` は Open WebUI の初回起動時にだけ読まれ、以降は DB に保存された値が使われる。接続先や API キーを変えるときは管理画面の「接続」から変更する。
