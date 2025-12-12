# Docker Compose の主要キー

[← 手順書に戻る](../README.md)

**概要:**
`docker-compose.yml` でよく使われる主要キーと運用上の注意点を整理します。Compose は複数サービスを定義して一括で管理するためのツールです。

**主要キー:**

- `services`: 各コンテナの定義
- `image` / `build`: 使用イメージ / ビルド設定
- `ports`, `volumes`, `networks`, `environment`
- `depends_on`: 起動順を示すがヘルスチェックは待たない

**実務上の注意:**

- 機密情報は `.env` やシークレットで管理する。
- `depends_on` だけでは DB の準備完了を保証しないため、リトライやヘルスチェックを組み合わせる。

**例:**

```
services:
  db:
    image: mysql:8.0
```

**参考:** Docker Compose ドキュメント

