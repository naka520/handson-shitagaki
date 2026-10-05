# 6. Webhook アクションで Discord に投稿する

1. AI アクションの後ろに **Webhook アクション** を追加
2. 以下のように設定

| 項目     | 設定値                            |
| -------- | --------------------------------- |
| メソッド | `POST`                            |
| URL      | 手順1で控えた Discord Webhook URL |
| ヘッダー | `Content-Type: application/json`  |

3. **ボディ** を設定

```json
{
  "username": "ご当地ボタン",
  "content": "🔘 ボタンが押されました！\n\n${payload.output.message}"
}
```

> ✅ AI アクションの出力がどの変数で参照できるかは、実行履歴で AI アクションの出力を見て確認し、`${payload.output.message}` の部分を読み替えてください。
>
> ⚠️ Discord の `content` は2000文字までです。プロンプトで文字数を制限しておくと安心です。また、AIの出力に `"` や改行が含まれるとJSONが壊れる場合があるので、うまく投稿されないときは実行履歴でリクエスト内容を確認しましょう。

4. 保存

---

[← 5. AI アクションでご当地情報を生成する](./06-ai-action.md) ｜ [目次](./README.md) ｜ [7. 動かしてみよう 🎉 →](./08-try-it.md)
