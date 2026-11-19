# セットアップ

## 前提条件

- Agent Skills に対応し、Web 検索やブラウジングを利用できるエージェント。[対応エージェント一覧](https://github.com/vercel-labs/skills/blob/main/docs/agents.md#supported-agents)
- `npx skills` を使う場合は、`npx` を実行できる Node.js 環境。

## GitHub からインストール

インストール先のプロジェクトのルートで実行します。エージェントの選択が表示されたら、利用するエージェントを選びます。

```sh
npx skills add howamun-day/anime-knowledge-skills --skill anime-primary-sources
```

リポジトリ内のスキルをすべてインストールする場合は、`--skill '*'` を指定します。

```sh
npx skills add howamun-day/anime-knowledge-skills --skill '*'
```

自分の複数のプロジェクトで使う場合は、いずれのコマンドにも `--global` を追加できます。以下は全スキルをユーザー単位でインストールする例です。

```sh
npx skills add howamun-day/anime-knowledge-skills --skill '*' --global
```

## ローカルのチェックアウトからインストール

手元で変更した版や、GitHub にまだ公開されていない版を使う場合は、インストール先のプロジェクトからローカルのパスを指定します。

```sh
npx skills add /path/to/anime-knowledge-skills --skill anime-primary-sources
```

ローカルのスキルをすべてインストールする場合も、`--skill '*'` を指定します。

## 手動で配置する

このリポジトリをクローンするか GitHub から ZIP をダウンロードして展開し、`.agents/skills/anime-primary-sources/` をフォルダごと利用先へコピーします。`SKILL.md` と `references/` は同じ構成で配置してください。手動配置は `npx` なしで行えます。

すべてのスキルを配置する場合は、リポジトリの `.agents/skills/` 直下にある各スキルのフォルダを、以下の配置先にコピーします。

| エージェント | プロジェクト単位の配置先 | ユーザー単位の配置先 |
| --- | --- | --- |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/` | `~/.claude/skills/` |
| [Codex](https://learn.chatgpt.com/docs/build-skills) | `.agents/skills/` | `~/.agents/skills/` |

プロジェクト単位のパスはインストール先のプロジェクトルートからの相対パスです。他のエージェントでは、そのエージェントのスキル配置先を確認してください。最終的に配置先の下に `anime-primary-sources/SKILL.md` と `anime-primary-sources/references/cue.md` があれば、フォルダ構成は正しい状態です。

## インストールを確認

`npx skills` を使った場合は、インストール先のプロジェクトで一覧を表示します。ユーザー単位でインストールした場合は `npx skills list --global` を使います。

```sh
npx skills list
```

手動配置の場合は、利用するエージェントのスキル一覧で `anime-primary-sources` を確認します。「『CUE!』でハムレットを演じる場面は何話？」と質問すると、Annict とピクシブ百科事典を検索し、話数を公式の各話紹介や正規配信ページで確認する流れを試せます。CLI の詳細は [skills のコマンドリファレンス](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)を参照してください。
