## Web制作について


「**Web 制作**」とは、**インターネット上で見ることができる Web サイトを作ること**です。

<img src="https://github.com/user-attachments/assets/f4dc59ed-1da0-4b63-93d6-560797bd7a37" width=400>

HTMLやCSS、JavaScriptという言語を使って、テキスト、写真、動画などのコンテンツを組み合わせて作られています。

HTML、CSS、JavaScriptにはそれぞれ役割があります

- HTML
    
    
    <img src="https://github.com/user-attachments/assets/c090afe9-45cd-47b2-bc54-cf3534be4e88" width=400>
    
    HTMLはWebページの骨組みとなる言語です。
    
    テキスト、画像、リンクなどをHTMLを使ってどこに表示するかを決めます。しかしHTMLだけでは配置やデザインなどはできません
    
- CSS
    
    
    <img src="https://github.com/user-attachments/assets/3794a026-7ecc-4b90-92bf-a0b2c1927f87" width=400>
    
    CSSを使ってWebページの見た目を整えます
    
    色、フォント、レイアウトなどを自由に設定でき、アニメーションや画面に合わせたサイズ調整などもできます。
    
- JavaScript
    
    
    <img src="https://github.com/user-attachments/assets/4dbb6ee6-af9d-46f4-935b-5ec844841b09" width=400>
    
    JavaScriptは、Webページに機能を追加する言語です。
    
    HTMLとCSSで文字や画像を表示させることはできますが、それだけでは動きはつけることはできません。JavaScriptを使うことによりボタンを押して画面が変わったりユーザーの操作に対して反応させることができるようになります。
    

## ブラウザについて

<img src="https://github.com/user-attachments/assets/872f01fc-ff80-4742-935f-05940b4562e6" width=400>


ブラウザとは、Webサイトを閲覧するために使うソフトウェアです

ブラウザを使ってWebサイトにアクセスして、ページの内容を画面に表示します

## ブラウザの種類

<img src="https://github.com/user-attachments/assets/1533e8bc-ffbd-4ee4-85ff-110da330f661" width=400>

ブラウザにはChrome（クローム）、Safari（サファリ）、Firefox（ファイアフォックス）などの様々な種類があります。

中でもGoogle Chromeが、ページの読み込みが速く、安全性も高いため最も多くの人に選ばれており、世界シェアと日本シェアでトップです。

## Web制作する時の注意点


Webサイトを作るときは、様々なブラウザや端末での表示を確認する必要があります。

<img src="https://github.com/user-attachments/assets/8d53ba6b-7a1f-48bd-bdfd-4972557955c7" width=400>

ブラウザやデバイスが異なると、Webサイトの見え方や動作が変わったりします。

Chrome、Firefox、Safariなどの複数のブラウザや、スマホ、タブレット、PCなどでWebサイトが適切に表示されているかを確認する必要があります。

## エディターについて


エディターとは、HTMLやCSSなどプログラミングのソースコードを編集することができるソフトウェアです。

<img src="https://github.com/user-attachments/assets/d074ac34-084a-4a6d-a0d4-8125d5933093" width=400>

Microsoftが開発している**Visual Studio Code（VScode）と**いうエディターがおすすです。

エディターを使ってハンズオンを進めていくのでまだダウンロードしていない方はダウンロードしましょう。

[Visual Studio Code（VScode）](https://code.visualstudio.com/download)

## ハンズオン：　エディターを使ってみる


実際にエディターを使ってみましょう。index.htmlに文字を入力してみましょう。


```html
<!-- index.html -->

Hello! RareTECH!

```

## Git Hubにプッシュしよう


VScodeで (ctl + @) を押すとターミナルを開けます。

ターミナルで以下のコマンドを実行します。

1. **ファイルをステージング**: 次のコマンドですべてのファイルをステージングします。
    
    ```bash
    git add .
    ```
    
2. **コミットを作成**: 次のコマンドでコミットメッセージをつけて保存します。
    
    ```bash
    git commit -m "Hello RareTECH"
    ```
    
3. **リモートリポジトリにプッシュ**: GitHubにリモートリポジトリを作成して、次のコマンドでプッシュします。
    
    ```bash
    git push origin main
    ```
    
