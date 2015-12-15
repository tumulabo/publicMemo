# git

## How to use

### パーミッションの変更を無視する

git config core.filemode false

Git でファイルパーミッションの変更（chmod）を無視する - git config core.filemode false « をぶろぐ http://tetsuwo.tumblr.com/post/36066698390/git-chmod-git-config

### Proxy
proxyを適用させる場合は下記コマンドを実行し~/.gitconfigに設定を追加する
    $ git config --global http.proxy http://proxy.example.com:8080
    $ git config --global https.proxy http://proxy.example.com:8080

Linuxのkernel source codeなどをcloseする場合はgitスキームとなっているため、下記のスキーム変換を追加する。
    $ git clone git://github.com/joyent/node.git

### 空白文字・空白行を無視する

    $ git diff -w -B
    -w: スペースの変更を無視する, -B 空行を無視する

### 過去のバージョンに一部分だけを戻す

```
$ git checkout BASE ./sample.file
$ git add -i ./sample.file
    patch でsample.fileを選択
patch モードで元に戻す部分だけをyで追加する
$ git commit -m "reverge BASE for sample.file" 
    上記patchの変更のみを反映
$ git reset HEAD --hard ./sample.file
    不要な変更部分は元に戻す
```

## References
* いつか見た惑星: プロキシ環境下でgitを使う http://sushichop.blogspot.jp/2013/09/git.html
