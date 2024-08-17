{% alert type="note", style="callout" %}
このドキュメントは今後更新されません
[最新版のドキュメントはこちらです](https://docs.ootr.jp/docs/TextZip/) 
{% endalert %}

# TextZip形式について
## TextZipとは
`StringDownloader` で複数の画像を一括で読み込むために開発したファイル形式です

## しくみ
### 1. 生の画像データに変換する
現状のUdonにおいて、バイナリデータから画像を読み込むためには `Texture2D.LoadRawTextureData` を用いる必要があります  
そのため、画像データをピクセルごとの色データに変換する必要があります  
バイナリデータの形式については `Unity` のドキュメントを参照してください  
https://docs.unity3d.com/ja/2019.4/ScriptReference/Texture2D.LoadRawTextureData.html

### 2. マニフェストデータを生成する
この後の工程でZip形式に圧縮するため、その際に画像データを配置するパスと、画像のサイズ(横幅と縦幅)をまとめます  
これを各画像に対して生成し、一つの配列にまとめたものを `JSON` 形式で保存します

### 3. Zip形式に圧縮する
マニフェストファイルを `<root-dir>/manifest.json`、 画像ファイルを各自指定したパスに保存し、Zip形式に圧縮します

### 4. Base64形式でテキストデータに変換する
Zip化したバイナリデータをBase64形式に変換します  
本来であればバイナリデータをそのまま読み込んだほうが容量効率は良いですが、 `StringDownloader` でバイナリデータを読み込んだ場合、無理やりバイナリデータを文字列に変換しようとするらしく、とても重くなってしまうため、回避策として文字列への変換を行っています

### 5. サーバーに配置する
以上でTextZip形式のファイルは完成です  
任意のサーバーやクラウドなどに配置して配信を行ってください

## 仕様の詳細
- [TextZip v1](./text-zip.v1.md)
    - ImageDeviceController v0.0.7以上から対応
- [TextZip v0](./text-zip.v0.md)
