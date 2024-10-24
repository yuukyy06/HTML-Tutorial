### textarea要素を使った入力

複数行のテキスト入力フィールドを作成するために使われる要素です。 `input` 要素と似ていますが、 `textarea` は1行以上のテキストを入力できるので、問い合わせ内容などの長文を入力するのに適しています。

また、 `label` 要素を使って関連づけすることもできます。

```html
<form>
  <label for="contact">お問い合わせ内容</label>
  <div>
    <textarea id="contact" name="contact"></textarea>
  </div>
</form>
```

<img src="https://github.com/user-attachments/assets/d3e9972d-0c81-413b-9474-eadded4e44c1" width="200">

### 主要な属性

- `rows` : 表示する行数を指定する
- `cols` : 表示する列数（横幅の文字数）を指定する
- `name` : フォーム送信時に使用されるフィールド名
- `placeholder` : ユーザーが入力する前に表示されるヒントテキストを指定する
- `required` : フィールドを必須にする

```html
<form>
  <label for="contact">お問い合わせ内容</label>
  <div>
    <textarea id="contact" name="contact" rows="5" placeholder="ここに入力してください"></textarea>
  </div>
</form>
```

<img src="https://github.com/user-attachments/assets/9b7ec10b-08d9-4d73-9360-d5265588119b" width="200">

`rows` 属性で行を増やし、 `placeholder` 属性で「ここに入力してください」と表示しています。

`cols` 属性は文字の大きさや種類で異なるのであまり使われません。指定したいときは `css` で設定するのがおすすめです。

## select要素を使った入力

`select` 要素は `select` タグを使ってセレクトボックスを作ることができます。

クリックすると選択肢が展開されます。 `select` タグの中に `option` タグを使って、選択肢を追加します。

```html
<form>
  <label for="animals">動物を選択 : </label>
  <select id="animals" name="animals">
    <option value="dog">犬</option>
    <option value="cat">猫</option>
    <option value="rabbit">ウサギ</option>
    <option value="elephant">ゾウ</option>
  </select>
</form>
```

<img src="https://github.com/user-attachments/assets/ccbc0fa6-7205-4ffc-a02d-4dabcea3a7b1" width="200">

ユーザーがリストから選択肢を選んだ場合、その値がフォームと一緒に送信されます。仮に「犬」を選んだ場合、 `value` で指定された `dog` がフォームで送信されます。

## ハンズオン問題： フィードバックフォームを作ろう

index.htmlに足りない記述を埋めてフィードバック入力欄とセレクトボックスを作成してください。

- フィードバック入力欄は縦に5行のサイズを指定
- セレクトボックスは交通手段を選択できるセレクトボックスを作成
    - 選択肢は「車」、「自転車」、「電車」、「バス」、「飛行機」を選択できるようにする

完成図：

<img src="https://github.com/user-attachments/assets/31ddecee-18d9-4ef0-9e2e-c7831705b37a" width="300">

<details>
<summary>解答例</summary>
    
```html
<form action="/submit" method="POST">
  <label for="feedback">フィードバック:</label>
  <div>
  <textarea id="feedback" name="feedback" rows="5" placeholder="フィードバックをここに入力してください"></textarea>
  </div>
  <label for="transport">交通手段を選択:</label>
  <select id="transport" name="transport">
    <option value="car">車</option>
    <option value="bike">自転車</option>
    <option value="train">電車</option>
    <option value="bus">バス</option>
    <option value="plane">飛行機</option>
  </select>

  <input type="submit" value="送信">
</form>
```

</details>

## Git Hubへプッシュしよう

---

編集したindex.htmlをGit Hubのリモートリポジトリにプッシュしましょう！

以下のコマンドを実行します。

```bash
git add .
git commit -m "textarea,selectタグの作成"
git push origin main
```