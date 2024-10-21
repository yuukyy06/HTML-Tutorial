## 「セマンティック」とは？

日本語に訳すと「意味」を表します。「セマンティックなHTML」とはつまり意味のあるHTMLということです。

## 目的

セマンティックなHTML要素を使うことで、以下のようなメリットがあります。

- SEOで検索しやすくなる
    
    検索エンジンがWebページの内容を理解し、適切な検索結果を表示しやすくなる
    
- アクセシビリティでユーザーが利用しやすくなる
    
    スクリーンリーダーやブラウザの機能を利用するときに、意味のある情報が提供されることで視覚障害を持った方や高齢者にも利用しやすくなります
    

## セマンティックタグを使おう

セマンティックタグはHTML5で導入されたタグで、代表的なタグは以下のようなものがあります

- header（ヘッダー）
- nav（ナビゲーション）
- main（メインコンテンツ）
- article（記事）
- section（セクション）
- aside（サイドバー）
- footer（フッター）

## headerタグの使い方

`header` タグはWebページ全体やセクションごとのヘッダーを定義するのに使われます。

下の画像のように、Webページの先頭や `article` タグの先頭に配置されます。

<img src="https://github.com/user-attachments/assets/b26d695a-a081-4135-a2f2-a520d7f15f83" width="400">

### 1. サイトのヘッダーとして使う

`header` タグは、ロゴや重要なタイトル、ナビゲーションバーなどを含めることが多いです。

```html
<header>
  <h1>私のウェブサイト</h1>
  <nav>
    <ul>
      <li><a href="#home">ホーム</a></li>
      <li><a href="#about">自己紹介</a></li>
      <li><a href="#contact">お問い合わせ</a></li>
    </ul>
  </nav>
</header>
```

### 2. セクションごとのヘッダーとして使う

`header` タグは、ページ全体だけでなく、特定のセクションのヘッダーとしても使えます。

例えば下のように、 `article` タグの中に `header` タグを使い、記事のタイトルと投稿日を表示したりできます。

```html
<article>
  <header>
    <h2>セマンティックHTMLとは？</h2>
    <p>投稿日: 2024年10月12日</p>
  </header>
  <p>セマンティックHTMLは、HTMLタグに意味を持たせることで、コンテンツをより構造化された形で表現する技術です。</p>
</article>
```

## navタグの使い方

`nav` タグは、Webページ内でナビゲーションメニューを定義するために使用されます。例えば、ヘッダーナビゲーション、目次、パンくずリスト、フッターにあるサイトマップなどがあります。

ボタンやリンクが並び、それをクリックするとこで、Webページ内の特定の場所に移動したり、他のページに飛ぶことができます。

- パンくずリストとは？
    
    ページ上部などに「ホーム > カテゴリ > サブカテゴリ > ページタイトル」のように表示されている、現在のページがどこに位置しているかを教えてくれているリストのことです。
    

下のコードは `nav` タグを使った例です。

`ul` タグと `li` タグでリストのアイテムを作り、 `a` タグでリンク先のURLを示しています。

```html
<header>
  <h1>私のウェブサイト</h1>
  <nav>
    <ul>
      <li><a href="#home">ホーム</a></li>
      <li><a href="#about">私について</a></li>
      <li><a href="#contact">お問い合わせ</a></li>
    </ul>
  </nav>
</header>
```

## mainタグの使い方

サイトの主要なコンテンツを囲むためのタグです。ページ内の中核となる最も重要な内容を囲むのに適しています。

<img src="https://github.com/user-attachments/assets/4e744808-becf-43de-b835-55c146f6d5ed" width="400">

`main` タグはページに１つしか使用できません。

また、 `header` 、 `footer` 、 `nav` 、 `article` 、 `aside` タグの中に `main` タグは使えません。

## sectionタグの使い方

`section` は日本語で「部分、節、区分」という意味があります。

Webページ内でトピックごとに分けたいコンテンツをグループ化するときに使います。

例えば一つのブログ記事で、いくつかの小さなテーマに分けられる場合、それぞれのテーマのまとまりを `section` タグで挟みます。

