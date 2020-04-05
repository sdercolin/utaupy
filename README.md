# oto2lab

setParamで歌唱ラベリングするための、UST→INI→LAB 変換ソフト。

## 目的

UTAUにおける既存インフラとノウハウの流用で、歌唱DBの充実を図る。

## 注意事項
- 「japanese.table」 を[きりたん歌唱DB](https://zunko.jp/kiridev/login.php)からお借りしています。
- バージョンアップでスクリプト名が変わることがあるのでご注意ください。

## 開発環境

-   Windows 10
-   Python 3.8

## 手順（全体）

1.  歌って WAV ファイルにする。
2.  UST を作る。
3.  WAV の歌い出しタイミングをUSTに揃える。
4.  本ツールで UST を INI に変換する。
5.  INI を setParam で編集して保存する。
6.  本ツールで LAB に変換する。
7.  完成

## 手順（詳細）

### SetParamでのパラメータ設定

ラベル変換目的のため、UTAUの原音設定とは違う使い方をします。  
以下のように設定してください。

-   左ブランク: 不使用
-   オーバーラップ: 発声開始位置
-   先行発声: 子音と母音の切れ目
-   固定範囲: 不使用（3音素から構成される場合のみ、2音めと3音めの境界）
-   右ブランク: 不使用

### 本ツールの使い方

1. oto2lab.exe をダブルクリックして起動
1. 表示に従ってモード選択
1. 表示されている画面に処理したいファイルをドラッグ＆ドロップ
1. 処理したいファイルの隣に変換後のファイルができます。
