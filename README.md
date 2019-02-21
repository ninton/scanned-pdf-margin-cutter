# scanned-pdf-margin-cutter (developing)

+ Ubuntu linux用、macos用のコマンドラインツールです。
+ Javascriptライブラリではありません。
+ 本をスキャンしたPDFの余白を削除します。
+ 表紙は、余白カットではなく、縮小します。
+ 中身は、左綴じ、右綴じ、奇数ページ、偶数ページを考慮して、左右の余白を計算して、カットします。

## 必要なもの

+ ImageMagick
+ GhostScript
+ PDFTK

### Ubuntu

    $ sudo apt install imagemagick
    $ sudo apt install ghostscript
    $ sudo apt install pdftk

### macos

    $ brew install imagemagick
    $ brew install ghostscript
    $
    $ wget https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/pdftk_server-2.02-mac_osx-10.11-setup.pkg
    $ open pdftk_server-2.02-mac_osx-10.11-setup.pkg

## インストール

    $ npm install -g scanned-pdf-margin-cutter

## 使い方

表紙をスキャンして、pdfに保存します。front.pdfとします。

中身をスキャンして、pdfに保存します。body.pdfとします。

    $ spmc-main-prompt
    表示pdf(ないときはENTER):front.pdf
    本文pdf:body.pdf
    左綴じ(Yes|no)[Yes]:
    上余白(mm)[0]:14
    右余白(mm)[0]:10
    幅(mm):155
    高さ(mm):233
    表示pdf   : front.pdf
    本体df    : body.pdf
    左綴じ    : 1
    上余白(mm): 14
    右余白(mm): 10
    幅(mm)    : 155
    高さ(mm)  : 233
    OK(yes/no)[yes]
