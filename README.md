# LLM Wiki Sample

このリポジトリは、運用中の LLM Wiki の一部を抜粋したサンプルです。
一次資料を `raw/` に置き、LLM が `wiki/` 配下の Markdown を整理・更新する構成を前提にしています。

## 構成

```
llm-wiki/
  raw/          # 一次資料。原則として追記のみ。LLM は勝手に改変しない
  wiki/         # LLM が保守する wiki
    concepts/   # 概念ページ
    sources/    # 一次資料・Web source の記録
    maps/       # 概念群の関係を整理する map page
    glossary.md # 専門用語の標準的な日本語訳を管理する対訳表
    index.md    # maps へのリンク 
    schema.md   # wiki のページ種別・必須要素・概念関係の schema
  AGENTS.md     # 運用ルール
```

- 導線は index -> maps -> concepts, sources の想定
- glossary で対訳表を管理することで表記揺れを緩和しています

## 内容

主に、グラフ理論、統計モデリング、因果推論、圏論、型理論などの概念整理を含みます。
Obsidian 互換の内部リンクを使い、資料間の関係を Markdown でたどれるようにしています。

## 運用

閲覧は Obsidian，エージェントは Codex app を使っています．
実際に運用しながら，`AGENTS.md` と `wiki/schema.md` で運用方針を調整しています．