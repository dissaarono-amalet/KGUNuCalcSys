# KGU栄養計算システム
## Overview

このソフトウェアは、栄養教育を補助することで、栄養に関する考え方などを楽しみながら学ぶ食育ツールとしての利用することで、広く栄養学を身近に感じてもらうことを目的として開発した教育・研究用ソフトウェアです。

## Features

- **NuCalcEncoder.html**
-- NuCalc で利用可能なCode128 バーコードをPNGフォーマットで生成します 
- **NuCalc_v\*\*.html**
-- バーコードリーダーとの組み合わせにより栄養計算と結果表示を行います
-- StageSetCode.pdf によりライフステージと身体活動レベルの設定を行うことができます
-- ServingCode.pdf により直前に読んだ栄養素コードの栄養素量を 特盛2倍・大盛り1.5倍・小盛り0.5 に変更することができます
- **NuCalcSlider_v\*.html**
-- バーコードリーダーとの組み合わせにより栄養計算と結果表示を行います
-- StageSetCode.pdf によりライフステージと身体活動レベルの設定を行うことができます
-- 食品成分表コード（StandardTableCode.pdf）との組み合わせで献立作成にも応用可能です
- **NuCalcQR_v\*.html**
-- 栄養素量のコードをQRコードとしたものです
-- StageSetCode.pdf によりライフステージと身体活動レベルの設定を行うことができます
-- バーコードリーダー同様にQRコードリーダーを通じて栄養素量を取り込むことが可能です
-- PC備え付けのカメラで実施することを想定していますが、スタンドアローンとしての利用は Mac用google Chrome でしか稼働を確認できません。ブラウザからのカメラ利用はセキュリティ上の観点から制限されているようでモバイル端末でもカメラを起動することができません（信頼できる証明書を持ったSSL通信上ならモバイル端末でも利用可能です）

## Requirements
- Google Chrome/FireFox/Safari/Microsoft Edge などの汎用Webブラウザが稼働するパーソナルコンピュータ
- その他の必要環境
-- Code128 を読むことができる1次元バーコードリーダー
-- NuCalcQR の場合は外付けQRコードリーダー

## インストール方法
- NuCalc\*\*\*.html ファイルを Webブラウザを搭載した汎用パーソナルコンピュータに複製し、任意のWebブラウザ（[Apple Safari](https://www.apple.com/jp/safari/switch/), [Microsoft Edge](https://explore.microsoft.com/ja-jp/edge?ep=2187&form=MA14LT&es=375&cs=1673980518), [google Chrome](https://www.google.com/intl/ja_jp/chrome/dr/download/?brand=OZZY&ds_kid=10484928882&gclsrc=aw.ds&gad_source=1&gad_campaignid=20752932842&gbraid=0AAAAAoY3CA4uDoWrj2QgUBOH4WmNodGQ3&gclid=CjwKCAjwzNTUBhAjEiwA7zcvWnN_fyzS9y6PKauFntOoVbX817NOZOi1DPMu3W7HrxZdx-QDIqX2vhoCILgQAvD_BwE) にて動作を確認しています）で起動する

## 使い方
### 栄養計算（NuCalc\*\*\*.html)
- バーコードリーダーをパーソナルコンピュータに接続し、読み取りモードを「キーボードモード・Code128・改行あり」に設定する
（それぞれのバーコードリーダーの説明書を参照願います）
- 当該ファイルをWebブラウザで起動
- 入力欄をクリックして入力可能な状態に
- 文字入力モードを「半角英数」に設定
- 利用者の属性バーコード ***「対象属性の設定コード.pdf」*** を読むか、ドロップダウンメニューで選択する
- 栄養素データの入ったバーコードを順に読む
- 盛り量を調節したい場合は、その行の枠を選択した上で盛り量のバーコードを読む
- 「合計を表示」を押す
- 日本人の栄養摂取基準2025を100%として、読み取ったバーコードの合計を数値および棒グラフで表示

### バーコードエンコーダー（NuCalcEncoder\-v\*\*.html)
- 当該ファイルを Webブラウザを搭載した汎用パーソナルコンピュータに複製し、任意のWebブラウザ（[Apple Safari](https://www.apple.com/jp/safari/switch/), [Microsoft Edge](https://explore.microsoft.com/ja-jp/edge?ep=2187&form=MA14LT&es=375&cs=1673980518), [google Chrome](https://www.google.com/intl/ja_jp/chrome/dr/download/?brand=OZZY&ds_kid=10484928882&gclsrc=aw.ds&gad_source=1&gad_campaignid=20752932842&gbraid=0AAAAAoY3CA4uDoWrj2QgUBOH4WmNodGQ3&gclid=CjwKCAjwzNTUBhAjEiwA7zcvWnN_fyzS9y6PKauFntOoVbX817NOZOi1DPMu3W7HrxZdx-QDIqX2vhoCILgQAvD_BwE) にて動作を確認しています）で起動する
- 栄養素など必要事項を入力
- 「**バーコード生成**」ボタンを押す
- バーコードが生成されたら「**バーコードPNG保存**」を押して，適当な名称をつけて保存する
- PNGを貼り付けられるアプリケーションに貼り付けて印刷を行う（タテヨコ比を変えるなどするとバーコードリーダーが読めないことがあります）

## Citation
本ソフトウェアを研究、教育または学会発表等で利用した場合は、
以下の文献またはソフトウェアを引用してください。
詳しくは citation.cffをご確認ください

日本栄養学教育学会雑誌第11巻
O-1:可搬性および体感性に優れた栄養教育向けICTソリューションの開発
◯由良亮*, 山本有希*, 桶家亜実*, 河井ますみ*, 大道文香*, 京極奈美*, 佐藤香菜子*, 平山雄大*, 安藤秀子*

## License
このソフトウェアはMITライセンスの元で公開されています

詳しくは LICENSE.ja.md/LICENSE ファイルをご確認ください


This software is released under the MIT License.

See the LICENSE file for details.


## Author
Makoto Yura  
[Kanazawa Gakuin Junior Colledge]

## Contact
yura@kanazawagakuin-u.ac.jp
までお知らせください
