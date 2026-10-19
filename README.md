# LLM WebUI

自分用のLLM webインターフェース。

- [Open WebUI](https://github.com/open-webui/open-webui): webインターフェース
- [Ollama](https://ollama.com/): ローカルLLM管理

API は [llm-api](https://github.com/310hz/llm-api) を `http://host.docker.internal:50012/v1` 経由で使う。

## 使い方

1. `svs up llm-api` で llm-api を起動する
2. 任意のコマンド名で`entrypoint.sh`にaliasを通す。サブコマンドは以下:

- `start`: 起動
- `stop`: 停止
- `restart`: 再起動
- `update`: コンテナイメージの更新と再起動

サーバーを起動すると以下のURLに各種ページが立ち上がる:

- Open WebUI: http://localhost:50011

`OPENAI_API_BASE_URL` は Open WebUI の初回起動時にだけ読まれ、以降は DB に保存された値が使われる。接続先を変えるときは管理画面の「接続」から変更する。API キーには llm-api の `BIFROST_VK_MAIN` を設定する。
