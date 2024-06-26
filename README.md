# Wikipedia 参照くん

このアプリケーションは、Streamlit と OpenAI を使用して、  
ユーザーの質問に対してWikipedia から情報を取得して回答するチャットボットです。

※精度はカイゼン中

![スクリーンショット 2024-05-05 14 58 31](https://github.com/kamada-maki/streamlit-langchain-app/assets/74590047/adb5f989-1ef7-47cb-984d-12256272b453)


## セットアップ

- 必要なパッケージをインストールします。これには、`os`, `streamlit`, `dotenv`, `langchain` などが含まれます。
- `.env` ファイルを作成し、OpenAI の API キーとモデル名を設定します。

## 使用方法

アプリケーションを起動すると、チャットボットが表示されます。ユーザーは質問を入力し、チャットボットはその質問に対する回答を生成します。

## コードの詳細

- `create_agent_chain` 関数は、OpenAI のチャットモデルと Wikipedia ツールを使用してエージェントチェーンを作成します。
- Streamlit のセッションステートを使用して、エージェントチェーンとメッセージのリストを管理します。
- ユーザーからの入力（prompt）がある場合、そのメッセージはセッションステートのメッセージリストに追加され、エージェントチェーンがそのプロンプトに対する回答を生成します。
- 生成された回答は、チャットボットからのメッセージとしてセッションステートのメッセージリストに追加されます。

このアプリケーションは、ユーザーとチャットボットの間の対話を管理し、ユーザーの質問に対して適切な回答を生成するためのツールとして OpenAI と Wikipedia を使用します。

## 起動方法
```
source myenv/bin/activate
streamlit run app.py --server.port 8080
```


## 参考

https://github.com/yoshidashingo/langchain-book
