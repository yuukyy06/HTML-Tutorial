# 4.画像を表示させよう

Webページに画像を追加すると、情報が視覚的に伝わりやすくなり、ページを見たユーザーに良い印象を与えることができます。

`img` タグを使ってHTMLで画像を追加する方法を学びましょう！

## imgタグとは


`img` （イメージ）タグは、HTMLで画像を表示するためのタグです。画像ファイルをWebページ上に埋め込むために使用されます。 `<img>` タグは空要素で、内容を持たないため終了タグは必要ありません。

## 基本の書き方


`img` タグには、 `src` 属性、 `alt` 属性というものを追加します。

### src属性（必須）

`src`（ソース）属性は、表示したい画像ファイルのパスやURLを指定します。

- urlの場合
    
    ```html
    <img src="https://example.com/sample.png">
    ```
    
- パスの場合
    
    ```html
    <img src="images/sample.png">
    ```
    

### alt属性

`alt` （オルト）属性は画像が表示されない場合や画像を読み込めない場合に、代わりに表示されるテキストを指定するための属性です。

```html
<img src="画像の場所" alt="画像の説明文">
```

## 画像を必要なタイミングで読み込もう


Webページに多くの画像や動画が含まれている場合、処理が重くなりページのロードが遅くなったりする原因になります。そこで `Lazy Loading` （レイジーローディング）が役に立ちます。

### Lazy Loadingとは

画像や動画などを必要になるまで読み込まないようにする技術です。具体的にはユーザーがそのリソースを表示される位置までスクロールして初めて読み込むようにして、初回のページ読み込みを高速化し、不要なリソースの読み込みを防ぎます。

- 書き方

    `loading` 属性を使って簡単にLazy loadingを実装できます。

    ```html
    <img src="example.jpg" alt="サンプル画像" loading="lazy">
    ```

## ハンズオン問題： imgタグを使ってみよう


imageディレクトリに画像を3つ用意しています。index.htmlにその画像を読み込んで表示させてみましょう！
alt属性も付けて画像の説明をしましょう！

なるべく解答を見ないでやってみましょう！

<details>
<summary>ヒント</summary>
src属性で画像ファイルのパスを指定します
</details>
<br>

<details>
<summary>解答</summary>
<img src="https://github.com/user-attachments/assets/8cad048f-57a4-40d3-a04c-9710c2673573" width=400>
</details>

## Git Hubへプッシュしよう


編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "画像の表示"
git push origin main
```
