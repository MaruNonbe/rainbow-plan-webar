# レインボープランながい WebARアプリ制作フォルダー

## 目的
山形県長井市の「レインボープラン」を、ARキャラクターが多言語・音声・半透明プレートで説明するWebARアプリを制作するためのフォルダーです。

## 主な機能
- iOS / Android ブラウザ対応WebAR
- ARキャラクター表示
- 多言語表示：日本語 / English / 中文 / 한국어
- 音声読み上げ
- 説明文のスクロール表示
- 簡易口パク / MorphTarget対応準備
- ARマーカー画像同梱

## フォルダー構成

```text
RainbowPlan_WebAR_App/
├─ index.html
├─ assets/
│  └─ rainbow_plan_character.glb
├─ audio/
│  ├─ rainbow_plan_ja.mp3 予定
│  ├─ rainbow_plan_en.mp3 予定
│  ├─ rainbow_plan_zh.mp3 予定
│  └─ rainbow_plan_ko.mp3 予定
├─ markers/
│  ├─ rainbow_plan_ar_marker.png
│  └─ rainbow_plan_ar_marker.svg
├─ design/
│  └─ rainbow_plan_sustainable_future_interface.png
└─ docs/
   └─ PROJECT_OVERVIEW.md
```

## 注意
現在のindex.htmlはHiroマーカー認識を前提にしています。オリジナルマーカーを認識させる場合は、AR.js用の .patt ファイル生成とindex.html側のmarker設定変更が必要です。

## 次に行う作業候補
1. オリジナルARマーカーを .patt 化する
2. 録音済みMP3音声に差し替える
3. GLBモデルに Mouth_Open / Blink のBlendShapeを追加する
4. GitHub Pages または Xserver にアップロードしてスマホ実機確認する
