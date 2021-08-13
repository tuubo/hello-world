## HTML

<details><summary>aria-hidden 属性</summary>

- `aria-hidden="true"` を設定することで、視覚的に非表示になっていないコンテンツを支援技術から外すことができる
- Modal の裏で表示されているコンテンツなどに適用することがある
- 表示すべきコンテンツも含んでしまうため、 `aria-hidden="true"` を `<body>` に指定することは推奨されない

参考URL：

- [コンテンツの非表示と更新  |  Web  |  Google Developers](https://developers.google.com/web/fundamentals/accessibility/semantics-aria/hiding-and-updating-content?hl=ja#aria-hidden)
- [[aria-hidden="true"] is present on the document<body></body>](https://web.dev/aria-hidden-body/)
</details>

## CSS

<details><summary>インラインブロックで画像の位置を揃える</summary>

- `vertical-align` のデフォルト値は `baseline`
- `display: inline-block` で画像を含むコンテンツと文字を含むコンテンツを並べると、画像の下端と文字の下端が揃うように並び、見た目上ずれが発生する

参考URL：

- [css – インラインブロックを並べて画像を表示するとずれてしまう | memorandum-plus](http://memorandum-plus.com/2018/04/04/css-%E3%82%A4%E3%83%B3%E3%83%A9%E3%82%A4%E3%83%B3%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E3%82%92%E4%B8%A6%E3%81%B9%E3%81%A6%E7%94%BB%E5%83%8F%E3%82%92%E8%A1%A8%E7%A4%BA%E3%81%99%E3%82%8B%E3%81%A8/)
</details>

## Storybook

<details><summary>Story rendering</summary>

- `.storybook/preview-head.html` を使えば、iframeの書き換えが可能？（調査中）

参考URL：

- [Story rendering](https://storybook.js.org/docs/react/configure/story-rendering#adding-to-head/)
</details>


<details><summary>Theme switcher Addon</summary>

- Storybook のテーマの切り替え（任意の要素のクラスの切り替え）ができる

参考URL：

- [Theme switcher Addon | Storybook](https://storybook.js.org/addons/storybook-addon-themes)
</details>

## Git

<details><summary>Git のチェリーピック</summary>

- 任意のコミットだけを別のブランチに適用することができる

参考URL：

- [Git のチェリーピック | Atlassian Git Tutorial](https://www.atlassian.com/ja/git/tutorials/cherry-pick)  
※分かりやすいサイトがあれば更新したい
</details>

<details><summary>revert</summary>

- 特定のコミットを打ち消すことができる
- 新しくコミットを追加するため、コミットの履歴は残る

参考URL：

- [revert｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/29/)
</details>

<details><summary>rebase</summary>

- コミットをまとめることができる
- リベースはブランチの統合が可能（マージ同様）
- コミット履歴を整理することができる
- 履歴の破壊をするため、リモートブランチの操作はご法度

参考URL：

- [rebase -i でコミットをまとめる｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/32/)
- [マージとリベース | Atlassian Git Tutorial](https://www.atlassian.com/ja/git/tutorials/merging-vs-rebasing)
</details>

<details><summary>tag</summary>

- コミットを参照しやすくするため、分かりやすい名前（タグ）を付けることができる

参考URL：

- [タグ｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/17/)

</details>

<details><summary>commit</summary>

- `--amend` のオプションをつけることで、直前のコミットの内容を変更することが可能
- `git add` の後に `git commit --amend` を実行すると、コミットメッセージだけでなく、コミットに含む変更内容も変わる

参考URL：

- [commit --amend｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/28/)

</details>

## Markdown

<details><summary>Markdown記法 チートシート</summary>

- 「折りたたみ」は `<details>` と `<summary>` で表現可能

```
<details><summary>表示される部分</summary>本文</details>
```

参考URL：

- [Markdown記法 チートシート - Qiita](https://qiita.com/Qiita/items/c686397e4a0f4f11683d#details---%E6%8A%98%E3%82%8A%E3%81%9F%E3%81%9F%E3%81%BF)
</details>

## Terminal

<details><summary>Linuxで新規ファイル作成をするコマンド</summary>

- `touch <ファイル名>` でファイル作成が可能
- `vi <ファイル名>` でファイルを vi で新規作成し、編集することが可能

参考URL：

- [【touch】Linuxで新規ファイル作成をするコマンド | UX MILK](https://uxmilk.jp/8395)
</details>