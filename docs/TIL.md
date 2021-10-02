## Web

<details>

  <summary>最適なフォームの作成</summary>

  <div>

- `type` 属性でモバイルで最適なキーボードレイアウトが表示されるように伝えることが可能
- `autocomplete` 属性はセクション名を伴うことが可能
- 異なるセクションの場合は、個別にオートコンプリートをすることができる
- `checkValidity()` でフォームが有効化の判断が可能

参考 URL：

- [最適なフォームの作成 | Web | Google Developers](https://developers.google.com/web/fundamentals/design-and-ux/input/forms?hl=ja)

  </div>

</details>

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

  <summary>position: absolute を使わないコンテンツの重ね合わせ</summary>

  <div>

- `display: grid` で要素を重ねることが可能
- `grid-aria: 1/-1;` で二つの要素を同じエリアに配置する

参考 URL：

- [モダン CSS による絶対配置（position: absolute;）の削減 | コリス](https://coliss.com/articles/build-websites/operation/css/less-absolute-positioning-modern-css.html)

  </div>

</details>

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

<details>

  <summary>counter-increment</summary>

  <div>

- `counter-increment: [名前];` で、CSS で連番を作成することができる。
- リスト毎に値をリセットしたい場合は、親に `counter-reset` を指定すればよい。

```SCSS
// 使用例

.list {
  counter-reset: list;

  &-item {
    counter-increment: list;

    &::before {
      content: list;
    }
  }
}
```

参考 URL：

- [counter-increment - CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/counter-increment)
- [CSS の counter-increment を使って簡単に自動で連番をつける方法 | ジーニアスブログ – WEB 制作会社ジーニアスウェブのお役立ちブログ](https://www.genius-web.co.jp/blog/web-programming/a-method-of-using-a-css-counter-increment-to-easily-get-a-sequential-number-automatically.html)

  </div>

</details>

## JavaScript

<details>

  <summary>無名関数・即時関数</summary>

  <div>

- 無名関数：関数名のない関数。1 回のみ使用する関数に使う。
- 即時関数：定義してすぐに実行される関数。1 回のみ使用する関数に使う。
  無名関数（アロー）を即時関数で書いた例

```
((a, b) => {
  const sum = a + b;
  console.log(sum);
})(1, 2);
```

参考 URL：

- [JavaScript で即時関数を使う方法【初心者向け】 | TechAcademy マガジン](https://techacademy.jp/magazine/5530)

  </div>

</details>

<details>

  <summary>some と every</summary>

  <div>

- 配列に使えるメソッド (使用例： `arr.every(elem => elem > 0)` )
- `some` : 配列の要素 1 つ以上が条件を満たす場合に `true` を返す
- `every` : 配列のすべての要素が条件を満たす場合に `true` を返す

参考 URL：

- [JavaScript の some と every がすごく便利 - Qiita](https://qiita.com/i_am_master_yoda/items/224ff73443b4566ec8e8)

  </div>

</details>

<details>

  <summary>Object.defineProperty</summary>

  <div>

- オブジェクトのプロパティを明示的に追加・変更することができる
- 代入でのプロパティ追加の場合、値の変更が可能だが `Object.defineProperty()` で追加した値は不変となる（ default では ）
- `get` : プロパティにアクセスすると、引数無しでこの関数が呼ばれる。戻り値はプロパティの値として使われる

参考 URL：

- [Object.defineProperty() - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)

  </div>

</details>

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

<details>

  <summary>配列操作</summary>

  <div>

- `reverse` メソッドで、配列を逆順にする事が可能
- `Array.from` でオブジェクトを配列に直すことが簡単にできる。

例

```JavaScript
    var friends = [
        { name: 'John', age: 22 },
        { name: 'Peter', age: 23 },
        { name: 'Mark', age: 24 },
    ]

    var friendsNames = Array.from(friends, ({name}) => name);
    console.log(friendsNames); // ["John", "Peter", "Mark"]
```

参考 URL：

- [JavaScript の配列操作に役立つ 13 のヒントとトリック - Qiita](https://qiita.com/rana_kualu/items/24e5b6009ad831102db4)

  </div>

</details>

<details>

  <summary>jQueryを使うのが難しい理由</summary>

  <div>

- 保守が必要：古い jQuery は脆弱性を持つこともあり、最新に保たれるよう定期的にコードを更新していく必要がある
- 速度：script タグの呼び出し完了を待つことで、遅延が発生する
  ユーザーを待たせないように読み込み順序のコントロールが必要

※jQuery 自体が悪ではないが、jQuery を選択するメリットは今や少ない

参考 URL：

- [そろそろなぜ jQuery を使うのが難しいのかをちゃんとまとめようと思う。｜榊原昌彦｜ note](https://note.com/rdlabo/n/ndfe07e0c0bcb)

  </div>

</details>

## TypeScript

<details>

  <summary>props・型のTips集</summary>

  <div>

- `React.ComponentProps` : 対象のコンポーネントの props の型を取得できる

参考 URL：

- [React + TypeScript で props と型を便利に扱う Tips 集](https://zenn.dev/so_nishimura/articles/e9afde3b7dc779)

  </div>

</details>

<details>

  <summary>TypeScript入門</summary>

  <div>

- 変数、関数、引数等の後ろに `:型名` を指定することで型宣言が可能
- `<型名> 値` `値 as 型名` の記述で型アサーションを使用し、型が不明な値に型付けが可能
- `Foo<S, T>` のような書き方で、型定義の中で `< >` で囲った名前を型変数として使うことができる

※勉強中

参考 URL：

- [とほほの TypeScript 入門 - とほほの WWW 入門](https://www.tohoho-web.com/ex/typescript.html)
- [TypeScript の型入門 - Qiita](https://qiita.com/uhyo/items/e2fdef2d3236b9bfe74a)

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

<details>

  <summary>Storybook Best Practices</summary>

  <div>

- コンポーネント毎に 1 つの Storybook ファイルを置き、Default, Playground, その他各ステータスのストーリー含める

※勉強中

参考 URL：

- [10 Storybook Best Practices | Better Programming](https://betterprogramming.pub/10-storybooks-best-practices-ad5fec0f145a)

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

<details>

  <summary>Gitの設定 ( git config ) </summary>

  <div>

- `git config <name> <value>` で各項目の設定を変更できる
- デフォルトでは、 local の設定が変更される

※人と作業するとき、`user.name` が設定されていないと宜しくなさそうなので慌てて調べた

参考 URL：

- [Git の設定を git config で確認・変更 | note.nkmk.me](https://note.nkmk.me/git-config-setting/)

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

```HTML
<details><summary>表示される部分</summary>本文</details>
```

参考 URL：

- [Markdown 記法 チートシート - Qiita](https://qiita.com/Qiita/items/c686397e4a0f4f11683d#details---%E6%8A%98%E3%82%8A%E3%81%9F%E3%81%9F%E3%81%BF)

  </div>
</details>

## Terminal

<details>

  <summary>chmod：権限変更</summary>

  <div>

- `ls -l`：カレントディレクトリ内のファイル・ディレクトリの情報の確認  
  `ls -la` コマンドでは、隠しファイルを含めた確認が可能
- `-rw-r--r--` 、 `drwxr-xr-x` などがパーミッションを表す
- 1 文字目：ファイル種別 ( `-` : ファイル `d` : ディレクトリ `l` : シンポリックリンク )
- 2-4 文字目：ファイル所有者の権限 ( `r` : 読み取り `w` : 書き込み `x` : 実行 )
- 5-7 文字目：ファイルの所有グループの権限
- 8-10 文字目：その他の権限
- `chmod モード 対象ファイル名` でパーミッションの変更が可能  
  例）`chmod 764 hoge.txt` : hoge.txt に対して `-rwxrw-r--` の権限を付与する  
   | モード(数字) | モード(アルファベット) | 権限 |
  | ------------ | ---------------------- | -------- |
  | 4 | r | 読み取り |
  | 2 | w | 書き込み |
  | 1 | x | 実行 |
  モード(数字)の合計値が、「所有者」「所有グループ」「その他」への権限を表す。

参考 URL：

- [Linux の権限確認と変更(chmod)（超初心者向け） - Qiita](https://qiita.com/shisama/items/5f4c4fa768642aad9e06)

  </div>

</details>

<details>

  <summary>mv：ファイル・ディレクトリの移動/名前変更</summary>

  <div>

- `mv <現在のファイル/ディレクトリ名> <変更後のファイル/ディレクトリ名>` でファイル・ディレクトリの移動と名称変更が可能
- 移動先のディレクトリが存在しない場合、ディレクトリ移動ではなくファイル名変更が行われる
- `-i` オプションで、ファイル上書き時に確認メッセージを表示する

参考 URL：

- [【Linux コマンド】mv でファイル・ディレクトリを移動する方法 | 侍エンジニアブログ](https://www.sejuku.net/blog/49611)

  </div>

</details>

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

<details>

  <summary>vi でのカット・コピー・ペースト方法</summary>

  <div>

- カット：`d` `d` のコマンドを打つと 1 行カット
- コピー：`y` `y` のコマンドを打つと 1 行コピー
- ペースト：`p` のコマンドを打つとペースト
- `p` の前に数字を入力するとコマンドを複数回呼び出せる（2 回ペーストなど）

参考 URL：

- [Vi (Vim) 超入門：第 3 回 Vi でカット・コピー・ペースト機能を用いて編集する](https://www.hpc.co.jp/support/hello_vi_03/)

  </div>

</details>

## 環境系

<details>

  <summary>yarn と npm の違い</summary>

  <div>

- npm が先発のパッケージマネージャー。npm 公式。
- yarn は npm のパフォーマンス・セキュリティ問題解決のために開発された。
- npm は Node.js に同梱されインストールされる。
- 比較記事だと yarn の方が優勢のようだが、 npm もパフォーマンスは改善されてきているらしい。

参考 URL：

- [npm と yarn と pnpm の違い 2021](https://zenn.dev/hibikine/articles/27621a7f95e761)
- [【JS】yarn の長所と yarn から npm に戻ってきた理由 | JavaScript に関するお知らせ](https://jsnotice.com/posts/2020-09-02/index.html)

  </div>

</details>

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

<details>

  <summary>Next.js × ESLint × Prettier</summary>

  <div>

- ESLint：構文解析を行う。Next.js で `<img>` を使用するとエラーになるなど。
- Prettier：コード整形を行う。
- スタイルファイルの構文解析は `ESLint` で行う

参考 URL：

- [Next.js (TypeScript) に ESLint と Prettier を導入し、コードを綺麗に保とう | fwywd（フュード）](https://fwywd.com/tech/next-eslint-prettier)

  </div>

</details>

## Google

<details>

  <summary>Google フォームのカスタマイズ</summary>

  <div>

- 通常のサイトのフォームと、内容の同じ Google フォームを作成することで、サイトの見た目で Google フォームに結果を送信させる事が可能
- Google フォームの `action`, `name` を連携させれば OK

※集計などが楽になると思われる

参考 URL：

- [Google フォームを自在にカスタマイズする - Qiita](https://qiita.com/sotatakahashi/items/fa077cbf820faca30598)

  </div>

</details>
