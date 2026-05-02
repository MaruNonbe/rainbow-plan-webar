# 長井市レインボープラン WebAR

長井市の「レインボープラン」を AR キャラクターが紹介する、スマートフォン向けの静的 WebAR アプリです。

## 内容

- `index.html`: iOS / Android ブラウザ向け WebAR ページ
- `assets/rainbow_plan_character.glb`: AR 表示用キャラクターモデル
- `design/rainbow_plan_sustainable_future_interface.png`: 起動画面背景
- `markers/rainbow_plan_ar_marker.svg`: 印刷用の案内マーカー画像
- `docs/PROJECT_OVERVIEW.md`: 企画と構成メモ

## 主な機能

- A-Frame + AR.js による WebAR 表示
- Hiro マーカー認識
- 日本語、英語、中国語、韓国語の字幕
- ブラウザ標準音声による読み上げ
- GLB の MorphTarget 検出、または簡易スケールによる口パク
- スマートフォンで操作しやすい下部 UI

## 起動方法

1. このフォルダー全体を GitHub Pages、Netlify、Xserver など HTTPS 対応サーバーにアップロードします。
2. スマートフォンの Safari または Chrome で `index.html` にアクセスします。
3. 「ARを開始」を押してカメラを許可します。
4. 別画面または印刷物に表示した Hiro マーカーをカメラに映します。

## 注意

- iPhone / Android の実機カメラ利用には HTTPS 配信が必要です。
- 現在の AR 認識は AR.js の `preset="hiro"` を使用しています。
- `markers/rainbow_plan_ar_marker.svg` は紹介・印刷用のビジュアルです。独自マーカーとして認識させる場合は `.patt` ファイルを生成し、`index.html` の `<a-marker>` 設定を変更してください。
- 音声は `speechSynthesis` を使った読み上げです。録音済み音声へ差し替える場合は `audio/` に MP3 を追加し、`<audio>` と WebAudio Analyser を使う構成へ変更できます。
