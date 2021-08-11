MathJax のメモ
============

Web ページで数式を表示できる MathJax の使い方のメモ．
ついでに知らない言葉も調べた．

- https://www.mathjax.org

使い方
-----

とりあえず使ってみるには

- https://docs.mathjax.org/en/latest/web/start.html

の指示に従う．

MathJax　はコンポーネントと呼ばれる個々の部品に分割されていて，必要なものだけを読み込んで利用できる．
入力を TeX，出力を CommonHTML にするときは，`<head>` に

```html
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js">
</script>
```

と書くことで，MathJax 3.x.x の最新版が読み込まれる．
その他のコンポーネントは https://docs.mathjax.org/en/latest/web/components/combined.html を見よ．

IE のような時代遅れのブラウザでも表示できるようにするには MathJax の読み込みの前に

```html
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
```

を追加する．



おまけ
----

| 概念		| 参考 |
| ---- 		| ---- |
| CDN		| https://developer.mozilla.org/ja/docs/Glossary/CDN |
| CommonHTML |  |
| Polyfill  | https://remysharp.com/2010/10/08/what-is-a-polyfill |