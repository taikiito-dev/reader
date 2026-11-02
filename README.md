# reader

長い文章を貼ると、画面の幅でページに組み直して読めるようにする1枚のHTMLです。
メールマガジンや記事を、スクロールではなくページをめくる形で読むために作りました。

https://reader.taikiito.com

## できること

- 貼り付けた文章を、画面の幅に合わせて2ページの見開き（狭い画面では1ページ）に組む
- 矢印キー、スペース、画面の左右端のクリック、縦スクロールでページをめくる
- ハードラップされた改行をたたんで段落に戻す（メールマガジン向け。切り替え可能）
- 書体の選択（日本語5種、英語5種）、行間3段、字の大きさ、地の色4種
- 日本語と英語の2言語表示。ブラウザの言語で初期値が決まる
- 日本語の文章は両端揃えと字下げ、英語の文章は左揃えと段落間のアキで組む（自動判定）

## 扱うデータ

貼り付けた文章はブラウザの中だけで処理します。サーバーへの送信はありません。保存もしないので、
タブを閉じると消えます。サーバー側のコードはなく、`index.html` 1枚で動きます。

通信が発生するのは Google Fonts からの書体の取得だけです。書体の選択で「端末のフォント」を選ぶと、
外部への通信はゼロになります。

## ローカルで使う

`index.html` をダウンロードしてブラウザで開くだけです。ビルドもサーバーも不要です。

## 使っている書体

いずれも SIL Open Font License 1.1。

Noto Sans JP, Zen Kaku Gothic New, Noto Serif JP, Zen Old Mincho,
Inter, Literata, Source Serif 4, EB Garamond

## 書いた人

設計と仕様の判断は taikiito、コードは Claude (Anthropic) が書きました。

## License

MIT

# reader (English)

A single HTML file that re-sets a long pasted text into pages that fit your screen,
so you can read newsletters and articles by turning pages instead of scrolling.

https://reader.taikiito.com

## What it does

- Lays the pasted text into a two-page spread (one page on narrow screens)
- Turn pages with arrow keys, space, clicks on the left/right edge, or vertical scroll
- Unwraps hard-wrapped line breaks back into paragraphs (for newsletters; can be turned off)
- Font choice (5 Japanese, 5 Latin), three leading steps, text size, four paper colors
- Japanese and English interface, picked from your browser language
- Justified text with first-line indent for Japanese, ragged right with paragraph spacing for English

## Your text

The text is laid out inside your browser. Nothing is sent to a server and nothing is stored,
so it is gone when you close the tab. There is no server-side code: `index.html` is the whole app.

The only network request is to Google Fonts. Choose the system font option and there is none.

## Running it locally

Download `index.html` and open it in a browser. No build step, no server.

## Fonts

All under the SIL Open Font License 1.1.

Noto Sans JP, Zen Kaku Gothic New, Noto Serif JP, Zen Old Mincho,
Inter, Literata, Source Serif 4, EB Garamond

## Who wrote this

Design decisions by taikiito. The code was written by Claude (Anthropic).

## License

MIT
