# roblox-rojo-project

Roblox Studio とローカルの Luau ソースを [Rojo 7.7.0](https://rojo.space/docs/v7/) で同期するプロジェクトです。Rojo のバージョンは `rokit.toml` で固定しています。

## 最初の同期

新しいターミナルを開き、このフォルダで次を実行します。

```bash
rojo build -o roblox-rojo-project.rbxlx
rojo serve
```

`roblox-rojo-project.rbxlx` を Roblox Studio で開き、**Plugins > Rojo > Connect** を選びます。以後は `src/` 内の Luau を編集すると Studio に同期されます。

## 構成

- `src/client/`: クライアント用コード
- `src/server/`: サーバー用コード
- `src/shared/`: クライアント／サーバー共通コード
- `default.project.json`: Studio サービスへの配置設定

## GitHub

GitHub リポジトリを接続した後は、通常どおり変更を記録します。

```bash
git add .
git commit -m "Describe your change"
git push
```

生成される `.rbxlx` と Studio のロックファイルは Git 管理対象外です。ソースコードと Rojo 設定のみを共有します。
