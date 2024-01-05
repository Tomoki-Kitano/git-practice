# 高度なヒント

## merge vs rebase

> git rebase コマンドは、初心者は避けるべき Git の魔法の呪文であるという評判を得ていますが、実際には、慎重に使用すれば開発チームの作業を非常に容易にしてくれます。  
> この記事では、git rebase を関連する git merge コマンドと比較し、典型的な Git ワークフローにリベースを組み込める可能性のあるすべての機会を特定します。  

`reabase`, `merge`ともに変更を１つのブランチから別のブランチを統合することを目的としている。  

* 用途  
  チーム開発では以下の状況が発生しうる  
  1. `main branch`から`feature branch`を作成
  2. `main branch`がチームメンバーによって新しいコミットで更新される  
  `main branch`の新しいコミットを自分の`feature branch`へ取り込む方法に`merge`, `rebase`の２つのオプションがある  

* The merge option  
最も簡単なオプションは、次のようなコマンドを使用して`main branch`を`feature branch`にマージすること  

```git
git checkout feature
git merge main
```  

または、`main branch`へ履歴の線を一本の直線にすることが以下のコマンドで可能です  
`git merge feature main`  
上記のコマンドにより、`feature branch`に両方のブランチを連結するマージコミットを作成する  

* The rebase option  
`rebase`は次のようにすることで  
`feature branch`を`main branch`にリベースできる  

```git
git checkout feature
git rebase main
```  

上記により、  
`feature branch`全体が`main branch`の先端から開始される  
新しいコミットのすべてを効率的に**マスター**に組み込む。  

* `rebase`のメリット  
  プロジェクト履歴がすっきりすること  \
  `rebase`によって履歴は完全に一直線になる  
  `feature`の先端からプロジェクトの開始までずっとフォークなしに辿ることが可能  

* `rebase`のデメリット  
  TBO  

* `rebase`の黄金律  
  `rebase`において実行してはいけないことがある  

## reset, checkout & revert

## 高度なGit log

## Git prune

## 参照URL  

[Merging vs. rebasing](https://www.atlassian.com/ja/git/tutorials/merging-vs-rebasing)  
[Resetting, checking out & reverting](https://www.atlassian.com/ja/git/tutorials/resetting-checking-out-and-reverting)  
[高度な Git ログ](https://www.atlassian.com/ja/git/tutorials/git-log)  
[Git prune](https://www.atlassian.com/ja/git/tutorials/git-prune)
