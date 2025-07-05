# CLAUDE.md

このファイルは、このリポジトリでコードを扱う際のClaude Code (claude.ai/code) へのガイダンスを提供します。

## プロジェクト概要

PERA はAstro.jsで構築された日本語のランディングページ生成ツールです。イベント用のシンプルな単一ページウェブサイト（LP = ランディングページ）を作成し、GitHub Pagesで公開します。

## 開発コマンド

```bash
# 開発サーバーを起動
npm run dev

# 本番用ビルド
npm run build

# 本番ビルドをローカルでプレビュー
npm run preview

# Astro CLIコマンドを実行
npm run astro
```

## プロジェクト構成

これはAstroベースの静的サイトジェネレーターで、以下の構造になっています：

- **ページ**: `src/pages/`内の各`.astro`ファイルがルートになります
  - `index.astro` - メインのランディングページ
  - `${event}.astro` - イベント固有のランディングページ（例：`centhiver.astro`、`kurayami202508.astro`）

- **アセット**: 画像は`src/assets/images/`にイベントフォルダで整理して保存

- **スタイリング**: Viteプラグイン統合でTailwind CSS v4を使用

- **デプロイ**: GitHub Pagesデプロイ用に設定済み
  - サイトURL: `https://miyanoyami.github.io/pera/`
  - mainブランチの変更でGitHub Actionsによる自動デプロイ

## 主要な設定

- **Astro設定**: GitHub Pages用にベースパス`/pera/`で設定
- **Tailwind**: Viteプラグイン経由で統合
- **TypeScript**: `tsconfig.json`で有効化
- **Prettier**: コードフォーマット用にAstroプラグインで設定

## 開発ノート

- ランディングページは`src/pages/`に新しい`.astro`ファイルを追加することで作成
- イベントアセットは`src/assets/images/`下のサブディレクトリに整理
- プロジェクトは主に日本語コンテンツを使用
- 現在テストフレームワークは設定されていません