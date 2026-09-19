# 見出し語入力トリガーの設定

標準的なSKKでは大文字のA〜Zが見出し語入力状態（▽モード）へのトリガーキーです。
CSKKではこのトリガーセットをルールファイルで自由に設定できます。

## ルールファイルでの設定

ルールファイルの`[options]`セクションに`composition_triggers`配列を追加します。

```toml
[metadata]
name = "default"
description = "My typing rule"

[options]
composition_triggers = [
    "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M",
    "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"
]

[conversion]
a = ["", "あ"]
# ...
```

キーシム名はxkbcommonの名称に従います（`[command]`セクションのキーバインド指定と同じ）。
`composition_triggers`を省略した場合は空のリストとして扱われます。

## 記号キーをトリガーに追加する

`Shift+1`（キーシム`exclam`）で見出し語入力状態に入り`！`を挿入したい場合は次のように設定します。

```toml
[options]
composition_triggers = [
    "A", "B", "C", ..., "Z",
    "exclam"
]

[conversion]
exclam = ["", "！"]
```

トリガーに指定したキーシムに対応する`[conversion]`エントリも必要です。

## 注意事項

- 範囲指定はできません。各キーシム名を個別に列挙してください（`"A-Z"`のような省略記法はありません）。
- `Shift+1`でも専用の`!`キーでも同一のキーシム`exclam`として扱われます。
