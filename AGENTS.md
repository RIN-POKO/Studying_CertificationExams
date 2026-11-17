# AGENTS.md

このリポジトリで作業する際は、以下のルールに従ってください。

## 1. HTML / Web UI の作成・編集
- HTML・CSS・クライアントサイド JavaScript を作成または更新するときは、必ず最初に `modern-web-guidance` スキル（`.agents/skills/modern-web-guidance/SKILL.md`）を参照・実行してください。
- PC（Windows / macOS）および iPhone・iPad での閲覧・学習を考慮して設計してください。
- 学習用 HTML ページには、原則として以下の機能・設定を組み込んでください：
  - **テーマ切替**: ライト／ダークモード、および白黒印刷用の **白黒（モノクロ）モード**
  - **印刷対応**: **印刷ボタン**の設置、および `@page` / `@media print` による A4 印刷最適化（表の折り返し、改ページ制御、白黒印刷対応）
  - **フォント設定**: Google Fonts（`BIZ UDGothic`・`BIZ UDPGothic`）を読み込みつつ、`@font-face`（`unicode-range`）により英語（ASCII）に `BIZ UDPGothic`、日本語に `BIZ UDGothic` を割り当て、環境非依存かつオフライン時はシステムフォントへフォールバックさせること
  - **Mermaid 図**: Windows での文字途切れを防ぐため、`flowchart` は `htmlLabels: false` とし、`themeVariables.fontFamily` に本文と同じフォント設定を指定したうえで、`await document.fonts.ready;` 後に描画すること

## 2. 日本語文章の作成・推敲
- 日本語の解説・ノート・ドキュメントを作成または編集するときは、必ず `yomiyasu` スキル（`.agents/skills/yomiyasu/SKILL.md`）を使用して検査・推敲してください。

## 3. 技術用語の表記ルール
- 試験範囲の技術用語・公式名称・CLI コマンド・フラグ・API パラメータ名は、無理に日本語訳せず公式の英語表記をそのまま使用してください。
