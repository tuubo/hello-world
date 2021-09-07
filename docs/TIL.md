## HTML

<details>
  <summary>aria-hidden 属性</summary>
  <div>

- `aria-hidden="true"` を設定することで、視覚的に非表示になっていないコンテンツを支援技術から外すことができる
- Modal の裏で表示されているコンテンツなどに適用することがある
- 表示すべきコンテンツも含んでしまうため、 `aria-hidden="true"` を `<body>` に指定することは推奨されない

参考 URL：

- [コンテンツの非表示と更新 | Web | Google Developers](https://developers.google.com/web/fundamentals/accessibility/semantics-aria/hiding-and-updating-content?hl=ja#aria-hidden)
- [[aria-hidden="true"] is present on the document<body></body>](https://web.dev/aria-hidden-body/)

  </div>
</details>

<details>
  <summary>スター実装テクニック（SVG）</summary>
  <div>

- アクセシビリティのため、aria-hidden 属性で評価に関する情報を含める
- `<symbol id="name">`, `<use href="#name">` 要素で SVG パスデータの再利用が可能
- `<mask>` を利用して、半透明スターを表現可能

参考 URL：

- [これから実装する人にオススメ！レイティングに使用するスター（星形）を実装する SVG のテクニック | コリス](https://coliss.com/articles/build-websites/operation/work/star-rating-svg-solution.html)

  </div>
</details>

## CSS

<details>
  <summary>インラインブロックで画像の位置を揃える</summary>
  <div>

- `vertical-align` のデフォルト値は `baseline`
- `display: inline-block` で画像を含むコンテンツと文字を含むコンテンツを並べると、画像の下端と文字の下端が揃うように並び、見た目上ずれが発生する

参考 URL：

- [css – インラインブロックを並べて画像を表示するとずれてしまう | memorandum-plus](http://memorandum-plus.com/2018/04/04/css-%E3%82%A4%E3%83%B3%E3%83%A9%E3%82%A4%E3%83%B3%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E3%82%92%E4%B8%A6%E3%81%B9%E3%81%A6%E7%94%BB%E5%83%8F%E3%82%92%E8%A1%A8%E7%A4%BA%E3%81%99%E3%82%8B%E3%81%A8/)

  </div>
</details>

<details>
  <summary>CSS設計：ITCSS</summary>
  <div>

- ITCSS：詳細度によって階層（レイヤー）を分けて CSS を管理する設計手法
- クラス名の命名ルールはない

参考 URL：

- [ITCSS を採用して共同開発しやすい CSS 設計を ZOZOTOWN に導入した話 - ZOZO Technologies TECH BLOG](https://techblog.zozo.com/entry/itcss-to-zozotown)

  </div>
</details>

<details>
  <summary>Atomic DesignとCSS設計</summary>
  <div>

- Atomic Design：UI 設計の考え方で、ページを Atoms（原子）の集まりと考える
- Atoms（原子） < Molecules（分子） < Organisms（有機体） < Templates（テンプレート） <div Pages（ページ）のように UI を階層構造で捉える

参考 URL：

- [Atomic Design と CSS 設計 | 第 1 回 Atomic Design とは何か | CodeGrid](https://www.codegrid.net/articles/2017-atomic-design-1/)

  </div>
</details>

## JavaScript

<details>
  <summary>Next.js</summary>
  <div>

- `npx create-next-app` or `yarn create next-app` で Next.js アプリが簡単に作成できる
- pages ディレクトリの構成と対応する形でページが作成される

参考 URL：

- [はじめに | Next.js](https://nextjs-ja-translation-docs.vercel.app/docs/getting-started)

  </div>
</details>

<details>
  <summary>window オブジェクト</summary>
  <div>

- window は画面の DOM 全体を収める：画面内の要素はなんでもアクセスできる
- window はスクリプトを実行するウィンドウ：グローバル変数は window の変数として定義される。script で定義される内容はグローバル変数として定義される？
- window は省略して書くことが可能：`window.document` も `document` も同じ

参考 URL：

- [Window - Web API | MDN](https://developer.mozilla.org/ja/docs/Web/API/Window)
- [【JavaScript】Window オブジェクトって結局何なの...?](https://tektektech.com/what-is-window-object/)

  </div>
</details>

## Storybook

<details>
  <summary>Story rendering</summary>
  <div>

- `.storybook/preview-head.html` を使えば、iframe の書き換えが可能？（調査中）

参考 URL：

- [Story rendering](https://storybook.js.org/docs/react/configure/story-rendering#adding-to-head/)

  </div>
</details>

<details>
  <summary>Theme switcher Addon</summary>
  <div>

- Storybook のテーマの切り替え（任意の要素のクラスの切り替え）ができる

参考 URL：

- [Theme switcher Addon | Storybook](https://storybook.js.org/addons/storybook-addon-themes)

  </div>
</details>

<details>
  <summary>Storybook deployer Addon</summary>
  <div>

- Storybook を github pages や S3 に簡単にデプロイできるようになる
- オプションで細かい指定も可能（現在はデプロイ時のディレクトリ名のみ指定している）

参考 URL：

- [Storybook Deployer](https://github.com/storybookjs/storybook-deployer)

  </div>
</details>

## Git

<details>
  <summary>Git のチェリーピック</summary>
  <div>

- 任意のコミットだけを別のブランチに適用することができる

参考 URL：

- [Git のチェリーピック | Atlassian Git Tutorial](https://www.atlassian.com/ja/git/tutorials/cherry-pick)
※分かりやすいサイトがあれば更新したい

  </div>
</details>

<details>
  <summary>revert</summary>
  <div>

- 特定のコミットを打ち消すことができる
- 新しくコミットを追加するため、コミットの履歴は残る

参考 URL：

- [revert ｜サル先生の Git 入門【プロジェクト管理ツール Backlog】](https://backlog.com/ja/git-tutorial/stepup/29/)

  </div>
</details>

<details>
  <summary>rebase</summary>
  <div>

- コミットをまとめることができる
- リベースはブランチの統合が可能（マージ同様）
- コミット履歴を整理することができる
- 履歴の破壊をするため、リモートブランチの操作はご法度

参考 URL：

- [rebase -i でコミットをまとめる｜サル先生の Git 入門【プロジェクト管理ツール Backlog】](https://backlog.com/ja/git-tutorial/stepup/32/)
- [マージとリベース | Atlassian Git Tutorial](https://www.atlassian.com/ja/git/tutorials/merging-vs-rebasing)

  </div>
</details>

<details>
  <summary>tag</summary>
  <div>

- コミットを参照しやすくするため、分かりやすい名前（タグ）を付けることができる

参考 URL：

- [タグ｜サル先生の Git 入門【プロジェクト管理ツール Backlog】](https://backlog.com/ja/git-tutorial/stepup/17/)

  </div>

</details>

<details>
  <summary>commit</summary>
  <div>

- `--amend` のオプションをつけることで、直前のコミットの内容を変更することが可能
- `git add` の後に `git commit --amend` を実行すると、コミットメッセージだけでなく、コミットに含む変更内容も変わる

参考 URL：

- [commit --amend ｜サル先生の Git 入門【プロジェクト管理ツール Backlog】](https://backlog.com/ja/git-tutorial/stepup/28/)

    </div>
  </details>

<details>
  <summary>grep</summary>
  <div>

- Git リポジトリ内の検索コマンド
- `-n` オプションで行数表示、`-E` で正規表現での検索などが可能

参考 URL：

- [Git リポジトリ内を grep する git grep はシンプルで超便利 | DevelopersIO](https://dev.classmethod.jp/articles/useful-git-grep-command/#%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E5%90%8D%E3%81%AE%E4%B8%80%E8%A6%A7%E3%82%92%E8%AA%BF%E3%81%B9%E3%81%9F%E3%81%84)

  </div>
</details>

<details>
  <summary>notes</summary>
  <div>

- `git notes` で git のコミットに Notes を追加できる
  ※利点はまだよくわかってない

参考 URL：

- [Git - git-notes Documentation](https://git-scm.com/docs/git-notes)

  </div>
</details>

<details>
  <summary>switch, restore</summary>
  <div>

- `git switch -c [branch-name]` で `git checkout -b [branch-name]` 同様に新規のブランチの作成＋切り替えができる
- `git add` 後に `git restore --staged [変更したファイル]` を実行すると、`git reset` 同様に add 前の状態に戻せる

参考 URL：

- [git checkout の代替としてリリースされた git switch と git restore - kakakakakku blog](https://kakakakakku.hatenablog.com/entry/2020/04/08/151627)

  </div>
</details>

## GitHub

<details>
  <summary>GitHubページの公開</summary>
  <div>

- Settings の Pages からページの公開を選択することができる
- 基本的には index.html が公開される。ない場合は README が公開される
  ※README.md が index.html より優先されるとの記事があったが、自分は index.html が優先されていた（2021/08/25 時点）

参考 URL：

- [Configuring a publishing source for your GitHub Pages site - GitHub Docs](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

  </div>
</details>

<details>

  <summary>GitHub Pages での details の表示方法</summary>

  <div>

- `_config.yml` ファイルを追加し、`markdown: CommonMarkGhPages` の記述をすることで、適切に表示されるようになる

参考 URL：

- [GitHub Pages で Markdown の`<details>`内要素がパースされない - Qiita](https://qiita.com/eggplants/items/673aba3637748346797c)

  </div>

</details>

## Markdown

<details>
  <summary>Markdown記法 チートシート</summary>
  <div>

- 「折りたたみ」は `<details>` と `<summary>` で表現可能

```
<details><summary>表示される部分</summary>本文</details>
```

参考 URL：

- [Markdown 記法 チートシート - Qiita](https://qiita.com/Qiita/items/c686397e4a0f4f11683d#details---%E6%8A%98%E3%82%8A%E3%81%9F%E3%81%9F%E3%81%BF)

  </div>
</details>

## Terminal

<details>
  <summary>Linuxで新規ファイル作成をするコマンド</summary>
  <div>

- `touch <ファイル名>` でファイル作成が可能
- `vi <ファイル名>` でファイルを vi で新規作成し、編集することが可能

参考 URL：

- [【touch】Linux で新規ファイル作成をするコマンド | UX MILK](https://uxmilk.jp/8395)

  </div>
</details>

<details>
  <summary>UNIXコマンド</summary>
  <div>

- `pwd`：現在の作業ディレクトリをプリントする
- `~`：ホームディレクトリを表す

参考 URL：

- [UNIX コマンドの使い方](http://psa2.kuciv.kyoto-u.ac.jp/staff/susaki/command/c_cd.html)

  </div>
</details>

## 環境系

<details>
  <summary>PHPの実行環境</summary>
  <div>

- PHP は、モジュール版と CGI 版の二種がありどちらかの実行環境が必要
- Apache：PHP モジュールを読み込み、PHP を実行する
- nginx + PHP-FPM：FastCGI を通して PHP を実行する

参考 URL：

- [nginx と PHP-FPM の仕組みをちゃんと理解しながら PHP の実行環境を構築する - Qiita](https://qiita.com/kotarella1110/items/634f6fafeb33ae0f51dc)

  </div>
</details>

<details>
  <summary>VSCode スニペット登録</summary>
  <div>

- markdown のスニペットはデフォルトで無効
- ユーザー設定で `"[markdown]": { "editor.quickSuggestions": true }` の設定を行う
- ファイル > ユーザー設定 > ユーザースニペット から任意の拡張子のファイルに対しスニペットを登録する

参考 URL：

- [Visual Studio Code で markdown のスニペットを登録する | コーヒー飲みながら仕事したい](https://coffee-nominagara.com/2019-01-25-094628)
- [VsCode のスニペットのススメ - Qiita](https://qiita.com/xx2xyyy/items/fd333368db548167f15a)

  </div>
</details>
