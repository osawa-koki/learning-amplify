# learning-amplify

🌭🌭🌭 `AWS Amplify`を学習してみる！  

## 準備方法

最初からプロジェクトを作成する場合には、以下のコマンドを実行します。  

```shell
# Amplify CLIをインストール
yarn add @aws-amplify/cli

# Amplify CLIを初期化
yarn amplify configure

# Amplifyプロジェクトを初期化
yarn amplify init
```

静的サイトを作成する場合には、以下のコマンドを実行します。  

```shell
# ホスティングを追加
yarn amplify add hosting

# ホスティングをデプロイ
yarn amplify publish
```

---

すでに作成されたプロジェクトをクローンした際には、セットアップとして以下のコマンドを実行します。  

```shell
# Amplify CLIをインストール
yarn install

# バックエンドを復元
yarn amplify pull --appId <appId> --envName <envName>
```

`appId`と`envName`は、`./amplify/team-provider-info.json`に記載されています。  
