# Mautic ドキュメンテーション

### イントロダクション
本文書はオープソースのマーケティング自動化システムである[Mautic のドキュメンテーション](https://www.mautic.org/docs/index.html)を担うものです。コードはオープソースであり誰でも入手が可能です。この文書もまたオープンソースです｡本情報に改善が必要であると考える方々の支援をお待ちしています。

### PDF 版をダウンロード
[このリンクをクリックして](https://mautic.org/docs/mautic_docs_jp.pdf) PDF 版をダウンロードしてください｡

### ドキュメンテーションの編集について
このレポジトリは [Gitbook](https://www.gitbook.com/) 向けのソースコードで [www.mautic.org/docs](https://www.mautic.org/docs/index.html) 上で公開されます。ソースコードは GitHub 上で共有されており，Mautic のコードをプログラマが編集するのと同じように誰でも編集が可能となっています。

#### 本文書の管理に Git を使う理由

- *バージョン*. 誰でも過去の版へアクセスができ，どのようなテキストだったか確認ができるため。
- *原著者*. 著者は各ファイルだけでなく一行一行に存在するため。.
- *コミュニティへのアシスト*. 同一文書内の誰かの文章を削除をしてしまう恐れが無いため。

クローン,変更，コミット，そして変更内容をプッシュするには Git に関するいくばくかの知識が必要です。GitHub のウェブインターフェイス上でファイルを直接変更しないようにする方法があります。すでに Git を使っている場合は好みのワークフローを使ってください｡まだ Git を使っていない場合は以下のガイドで Git を使って簡単に編集作業へ参加する方法を紹介します。

#### ブラウザ上でドキュメントを編集する

1. あなたのアカウントにあるこのレポジトリには編集権限がまだありませんので最初に[フォーク](https://github.com/mautic/documentation#fork-destination-box) してください。
2. 編集したいファイルを選択してください。選択するとファイル構造が下の方に表示されます｡ファイルの中身がどのようになっているかを確認するためにまず *README.md* ファイルをクリックして編集してみましょう。
3. *README.md* の中身が表示されます。上の方には鉛筆アイコンの *Edit* ボタンも表示されます。このボタンをクリックしましょう。
4. コンテンツは [Markdown フォーマット](https://daringfireball.net/projects/markdown/) で書かれています｡. とても簡単なテキストベースのフォーマットです｡
5. ファイルに変更を加えてください｡たとえば末尾に`これが最初の貢献`と加えるのもいいでしょう｡
6. 変更を加えたときにはページをスクロールして *変更内容をコミットする*というフォームを使って変更したことを伝えてください。変更をした旨を伝えることはとても重要です｡変更を保存しするには何を変更したのかそしてなぜ変更したのかを伝えなくてはなりません。たとえば `テストのために一行を追加した` と入力してください｡入力だけで保存はまだしないでください！
7. GitHub のウェブインターフェイスは Git の一部の機能を提供していないため，ファイルを元の状態へ復元する簡単な方法が無いのです｡復元するにはファイルへ追加された行を削除する別のコミットを作らなくてはなりません。これではコミットの履歴を汚してしまうことになります。コミット履歴を汚す代わりに新しいブランチを作りましょう。そのために"新規ブランチを作成する..."というチェックボックスがあります。ブランチには名前を付けなくてはなりません。`{あなたのユーザ名}-patch-1` とすでに入力されているでしょう｡これを`{あなたのユーザ名}-test` と変更しましょう。変更したら *ファイルの変更を申請する*をクリックしてください｡
8. あなたのレポジトリへは変更がすぐに反映されます。公式のレポジトリへ変更を申請するにはプルリクエスト(PR) を送らなくてはなりません。すでにプルリクエストのページへリダイレクトされているはずです。申請した変更内容を書き加えて *プルリクエストを作成する*をクリックしてください。テストのプルリクエストは送らないでください｡

テストの後にブランチをクリーンにするには *ブランチ* セクションへ移動しテストブランチを削除してください｡

#### ファイル構造について

前セクションでは *README.md* ファイルについて作業をしました。このファイルは GitHub レポジトリのホームページに表示されているのですぐに内容を読めるでしょう。Mautic のドキュメンテーションにかんする内容は書かれていません｡

*SUMMARY.md* ファイルはドキュメンテーションの目次を定義しています。ドキュメンテーションへ新しくページを追加する場合はタイトルとリンクをこのファイルへ定義しなくてはなりません。現在のメニューにある項目へ追加するためのとても単純な方法です｡

フォルダーは同じトピックをひとまとめにしたものです｡ *アセット*フォルダを開いてみてください｡アセット用の *README.md* がでてきます。このファイルはアセットメニューをクリックした際に表示されるコンテンツです｡ *manage_assets.md*ファイルがサブファイルです｡*メディア* サブフォルダへ *md* ファイルで使われている画像をまとめます。

#### リンク

他の場所にあるドキュメントへリンクを張りたい場合がよくあると思います｡ Markdown フォーマットではリンクはこのように表示されます:

```
[リンクのタイトル](http://example.com)
```

これは絶対 URL を使った外部サイトへのリンクを貼る方法です。ドキュメント内部へのリンクを張るには相対リンクを使います:

```
[次のステップ](./../plugins/integration_test.html)
```
このリンクは *md* ソースファイルから生成される ドキュメンテーションのウェブサイト内の `plugins/integration_test.html` へのリンクが作成されます。

#### 画像

上でも書いたように画像はメディアサブフォルダへ入れてください｡画像は GitHub ウェブインターフェイス上からはアップロードできないので，パブリックな URL へアップロードしてそこへのリンクを貼ってください｡

```
![画像のオルタナティブテキストを入力](http://example.com/images/apple.png "画像のツールチップテキストを入力")
```
またはドキュメンテーションのレポジトリへアップロード済みの画像を表示させたい場合は相対パスを使うこともできます: 

```
![画像のオルタナティブテキストを入力](/assets/media/assets-newcategory.png "画像のツールチップテキストを入力")
```
