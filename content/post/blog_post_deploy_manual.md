+++
title = "ブログの記事をデプロイする方法のメモ"
date = "2018-02-26T23:28:49+09:00"
draft = false
description = ""
tags = []
categories = ["未分類"]
images = []
banner = ""
menu = ""
+++

自分でも良く忘れるのでメモとして書いておきます。

#### 1. 記事作成

```
$ hugo new post/hogehoge_fugafuga.md
```

#### 2. draft = false

```
+++
title = "hogehoge_fugafuga"
date = "2018-02-20T11:45:14+09:00"
- draft = true
+ draft = false
description = ""
tags = []
categories = []
images = []
banner = ""
menu = ""
+++
```

#### 3. `hugo server -D` でプレビューする

[localhost:1313](http://localhost:1313/blog/)へアクセス

この内容でいいか調べます。

#### 4. 変更をadd, commit, pushする

#### 5. commit-gh-pages-files.sh を実行する

#### 6. git push origin gh-pages する