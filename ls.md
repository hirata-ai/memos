# ls コマンド打つときに除外するファイルを指定する
## --ignore オプション
`ls --ignore` で指定したファイルを除外できる．  
`ls app/ --ignore *.pyc` だと ~.pyc ファイルを除外できる．  
`ls app/ --ignore={*.pyc,__init__*}` のように{}で囲むと複数指定できる．

参考：http://takuya-1st.hatenablog.jp/entry/2014/05/23/045013
