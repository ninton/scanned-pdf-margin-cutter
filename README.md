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


    $ spmc-main front.pdf body.pdf 1 1594 2126 177 236

    $ spmc-main 表紙pdf 本体pdf 左綴じ 幅　高さ　上余白 綴じていない側の余白

    左綴じ: 1=左綴じ、0=右綴じ
    幅: ピクセル数、15mmなら15 / 25.4 x 300dpi = 177ピクセル
    高さ: ピクセル数、180mmなら、180 / 25.4 x 300dpi = 2126ピクセル

    綴じていない側の余白: ピクセル数、15mmなら、180 / 25.4 x 300dpi = 177ピクセル

    上の余白: ピクセル数、20mmなら、180 / 25.4 x 300dpi = 236ピクセル
