{% alert type="note", style="callout" %}
このドキュメントは今後更新されません
[最新版のドキュメントはこちらです](https://docs.ootr.jp/docs/TextZip/v1) 
{% endalert %}

# TextZip v1
## v0との変更点
突貫ででっち上げたフォーマットだったため、後方互換性を維持するための仕組みなどが整備されておらず、今後拡張していくにあたって障害となることが見込まれたため変更を行いました

変更点は以下のとおりです
- 直下にあったファイルの配列を`files`以下に移動
- 画像データのフォーマットを指定するための`format`を追加
- manifestファイルに読み込みに必要なバージョン`requiredVersion`を追加
- 特定の機能が必要な場合に利用できる配列`requiredFeatures`を追加

## 定義
```typescript
type Rect = {
    width: number;
    height: number;
}

type ManifestItem = {
    path: string;
    format: string; //データのフォーマット
    rect: Rect;
    extensions?: {[ext_name: string]: string} //各機能ごとにKV形式でデータを格納する／extensionに何も指定がない場合は定義しなくても良い
}

type Manifest = {
    files: ManifestItem;
    manifestVersion: number; //マニフェストの仕様版
    requiredFeatures: string[]; //フォーマットの読み込み機能など必須要件
    extensions: string[]; //読み込み自体には支障がないが、あった方が良い要件
}
```

## サンプルデータ
### manifest.json
```
{
    "files": [
        {
            "path": <path-to-image>,
            "format": <texture-format>,
            "rect": {
                "width": <number>,
                "height": <number>
            },
            "ext":{
                "note": <content-string>,
            }
        }
    ],
    "requiredVersion": 1,
    "requiredFeatures": ["rgb24"],
    "extension": ["note"],
}
```
