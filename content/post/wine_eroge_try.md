+++
title = "Wineでえっちげを遊ぶ方法"
date = "2018-03-15T20:21:13+09:00"
draft = false
description = ""
tags = []
categories = []
images = []
banner = ""
menu = ""
+++

~~えっちげのためにWindows買うのなんかなー、うーん。、と思ったので~~

ここを見て作業をしました。

[【微妙】HomebrewでWineを使う | cozy attic](https://cozyattic.wordpress.com/2015/02/16/homebrew%E3%81%A7wine%E3%82%92%E4%BD%BF%E3%81%86/)

## 1. Wineを入れる
brewで入れます。

```
$ brew install wine             
==> Downloading https://homebrew.bintray.com/bottles/wine-3.0.high_sierra.bottle
Already downloaded: /Users/mimikun/Library/Caches/Homebrew/wine-3.0.high_sierra.bottle.tar.gz
==> Pouring wine-3.0.high_sierra.bottle.tar.gz
==> Regenerating font cache, this may take a while
==> /usr/local/Cellar/wine/3.0/libexec/bin/fc-cache -frv
==> Caveats
You may want to get winetricks:
  brew install winetricks

By default Wine uses a native Mac driver. To switch to the X11 driver, use
regedit to set the "graphics" key under "HKCU/Software/Wine/Drivers" to
"x11" (or use winetricks).

For best results with X11, install the latest version of XQuartz:
  https://www.xquartz.org/
==> Summary
🍺  /usr/local/Cellar/wine/3.0: 8,643 files, 608.7MB
➜  ~ git:(master) ✗
```

## 2. winetricks インストール

なにか必要らしいので入れました。

```
$ brew install winetricks
==> Installing dependencies for winetricks: cabextract, p7zip, unrar
==> Installing winetricks dependency: cabextract
==> Downloading https://homebrew.bintray.com/bottles/cabextract-1.6.high_sierra.
######################################################################## 100.0%
==> Pouring cabextract-1.6.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/cabextract/1.6: 10 files, 135.7KB
==> Installing winetricks dependency: p7zip
==> Downloading https://homebrew.bintray.com/bottles/p7zip-16.02_1.high_sierra.b
######################################################################## 100.0%
==> Pouring p7zip-16.02_1.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/p7zip/16.02_1: 103 files, 4.7MB
==> Installing winetricks dependency: unrar
==> Downloading https://homebrew.bintray.com/bottles/unrar-5.6.1.high_sierra.bot
######################################################################## 100.0%
==> Pouring unrar-5.6.1.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/unrar/5.6.1: 6 files, 508.5KB
==> Installing winetricks
==> Downloading https://github.com/Winetricks/winetricks/archive/20180217.tar.gz
==> Downloading from https://codeload.github.com/Winetricks/winetricks/tar.gz/20
######################################################################## 100.0%
==> Caveats
winetricks is a set of utilities for wine, which is installed separately:
  brew install wine
==> Summary
🍺  /usr/local/Cellar/winetricks/20180217: 6 files, 731.9KB, built in 4 seconds
```

## 3. フォントを入れる
フォントを入れます。

```
$ winetricks allfonts
```
すると沢山ログが流れます。

結構時間かかるのでソシャゲでもして待ちましょう。

戦艦少女、少女前線、魔女兵器、とてもオススメです。

## 4. デフォルトロケールの設定
どちらか一方で良いらしいですが、僕は両方設定しておきました。

```
echo "export LANG=ja_JP.UTF-8" >> ~/.zshrc
echo "export LC_ALL=ja_JP.UTF-8" >> ~/.zshrc
```

## 5. 初期設定ファイルの置き換え

```
$ git clone https://github.com/mattintosh4/osx-wine-inf.git osx-wine-inf
$ wine rundll32 setupapi,InstallHinfSection DefaultInstall 128 ./osx-wine.inf
```

## 6. 使ってみる

```
wine hoge.exe
```

なお、起動しないものもあるらしいです。
