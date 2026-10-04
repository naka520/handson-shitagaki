# このハンズオンでつくるもの

SORACOM LTE-M Button（通称「白ボタン」）を押すと、ボタンのおおよその位置を SORACOM Flux の AI アクションが読み取り、その場所に近いご当地情報（名物・観光スポット・豆知識など）を生成して Discord のチャンネルに投稿します。

```
[白ボタン] --LTE-M--> [SORACOM Air + 簡易位置測位]
                              |
                              v
                     [SORACOM Flux アプリ]
                       ├─ イベントソース：IoTデバイス
                       ├─ AIアクション：位置からご当地情報を生成
                       └─ Webhookアクション：Discordへ投稿
                              |
                              v
                     [Discord チャンネル]
```

## 学べること

- LTE-M Button のセットアップと SIM グループ設定
- 簡易位置測位機能（基地局情報ベースの位置推定）の使い方
- SORACOM Flux のイベントソース・AIアクション・Webhookアクションの組み立て方
- Discord Webhook を使った外部通知

## 所要時間の目安

約60〜90分

---

[目次](./README.md) ｜ [0. 事前準備 →](./01-preparation.md)
