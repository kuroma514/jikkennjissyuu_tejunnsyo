# Docker Compose

[← 手順書に戻る](../README.md)

**概要:**
Docker Compose は複数のコンテナサービスを一括で定義・起動するためのツールです。`docker-compose.yml`（または `docker compose`）でサービス、ボリューム、ネットワークを宣言します。

**主なポイント:**

- サービス定義により複数コンテナを一括管理できる。
- `ports`, `volumes`, `environment`, `depends_on` などのキーが主要。

**実務上の注意:**

- `depends_on` は起動順を示すのみでヘルスチェックを待たない。
- 本番環境ではリソースやシークレット管理を別途設計する。

**例:**

```
docker compose up -d
```

**参考:** Docker Compose ドキュメント

