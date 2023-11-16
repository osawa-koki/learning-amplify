# learning-amplify

🌭🌭🌭 `AWS Amplify`を学習してみる！  

## 準備方法

最初からプロジェクトを作成する場合には、以下のコマンドを実行します。  

```shell
# Amplify CLIをインストール
yarn [global] add @aws-amplify/cli

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

---

Amplifyはフレームワーク(Next.js SSR or Next.js SSGなど)を`package.json`から自動で判断しますが、Next.jsはバージョン`14`から`next build && next export`がNGとなり、Amplifyの自動判定が失敗します。  

したがって、以下のコマンドを実行して、フレームワークを明示的に指定する必要があります。  

```shell
aws amplify update-app --app-id <APP_ID> --platform WEB
aws amplify update-branch --app-id <APP_ID> --branch-name main --framework 'Next.js - SSG'
```
