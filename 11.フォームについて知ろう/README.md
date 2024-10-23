HTMLでWebページ上にフォームを作るために `form` タグを使います。フォームはユーザーが情報を入力して送信するために使われます。

例えば、お問合せフォームやログインフォームなどでは全体に `form` タグが使われ、いくつかのパーツで構成されています。

<img src="https://github.com/user-attachments/assets/9e86807f-5a6b-409b-8d1c-3e13623a2627" width="800">

`form` タグは以下のようなパーツで構成されています。

### action属性

フォームが送信された際に、データを送信する先のURLを指定するための属性です。例えば、ユーザーがフォームに入力した情報をサーバーに送信する場合、そのサーバーのエンドポイント（URL）を `action` 属性で指定します。

```html
<form action="http://example.com">
```

この場合、フォームが送信されたときに “http://example.com” に対してデータが送信されます。

### method属性

フォームがデータを送信する際のHTTPメソッドを指定する属性です。主に以下の2つがあります。

- `GET` : URLのクエリパラメータとしてデータを送信。データがURLに含まれるため、検索フォームなどに使用されます。
- `POST` : データをHTTPリクエストの本文として送信。大きなデータや機密情報の送信に適しています。

method属性で何も指定しない場合は、GETメソッドとして送信されます。

## input要素について知ろう

ユーザーから入力を受け取るためのHTML要素です。フォーム内で様々な形式のデータ（テキスト、パスワード、ボタン、チェックボックスなど）を入力できるフィールドを作成します。

```html
<form>
  <input type="text" name="name" value="名前" placeholder="名前を入力してください">
</form>
```

- `type` 属性 : 入力フィールドの種類を指定する
- `name` 属性 : 入力フィールドの名前を指定。送信されたデータをサーバー側で識別するために使われます。
- `value` 属性 : 入力フォームの初期値を設定
- `placeholder` 属性 : 入力フィールド何に表示されるヒントや例示のテキストを指定。入力が始まると消えます。
- `required`: フィールドを必須にする。空のままフォームを送信できなくなります。
    - 例: `<input type="email" required>`

### type属性とは？

type属性の値に応じて、表示される入力欄の種類が変わります。以下のような種類があります。

- `text` : テキストボックス（入力欄）を表示
- `password` : パスワード入力フィールド（入力が隠される）
- `email` : メールアドレス入力フィールド
- `number` : 数値入力フィールド
- `checkbox` : チェックボックスを表示
- `radio` : ラジオボタンを表示
- `submit` : 送信ボタンを表示

例：

```html
<input type="text" name="username" placeholder="名前を入力してください">
<input type="submit" value="送信">
```

<img src="https://github.com/user-attachments/assets/16155f1a-409f-404a-bdac-fb3f6d536f28" width="300">

このようにinput要素に属性を組み合わせることで入力フォームと送信ボタンが作成できました。

### name属性とは？

送信されたデータをサーバー側で識別するために使用される属性です。

例えば以下のフォームでは `username` と `password` という2つの `name` 属性が設定されています

```html
<input type="text" name="username" placeholder="名前を入力">
<input type="password" name="password" placeholder="パスワードを入力">
```

- `name` 属性はサーバー側でフォームデータを受け取るのに必ず必要です。
- 同じ `name` 属性を持つinput要素が複数ある場合、配列として送信されます。例としてチェックボックスなどで使います。

### value属性とは？

ユーザーが入力した値や選択した値を取得したり、初期値を設定したりするために使われます。

1. **テキストフィールド (`type="text"`)**
    
    `value`属性で、テキスト入力フィールドの初期値を設定できます。
    
    ```html
    <input type="text" name="username" value="田中太郎">
    ```
    
    この場合、フィールドには最初から「田中太郎」という値が入力されています。
    
