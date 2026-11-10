<p align="center">
  <img src="assets/logo.png" alt="management-consulting" width="128">
</p>

# management-consulting

AIエージェント向けの戦略思考・意思決定支援スキルです。

このリポジトリは、経営コンサルティングで使われる実務フレームワークを、AIエージェントがそのまま使える形に整理した知識セットです。単なる理論の一覧ではなく、問題をどう分解し、仮説をどう立て、証拠をどう扱い、結論をどう出すかまでを一貫して学べるように構成されています。

主な狙いは、AIに「コンサル風の話」をさせることではなく、次のような戦略的思考のルーチンを身につけさせることです。

- 何を決めるべきかを明確にする
- どこで思考を分解すべきかを整理する
- どの仮説が重要なのかを優先順位付けする
- どの主張が根拠付きなのかを区別する
- どんなデータが必要かを具体化する

## このリポジトリの価値

### 1. フレームワークを「知る」だけでなく「使える」ようにする

このリポジトリには、Five Forces、Value Chain、VRIO、MECE、Issue Tree、Pyramid Principle、Decision Matrix、TAM/SAM/SOM、ADKAR など、実務でよく使うフレームワークが整理されています。

各フレームワークには、次のような内容が含まれています。

- いつ使うべきか
- どの順番で進めるべきか
- 良い出力例と悪い出力例
- よくあるミス
- 使いどころがズレるケース
- 他のフレームワークとの組み合わせ

つまり、理論の暗記ではなく、判断の現場で「選んで使う」ための実践知として整理されています。

### 2. AIの回答を「フレームワークのサラダ」から守る

一般的なAIへの質問では、次のような問題が起きやすくなります。

- どのフレームワークを使うべきかが曖昧になる
- 制約や前提が抜ける
- 仮説と証拠が混ざる
- 結論が先走る

このリポジトリでは、分析前に文脈を固定し、仮説を優先し、根拠をラベル付けし、結論を明確にする設計思想が採用されています。これにより、AIの回答が単なる「コンサルっぽい文章」ではなく、意思決定に使える構造化された提案になります。

### 3. 3つのモードで、質問の深さに合わせて使う

このリポジトリは、依頼の粒度に応じて3つのモードを使い分けます。

- Quick Structure: ざっくりした整理、思考の初期段階
- Full Case: 実務上の重要な意思決定
- Client Deliverable: 提案書・戦略メモ・経営会議向け成果物

軽い相談から、経営層向けの提案まで、同じ土台を使って、出力の粒度だけを調整できます。

## 向いている課題

このリポジトリは、次のようなテーマに特に有効です。

- 市場参入、事業拡大、新規商品検討
- 競争環境分析、ポジショニング、競争優位の整理
- 経営判断（買うか作るか、撤退すべきか、どこに投資するか）
- 組織や変革の設計
- 価格戦略、財務分析、投資判断
- 提案書、戦略メモ、経営会議向けの準備

一方で、次のような用途には向いていません。

- 単純な事実確認
- 日常的なコーディング作業
- すでに明確な計画があり、その実行だけを求めているケース

## リポジトリ構成

```text
management-consulting/
├── SKILL.md                     # 中核ルール: モード、思考ステップ、出力契約
├── README.md                    # 英語のメイン説明書
├── README_JP.md                 # 日本語版の説明書
├── references/
│   ├── frameworks-index.md      # 42フレームワークの要約索引
│   ├── frameworks-strategy.md   # 戦略系フレームワーク
│   ├── frameworks-financial.md  # 財務・市場規模・経営判断
│   ├── frameworks-decision.md   # 意思決定・優先順位付け
│   ├── frameworks-pricing.md    # 価格戦略
│   ├── frameworks-problem-solving.md  # 問題分解と論点整理
│   ├── frameworks-operations.md # 組織変革・顧客体験
│   ├── frameworks-innovation.md # イノベーションと事業モデル
│   ├── diagram-templates.md     # 図解テンプレート
│   ├── tooling-appendix.md      # 図の出力やテーマ補足
│   ├── evidence-standards.md    # 事実/推論/仮定/見積の区分
│   └── ...
├── examples/
│   ├── end-to-end-full-case.md   # 完全な意思決定ケース演習
│   ├── end-to-end-quick-structure.md  # 簡略版の例
│   ├── issue-tree-good-vs-bad.md  # 問題分解の良い例と悪い例
│   ├── recommendation-good-vs-bad.md # 提言の良い例と悪い例
│   └── ...
├── variants/
│   ├── strategy-memo.md         # 戦略メモの書き方
│   ├── due-diligence.md         # デューデリジェンス
│   ├── market-entry.md          # 市場参入戦略
│   ├── org-effectiveness.md     # 組織効果性
│   └── ...
├── docs/
│   └── index.html               # フレームワークの可視化ページ
├── assets/
│   ├── logo.png
│   └── eval-results.png
├── LICENSE
├── SKILL.md
└── README.md
```

