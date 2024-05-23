# ImageTab

![MIT license](https://img.shields.io/badge/license-MIT-blue.svg)
![Booth](https://img.shields.io/badge/BOOTH-c54245)

VRCImageDownloaderを用いた画像表示用のタブレットモデルとUdonSharpスクリプトです

## サンプルワールド
https://vrchat.com/home/world/wrld_c6cb0712-e5bd-4c53-a340-4273b866eede

## 各ギミックについて
### ImageTab
URLを入力することによって任意の画像を表示できる他、あらかじめ設定したURLからの読み込みや履歴機能、投影機能などを搭載しています  
また、自動回転や画面内での最大化など一般的な機能も搭載しています

### ImageSlide
会議などで使用することを想定したスライド投影用端末です  
画像URLをあらかじめ登録しておくことで端末を切り替えることなく、スムーズに画像を切り替えることができます  
また、TextZip形式を用いることで一括で画像を読み込むこともできます  
投影先の選択後、「Prev」「Current」「Next」のいずれかの画像を押すことで画像を投影できます  

## 利用規約 / 改変・再配布などについて

このプロダクトはMITライセンスでリリースしています  
また、一部私以外によって MIT LICENSE やApache License 2.0、SLI OPEN FONT LICENSE でリリースされたファイルが含まれます  
ライセンスに従ってさえいれば改変や再配布などは自由に行っていただいて構いません  

ただ、改変したものを配布される場合などは一報入れていただけると私が喜びます  

## 使い方
詳細は以下のリンクをご確認ください  
https://slide.ootr.jp/  

## サポート
BOOTHの購入履歴またはTwitterのDMに連絡をいただければ対応します

## 更新履歴
[Releases](https://github.com/o-tr/image-tab/releases) を参照してください

## 現時点で確認している不具合
現時点ではありません

### 過去の不具合
- 管理スクリプトのElement0に設定されたImageTabまたはImageSlideの投影対象一覧が空になる
  - Element0にImageScreenを割り当てることで回避できます
  - v0.0.2で修正しました

## 今後の更新予定
- プレイヤーと統合できるスクリーンの追加
- セットアップをサポートするエディタースクリプトの追加
- タブレットをマウントできる台の追加

