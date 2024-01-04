# git-practice
## 目的
ここはgitについてを学ぶ・実践するレポジトリです。
学んだ内容の記述や実践を行います。

## Intro  

* [Gitの知識入門](intro/overview.md)  
* [運用方法 Git(GitHub) Flow](intro/git-github_flow.md)  

## Practice  

Gitの操作を理解するためにリポジトリを複製する

### 実践環境の構築  

1. 任意のディレクトリへ移動  
   `cd project`  
2. 任意のディレクトリでフォルダーを新規作成  
   `mkdir work-a`  
3. 新規作成したフォルダーへ移動  
   `cd work-a`  
4. 当レポジトリをcloneし、レポジトリを複製する  
   `git clone <当レポジトリ>`  
5. はじめのディレクトリへ戻り、2~4の操作を再度行う  

   ```bash  
   git cd ../  
   git mkdir work-b  
   git clone <当レポジトリ>
   ```  
