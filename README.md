# SekireiTools

物性研共同利用スパコンシステムB (sekirei) のためのツールです。

## `qnodes`
現在動いているジョブの一覧およびキューごとの使用中ノードの数を、
通常キュー(F)、長時間キュー(L)、バックグラウンドキュー(L) の区別なく表示します。

たとえば `qnodes small` とすると、 `F4cpu`, `L4cpu`, `B4cpu` キューで動いているジョブおよび専有ノードの合計数が表示されます。
`qnodes` と実行すると、有効な引数の一覧が出力されるので、適当なキューを選んで再度実行してください。

## `myjobs`
自分の投入したジョブの一覧を表示します。
最終列は、ステータスが `R` の場合には実行時間を、
ステータスが `Q` （実行待ち）の場合には実行開始予想時刻を表示します。

ユーザ名を空白区切りもしくは改行区切りで列挙して記入したファイルを、
`myjobs` と同じディレクトリに `users.txt` という名前でおいておくと、
複数ユーザについてジョブ状況を確認できます。

## `touch.sh`
ユーザの `/work` 領域にある全てのファイルのうち、最終更新が1週間以上前のファイルのタイムスタンプを更新します。

## ライセンス
Copyright: Yuichi Motoyama y-motoyama@issp.u-tokyo.ac.jp

`utconv` を除き、[Boost Software License Version 1.0](http://www.boost.org/LICENSE_1_0.txt) の元で公開しています。
`utconv` は[パブリックドメインにて公開されているもの](https://github.com/ShellShoccar-jpn/misc-tools)を再配布しています。
