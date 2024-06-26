## インストール  
* 現場へ参画する際には**必ず**どのようなGit運用ルールなのか確認をする  
* Git/GitHub flowは厳格な規則ではない  
開発現場によっては多少の差異は起こりえる  
* 多くの開発現場では**GitHub Flowで十分**  
Git Flowの運用は5つのブランチがあり、複雑になりがちなため  

### 代表的なGit Flow  

#### 5つのブランチ  

##### メインブランチ  
* master  
リリース済みのソースコードを管理する  

* develop  
開発中のソースコードを管理する  

##### サポートブランチ  
* feature  
機能実装やバグ修正などの開発作業を行う  
** 分岐元  
develop
** マージ先  
develop

* release  
リリース準備作業を行う
** 分岐元  
develop
** マージ先  
develop/master

* hotfix  
緊急の修正作業を行う
** 分岐元  
master
** マージ先  
develop/master

#### 開発例

1. masterブランチを作成  
1. masterブランチからdevelopブランチを作成  
1. 機能実装
   1. 機能実装を開始する  
      1. developブランチからfeatureブランチを作成する  
      2. 機能実装を開始  
コミットはfeatureブランチに対して行う
   1. 機能実装を完了する  
      1. featureブランチでの作業が完了させる  
      2. featureブランチをdevelopブランチへマージする  
      3. マージ完了後にfeatureブランチを削除する  
1. リリース  
   1. リリース準備を開始する  
      1. 機能実装が終わりリリースできる状態にする  
      2. developブランチからreleaseブランチを作成する  
      3. バージョン番号やドキュメントの更新などのリリース準備作業を行う  
   2. リリース準備を完了する  
      1. releaseブランチでの作業を完了させる  
      2. releaseブランチをmasterとdevelopブランチにマージする  
      3. マージ完了後、リリースブランチを削除する  
      4. 緊急の修正作業  
   3. 緊急の修正作業を開始する  
リリース後に緊急の修正作業が発生した場合  
      1. masterブランチからhotfixブランチを作成する  
      2. 修正作業を行う  
   1. 緊急の修正作業を完了する  
      1. hotfixブランチでの作業を完了させる  
      2. hotfixブランチをmaseterとdevelopブランチへマージさせる  
      3. マージ完了後にhotfixブランチを削除する  

### 代表的なGitHub Flow  
#### 6つのルール  
1. masterブランチは常にデプロイ可能である
1. 作業ブランチをmasterから作成する
1. 作業用ブランチを定期的にプッシュする
1. プルリクエストを活用する
1. プルリクエストが承認されたらmasterへマージする
1. maseterへのマージが完了したら直ちにデプロイを行う

#### 開発例

1. 開発作業を行う  
   1. 作業開始時に作業用ブランチをmasterブランチから作成する  
   2. GitHub Flowではすべてのブランチから作成する  

2. プルリクエストを行う  
   1. 作業ブランチをmasterブランチへマージできる状態になる
   2. プルリクエストを作成して他の開発者にコードレビューを依頼する
   3. プルリクエストが承認されたらmasterへマージする  

3. デプロイする  
   1. masterへのマージが完了したら直ちにデプロイをする


参照URL  
[【図解】git-flow、GitHub Flowを開発現場で使い始めるためにこれだけは覚えておこう](https://atmarkit1.itmedia1.co1.jp/ait/articles/1708/01/news0151.html#02)   
[【Git基礎】Git学習ロードマップ](https://zenn1.dev/mukkun69n/articles/81e9d29d644aa0)  