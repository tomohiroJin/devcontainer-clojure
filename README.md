# Clojure開発用DevContainer

このリポジトリは、Visual Studio Code（VS Code）のDevContainer機能を使用して、Clojureの開発環境を構築するための設定を提供します。

## 特徴

- **Clojure CLIツール**: 最新のClojure CLIツールをインストール済み。
- **Leiningen**: ClojureのビルドツールであるLeiningenをインストール済み。
- **Node.js**: ClojureScriptの開発をサポートするため、Node.jsをインストール済み。
- **VS Code拡張機能**: Clojure開発を支援する以下の拡張機能をプリインストール。
  - Calva: Clojure & ClojureScriptの統合開発環境。
  - clj-kondo: 静的解析ツール。

## 使用方法

1. **リポジトリのクローン**:
   ```bash
   git clone https://github.com/tomohiroJin/devcontainer-clojure.git
   cd devcontainer-clojure
   ```

2. **VS Codeでフォルダを開く**:
   VS Codeで`devcontainer-clojure`フォルダを開きます。

3. **DevContainerの起動**:
   VS Codeのコマンドパレット（`Ctrl+Shift+P`または`Cmd+Shift+P`）で「Dev Containers: Reopen in Container」を選択します。これにより、定義されたDevContainer内でワークスペースが再オープンされます。

4. **新しいClojureプロジェクトの作成**:
   コンテナ内のターミナルで以下のコマンドを実行して、新しいLeiningenプロジェクトを作成します。
   ```bash
   lein new app my-app
   cd my-app
   ```

5. **テストの実行**
   ```bash
   lein test
   ```

6. **対話型開発を行うには**
   ```bash
   lein repl
   ```

7. **Calva**:
   Calva拡張機能を使用してREPLを起動し、コードの実行やテストを行います。

## カスタマイズ

必要に応じて、`.devcontainer/devcontainer.json`や`Dockerfile`を編集して、開発環境をカスタマイズできます。例えば、追加のVS Code拡張機能をインストールしたり、特定のバージョンのツールを指定したりすることが可能です。

## 参考資料

- [VS Code Remote Development](https://code.visualstudio.com/docs/remote/remote-overview)
- [Clojure公式サイト](https://clojure.org/)
- [Leiningen公式サイト](https://leiningen.org/)