2. **ボタン (`type="submit"`, `type="button"`)**
    
    `submit`ボタンや`button`要素では、ボタンに表示されるラベルを`value`で指定します。
    
    ```html
    <input type="submit" value="Submit Form">
    ```
    
    この場合、ボタンには「Submit Form」というラベルが表示されます。
    
3. **チェックボックス (`type="checkbox"`)**
    
    チェックボックスやラジオボタンでは、選択された場合に送信される値を`value`属性で指定します。
    
    ```html
    <input type="checkbox" name="subscribe" value="yes"> Subscribe to newsletter
    ```
    
    チェックが入った状態で送信されると、`subscribe=yes`がサーバーに送信されます。
    
4. **隠しフィールド (`type="hidden"`)**
    
    ユーザーに表示せずにサーバーに送信したい値を隠しフィールドで設定できます。
    
    ```html
    <input type="hidden" name="userID" value="12345">
    ```
    
    この場合、フォーム送信時に`userID=12345`がサーバーに送信されます。
    

まとめると、 `value` 属性は、フォーム要素が持つ初期値や送信される値を指定する重要な属性です。 

## label要素を使って関連付けしよう

`label` 要素は、フォーム部品とラベルを関連づけるために使われます。

`label` 要素には2つの使い方があります。

1. **`for`属性を使う方法**
    
    `label`要素の`for`属性に、関連付けたい`input`要素の`id`属性を指定します。
    
    ```html
    <label for="username">Username:</label>
    <input type="text" id="username" name="username">
    ```
    
    この場合、`label`の「Username:」をクリックすると、自動的に`id="username"`の`input`フィールドにフォーカスが移ります。
    
2. **`input`要素を直接内包する方法**
    
    `label`要素の中に`input`要素を直接含めることでも、ラベルと入力フィールドを関連付けることができます。
    
    ```html
    <label>Username: <input type="text" name="username"></label>
    ```
    
    この方法でも、ラベルをクリックすると入力フィールドにフォーカスが移ります。
    

上記のように `label` 要素を使うことで、ラベルをクリックすると、そのラベルに対応する入力フィールドにフォーカスが移り、フォームの使いやすさが向上します。

## ハンズオン問題： 基本的なフォームを作成しよう

### **目標**

ユーザー名、パスワード、性別、ニュースレター購読のオプションを含むフォームを作成します。ユーザーが送信する際、すべての必須項目が正しく入力されている必要があります。入力されたデータはサーバーへ送信され、対応するURLにデータがPOSTメソッドで送られます。

### **課題内容**

1. ユーザー名（`username`）とパスワード（`password`）の入力フィールドを作成します。それぞれ必須項目とし、適切なラベルを付けてください。
2. 性別を選択できるラジオボタン（男性、女性）を作成し、適切なラベルを付けてください。
3. 「ニュースレターを購読する」というチェックボックスを追加します。
4. 送信ボタン（`Submit`）を作成し、`action`属性で`/submit`エンドポイントにデータを送信するようにします。`POST`メソッドを使用してください。

index.htmlのコードにいくつか空欄があるので、適切なコードを埋めて正しいフォームを完成させてください。

なるべく解答は見ないでやってみましょう。

- 解答例
    
    ```html
    <form action="/submit" method="POST">
      <label for="username">名前:</label>
      <input type="text" id="username" name="username" placeholder="名前を入力" required>
    
      <label for="password">パスワード:</label>
      <input type="password" id="password" name="password" placeholder="パスワードを入力" required>
    
      <p>性別を選択:</p>
      <label>
        <input type="radio" name="gender" value="male" required> 男
      </label>
      <label>
        <input type="radio" name="gender" value="female" required> 女
      </label>
      <br>
    
      <label>
        <input type="checkbox" name="subscribe" value="yes"> ニュースレターを購読する
      </label>
    
      <input type="submit" value="送信">
    </form>
    
    ```
    

## Git Hubへプッシュしよう

---

編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "基本的なフォームの作成"
git push origin main
```