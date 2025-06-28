## PERA

PERA はペライチの簡易LPを公開するための開発ツール・ホスティング用リポジトリです。

astro を用いて即席で LP を生成し、Github Pages によって公開します。


### プロジェクト構造

```text
.
├── public/
├── dist # 公開ディレクトリ
│   ├── index.html
│   └── ${event}
├── src/ # 実装ディレクトリ
│   └── pages/
│       ├── index.astro
│       └── ${event}.astro
└── package.json
```

## 開発
```bash
# local での動作確認
npm run dev

# ビルド
npm run build 

# ビルド成果物の動作確認
npm run preview
```


