# リンクタグをマスターしよう

今回は、クリックしたら別のページや特定の場所に移動できる、 `a` タグについて学びます。

## aタグとは


`a` タグは「anchor」（アンカー）の略。anchorは船のイカリを意味しています。

HTMLでリンクを作るために使われます。 `a` タグはウェブ上でナビゲーションの基本要素となる重要なタグです。

## 基本的な書き方


```html
<a href="https://example.com">Exampleサイトへ移動</a>
```

この例では「Exampleサイトへ移動」というテキストがリンクとなり、クリックすると https://example.comに移動します。

<img src="https://github.com/user-attachments/assets/060be733-e656-48a1-9ae5-d17fd3086378" width=300>

`a` タグで囲まれた文字を `アンカーテキスト` と呼びます。アンカーテキストの文字部分は通常、画像のように文字色が変わりアンダーラインが引かれます。

## 別タブで開く


リンク先を新しいウインドウ、またはタブで表示したい場合は、 `a` 要素に、 `target="_blank"` を指定します。

```html
<a href="https://example.com" target="_blank">Exampleサイトへ移動</a>
```

### 別タブで開く時のセキュリティについて

`target="_blank"` を指定するときは下のコードのように `rel` （レル）属性に `noopener` （ノーオープナー）を指定することが一般的です。

これにより移動先のページから元のページを悪意あるコードによって操作されることを防ぐことができます。

ただし、最近のブラウザではこの `noopener` を指定していなくても、移動先のページから操作できないようになっています。

```html
<a href="https://example.com" target="_blank" rel="noopener">>Exampleサイトへ移動</a>
```

## ハンズオン問題： aタグを設定してみよう


index.htmlを編集し、**別タブ**でエンベーダーへ移動できるように `a` タグ 作成してみよう！
問題で使うURLは https://envader.plus/ です。

なるべく解答は見ないでやってみましょう！

<details>
<summary>解答</summary>

```html
<h1>エンベーダーでLinuxを学ぼう</h1>

<!-- 新しいタブでエンベーダーを開くリンク -->
<a href="https://envader.plus/" target="_blank">
  エンベーダーでLinuxを学ぶ
</a>
```
</details>

## Git Hubへプッシュしよう


編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "リンクの作成"
git push origin main
```

