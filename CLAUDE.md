# 千鳥印刷株式会社 採用サイト（引き継ぎメモ）

このフォルダは claude.ai のチャットで制作した採用サイトです。Claude Code ではここから公開作業を引き継ぎます。

## サイト概要
- 会社：千鳥印刷株式会社（島根県松江市春日町344-2／https://chidori-printing.com/）
- 種類：1ページ完結の静的サイト（HTML/CSS/JavaScript を index.html 1ファイルに記述。ビルド不要、外部ライブラリなし）
- フォント：Google Fonts「Zen Kaku Gothic New」
- メインカラー：#2E9E5B（緑）／ダーク #1F6B3F／ライト #E8F5EC／アクセント #F5B82E

## ファイル構成
- index.html … サイト本体
- images/ … 画像18枚（JPEG、合計約1.2MB）
  - hero-1〜4.jpg：トップのスライドショー（1920×1080）
  - about.jpg：私たちについて／workstyle.jpg：働き方
  - dept-sales / dept-print / dept-prepress / dept-general.jpg：部署紹介（営業課・印刷課・製版課・総務課）
  - training.jpg：研修メイン／training-new / -ojt / -sales / -ai / -sdgs.jpg：研修カード
  - benefits.jpg：福利厚生／entry-bg.jpg：エントリー背景
- 写真を差し替えるときは同じファイル名で上書きする（HTML内に「写真差し替え」コメントあり）

## ページ構成
ヘッダー（固定・スマホはハンバーガー）→ トップ（Ken Burns スライドショー、縦書きキャッチ「想いを、刷り上げる仕事。」、CMYK網点・トンボ・カラーバー演出、バッジ3つ）→ 私たちについて → 働き方（年間休日110日のカウントアップ、休日内訳、休日カレンダー）→ 部署紹介（4課）→ 研修制度（成長ステップ＋5研修）→ 福利厚生（6項目）→ エントリー（mailto）→ フッター（会社情報）

## これからやること（公開）
1. git リポジトリを初期化し、GitHub アカウント「chidoriprinting」に Public リポジトリ「chidori-recruit」を作成して push する（gh CLI があれば `gh repo create`、なければ手順を案内）
2. Vercel で公開する（Vercel CLI の `vercel --prod`、または Vercel の画面で GitHub リポジトリを Import。Framework Preset は「Other」、ビルド設定なし）
   - ユーザーは当初「v0で公開」を希望していたが、v0 の公開先は Vercel なので Vercel への直接デプロイで同等
3. 公開URL（*.vercel.app）をユーザーに伝える
4. 任意：独自ドメイン（例：recruit.chidori-printing.com）の設定方法を案内

## 注意
- ユーザーはプログラミングに詳しくないため、操作が必要な場面は1ステップずつ日本語で案内する
- アカウントのログインや認証が必要な操作はユーザー本人に行ってもらう
- 文章やデザインの変更はユーザーの指示があったときだけ行う

## 公開前にユーザーへ確認したい残タスク
- 部署紹介の「仕事内容・向いている人・やりがい」、研修の成長ステップの文章は仮の内容なので、実際の業務に合わせて修正するか確認
- 「エントリーする」ボタンは現在 info@chidori-printing.com 宛ての mailto。応募フォームや求人サイトがあればリンクを差し替え
- 画像はAI生成のイメージ。可能であれば実際の社員写真に差し替えるのが望ましい
