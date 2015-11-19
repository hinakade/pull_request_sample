# pull_request_sample

hogehoge

##pullの流れ
1 リモートリポジトリをローカルより育てる
2 `git pull origin master`コマンドでリモート上の最新リポジトリをローカルに持ってくる。

## Pull Request のk流れ
1 `git checkout -b ブランチ名`コマンドで新規ブランチを作成（同時にブランチの切り替えも行ってくれる）
2 何かしらのアップデートをする
3 `git add.`,``git commit -m"コメント"の順で保存する
4 `git push origin 新しいブランチ名`コマンドでリモート上に新しくブランチを作成してpush important
5 Github上でpul request を送る
6 管理者がrequestをレビューする
7 問題があれば差し戻す (コメントを自由に付けられる)
8 再度問題を修正し、`add`,`commit`,`push`で修正内容をpull reqに上乗せして送る
    + pull req中に同じブランチに修正内容をpushすると、それだけで修正内容がpull reqに乗っかる
9 修正内容を確認しmergeする 結構大事 
10 ブランチの削除
### ブランチの切り替え方
+`git checkout`ブランチ名` コマンドでブランチを行き来きできる
  +現在いるブランチ上で何かしらの変更を行っていた場合はその変更内容を保存内容くぉ保存もしくは削除してからブランチを移動すること

###commitコメントの修正
+`git commit --amend -m`"新規コメント"コマンドで編集可能

###指定したcommitまでコードを遡る方法
1 github上(もしくはlog上)でコミットハッシュをコピー
2 
3 

