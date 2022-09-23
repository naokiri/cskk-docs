# cskk, fcitx5-cskkのインストール
ここではUbuntu 22.04を例としてインストール方法を紹介します。

## 前提パッケージ
いくつかの前提パッケージを次のようにインストールします。

LibCSKKの前提パッケージ

    sudo apt install libxkbcommon0 libc6

Fcitx5-cskkの前提パッケージ

    sudo apt install fcitx5
    

## 本体のインストール
debパッケージを各プロジェクトのリリースページからダウンロードします。

[CSKK](https://github.com/naokiri/cskk/releases)
[Fcitx5-cskk](https://github.com/naokiri/fcitx5-cskk/releases)

Assets内の.deb拡張子のパッケージをダウンロードして

    sudo dpkg -i libcskk_{バージョン}_amd64.deb
    sudo dpkg -i fcitx5-cskk_{バージョン}_amd64.deb

のコマンドでインストールできます。

# 辞書

辞書はSKKの辞書を利用することを想定しています。

## Linuxのディストリビューションからインストールする
多くのディストリビューションでskk辞書のパッケージが用意されています。
Debian (Ubuntu) では`skkdic`や`skkdic-extra`という名称のパッケージです。 

    sudo apt install skkdic skkdic-extra

でインストールされます。

## SKK Openlab のサイトからダウンロードする
SKK Openlabが辞書をgithubで公開しています。[辞書](https://skk-dev.github.io/dict/)ページから必要な辞書をダウンロードできます。

## 公開されている辞書をダウンロードする
[Github](https://github.com/search?q=SKK%E8%BE%9E%E6%9B%B8) などで多くの有志が目的に沿った辞書を公開しています。