## 取り扱うフレームワークの大まかな分類

このリポジトリで扱うフレームワークは、主に7つのカテゴリに分かれています。

### 戦略
- Five Forces
- Value Chain
- 7S
- VRIO
- 3 Horizons
- Ansoff
- Growth-Share Matrix
- Nine-Box
- Blue Ocean
- Wardley Mapping
- Scenario Planning

### 問題解決
- MECE
- Issue Tree
- Hypothesis Tree
- 7-Step Problem Solving
- Pyramid Principle
- SCQA

### 意思決定
- RAPID
- Decision Matrix
- Pre-Mortem
- Second-Order Thinking
- Inversion

### 財務・規模感
- Profit Tree
- Revenue Tree
- TAM/SAM/SOM
- Unit Economics
- Waterfall / Bridge

### 組織・運営
- ADKAR
- Kotterの8ステップ
- Lewinの変革モデル
- Influence Model
- Customer Journey Map
- NPS

### イノベーション
- Jobs to Be Done
- Business Model Canvas
- Value Proposition Canvas
- Advantage Matrix

### 価格戦略
- Value-Based Pricing
- Cost-Plus
- Competitive Pricing
- Dynamic Pricing
- Freemium

## 使い方

### インストール

```bash
# Claude Code
cp -r management-consulting/ ~/.claude/skills/management-consulting/

# または npx で追加
npx skills add gcamilo/management-consulting
```

### 利用例

このリポジトリは、自然な英語または日本語でそのまま使えます。例えば次のような質問が適しています。

> 「買うべきか、自前で作るべきかを整理して」

> 「なぜリテンションが落ちているのか、仮説を立てて分析して」

> 「新市場への参入を判断するための戦略メモを作って」

> 「この事業の優先順位をフレームワークで整理して」

AIエージェントは、依頼の粒度に応じて Quick Structure、Full Case、Client Deliverable のいずれかを選び、論点整理と結論づけを行います。

## 重要な設計思想

### 1. 決定の前に文脈を固定する

まず、何を決めるべきか、誰が意思決定者か、成功条件は何か、スコープは何かを明確にします。ここが曖昧だと、AIは手当たり次第にフレームワークを並べてしまいます。

### 2. 問題をMECEで分解する

問題は、重なりなく、漏れなく分割します。これにより、主題がぶれてしまうことを防ぎます。

### 3. 仮説と根拠を分ける

事実と推論と仮定は区別します。特に、AIが数値や断定を出すときには、その裏付けがどこにあるかを意識させるのが重要です。

### 4. 結論を先に書く

Pyramid Principle や SCQA の思想に沿って、最初に結論を述べてから裏付けを積み上げます。これにより、提案書や戦略メモが「説明の寄せ集め」ではなく、意思決定につながる構成になります。

### 5. 反対意見も提出する

良い提案は自分の意見だけでなく、反対論点も検討します。反対意見を明示することで、判断の弱い仮定に気づきやすくなります。

## 例: どんな成果物が作れるか

- 事業判断のためのIssue Tree
- 市場参入の評価レポート
- 戦略メモのドラフト
- 競争優位の整理
- 価格戦略の検討
- 組織変革のロードマップ
- 財務モデルの前提整理

たとえば [examples/end-to-end-full-case.md](examples/end-to-end-full-case.md) には、B2B SaaS の中堅市場参入を題材にした完全な意思決定ケースがあり、[variants/strategy-memo.md](variants/strategy-memo.md) には経営会議向けメモのテンプレートが用意されています。

## 参考資料

- [SKILL.md](SKILL.md)
- [README.md](README.md)
- [references/frameworks-index.md](references/frameworks-index.md)
- [docs/index.html](docs/index.html)
- [examples/end-to-end-full-case.md](examples/end-to-end-full-case.md)
- [variants/strategy-memo.md](variants/strategy-memo.md)

## ライセンス

このリポジトリは [LICENSE](LICENSE) に従います。

## まとめ

このリポジトリは、AIに「コンサルタントのような発言」をさせるためのものではありません。AIに「構造化された思考」を持たせ、問題を分解し、証拠と仮説を分け、結論につなげるための実務知を提供するものです。

経営判断に悩んだとき、戦略を考えるとき、提案書を書きたいとき、このリポジトリはAIとの対話をより経営的に、より説得的にしてくれます。