## articleタグの使い方

`article`タグは、Webページ上で独立して再利用可能なコンテンツの部分を囲むために使われます。具体的には、ニュース記事、ブログ記事、フォーラムの投稿、コメントなど、それだけで意味が成り立つような独立したまとまりに対して使います。

### sectionタグとarticleタグの使い分け

以下は `article` と `section` タグを使い分けた例です。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>記事とセクションの使い分け例</title>
</head>
<body>
  <header>
    <h1>ニュースサイト</h1>
    <nav>
      <ul>
        <li><a href="#news">最新ニュース</a></li>
        <li><a href="#sports">スポーツ</a></li>
        <li><a href="#tech">テクノロジー</a></li>
        </ul>
    </nav>
  </header>
  <main>
  <!-- セクションでニュースのカテゴリをまとめる -->
    <section id="news">
      <h2>最新ニュース</h2>

      <!-- 各記事は独立しているため、articleを使う -->
      <article>
        <h3>ニュース記事1</h3>
        <p>ここにニュースの内容が入ります。この記事は独立した内容です。</p>
        <footer>投稿日: 2024年10月12日</footer>
      </article>

      <article>
        <h3>ニュース記事2</h3>
        <p>ここにもニュースの内容が入ります。この記事も独立した内容です。</p>
        <footer>投稿日: 2024年10月11日</footer>
      </article>
    </section>

    <!-- スポーツセクション -->
    <section id="sports">
      <h2>スポーツニュース</h2>

      <article>
        <h3>スポーツ記事1</h3>
        <p>スポーツに関するニュースがここに表示されます。</p>
        <footer>投稿日: 2024年10月10日</footer>
      </article>
    </section>

    <!-- テクノロジーセクション -->
    <section id="tech">
      <h2>テクノロジーの進展</h2>
      <p>このセクションでは、テクノロジーに関連するニュースや情報を提供します。</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2024 ニュースサイト</p>
  </footer>

</body>
</html>
```

`section` : ニュース、スポーツ、テクノロジーの各トピックごとにページをグループ化しています。

`article` : 各ニュース記事が独立したコンテンツであるため、 `article` タグで囲んでいます。

使い分けのポイントは、トピックやテーマのまとまりは `section` でグループ化し、個別の記事は `article` で独立させます。

### articleの誤った使い方の例

```html
<!-- 誤った使い方の例 -->
<main>
  <article>
    <h2>パンケーキの作り方</h2>
    <p>まずは、材料を用意します...</p>
  </article>
  
  <article>
    <h2>卵と牛乳の混ぜ方</h2>
    <p>ボウルに卵を割り入れ...</p>
  </article>
  
  <article>
    <h2>焼き方のポイント</h2>
    <p>中火でフライパンを熱し...</p>
  </article>
</main>
```

この例ではパンケーキを作る手順が `article` で分かれています。しかしこれらは「パンケーキを作る」という一つのトピックに関連した内容であり、このような小さなまとまりに対しては `section` で分けるべきです。

### 記事の中にheaderタグを使う

以下のように `header` タグを記事の中で使うことで、記事の見出しや情報をわかりやすくすることができます。

```html
<article>
  <header>
    <h1>記事タイトル</h1>
    <p>投稿日: 2024年10月12日</p>
  </header>
  <p>記事の本文</p>
</article>
```

## asideタグの使い方

`aside` は日本語に訳すと「脇に」「離れて」「余談」などの意味で、HTMLでは「補足情報」という意味があります。

例えば、記事の横に表示する広告や、ブログのサイドバーにあるプロフィールやリンク集、関連記事などに適しています。

```html
<h2>HTMLはマークアップ言語です。</h2>
<aside>
  <h2>用語解説</h2>
  <p>HTMLは「HyperText Markup Language」の略です。</p>
