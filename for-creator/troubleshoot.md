{% alert type="note", style="callout" %}
このドキュメントは今後更新されません
[最新版のドキュメントはこちらです](https://docs.ootr.jp/docs/Packages/ImageDeviceController/creator/Troubleshoot) 
{% endalert %}

# トラブルシュート
## インポート時にコンパイルエラーになる
VRCSDKのバージョンが最小要件を満たしているか確認してみてください  
このギミックでは積極的に新機能を活用しているため、最新版でないと動かない可能性があります

## パッケージアップデート後に動かなくなった
一度パッケージ全体を削除してみてください

## `ImageTab` に `Cast` ボタンが表示されない
以下の場合は `Cast` ボタンが自動的に非表示になります
- `ImageTab-Standalone` プレハブを使用している場合
- `ImageDeviceController` に画像の投影先として指定可能なデバイス (`ImageTab`, `ImageScreen`) が自分以外に存在しない場合

## `ImageTab` に `Library` ボタンが表示されない
ブックマークが指定されていない場合は履歴機能のみが有効化されるため、代わりに `History` ボタンが表示されます

## 投影先一覧にデバイスが出てこない
同じ `ImageDeviceController` に登録されているか確認してみてください  
また、デバイスの名前を正しく設定できているか確認してみてください

## 画像を読み込もうとすると応答がなくなる
端末が `ImageDeviceController` に登録されているか確認してみてください  
登録されていない場合エラーとなって応答が無くなる場合があります

## UIの表示をカスタマイズしたい
軽量化のため、スクリプト側にもUIのロジックが入っています  
テクスチャの差し替え程度であれば問題ありませんが、削除してからの再配置などはエラーの原因となります

