# anime-knowledge-skills

[![インストール npx skills](https://img.shields.io/badge/Install-npx%20skills-412991)](https://github.com/vercel-labs/skills)
![回答言語 日本語](https://img.shields.io/badge/Response-Japanese-2563eb)

アニメ作品の調査に使う Agent Skills をまとめたリポジトリです。

## Quickstart

エージェントに設定を任せる場合は、以下のどちらかを貼り付けてください。

### 日本語

```text
https://github.com/howamun-day/anime-knowledge-skills の SETUP.md に従って、このプロジェクトに全スキルを設定し、配置先を確認してください。
```

### English

```text
Follow SETUP.md at https://github.com/howamun-day/anime-knowledge-skills to install all skills for this project and verify where they were installed.
```

## スキル一覧

| スキル名 | 用途 | 調査例 |
| --- | --- | --- |
| [`anime-primary-sources`](.agents/skills/anime-primary-sources/SKILL.md) | Annict とピクシブ百科事典を参照し、公式サイト・キャスト・各話の出来事を出典付きで調べる。 | [『CUE!』](.agents/skills/anime-primary-sources/references/cue.md) |

## インストール

インストール先のプロジェクトで `--skill` に表のスキル名を指定します。以下は `anime-primary-sources` の例です。

```sh
npx skills add howamun-day/anime-knowledge-skills --skill anime-primary-sources
```

リポジトリ内のスキルをすべてインストールする場合は、`--skill '*'` を指定します。

```sh
npx skills add howamun-day/anime-knowledge-skills --skill '*'
```

手動配置、未公開の作業コピーからのインストール、エージェントごとの配置先は [SETUP.md](SETUP.md) を参照してください。

## 使い方

インストール先のエージェントで調べたいことを質問します。スキルを明示する場合は、利用するエージェントの方法で表のスキル名を指定します。
