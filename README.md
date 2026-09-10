# KGU栄養計算システム
## Overview

このソフトウェアは、栄養教育を補助することで、栄養に関する考え方などを楽しみながら学ぶ食育ツールとしての利用することで、広く栄養学を身近に感じてもらうことを目的として開発した教育・研究用ソフトウェアです。

## Features

- **NuCalcEncoder.html**
  
  - NuCalc で利用可能なCode128 バーコードをPNGフォーマットで生成します 

- **NuCalc_v\*\*.html**
  
  - バーコードリーダーとの組み合わせにより栄養計算と結果表示を行います

  - StageSetCode.pdf によりライフステージと身体活動レベルの設定を行うことができます

  - ServingCode.pdf により直前に読んだ栄養素コードの栄養素量を 特盛2倍・大盛り1.5倍・小盛り0.5 に変更することができます

- **NuCalcSlider_v\*.html**
  
  - バーコードリーダーとの組み合わせにより栄養計算と結果表示を行います

  - StageSetCode.pdf によりライフステージと身体活動レベルの設定を行うことができます

  - 食品成分表の栄養素量を反映したコード表（StandardTablesCode.pdf）との組み合わせで献立作成にも応用可能です

- **NuCalcQR_v\*.html**
  - 栄養素量のコードをQRコードとしたものです
  - StageSetCode.pdf によりライフステージと身体活動レベルの設定を行うことができます
  - バーコードリーダー同様にQRコードリーダーを通じて栄養素量を取り込むことが可能です
  - PC備え付けのカメラで実施することを想定していますが、スタンドアローンとしての利用は Mac用google Chrome でしか稼働を確認できません。ブラウザからのカメラ利用はセキュリティ上の観点から制限されているようでモバイルスマートデバイスでカメラを起動することができません（信頼できる証明書を持ったWebサイトに置き、SSL通信を経由することでモバイル端末でも利用可能な情報を得ておりますが，まだWeb経由のスマートデバイスによるテストは済んでおりません（完全な動作確認は済んでおりません））

