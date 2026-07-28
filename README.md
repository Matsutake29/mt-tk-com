# mt-tk.com — Personal Hub Site

松尾赳治（Takeharu Matsuo）の個人サイト。
ポートフォリオ・ブログ・SNS の入り口を1箇所にまとめたハブサイト。

🔗 **Live**: https://mt-tk.com

## 設計コンセプト

- **Bento Grid 型レイアウト**（2026トレンド）× 日本のミニマル
- 派手な機能を足すより、見えないところに配慮する方向
- JavaScript なし・依存関係ゼロで完結

## 主な技術仕様

| 項目 | 内容 |
|------|------|
| HTML | セマンティック・aria 属性・lang=ja |
| CSS | CSS Grid（grid-template-areas）・CSS 変数で色管理 |
| JavaScript | なし |
| フォント | Cormorant Garamond / Shippori Mincho B1（Google Fonts）|
| アクセシビリティ | `prefers-reduced-motion` 対応 |
| ダークモード | `prefers-color-scheme: dark`（OS設定追従・JSなし）|
| ブランドガイドライン | X / Zenn / GitHub の公式アイコンカラー準拠 |

## ディレクトリ構成

```
mt-tk.com/
├── index.html                 # ハブサイト本体
├── assets/
│   ├── css/
│   │   └── style.css          # スタイル一式
│   └── img/
│       ├── icon-matsutake.png # アバターイラスト
│       └── sns/               # SNS アイコン（SVG）
└── .gitignore
```

## デプロイ

ConoHa WING 上で SSH + GitHub Deploy Key + `git pull` 運用。
**本番が追従しているブランチは `develop`**（`main` ではない）。

```bash
ssh user@server "cd ~/public_html/mt-tk.com/ && git pull"
```

サーバー上のファイルを直接編集しないこと。未コミットの変更が残ると `git pull` が中断する。

`.htaccess` で `.git` フォルダへのアクセスは 404 に。

## ライセンス

このリポジトリのコード・デザインは個人利用目的で公開しています。
学習目的での参考はご自由にどうぞ。
画像（アバターイラスト・写真）の二次利用はご遠慮ください。

## 作者

Takeharu Matsuo — info@mt-tk.com
