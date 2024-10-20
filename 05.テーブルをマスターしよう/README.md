# テーブルをマスターしよう

今回は、HTMLの「入れ子構造」と「table」タグについて学びます。

## HTMLの入れ子構造について


HTMLでは、要素を要素の中に配置することがよくあります。これを「入れ子構造」といいます。

```html
<div>
  <p>これは段落です。</p>
  <ul>
    <li>リストアイテム1</li>
    <li>リストアイテム2</li>
  </ul>
</div>
```

<img src="https://github.com/user-attachments/assets/eb784cef-7c7e-4294-91bb-87bf7592fd27" width=300>

この例では`div`タグの中に`p`タグと`ul`（リストタグ）を入れ子にしています。

- `div`タグ: は特定の意味を持っていないタグで、HTMLの様々な要素をグループ化するのによく使われます。
- `ul`タグ: 順序の無いリスト（Unordered List）を作成するためのタグです。リストの項目は`li`タグを使って定義します。

## tableタグとは？


`table`タグはHTMLで表（テーブル）を作るのに使用します。

例）

```html
<table border="1">
	<tr>
		<th>名前</th>
		<th>年齢</th>
		<th>職業</th>
	</tr>
	<tr>
		<td>田中太郎</td>
		<td>30</td>
		<td>エンジニア</td>
	</tr>
	<tr>
		<td>佐藤花子</td>
		<td>25</td>
		<td>デザイナー</td>
	</tr>
</table>

```

<img src="https://github.com/user-attachments/assets/0c199f46-4cdf-46c8-8593-d51227fa47a8" width=300>

## tableタグの構成

<img src="https://github.com/user-attachments/assets/32fede59-22c8-4c5c-9090-fad5ffff3d48" width=400>


- `table` タグ: 表全体を定義するために使います。このタグの中に表があることを示します。
- `tr`タグ: 「table row」の略で表の行を作ります。
- `th`タグ: 「table header」の略で表の見出し部分を作るのに使います。列のタイトルなどがここに入ります。
- `td`タグ: 「table data」の略で、「データ」を意味します。表の各セルに具体的な値や情報を入れるために使います。

## theadとtbodyの活用


以下は、`<thead>`と`<tbody>`を使用した例です。このタグを使うことで、テーブルの見出し部分とデータ部分を明確に分けることができます。

```html
<table border="1">
	<thead>
		<tr>
			<th>名前</th>
			<th>年齢</th>
			<th>職業</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>田中太郎</td>
			<td>30</td>
			<td>エンジニア</td>
		</tr>
		<tr>
			<td>佐藤花子</td>
			<td>25</td>
			<td>デザイナー</td>
		</tr>
	</tbody>
</table>
```

- **`<table border="1">`**: テーブル全体を囲むタグで、`border="1"`でテーブルに境界線を付けています（オプション）。
- <thead>タグ: テーブルの見出し部分を定義します。ここでは列の見出し（名前、年齢、職業）が含まれます。
- <tbody>タグ:  テーブルのデータ部分を定義します。ここでは、<tr>タグでデータ行を定義しています。

このように、`<thead>`と`<tbody>`を使うことで、テーブルの構造がより明確になり、HTMLを整理された状態で書けるようになります。また、これによりスタイリングやスクリプト処理を見出し部分とデータ部分で分けて実装しやすくなるなどのメリットがあります。

## scope属性について


scope属性には、主に `col` と `row` の2つの値があります。

- col : 列の見出しであることを示します。
- row : 行の見出しであることを示します。

### 書き方

```html
<tr>
	<th scope="col">名前</th>
	<th scope="col">年齢</th>
	<th scope="col">職業</th>
</tr>
```

`col` を指定することで列の見出しであることをしましています。

```html
<tr>
	<th scope="row">田中太郎</th>
	<td>30</td>
	<td>エンジニア</td>
</tr>
```

`row` を指定することで各行の最初の列が、その行の見出しであることを示しています。

<img src="https://github.com/user-attachments/assets/0c199f46-4cdf-46c8-8593-d51227fa47a8" width=300>


`scope` を使うことによりHTMLコードを見た時に、見出しがどの行や列にあるかが明確になり、SEOにも有利に働きます。

## **入れ子構造の良い書き方**


HTMLはスペースや改行を無視するため、同じ内容でも以下の2つの書き方は表示結果が同じになります。

```html
<!-- その1 -->
<div><h3>あいさつ</h3><p>お元気ですか？</p><ul><li>今日の天気</li></ul></div>
```

```html
<!-- その2 -->
<div>
	<h3>あいさつ</h3>
	<p>お元気ですか？</p>
	<ul>
		<li>今日の天気</li>
	</ul>
</div>
```

**書き方のポイント**:

- **インデント**: 要素の親子関係を明確にし、タグの対応を把握しやすくします。
- **可読性**: インデントや改行を使ってコードを整理し、他の人が理解しやすいコードを書くことが大切です。


## **テーブル構造と行単位の整理**


テーブルを作成する際、シンプルなテーブルであれば行単位でHTMLを整理すると可読性が向上します。例えば、次のようなテーブルでは、1行の内容を1つの`tr`タグでまとめて書くことで見やすくなります。

```html
<table>
  <tr><th>品名</th><td>タオル</td><td>シャンプー</td></tr>
  <tr><th>値段</th><td>@500</td><td>@600</td></tr>
  <tr><th>在庫数</th><td>89</td><td>26</td></tr>
</table>
```

<img src="https://github.com/user-attachments/assets/5de85eba-0048-4c74-8029-619eb98cb8e9" width=300>

- **行ごとにタグをまとめる**: 各行を`tr`タグでグループ化することで、表の構造を明確にし、管理しやすくなります。

シンプルなテーブルであれば1行ごとや1つの機能ごとにまとめると、HTMLが読みやすくなります。ただし、大きなテーブルや複雑な構造の場合可読性が低下する恐れもあるので状況に応じて使い分けましょう。

## ハンズオン問題： 表を作ってみよう


次のプログラミング言語のリストと出力イメージを参考にして、`<thead>`と`<tbody>`タグを使ったテーブルをindex.htmlに作成してください。

なるべく解答を見ないでやってみましょう！

### **プログラミング言語のリスト**

- **言語1**: Python, 1991年, 高度な汎用プログラミング言語
- **言語2**: JavaScript, 1995年, Web開発で広く使用される
- **言語3**: Go, 2009年, Googleによって開発された言語

### **必要な手順:**

1. **テーブルの見出し部分**を`<thead>`タグで作成。
2. **プログラミング言語のデータ部分**を`<tbody>`タグで作成。


### 出力イメージ

<img src="https://github.com/user-attachments/assets/c36c90e6-1bc4-41c6-9058-a563f0ef9c48" width=400>

<details>
<summary>解答例</summary>

```html
<h1>プログラミング言語の詳細表</h1>

<table border="1">
	<thead>
		<tr>
			<th>プログラミング言語</th>
			<th>発表年</th>
			<th>説明</th>
		</tr>
	</thead>
<tbody>
		<tr>
			<td>Python</td>
			<td>1991年</td>
			<td>高度な汎用プログラミング言語</td>
		</tr>
		<tr>
			<td>JavaScript</td>
			<td>1995年</td>
			<td>Web開発で広く使用される</td>
		</tr>
		<tr>
			<td>Go</td>
			<td>2009年</td>
			<td>Googleによって開発された言語</td>
		</tr>
	</tbody>
</table>
```
</details>

## Git Hubへプッシュしよう


編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "テーブルの作成"
git push origin main
```