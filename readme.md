- 「データサイエンティスト協会スキル定義委員」の「データサイエンス100本ノック（構造化データ加工編）」を行い、その結果を記録する
- もともとあった.gitは削除して新たに.gitを作成し、自身がどのようなコードを書いたか記録した
# 運用方法
- ipynbはjupyter labでいじる
- 
# 起動方法
- `docker-compose up -d`
    - dオプションはつけるとログが出なくなる
- `http://localhost:8888/lab/tree/work`にアクセス
    - jupyter labが立ち上がるためそこで作業する

# もともと入っていたgit関連のjupyter lab拡張機能
- jupyterlab-git
    - guiでコミットができる
- nbdime-jupyterlab
    - gitのdiffをわかりやすく表示
# その他
- 100knocks_guide.pdfに使い方などが書いてある
    - 現在のdockerコマンドとは異なるコマンドが書いてある
- jupyter-labで開いたときにはdocker/work,docker/docディレクトリだけが表示されるため、他のディレクトリを見たり編集する際は他のエディターを使うほうがスマート
- sqlを実行する場合1つ目のセルはコンテナ起動時は毎回実行したほうがいい
- jupyter-labではFile Browserがどの階層に入るかでカレントディレクトリが決まり、そこで.gitの判別を行っている
    - そのためデフォルトではworkフォルダでgitの初期化が行われやすい状態になっている
    -  2つのPCで作業する場合だと変えた方が良い
# やりたいこと
- githubのパブリックリポジトリで管理したい
- 出先のpcでも行えるようにworkフォルダだけではなく、全てを管理したい
- git hub, vscodeで差分を見やすいように管理したい
- 「jupyterが開くディレクトリ!=.gitがあるディレクトリ」のため、そこの解決も図りたい
- work用とそれ以外でリポジトリを2つ作成したくない
- jupyterlab + jupytextで生成したpyファイルを管理 or nbstripoutでipynbの出力を削除し管理
