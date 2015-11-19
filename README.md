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

### ブランチの切り替え方
+`git checkout`ブランチ名` コマンドでブランチを行き来きできる
  +現在いる
