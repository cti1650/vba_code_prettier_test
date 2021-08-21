# vba_code_prettier_test

## このリポジトリを作成した理由

業務改善など、VBA でマクロを作成する際に、  
コーディングルールが社内で一切統一されていないため（そもそも管理されていない…）  
スパゲッティコードの温床と化している状況をなんとか打破すべく、  
VBA で Prettier と同じようなことが出来ないか検証したあとの残骸となります。

残念ながら VBA を Prettier で扱えるようにするプラグインは見つかりませんでしたが、  
単純に VSCode でコーディングした方が効率が良かったため公開した状態で置いておこうと思います！

## ソースコードを編集する流れ

0. 編集したいファイル（編集ファイル）を`bin`に格納
1. ソースコード抽出を実行
   ```
   yarn decombine
   ```
2. `src`に編集ファイルと同一名称のフォルダが生成される
3. `src`内のファイルを編集
4. ソースコード結合を実行
   ```
   yarn combine
   ```

---

## 設定した npm パッケージ

### ESLint

#### インストール

```
yarn add -D eslint
```

#### 初期設定

```
yarn run eslint --init
```

#### prettier 連携

```
yarn add -D eslint-config-prettier
```

### prettier

#### 用途

コード整形

#### インストール

```
yarn add -D prettier
```

## 使用する拡張機能

### Prettier - Code formatter

```
名前: Prettier - Code formatter
ID: esbenp.prettier-vscode
説明: Code formatter using prettier
バージョン: 8.1.0
パブリッシャー: Prettier
VS Marketplace リンク: https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
```

### VSCode VBA

```
  名前: VSCode VBA
  ID: spences10.vba
  説明: VBA language syntax highlighting support and code snippets for VSCode
  バージョン: 1.7.1
  パブリッシャー: Scott Spence
  VS Marketplace リンク: https://marketplace.visualstudio.com/items?itemName=spences10.VBA
```

## 参考にしたサイト

### VBA ソースコードを VBAC を使って Git で差分管理する方法

- Office ファイルから VBA のソースコードを抽出したり結合できる

[https://webbibouroku.com/Blog/Article/vbac](https://webbibouroku.com/Blog/Article/vbac)
