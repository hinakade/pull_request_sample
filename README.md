pull request の練習リポジトリ
GithubのREADMEファイルはGithubマークダウン記法を使って記述する。 markdownで行こう

git -> Githubへのpush(流れ)

ローカル上でディレクトリ作成(プロジェクト)
ディレクトリ内でgit init コマンドを使い初期化
何かしらの作成 or 編集
git add ファイル名コマンドで更新したものをステージングエリアに上げる
git commit -m "コメント"コマンドで変更を保存する
Github上でリモートリポジトリを作成
git remote add と git pushのコマンドをコピー
git remote add origin githubのURLコマンドでローカルとリモートを接続
git push -u origin masterコマンドで保存したソースコードをリモートへ送る
pullの流れ

リモートリポジトリをローカルより育てる
git pull origin masterコマンドでリモート上の最新リポジトリをローカルに持ってくる
Pull Requestの流れ

git checkout -b ブランチ名コマンドで新規ブランチを作成(同時にブランチの切り替えも行ってくれる)
なにかしらのアップデートをする
git add .git commit -m "コメント"の順で保存する
git push origin 新しいブランチ名コマンドでリモート上に新しくブランチを作成してpush
Github上でpull requestを送る
管理者がrequestをレビューする
問題があれば差し戻す（コメントを自由に付けられる）
再度問題を修正し、add、commit、pushで修正内容をpull reqに上乗せして送る +pull req中に同じブランチに修正内容をpushすると、それだけで修正内容がpull reqに乗っかる
修正内容を確認し、mergeする
ブランチを削除する
ブランチの切り替え方

git checkout ブランチ名 コマンドでブランチを行き来出来る
現在いるブランチ上で何かしらの変更を行っていた場合はその変更内容を保存もしくは削除してからブランチを移動すること
commitコメントの修正

git commit --amend -m "新規コメント"コマンドで編集可能
指定したコミットまでコードを遡る方法

Github上（もしくはlog上）でコミットのハッシュをコピー
git checkout ハッシュコマンドで指定したコミットまで戻る
git checkout ブランチ名コマンドで最新のコミットに戻る
別ブランチのコミットをmasterブランチへ追加する方法

別ブランチでの変更をcommitしきる
git log --onelineでコミットのハッシュを見る
git checkout master でmasterブランチへ移動
git cherry-pick ハッシュで別ブランチのコミットをmasterへ追加
ローカルブランチの削除

'git branch -d ブランチ名'
もしerror: The branch 'ブランチ名' is not fully merged.が出れば、
git branch -D ブランチ名で強制削除も可能

