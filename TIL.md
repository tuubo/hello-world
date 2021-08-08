## CSS

<details><summary>インラインブロックで画像の位置を揃える</summary>

URL : [css – インラインブロックを並べて画像を表示するとずれてしまう | memorandum-plus](http://memorandum-plus.com/2018/04/04/css-%E3%82%A4%E3%83%B3%E3%83%A9%E3%82%A4%E3%83%B3%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E3%82%92%E4%B8%A6%E3%81%B9%E3%81%A6%E7%94%BB%E5%83%8F%E3%82%92%E8%A1%A8%E7%A4%BA%E3%81%99%E3%82%8B%E3%81%A8/)

概要 : 

- `vertical-align` のデフォルト値は `baseline`
- `display: inline-block` で画像を含むコンテンツと文字を含むコンテンツを並べると、画像の下端と文字の下端が揃うように並び、見た目上ずれが発生する
</details>

## Storybook

<details><summary>Story rendering</summary>

URL：[Story rendering](https://storybook.js.org/docs/react/configure/story-rendering#adding-to-head/)

概要：

- `.storybook/preview-head.html` を使えば、iframeの書き換えが可能？（調査中）
</details>


<details><summary>Theme switcher Addon</summary>

URL：[Theme switcher Addon | Storybook](https://storybook.js.org/addons/storybook-addon-themes)

概要：

- Storybook のテーマの切り替え（任意の要素のクラスの切り替え）ができる
</details>

## Git

<details><summary>Git のチェリーピック</summary>

URL：[Git のチェリーピック | Atlassian Git Tutorial](https://www.atlassian.com/ja/git/tutorials/cherry-pick)  
※分かりやすいサイトがあれば更新したい

概要：

- 任意のコミットだけを別のブランチに適用することができる
</details>

<details><summary>revert</summary>

URL：[revert｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/29/)

概要：

- 特定のコミットを打ち消すことができる
- 新しくコミットを追加するため、コミットの履歴は残る
</details>

<details><summary>rebase</summary>

URL：[rebase -i でコミットをまとめる｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/32/)

概要：

- コミットをまとめることができる

URL：[マージとリベース | Atlassian Git Tutorial](https://www.atlassian.com/ja/git/tutorials/merging-vs-rebasing)

概要：

- リベースはブランチの統合が可能（マージ同様）
- コミット履歴を整理することができる
- 履歴の破壊をするため、リモートブランチの操作はご法度
</details>

<details><summary>tag</summary>

URL：[タグ｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/17/)

概要：

- コミットを参照しやすくするため、分かりやすい名前（タグ）を付けることができる
</details>

## Markdown

<details><summary>Markdown記法 チートシート</summary>

URL：[Markdown記法 チートシート - Qiita](https://qiita.com/Qiita/items/c686397e4a0f4f11683d#details---%E6%8A%98%E3%82%8A%E3%81%9F%E3%81%9F%E3%81%BF)

概要：

- 「折りたたみ」は `<details>` と `<summary>` で表現可能

```
<details><summary>表示される部分</summary>本文</details>
```
</details>