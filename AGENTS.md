## 目的

このリポジトリは LLM Wiki です。`raw/` に不変の一次資料を置き、LLM が `wiki/` に構造化された Markdown wiki を作成・更新します。

## 構造

```
llm-wiki/
  raw/        # 一次資料。原則として追記のみ。LLM は勝手に改変しない
  wiki/       # LLM が保守する wiki
    concepts/ # 概念ページ
    sources/  # 一次資料・Web source の記録
    maps/     # 概念群の関係を整理する map page
    glossary.md # 専門用語の標準的な日本語訳を管理する対訳表
    schema.md # wiki のページ種別・必須要素・概念関係の schema
  AGENTS.md   # この運用ルール
```

## 基本ルール

- Web 上の一次資料は、原則として URL、取得日、バージョン、要約を `wiki/sources/` に記録し、snapshot は保存しない。
- `raw/` に保存した一次資料は source of truth として扱う。誤字修正や要約目的で上書きしない。
- `raw/` には、消失・改変リスクが高い資料、安定URLがない資料、または再現性のために snapshot が必要な資料だけを保存する。
- `wiki/` は LLM が編集してよい。新しい資料や質問から得た有用な整理は、会話だけで終わらせずページとして残す。
- `wiki/` の本文・見出し・要約・ログは原則として日本語で書く。専門用語は必ず標準的な日本語訳を調べ、存在する場合は日本語で書く。固有名詞、英語タイトル、引用、raw source のファイル名やURLは必要に応じて原文を残してよい。
- `wiki/concepts/`、`wiki/sources/`、`wiki/maps/` の本文は、wiki 固有の事情、現在の収録状況、作業状態、運用判断ではなく、概念、資料内容、概念間の関係の整理に徹する。`この wiki では`、`現時点でこの wiki にある`、`既存ページ`、`source page に残す` のような自己言及は避ける。
- wiki 固有の運用方針、作業理由、現在の状態、点検結果は、`AGENTS.md`、`wiki/schema.md`、`wiki/log.md`、必要に応じて `wiki/glossary.md` の運用ルール欄に記録し、concept page、source page、map page へ混ぜない。
- 重要な主張には、可能な限り `raw/` 内の資料への参照を付ける。
- concept page の根拠資料や概念関係への内部リンクは、原則として本文、要点、関係説明の中に置く。末尾に `関連ページ` や `関連` として内部リンクだけの出口リンク集を作らない。
- 既存ページと矛盾する情報を見つけたら、黙って置き換えず、矛盾・更新・不確実性を明記する。
- Obsidian 互換を意識し、内部リンクは `[[page-name]]` 形式を優先する。
- 新しい wiki ページや構造を追加するときは、`wiki/schema.md` のページ種別・必須要素・概念関係の語彙に従う。
- 新しい専門用語を使うときは、まず `wiki/glossary.md` を確認する。対訳表にない場合は、信頼できる日本語資料で標準訳を調べ、採用訳・状態・根拠・確認日を対訳表へ追加する。J-GLOBAL の機械翻訳や同種の自動翻訳ページは、訳語採用の根拠にしない。

## Web Source と Raw Source の扱い

- arXiv、DOI、公式 docs など、安定した参照先やバージョン固定URLがある資料は、リンクを一次参照として扱う。
- Web source は、元URL、取得日、バージョン、要約、参照方法を wiki source page に記録する。
- Web source の PDF、HTML、抽出テキストは原則 Git に入れない。
- snapshot が必要な場合だけ `raw/` に保存し、その理由を wiki source page または `wiki/log.md` に残す。
- `raw/` の既存ファイルは原則変更しない。修正が必要な場合は、別ファイルとして追加するか、変更理由を `wiki/log.md` に残す。
- 大容量の動画、音声、データセット、再生成可能なキャッシュ、secret を含むファイルは Git 管理しない。

## Wiki の必須ファイル

- `wiki/index.md`: wiki 全体の入口。map page へのリンクだけを置き、concept page や source page の一覧は各 map page に任せる。
- `wiki/log.md`: 追記専用の作業ログ。ingest、query、lint、整理作業を時系列で記録する。ログからは内部リンクを張らず、ページ名やファイルパスは通常テキストまたはコード表記で残す。
- `wiki/schema.md`: wiki の page type、配置、必須要素、概念関係の語彙、lint 観点を定義する。
- `wiki/glossary.md`: 専門用語の英日対訳、採用訳、確認状況、根拠、確認日を管理する。対訳表からは内部リンクを張らず、根拠欄には標準訳確認に使った外部資料または訳語判断の短い理由を残す。リンクにならない wiki 内ファイルパスは記入しない。

## Wiki Schema

