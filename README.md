# Atlas DataLake `_public_feed/`

PROVE Global Data Hub 向けの**公開用 JSON フィード**置き場。
Atlas が生成・更新し、Smith が provej.jp で読む**唯一の受け渡し口**。

```
_public_feed/
├─ README.md                 ← 本ファイル
├─ schema/                   ← JSON Schema v1（契約）
│  ├─ manifest.schema.json
│  └─ macro_scores.schema.json
├─ samples/                  ← Phase 0 サンプル（UI 試作用・本番値ではない）
│  ├─ _manifest.json
│  └─ macro_scores.json
└─ （Phase 1 以降）本番 JSON をルート直下に配置予定
```

## 原則

1. 各 JSON に `schema_version` / `last_updated` / `source` を必須
2. 国コードは **ISO 3166-1 alpha-2**（VN, TH, US…）
3. 数値の語彙は σ層 `metrics.yaml` の `metric_id` に紐づける
4. スキーマ変更は **マイナー互換を優先**。破壊的変更は `schema_version` を上げて Smith と合意

## 参照

- Phase 0 納品説明：`UDX事業/atlas/from_atlas/2026-07-12_REQ-SMITH-20260712-001_phase0_schema_v1.md`
- 構想ヒント：`UDX事業/atlas/from_atlas/2026-07-10_prove_global_data_hub_hints.md`
