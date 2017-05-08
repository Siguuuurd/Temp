

7. masterブランチを右クリックして「リモートブランチを追跡」から「upstream/master」を選択します（これでfork元の変更が随時反映される）



### Pull Request



1. developブランチからdevelop_testブランチを作成します

2. develp_testブランチをチェックアウトした状態で作業を進めます

3. developブランチをチェックアウトしてから、develop_testブランチを右クリックして「現在のブランチにdevelop_testブランチをマージ」を選択します（作業内容がdevelopブランチに反映されました）

4. masterブランチを右クリックして「現在の変更をmasterにリベース」を選択します

5. developブランチでpushします（これがPull Requestの元になるブランチになります）

6. 自分のGitHubページから、Pull Requestしたいブランチを選択してから左にあるアイコンをクリックします

7. タイトルと説明を入力したら「Create pull request」ボタンをクリックします

8. Pull Requestがマージされてfork元が更新されたら、masterブランチにチェックアウトしてからpullします（これでfork元とmasterブランチは同じ状態になります）

9. developブランチにチェックアウトしてから、masterブランチとマージします



## GitHubのテクニック



### ショートカット

GitHubをブラウザで表示している時にキーボードの?を押すとその画面で使用できるショートカットが表示されます。



### Gist

GistはGitHubの機能の１つでコードを共有することができます。ディレクトリを作ることはできませんが、バージョン管理やシンタックスハイライト、シークレットモードや複数のファイルで保存することができます。



シークレットモードは検索エンジンにクロールされない、Gist一覧に表示されなくなる特徴があります。ただし、URLが分かれば見れてしまうので注意しましょう。



### ホワイトスペースの差分を表示しない

diffのURLの末尾に`?w=1`を付け足すとホワイトスペース（空白文字、タブ、改行文字）の差分を表示しなくなります。HTMLなどホワイトスペース（インデントなど）が頻繁に変更される言語で特に有効な機能です。



## .gitignoreファイルでバージョン管理しないファイルを指定する

OSが自動で作成するファイルなど、共有する必要のないファイルは.gitignoreというファイルをプロジェクトトップの階層に保存することで指定できます。



homebrew（ホームブリューまたはホームブルー）を使用している場合にはgiboという.gitignoreを自動で生成してくれるツールがあります。homebrewでgiboをインストールするには、



```bash

brew install gibo

```



以下のようにOSやエディタ名を入力します。



```bash

gibo OSX Windows SublineText Vim Emacs >> .gitignore

```



## 参考リンク

* [GitHub Cheat Sheet（日本語訳）](https://github.com/jposts/github-cheat-sheet)

* [Web制作者のためのGitHubの教科書](http://www.amazon.co.jp/Web%E5%88%B6%E4%BD%9C%E8%80%85%E3%81%AE%E3%81%9F%E3%82%81%E3%81%AEGitHub%E3%81%AE%E6%95%99%E7%A7%91%E6%9B%B8-%E3%83%81%E3%83%BC%E3%83%A0%E3%81%AE%E5%8A%B9%E7%8E%87%E3%82%92%E6%9C%80%E5%A4%A7%E5%8C%96%E3%81%99%E3%82%8B%E5%85%B1%E5%90%8C%E9%96%8B%E7%99%BA%E3%83%84%E3%83%BC%E3%83%AB-%E5%A1%A9%E8%B0%B7-%E5%95%93-ebook/dp/B00QPSXY1I/ref=sr_1_3?s=books&ie=UTF8&qid=1453903533&sr=1-3&keywords=github)