- `wiki/sources/` は source page を置く。元URL、取得日、バージョン、参照方法、要約、要点、関連ページを持つ。
- `wiki/concepts/` は concept page を置く。資料や質問から再利用できる概念、主張、関係を統合し、根拠となる source page へリンクする。
- `wiki/maps/` は map page を置く。読む順序ではなく、上位概念、下位概念、特殊例、道具、交差、隣接領域、根拠資料などの概念関係を整理する。
- `wiki/glossary.md` は glossary page として、専門用語の標準的な日本語訳を管理する。標準訳が確認できた語は本文では日本語を優先し、標準訳が見つからない語は `未確立` として記録する。対訳表からは Obsidian 内部リンクを張らない。
- `wiki/index.md` は index page として、map page への入口だけを保つ。concept page、source page、`wiki/schema.md`、`wiki/log.md` への導線は、必要な map page や運用ルールから辿る。
- `wiki/log.md` は log page として、`## [YYYY-MM-DD] 種別 | タイトル` 形式で追記する。ログからは Obsidian 内部リンクを張らない。
- 詳細な schema は `wiki/schema.md` を正とする。schema と AGENTS.md がずれた場合は、作業時に両方を更新する。

## Ingest 手順

新しい資料を取り込むときは、以下を行う。

1. 資料の URL、取得日、バージョンを記録し、必要な場合だけ `raw/` に snapshot を保存する。
2. 資料を読み、要点・登場する概念・今後ページ化すべき対象を整理する。新しい専門用語は `wiki/glossary.md` を確認し、未登録なら標準的な日本語訳を調べて対訳表へ追加する。
3. 必要なら `wiki/sources/`、`wiki/concepts/`、`wiki/maps/` などを作り、`wiki/schema.md` に従って適切なページを追加・更新する。
4. 新しい map page を追加した場合、または map page の説明を変えた場合だけ `wiki/index.md` を更新する。
5. `wiki/log.md` に `## [YYYY-MM-DD] 取り込み | タイトル` 形式で記録する。

## Query 手順

質問に答えるときは、まず `wiki/index.md` から関連する map page を探し、map page から concept page や source page へ降りる。必要に応じて wiki source page に記録された元URLまたは `raw/` 内の保存済み資料を確認する。比較表、分析、まとめなど再利用価値がある回答は、ユーザーに確認せず `wiki/` にページとして保存してよい。

## Lint 手順

定期的に以下を確認する。

- 孤立ページやリンク切れ
- 同じ概念の重複ページ
- 古い記述と新しい資料の矛盾
- ページ化されていない重要概念
- `index.md` が実在する map page だけを入口として持っているか
- `wiki/schema.md` で定義したページ種別・必須セクション・概念関係の表し方との不一致
- 内部リンクが、根拠、上位下位関係、特殊例、道具、交差、隣接領域などの意味ある関係を表しているか。単なる出口リンク、重複リンク、習慣的に置いただけのリンクは削る。
- concept page 末尾に、関係説明のない内部リンクだけの `関連ページ` または `関連` 節が残っていないか。source page の `関連ページ` は必須節として残すが、資料内容と直接対応するページに絞る。
- concept page、source page、map page の本文に、wiki 固有の事情、現在の収録状況、作業状態、運用判断、自己言及表現が混入していないか。
- `wiki/log.md` に Obsidian 内部リンクが残っていないか
- `wiki/glossary.md` に Obsidian 内部リンクが残っていないか
- 専門用語が `wiki/glossary.md` の採用訳と矛盾していないか
- 英語の専門用語が残っている場合、固有名詞、論文タイトル、URL、コード、引用、略語、未確立語、初出併記のいずれかとして妥当か

## Git 運用

- 基本は `main` 一本で運用する。
- commit message は `raw:`, `wiki:`, `ingest:`, `query:`, `lint:`, `ops:` のいずれかで始める。
- Ingest、Query、Lint、運用ルール更新などでファイルを編集した場合、作業完了後に原則として LLM が自動で commit まで行う。
- 自動 commit 前には、必ず `git status` と `git diff` を確認し、今回の作業に関係する変更だけを stage する。ユーザーや別作業による未関係の変更は巻き込まない。
- 自動 commit 前には、可能な範囲でリンク検査、形式確認、または作業内容に応じた軽い検証を行い、結果を `wiki/log.md` または最終応答に残す。
- commit message は作業種別に合わせる。例: 資料取り込みは `ingest: タイトル`、質問から作った wiki 更新は `query: トピック`、lint は `lint: wiki consistency`、運用ルール変更は `ops: 内容`。
- snapshot を保存する場合は、可能なら raw source の追加と wiki 更新は別 commit にする。この場合も各 commit 前に status と diff を確認する。
- LLM は commit 前に必ず `git status` と `git diff` を確認する。
- 大規模なページ再編、リネーム、分類変更は一時ブランチで作業する。
- 重要な節目では tag を作って snapshot として残してよい。