</aside>
```

### サイドバーとして利用する

サイドバーとして使う場合は、下の画像のように `aside` タグは本文とは別に配置される情報を示します。

<img src="https://github.com/user-attachments/assets/b26d695a-a081-4135-a2f2-a520d7f15f83" width="400">

Webページの主要なコンテンツとの関連はあるが、本文とは独立した情報として使います。下は関連記事のリンクをサイドバーとして使う例です。

```html
<aside class="sidebar">
  <h2 class="sidebar-title">おすすめリンク</h2>
  <ul class="sidebar-menu">
    <li><a href="#">リンク1</a></li>
    <li><a href="#">リンク2</a></li>
    <li><a href="#">リンク3</a></li>
  </ul>
</aside>
```

## footerタグ

`footer` タグは、ページ全体やセクションの末尾に置かれるフッター（注釈部分）を定義するために使われます。著作権情報や連絡先、サイトマップ、関連リンクなどを含むことが多いです。

ページ全体のフッターとしての使用例：

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>footerタグの例</title>
</head>
<body>

  <header>
    <h1>私のウェブサイト</h1>
  </header>

  <main>
    <article>
      <h2>セマンティックHTMLとは？</h2>
      <p>セマンティックHTMLは、タグに意味を持たせてコンテンツをより構造化する方法です。</p>
    </article>
  </main>

  <!-- ページ全体のフッター -->
  <footer>
    <p>&copy; 2024 私のウェブサイト. All Rights Reserved.</p>
    <p><a href="privacy.html">プライバシーポリシー</a> | <a href="terms.html">利用規約</a></p>
  </footer>

</body>
</html>
```

セクションや記事のフッターとしての使用例：

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>記事のfooterタグの例</title>
</head>
<body>

  <main>
    <article>
      <h2>セマンティックHTMLとは？</h2>
      <p>セマンティックHTMLは、HTMLタグに意味を持たせてコンテンツを構造化する方法です。</p>

      <!-- 記事のフッター -->
      <footer>
        <p>著者: 田中太郎</p>
        <p>投稿日: 2024年10月12日</p>
      </footer>
    </article>
  </main>

  <!-- ページ全体のフッター -->
  <footer>
    <p>&copy; 2024 私のウェブサイト. All Rights Reserved.</p>
  </footer>

</body>
</html>
```

`footer` タグは、ページ全体やセクションの末尾に配置され、著作権情報、リンク、連絡先などの捕捉情報を表示するために使います。

## ハンズオン問題： セマンティックなHTMLにしよう

index.htmlを開いて、`dev` タグで書かれているところを `header`、 `article` 、 `aside` 、 `footer` 、 `nav` 、 `main` タグを使って、セマンティックなHTMLに書き換えましょう。

<details>
<summary>解答例</summary>

```html

<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>サンプルサイト</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <!-- headerに変更 -->
    <header class="header">
      <h1>サンプルサイト</h1>
      <!-- navタグを使用 -->
      <nav class="global-nav">
        <ul>
          <li><a href="#">トップページ</a></li>
          <li><a href="#">サービス紹介</a></li>
          <li><a href="#">製品情報</a></li>
          <li><a href="#">ご連絡</a></li>
        </ul>
      </nav>
    </header>
    
    <!-- mainタグを使用 -->
    <main class="container">
      <!-- articleタグを使用 -->
      <article class="main">
        <!-- sectionタグを使用-->
        <section class="article">
          <h2>ニュース1</h2>
          <p>ここにニュースの内容が表示されます。</p>
        </section>
        <!-- sectionタグを使用-->
        <section class="article">
          <h2>ニュース2</h2>
          <p>ここにニュースの内容が表示されます。</p>
        </section>
      </article>
      
      <!-- asideタグを使用 -->
      <aside class="related">
        <h2>おすすめリンク</h2>
        <ul>
          <li><a href="#">リンクA</a></li>
          <li><a href="#">リンクB</a></li>
          <li><a href="#">リンクC</a></li>
        </ul>
      </aside>
    </main>
    
    <!-- footerに変更 -->
    <footer class="footer">
      <p>&copy; 2024 サンプルサイト. All rights reserved.</p>
    </footer>
  </body>
</html>

```
</details>

## Git Hubへプッシュしよう

---

編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "セマンティックHTMLの作成"
git push origin main
```