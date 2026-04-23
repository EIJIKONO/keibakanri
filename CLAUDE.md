# 勝ち筋帖 (Kachisuji-chō)

馬券の成功パターンを記録する静的Webアプリ。

## 構成

- `index.html` — アプリ本体。単一HTMLファイル、Vanilla JS(フレームワーク・ビルドツールなし)
- `otakara-master.csv` — お宝条件マスタデータ。アプリから取り込んで使う

## 主要機能

- 競馬場別の成功パターン記録
- お宝条件マスタ(CSVインポート)
- スクリーンショット添付
- JSONバックアップ/リストア

## デプロイ

Netlifyで静的配信。ビルドステップなし、`index.html` をそのまま配信する。

## 開発時の注意

- **ストレージは `localStorage` を使う**。保存は `safeStorageSet(key, value)` ヘルパー経由で、QuotaExceededError を補足して具体的なエラーメッセージを出す。
- **モバイル前提のUI**。タップ領域・フォントサイズ・縦スクロールを優先。デスクトップはおまけ。
- 依存追加なし。外部ライブラリは既に読み込まれているもの(Google Fonts等)のみ。

## デザイン方針

- **墨 × 朱の和モダン**。黒基調に朱色のアクセント。
- フォント: **Shippori Mincho** + **Noto Serif JP**(Google Fonts)。サンセリフは使わない。
