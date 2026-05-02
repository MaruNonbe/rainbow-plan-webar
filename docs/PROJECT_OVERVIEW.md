# レインボープラン紹介 WebAR アプリ概要

## 目的

山形県長井市の「レインボープラン」を、AR キャラクターが多言語の字幕と音声で紹介する WebAR アプリとして提供します。イベント、展示、学校見学、観光案内などで、スマートフォンからすぐ体験できる構成を想定しています。

## 体験の流れ

1. 参加者がスマートフォンで Web ページを開く。
2. 「ARを開始」を押してカメラを許可する。
3. Hiro マーカーをカメラに映す。
4. AR キャラクターと説明プレートが表示される。
5. 言語を選び、字幕または音声でレインボープランの説明を聞く。

## 実装構成

```text
RainbowPlan_WebAR_App/
├─ index.html
├─ assets/
│  └─ rainbow_plan_character.glb
├─ audio/
├─ design/
│  └─ rainbow_plan_sustainable_future_interface.png
├─ docs/
│  └─ PROJECT_OVERVIEW.md
└─ markers/
   ├─ rainbow_plan_ar_marker.png
   └─ rainbow_plan_ar_marker.svg
```

## 技術要素

- A-Frame 1.4.2
- AR.js 3.4.5
- Web Speech API `speechSynthesis`
- GLB モデル表示
- MorphTarget 検出による口パク補助

## 今後の拡張案

- オリジナル AR マーカー用の `.patt` ファイル作成
- 録音済みナレーション MP3 への差し替え
- GLB モデルへの Mouth_Open / Blink などの BlendShape 追加
- 説明文の監修版への差し替え
- GitHub Pages などへの公開と実機検証
