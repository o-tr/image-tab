{% alert type="note", style="callout" %}
このドキュメントは今後更新されません
[最新版のドキュメントはこちらです](https://docs.ootr.jp/docs/Packages/ImageTab/creator/Intro) 
{% endalert %}

# クイックスタート
{% alert type="note", style="callout" %}
Unityや各パッケージの最小バージョンは対応するバージョンのリリースノートを参照してください
{% endalert %}
## 1. パッケージのインポート
<img src="./img/quick-start-1.png" width=400>

ダウンロードしてきたUnityPackageファイルをインポートします

{% alert type="note", style="callout" %}
旧バージョンからアップデートされる場合は一旦削除してから再度インポートすることをおすすめします
{% endalert %}

{% alert type="note", style="callout" %}
<img src="./img/quick-start-2.png" width=400>

UdonSharpのコンパイルに成功していることを確認してください  
もし、コンパイル時にエラーが発生している場合はSDKのバージョンが最小バージョンを満たしているか確認してください  
要件を満たしているのにエラーになる場合は開発者までお問い合わせください
{% endalert %}
{% alert type="note", style="callout" %}
<img src="./img/quick-start-6.png" width=400>

TMPのインポートダイアログが表示された場合は `Import TMP Essentials` を押してパッケージのインポートをお願いします
{% endalert %}

## 2. ギミックの配置
<img src="./img/quick-start-3.png" width=400>  
`jp.ootr/imagetab/prefabs` 内にある各プレハブを必要に応じて配置してください  

各ギミックの使い方についてはユーザ向けガイドを確認してください

## 3. `ImageDeviceController` の配置
{% alert type="note", style="callout" %}
`ImageTab-Standalone`以外のギミックを配置していない場合はこの手順を飛ばしてください
{% endalert %}

<img src="./img/quick-start-4.png" width=400>

`jp.ootr/ImageDeviceController` 内にある `_OotrDeviceController` というプレハブをシーンに配置してください  

<img src="./img/quick-start-5.png" width=400>

次に、同一シーン内にある `ImageTab-Standalone` 以外のギミックすべてを `_OotrDeviceController` の `ImageDeviceController` スクリプトにある `管理対象デバイス(任意)` の欄に登録してください

## 4. ビルド&アップロード
以上でギミックの導入は完了です  
お疲れ様でした  