## Requirements
- Google Chrome/FireFox/Safari/Microsoft Edge などの汎用Webブラウザが稼働するパーソナルコンピュータ
- その他の必要環境
  - Code128 を読むことができる1次元バーコードリーダー
  - NuCalcQR の場合は外付けQRコードリーダー(まだテスト途中であり正式バージョンではありません）
- MITライセンスの遵守

## インストール方法
- NuCalc\*\*\*.html ファイルをダウンロードしていただき、Webブラウザを搭載した汎用パーソナルコンピュータに複製し、任意のWebブラウザ（[Apple Safari](https://www.apple.com/jp/safari/switch/), [Microsoft Edge](https://explore.microsoft.com/ja-jp/edge?ep=2187&form=MA14LT&es=375&cs=1673980518), [google Chrome](https://www.google.com/intl/ja_jp/chrome/dr/download/?brand=OZZY&ds_kid=10484928882&gclsrc=aw.ds&gad_source=1&gad_campaignid=20752932842&gbraid=0AAAAAoY3CA4uDoWrj2QgUBOH4WmNodGQ3&gclid=CjwKCAjwzNTUBhAjEiwA7zcvWnN_fyzS9y6PKauFntOoVbX817NOZOi1DPMu3W7HrxZdx-QDIqX2vhoCILgQAvD_BwE),[Mozilla FireFox](https://www.firefox.com/ja/landing/get/?mozcb=y&gclid=17438ff673cd1e1a8058e5692007dbee&gclsrc=3p.ds&utm_campaign=ms_v1_firefox_test_expansion_jp_national-test_jp_desktop_all_search_conversion_brand_cpc_install_adgap&msclkid=17438ff673cd1e1a8058e5692007dbee)  にて動作を確認しています）で起動する

## 使い方
### 栄養計算（NuCalc\*\*\*.html)
- バーコードリーダーをパーソナルコンピュータに接続し、読み取りモードを「キーボードモード・Code128・改行あり」に設定する
（それぞれのバーコードリーダーの説明書を参照願います）
- 当該ファイルをWebブラウザで起動
- 入力欄をクリックして入力可能な状態に
- 文字入力モードを「半角英数」に設定
- 利用者の属性バーコード ***対象属性の設定コード「StageSetCode.pdf」*** を読むか、ドロップダウンメニューで選択する
- 栄養素データの入ったバーコードを順に読む
- 盛り量を調節したい場合は、その行の枠を選択した上で盛り量のバーコードを読む
- 「合計を表示」を押す
- 日本人の栄養摂取基準2025を100%として、読み取ったバーコードの合計を数値および棒グラフで表示

#### バーコードリーダーをお持ちでない場合
> Aタグ（StageSetCode.pdf）・Nタグ（Encoderで出力もしくはSampleCode.pdfなど）のバーコード下の文字列を入力してEnterしても動きます
- Aタグ：年齢・性別・身体活動レベルの設定ができます
  - A45・・・・・・・6-7歳 女性 活動レベル1
  - A5A・・・・・・・18-29歳 女性 活動レベル2 
- Nタグ：栄養素量の設定ができます
- Dタグ：大盛り・小盛りなどの設定ができます（ServingCode.pdf）NuCalcSliderでは使用できません

### バーコードエンコーダー（NuCalcEncoder\-v\*\*.html)
- 当該ファイルを Webブラウザを搭載した汎用パーソナルコンピュータに複製し、任意のWebブラウザ（[Apple Safari](https://www.apple.com/jp/safari/switch/), [Microsoft Edge](https://explore.microsoft.com/ja-jp/edge?ep=2187&form=MA14LT&es=375&cs=1673980518), [google Chrome](https://www.google.com/intl/ja_jp/chrome/dr/download/?brand=OZZY&ds_kid=10484928882&gclsrc=aw.ds&gad_source=1&gad_campaignid=20752932842&gbraid=0AAAAAoY3CA4uDoWrj2QgUBOH4WmNodGQ3&gclid=CjwKCAjwzNTUBhAjEiwA7zcvWnN_fyzS9y6PKauFntOoVbX817NOZOi1DPMu3W7HrxZdx-QDIqX2vhoCILgQAvD_BwE),[Mozilla FireFox](https://www.firefox.com/ja/landing/get/?mozcb=y&gclid=17438ff673cd1e1a8058e5692007dbee&gclsrc=3p.ds&utm_campaign=ms_v1_firefox_test_expansion_jp_national-test_jp_desktop_all_search_conversion_brand_cpc_install_adgap&msclkid=17438ff673cd1e1a8058e5692007dbee) にて動作を確認しています）で起動する
- 栄養素など必要事項を入力
  > 入力例：エネルギー：567 kcal, 炭水化物：89.0 g, タンパク質：12.0 g, 脂質：34.5 g, 塩分：6.7 g
- 「**バーコード生成**」ボタンを押す
- バーコードが生成されたら「**バーコードPNG保存**」を押して，適当な名称をつけて保存する
> 入力例から生成されるNタグ：N8DF7A1E15910C0
- PNGを貼り付けられるアプリケーションに貼り付けて印刷を行う（タテヨコ比を変えるなどするとバーコードリーダーが読めないことがあります）

## Citation
本ソフトウェアを研究、教育または学会発表等で利用する場合は、
以下の文献またはソフトウェアを引用してください。

> 日本栄養学教育学会雑誌第11巻 pp. 82
> O-1:可搬性および体感性に優れた栄養教育向けICTソリューションの開発
> ◯由良亮*, 山本有希*, 桶家亜実*, 河井ますみ*, 大道文香*, 京極奈美*, 佐藤香菜子*, 平山雄大*, 安藤秀子*

## ToDo
- 今後SSL通信を介したスマートデバイスのコードスキャナ機能の利用可能性に関するテスト
- QRコードバージョンの　Encoder Webアプリ　の開発
- 様々な応用方法（実際の栄養教育の展開法）の実施と検証

## License
このソフトウェアはMITライセンスの元で公開されています

詳しくは LICENSE.ja.md/LICENSE ファイルをご確認ください


This software is released under the MIT License.

See the LICENSE file for details.


## Author
[Yura Makoto](https://www.kanazawa-gu.ac.jp/college/aboutus/teacher/foodnutrition-yura/)
[Kanazawa Gakuin Junior Colledge]

## Contact
yura@kanazawagakuin-u.ac.jp
までお知らせください
