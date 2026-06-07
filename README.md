# LikedImageDLer v2

## 概要

- https://github.com/Fumin26u/illust_manager をvue化したもの
- twitter APIが有料化して詰んだ
- 制作時期: 2022年頃 (インターンでvueの知識付いた後)

## 機能

- Vue.js 3 による SPA フロントエンド
- Twitter いいね画像・Pixiv ブックマーク画像のダウンロード
- ユーザー登録・ログイン（PHP API バックエンド）

## 技術スタック

| レイヤー | 技術 |
|----------|------|
| フロントエンド | Vue.js 3 / TypeScript / Vue Router / axios |
| バックエンド | PHP / MySQL（PDO） |
| ビルドツール | Vue CLI 5 |
| 主要ライブラリ | abraham/twitteroauth ^4.0、sass |

## セットアップ

```bash
# フロントエンド
npm install
npm run serve    # 開発サーバー
npm run build    # 本番ビルド

# バックエンド
composer install
# api/system-conf.php, api/commonlib.php に設定を記述
```

## ディレクトリ構成

```
old-illust_manager_v2/
├── api/
│   ├── account/          # アカウント管理 API
│   ├── twi/              # Twitter 画像取得 API
│   └── pix/              # Pixiv 画像取得 API
├── src/
│   ├── views/            # index, pix, account/*, termsofuse/*
│   └── components/
│       ├── account/      # LoginComponent, RegisterComponent 等
│       └── organisms/    # HeaderComponent, TwiForm, PixForm
├── package.json
└── composer.json
```
