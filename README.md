# oto2lab

setParamで歌唱ラベリングするための、UST→INI→LAB 変換ソフト。

## 目的

UTAUにおける既存インフラとノウハウの流用で、歌唱DBの充実を図る。

## 開発環境

-   Windows 10
-   Python 3.8

## 手順（全体）

1.  歌って WAV ファイルにする。
2.  UST を作る。
3.  WAV の歌い出しタイミングをUSTに揃える。
4.  oto2lab で UST を INI に変換する。
5.  INI を setParam で編集して保存する。
6.  oto2lab で LAB に変換する。
7.  完成

## oto2lab 利用作手順

### SetParamでのパラメータ設定

ラベル変換目的のため、UTAUの原音設定とは違う使い方をします。  
以下のように設定してください。

<u>**※v2.0.0から仕様が変わりました。**</u>

-   左ブランク　　 :  不使用
-   オーバーラップ :  **子音** 開始位置（1音素の場合は不使用）
-   先行発声　　　 :  **母音** 開始位置（3音素の場合は2音素目開始位置）
-   子音部固定範囲 :  不使用（3音素の場合のみ、3音素目開始位置）
-   右ブランク　　 :  不使用

### 本ツールの使い方

1. oto2lab.exe または oto2labGUI.exe をダブルクリックして起動
1. 表示に従ってモード選択
1. 表示されている画面に処理したいファイルをドラッグ＆ドロップ
1. 処理したいファイルの隣に変換後のファイルができます。

---

© 2020 oatsu, Haruqa  
© 2001-2020 Python Software Foundation
