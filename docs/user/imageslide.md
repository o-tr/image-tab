# ImageSlideの使い方

<img src="https://github.com/o-tr/image-tab/assets/155529332/a61b4b6e-76e4-4064-88a9-e00af8088b50" width=400/>

ImageSlideは画像投影用のギミックです  
あらかじめ複数の画像を読み込んでおくことで、端末を切り替えたり画像を読み込み直したりする手間なくスライドなどの資料を投影できます

## ① List

<img src="https://github.com/o-tr/image-tab/assets/155529332/9f7205a2-9cbd-49d8-93ec-749511f65061" width=400/>

画像を読み込むための画面です

### ①画像URL用入力欄

ImageTabの入力欄と同様、画像のURLを入力できます

### ②TextZip形式URL用入力欄

一括で複数枚の画像を読み込むための独自形式 `TextZip` を用いたファイルのURLを入力できます

> [!NOTE]
> 以下のサイトからPDFや画像をTextZip形式のファイルに変換できます  
> https://slide.ootr.jp/

### ③URL

読み込まれている画像のURLを表示します

> [!NOTE]
> 通常の画像の場合は`https://`から始まる実際のURL、TextZip形式の画像の場合は`zip://<元のURL>/<Zip内のパス>`という形式になります

### ④コピー

③で表示されているURLをコピーすることができます

### ⑤削除

該当する画像をリストから削除することができます

## ② Screens

<img src="https://github.com/o-tr/image-tab/assets/155529332/926ca8ac-92ca-41b3-b0d8-ab335592524e" width=400/>

投影対象として使用する端末を選択することができます

## ③ Control

![slide-screens-control](https://github.com/o-tr/image-tab/assets/155529332/1882a55b-618f-4b77-b5a3-d258024fc1b3)

### Prev

1枚前の画像を選択した画面に投影します

### Current

現在の画像を選択した画面に投影します

### Next

1枚後の画像を選択した画面に投影します

## ④ Settings

ImageTabと同様です
