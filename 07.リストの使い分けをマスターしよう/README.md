# リストの使い分けをマスターしよう

今回はHTMLで使う様々なリストの作り方を学びます。

## liタグとは？


`<li>` タグは `List Item`の略で**リストの項目**を定義するために使用します。

順序のないリスト `<ul>` タグや、順序のあるリスト `<ol>` タグの中に配置され、各項目を表します。

```html
<ul>
  <li>リンゴ</li>
  <li>バナナ</li>
  <li>オレンジ</li>
</ul>
```

## ulタグとは？


`<ul>` タグは `Unordered List` の略で**順序のないリスト**を作成するためのタグです。このタグを使うと、箇条書きのリストが表示され、リスト項目は黒い丸が表示されます。各リスト項目は、 `<li>` タグを使って定義します。

リストの中にリストを入れることもできます。

```html
<ul>
  <li>フルーツ
  <ul>
    <li>リンゴ</li>
    <li>バナナ</li>
  </ul>
  </li>
  <li>野菜
  <ul>
    <li>トマト</li>
    <li>キュウリ</li>
  </ul>
  </li>
</ul>
```

<img src="https://github.com/user-attachments/assets/ae0d69b5-118a-4343-ba33-4b97262448e2" width=200>

## olタグとは？


`<ol>` タグは `Ordered List` の略で**順序のあるリスト**を作成するために使用されます。このタグを使うと、リストの各項目に番号やアルファベットが付与され、順序付きのリストを表現できます。各リスト項目は、 `<li>` タグを使って定義します。

```html
<ol>
  <li>リンゴ</li>
  <li>バナナ</li>
  <li>オレンジ</li>
</ol>
```

<img src="https://github.com/user-attachments/assets/aa4089c0-433d-4af7-a10c-1d130f287cb1" width=200>

## dlタグとは？


`<dl>` タグは、 `Description List` の略で説明リストと呼ばれ、新しい言葉や用語を説明する時に使用します。 `<li>` の代わりに `<dt>` 、 `<dd>` タグを組み合わせて定義します。

### dlタグの構成

- `<dl>` : 説明リスト全体を囲むタグ
- `<dt>` : 説明する用語 （Description Term）を記述するタグ
- `<dd>` : 用語の説明（Description definition）を記述するタグ

```html
<dl>
  <dt>HTML</dt>
  <dd>ウェブページを作成するためのマークアップ言語です。</dd>
  
  <dt>CSS</dt>
  <dd>ウェブページのスタイルを定義するための言語です。</dd>

  <dt>JavaScript</dt>
  <dd>ウェブページに動的な機能を追加するプログラミング言語です。</dd>
</dl>
```

<img src="https://github.com/user-attachments/assets/d3ebd889-5f50-4ff7-b81e-ba682e80a4ce" width=400>

`dt` の内容を `dd` で説明している形式になっていればOKです。

## **ハンズオン問題: 目次用のリストを作ってみよう**


以下の要件と完成図を参考にして、index.htmlにリストを作成してみましょう。

なるべく解答は見ないでやってみましょう。

1. 「見出し1」**と**「見出し2」を目次として表示してください。
2. 「見出し2」**の中にサブリストとして**「見出し2-1」**と**「見出し2-2」を作成してください。


完成図

<img src="https://github.com/user-attachments/assets/b7b7d484-aebf-4980-9a47-ce1dd87eda27" width=200>

<details>
<summary>ヒント</summary>

- `<ol>` タグは、順序のあるリスト（番号付きリスト）を作成します。
- `<li>` タグは、リストの項目を定義します。
- リストの中にリストを作るには、入れ子構造を使用します。

</details>

<br>

<details>
<summary>解答例</summary>

```html
<div class="toc">
  <div>
  目次
  </div>
  <!-- ここに目次用のリストを作ってください -->
  <ol>
  <li>見出し1</li>
  <li>
    見出し2
    <ol>
    <li>見出し2-1</li>
    <li>見出し2-2</li>
    </ol>
  </li>
  </ol>
</div>
```
</details>    

## Git Hubへプッシュしよう


編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "リストの作成"
git push origin main
```

