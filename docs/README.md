# SKK について

SKKは日本語入力方式です。Simple Kana to Kanji conversion の頭文字から命名されました。

漢字に変換したい単語の頭文字のローマ字を大文字で入力し、単語の読みを入力し、スペースキーで変換します。複数の候補がある場合、スペースキーで候補を順に見ていけます。

`K a n j i space` → `漢字`

送り仮名がある場合は、漢字の一番初めのローマ字と送り仮名の初めのローマ字を大文字で入力します。複数の候補がある場合はスペースキーで候補を順に見ていけます。

`K a K u` → `書く`

変換したい候補が一つずつ表示されているうちに見つかったら、Returnで決定することも、そのまま文章の続きを書くこともできます。

`K a n j i space w o K a K u Return` → `漢字を書く`

このように文頭から順に単文節ずつ変換していく日本語入力方式です。

現在、オリジナルのSKKから発展したDDSKKが [SKK Openlab](http://openlab.ring.gr.jp/skk/index-j.html) で開発・メンテナンスされています。

# CSKK について

[CSKK](https://github.com/naokiri/cskk)はSKK方式の入力をIMEで可能にするためのライブラリです。

# Fcitx5-cskk について

[Fcitx5-cskk](https://github.com/naokiri/fcitx5-cskk)はFcitx5でCSKKライブラリを使うためのFcitx5のアドオンです。
