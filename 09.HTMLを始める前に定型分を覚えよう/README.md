# HTMLを始める前に定型分を覚えよう

ここまでHTMLの基本の書き方やタグについて学びました。

今回はHTMLで行う宣言について学びましょう。

## 基本的な定型分


```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="ここにページの概要が入ります。">
  <title>ページタイトル</title>
</head>
<body>
  <h1>見出し</h1>
  <p>ここに本文を書きます。</p>
</body>
</html>
```

## 宣言


```html
<!DOCTYPE html>
```

`DOCTYPE宣言` はHTMLファイルの最初に記述されるもので、HTMLがHTML5で書かれていることをブラウザに伝え、適切にレンダリングするために必要です。

## htmlタグ


```html
<html lang="ja">
```

`<html>` タグはHTMLドキュメント全体を囲むタグです。この例のように `lang="ja"` とすることで、ドキュメントの言語を日本語に指定します。

## headタグ


ページのメタ情報や外部リソース（スタイルシート、スクリプトなど）を含める部分です。ユーザーには表示されませんが、ブラウザや検索エンジンがこの情報を使用します。

- `<meta charset="UTF-8">` : ドキュメントの文字エンコードをUTF-8に指定します。これにより、日本語を含むあらゆる言語の文字が正しく表示されます。

```html
<meta name="description" content="ここにページの概要が入ります。">
```

- `name="description"` : ページの概要や説明を設定するための属性です。この情報は、検索エンジンの結果ページに表示されたり、ソーシャルメディアのプレビューに利用されます。 `content` にページの具体的な内容を簡潔に説明します。
  
  また、他にもOGP（Open Graph Protocol）というSNSでシェアされた時に表示される情報をより豊かに表現するためのメタデータを定義するプロトコルもあります。
  
  ### **OGP（Open Graph Protocol）とは？**
  
  ```html
  <meta property="og:title" content="OGPについての説明">
  <meta property="og:description" content="OGPとは、ソーシャルメディアでリンクを共有したときに表示される情報を制御するプロトコルです。">
  <meta property="og:image" content="https://example.com/image.jpg">
  <meta property="og:url" content="https://example.com/ogp-explanation">
  ```
  
  - **`og:title`**: ページのタイトルを指定します。リンクが共有されたときにこのタイトルが表示されます。
  - **`og:description`**: ページの説明を指定します。ソーシャルメディアでのプレビューに表示される説明文です。
  - **`og:image`**: リンクプレビューに表示される画像のURLを指定します。視覚的にインパクトのある画像を選ぶことで、リンクのクリック率を向上させることができます。
  - **`og:url`**: ページのURLを指定します。通常は現在のページのURLです。

```html
<title>ページタイトル</title>
```

- `<title>` : ウェブページのタイトルを指定します。このタイトルは、ブラウザのタブや検索エンジンの結果ページに表示されます。

## bodyタグ


```html
<body>
  <h1>見出し</h1>
  <p>ここに本文を書きます。</p>
</body>
```

`body` タグの中身には、実際にブラウザに表示したい内容を入力します。

これまで学んできたタグを使ったものなどは全て `body` タグの中に書きます。

このように、HTMLは `html` タグの中に `head` タグの領域と `body` タグの領域に分かれています。

```html
<!DOCTYPE html>
<html lang="ja">

<!-- ブラウザに表示されない領域 -->
<head>   
  <meta charset="UTF-8">
  <meta name="description" content="ここにページの概要が入ります。">
  <title>ページタイトル</title>
</head>
<!-- ブラウザに表示されない領域 -->

<!-- ブラウザに表示される領域 -->
<body>  
  <h1>見出し</h1>
  <p>ここに本文を書きます。</p>
</body>
<!-- ブラウザに表示される領域 -->

</html>
```

## ハンズオン問題： headとbodyを編集しよう


index.htmlを開いて、以下の手順に従って編集してください。

1. `<head>` タグに以下の内容を追加してください。
  - ページのタイトルを「私のWebページ」と設定してください。
  - メタデータとして、ページの概要を「このページは私の自己紹介です」として追加してください。
2. `<body>` タグに以下のコンテンツを追加してください。
  - 一番大きな見出しで「私の自己紹介」と表示してください。
  - 本文として、簡単な自己紹介文「こんにちは、私はWeb開発を学んでいます。」を表示してください。
  

<details>
<summary>ヒント</summary>
meta name="description" content="ここに概要を入力"

のように`meta`タグを使ってページの概要を追加します。
- `title`タグを使ってページのタイトルを設定します。
- `h1`タグはページの一番大きな見出しを表示するために使用します。
- `p`タグは段落を表示するために使います。
</details>

<br>

<details>
<summary>解答例</summary>

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="このページは私の自己紹介です。">
  <title>私のWebページ</title>
</head>
<body>
  <h1>私の自己紹介</h1>
  <p>こんにちは、私はWeb開発を学んでいます。</p>
</body>
</html>
```
</details> 

## Git Hubへプッシュしよう


編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "定型文の作成"
git push origin main
```