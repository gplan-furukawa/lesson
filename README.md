# lesson
勉強用サンプルリポジトリ

# memo
特に断りがない限り、ターミナルにはbashを使用します
参考
https://zenn.dev/praha/articles/db1c4bcc4ef48c

## まずClone
```
git clone https://github.com/gplan-furukawa/lesson.git
```

## cloneしたディレクトリに移動
cd コマンドを使って、自分がcloneしたディレクトリに移動

## 表示を確認
- [ ]  `（任意のディレクトリ）/lesson`ができていることを確認
- [ ]  ↑の右に（main）が表示されていることを確認　→今いるブランチ名です

## ブランチを作成
### GUIでやる場合
1. 左メニューの「ソース管理」のアイコンをクリック
1. 「ソース管理」にマウスオーバーしたときにあらわれる「**…**」をクリックし、「**ブランチ**」＞「**ブランチの作成**」の順にクリック
![image](https://github.com/user-attachments/assets/59ba31c9-df05-400b-8f98-2ddcc5cb85a1)
1. 画面上部にブランチ名入力欄が表示されるので、ブランチ名を入力してEnter
1. ターミナルで何も書かずにEnterすると（main）になっていたところが、作成したブランチ名になっている　→新規ブランチを作成してcheckoutした状態

### CUIでやる場合
1. ターミナルで以下のコマンドを打つ
   ```
   git checkout -b ブランチ名
   ```
1. （main）になっていたところが、作成したブランチ名になっている　→新規ブランチを作成し、checkoutした状態

## ファイルを追加
VSCodeのエクスプローラーからファイルを新規作成

cf) VSCodeでは以下をプラグインなしでできます
* Emmet（ZenCoding）
* ファイル整形 https://kakechimaru.com/vscode_alignment/
* diff表示（Gitのブランチの更新差分、Gitのコミットの差分、ファイルを指定しての差分）

## 作成したファイルをコミットしてリモートにPushする
### GUIでやる場合
1. 左メニューの「ソース管理」のアイコンをクリック
2. コミットしたいファイルにマウスカーソルをあわせ、表示された「＋」をクリック or 変更すべてをコミットしたい場合は「変更」にマウスカーソルを合わせたときに表示される「＋」をクリック
3. 「ステージされている変更」にファイルが追加されているのを確認（※SourceTreeでコミットするとき、左下の作業ツリーペインから、左上のステージペインに「すべてインデックスに追加」というのをやると思います、あの作業です）
4. コミットメッセージを入力して［**コミット**］ボタンをクリック
5. 「Branchの発行」をクリックするとリモートにpushされる
### CUIでやる場合
1. ターミナルで以下のコマンドを入力し、対象ファイルを確認
    ```
    git status
    ```
1. 以下のコマンドを入力し、ステージングに追加
    ```
    git add .
    ```
    cf) 「.」は現在のディレクトリ以下のファイルを全部追加の意味。特定のファイルだけコミットしたいときは、個別にファイルパスを指定することができる
1. コミットメッセージを入力してコミット
    ```
    git commit -m "コミットメッセージ"
    ```
1. ブランチをリモートにpushする（※SourceTreeだと「変更をすぐにPushするという」項目にチェックをしてコミットすると思いますが、あれはコミット＋pushを同時にしています）
    ```
    git push origin ブランチ名
    ```

## 入れとくと便利なVSCodeプラグイン
* Git Lens https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens
* Live Server https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer
