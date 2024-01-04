## Gitってなに?  

```
Git（ギット）は、プログラムのソースコードなどの変更履歴を記録・追跡するための分散型バージョン管理システムである。
```  

* 分散型  
  各自のパソコン上でリポジトリを作成し、  
  任意のタイミングで任意のリポジトリに同期する

* GitとGitHub  
  Gitはツール  
  GitHubはサービス  

* Gitの特徴  
  * ファイルの変更の履歴が残る  
  * 履歴のある時点までのファイル内容を復元することが可能  
  * チーム開発の煩雑さをなくしてくれる

### Gitの用語
* repository リポジトリ  
  ファイルやデータ、ディレクトリの状態を保存する場所。  
  repositoryでは変更履歴が保存されている。  

* remote リモート  
  オンライン上にある皆がアクセスできる共通の場所。  
  * remote repository
    オンライン上の皆がアクセスできる`repository`　のこと  

* local ローカル  
  手元のパソコン  
  * local repository  
    手元のパソコン内にある`repository`のこと

* branch ブランチ  
  履歴の流れを分岐して記録していくもの。  
  分岐したブランチは他のブランチの影響を受けないため、同じ`repository`で複数の変更を同時に進めることができる。  

* fetch フェッチ  
  `remote repository`の最新内容を`local repository`に取り入れる操作。  
  **あくまで取り入れるだけ**  
  `local repository`の`branch`に変更を反映させるものではない。  
  * `git fetch`  
    `remote repository`のすべての変更を取得  
  * `git fetch <remote repository name>`  
    指定した`remote repository`のすべての変更を取得。  
  * `git fetch <remote repository name> <branch name>`  
    指定した`remote repository`の`branch`の変更を取得する  

* merge マージ  
  異なる`branch`で行われた変更を統合し、１つの`branch`にまとめる操作。  
  `fetch`で取り込まれた`remote repository`の変更を`local repository`の特定の`branch`に反映させる。  
  * `git merge <branch name>`  
    `local repository`の実行した`branch`へ変更を反映させる。  

* pull プル  
  `fetch`と`merge`を同時に行う操作。  
  * `git pull <remote repository name> <branch name>`  
  * `pull`と`fetch`の使い分け  
    `remote repository`の中身を確認したい場合→`fetch`  

* add アッド  
  変更したファイルをステージングする操作。  
  * staging ステージング  
    ファイルの変更をバージョン管理の対象にするための登録。  

* commit コミット  
  ステージングされた変更内容を`local repository`に反映させる操作。  
  ステージングされたファイルの変更内容は、`commit`時はまだ`local repository`に反映されていない。  
  * `git commit -m '<commit message>'`  
    コミットメッセージと共にステージングされている箇所をローカルリポ時とるへ反映。  
    **基本的にコミットメッセージは残すこと**  

* push プッシュ  
  `local repository`の内容を`remote repository`へ反映される。  

* conflict コンフリクト  
  異なるブランチやコミットで同じファイルの同じ箇所が編集され、Gitがそれを自動的に解決できない状態。  
  **表示されたときは、どちらかを選択しなければならない**  

:::note info
`<>`で挟まれた箇所は適宜変更してください。 　
:::

参照URL  
[11. Gitで管理](https://qiita.com/nuco_bk/items/27f5ad03d0c4b41241fc#11-git%E3%81%A7%E7%AE%A1%E7%90%86)  
[Git branch](https://the-turing-way.netlify.app/reproducible-research/vcs/vcs-git-branches.html)  
