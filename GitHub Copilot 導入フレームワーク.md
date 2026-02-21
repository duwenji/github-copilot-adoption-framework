# GCAF（GitHub Copilot Adoption Framework）v1.0

## 0. エグゼクティブサマリ

*   **目的**：Copilotを“開発者の拡張（Augmentation）”として定着させ、**品質・速度・開発者体験**を同時に改善する。GitHub Copilotは、開発者の生産性を向上させるためのAIツールであり、コードの提案や補完を通じて開発プロセスを効率化します。これにより、開発者は反復的な作業から解放され、より創造的なタスクに集中できるようになります。さらに、導入後の効果を測定するための指標やベストプラクティスも提供されており、組織全体での価値を最大化することが可能です。 [measuring-the-impact-of-github-copilot](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

*   **導入原則**：
    1.  **段階導入**（Pilot→Scale）で学習しながら広げる。段階的な導入は、初期段階での学びを活かし、リスクを最小限に抑えながらスムーズに拡大するための重要な戦略です。これにより、組織はCopilotの効果を実証し、必要に応じてプロセスを調整することができます。 [enable-developers/drive-adoption](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [copilot-adoption](https://samqbush.github.io/copilot-adoption/)
    2.  **ガバナンス先行**（ポリシー/除外/監査/責任分界）。ガバナンスを先行させることで、Copilotの利用に伴うリスクを事前に管理し、組織全体での信頼性を確保します。これには、利用ポリシーの策定やコンテンツ除外ルールの設定が含まれます。 [manage-enterprise-policies](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies), [content-exclusion](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [copilot-trust-center](https://resources.github.com/ja/copilot-trust-center/)
    3.  **メトリクスで改善**（使用状況・受入率・PRサイクル）。メトリクスを活用することで、Copilotの導入効果を定量的に評価し、継続的な改善を図ることができます。これにより、開発プロセスの効率化や品質向上が実現します。 [copilot-metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [view-usage-and-adoption](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption), [measuring-the-impact-of-github-copilot](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

*   **成果物**：ポリシー、利用ガイド、教育、環境標準、KPIダッシュボード、改善バックログ。これらの成果物は、Copilotの導入と運用を成功させるための基盤となります。具体的には、利用ポリシーの策定や教育プログラムの提供、KPIダッシュボードを活用した効果測定が含まれます。 [roll-out-at-scale](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [copilot-usage-metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [prompt-engineering](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering)

***

## 1. CAF対応：GCAFの6つの視点（Perspectives）

AWS CAFの「観点」をCopilotに置き換え、**6視点×成果物**で標準化します。GitHub側にも“導入・測定・設計原則”が分散資料として存在するため、それを統合してCAF相当の枠組みにします。 [wellarchitected.github.com](https://wellarchitected.github.com/features/copilot/), [enable-developers/drive-adoption](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [measuring-the-impact-of-github-copilot](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

### 1) Business（価値・投資対効果）

**ゴール**：経営/管理層が投資判断できるように、価値仮説と測定方法を定義する。

**主要論点**
GitHub Copilotの導入効果を測定するための指標として、開発速度の向上（55%のタスク解決時間短縮）、コードレビューの効率化（67%の高速化）、コード品質の向上（85%の信頼性向上）が挙げられます。これらの指標は、開発者の生産性向上やチームのモチベーション維持に寄与します。また、GitHub Copilot Chatを活用することで、リアルタイムでのコードレビューやフィードバックが可能となり、開発プロセス全体の効率化が期待されます。さらに、GitHub Copilotの使用状況を可視化するダッシュボードやAPIを活用することで、導入効果を定量的に把握し、経営層への説明資料として活用できます。

**成果物（Artifacts）**

- 価値仮説・KPI定義書（後述のKPIセット）
- PoC評価レポート（Before/After）
- 導入判断メモ（リスク・費用・効果）

---

### 2) People（人材・組織・チェンジマネジメント）

**ゴール**：AIと協働できる開発者を増やし、学習曲線と抵抗感を下げる。

**主要論点**
GitHub Copilotの導入を成功させるためには、チャンピオンプログラムの運用やワークショップの開催が重要です。具体的には、導入前に成功指標を定義し、チャンピオンを育成することで、社内での普及を促進します。また、プロンプトエンジニアリングの基本を学ぶことで、開発者がCopilotを効果的に活用できるようになります。さらに、オンボーディング資料やFAQ、トラブルシューティングガイドを整備することで、導入初期の課題を軽減します。これにより、開発者がAIツールを活用するスキルを向上させ、組織全体の生産性を高めることができます。

**成果物**

- Copilot 利用ガイド（開発者版）
- Champion Program運用（FAQ、相談窓口、Tips配信）
- 研修（基礎：Prompt/レビュー/セキュア、応用：テスト生成/リファクタ/設計相談）
- “Promptパターン集”（例：テスト生成、既存コード説明、リファクタ方針、脆弱性観点レビュー）

---

### 3) Governance（ポリシー・知財・コンプライアンス）

**ゴール**：「使っていい/悪い」を明確にして、リスクを事前に潰す。

**主要論点**
GitHub Copilotの利用におけるリスク管理には、エンタープライズポリシーの策定が不可欠です。具体的には、機密情報や規制対象データをContent Exclusion機能で除外することで、AIが不適切なデータを参照するリスクを軽減します。また、Trust Centerを活用して、セキュリティやプライバシーに関する透明性を確保し、経営層や法務部門への説明責任を果たします。さらに、AI生成コードのレビュー基準を明確化し、通常のコードと同等の品質管理を行うことで、開発プロセス全体の信頼性を向上させます。

**成果物**

- Copilot利用ポリシー（目的、対象範囲、禁止事項、責任分界点）
- コンテンツ除外ルール（パス/拡張子/リポジトリ単位の方針）
- レビュー標準（AI生成コードも“通常のコード”として同等レビュー）
- 例外申請フロー（高リスク領域での利用手続き）

---

### 4) Platform（開発環境・標準化・拡張）

**ゴール**：Copilotが効果を出しやすい環境とリポジトリ標準を整える。

**主要論点**
GitHub Copilotの効果を最大化するためには、開発環境の標準化と拡張が重要です。具体的には、セットアップやトラブルシューティングの手順を明確化し、運用の効率化を図ります。また、Copilot Chatの活用方法を標準化することで、チーム全体の生産性を向上させます。さらに、VS Codeのprompt files（.prompt.md）を活用して、よく使う作業をテンプレート化し、社内でのプロンプト資産を構築します。これにより、開発者が効率的に作業を進められる環境を提供します。

**成果物**

- 標準IDE/拡張構成（推奨設定、社内テンプレ）
- リポジトリ標準（README、CONTRIBUTING、テスト方針、Lint/Format）
- プロンプト資産（prompt files、ガイド、例題集）

---

### 5) Security（セキュリティ・プライバシー・サプライチェーン）

**ゴール**：データ取り扱いと生成コードの安全性を担保する。

**主要論点**
GitHub Copilotのセキュリティを確保するためには、Trust Centerを活用して暗号化やデータ保持に関する透明性を確保することが重要です。また、Content Exclusion機能を利用して機密情報がAIの学習対象にならないように設定することで、データ漏洩リスクを軽減します。さらに、生成コードのレビューやテスト、SAST（静的解析ツール）を活用して、セキュリティリスクを早期に発見・対応する体制を整えます。これにより、開発プロセス全体の安全性を向上させることができます。

**成果物**

- セキュリティ利用ガイド（入力禁止：秘密情報、個人情報、鍵、顧客データ等）
- “AI生成コード”レビュー観点チェックリスト（認可/暗号/入力検証/依存関係/例外処理）
- 監査・証跡（ポリシー設定の記録、運用ログ方針）

---

### 6) Operations（運用・測定・改善）

**ゴール**：導入して終わりではなく、データで定着と改善を回す。

**主要論点**
GitHub Copilotの運用を最適化するためには、Copilot usage metricsを活用して採用状況や利用状況を可視化することが重要です。これにより、導入効果を定量的に把握し、改善点を特定できます。また、定期的なChampion会議や品質会議を通じて、現場からのフィードバックを収集し、改善バックログに反映させる仕組みを構築します。さらに、PoC（概念実証）から全社展開までの振り返りを行い、成功事例や課題を共有することで、継続的な改善サイクルを実現します。

**成果物**

- Copilot運用ダッシュボード（公式メトリクス＋社内BI）
- 定例（Champion会/品質会/改善バックログ）
- PoC→全社展開の振り返りテンプレ

---

## 2. KPI / メトリクス（測定設計）

「生産性は測りにくい」前提で、**テレメトリ＋サーベイ＋成果指標**を組み合わせます（公式もこの立場）。 [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)

### 2.1 Leading Indicators（先行指標：早期に効く）

*   アクティブユーザー、利用頻度、受入率、言語/IDE別傾向（Copilot usage metrics） [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [github.blog](https://github.blog/changelog/2025-10-28-copilot-usage-metrics-dashboard-and-api-in-public-preview/)
*   開発者アンケ（有用性/ブロッカー/満足度） [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

### 2.2 Lagging Indicators（遅行指標：成果）

*   PR throughput、time to merge 等（影響を見る） [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)
*   品質（欠陥混入率、レビュー指摘、セキュリティ検知など） [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/)

### 2.3 計測基盤

*   公式：ダッシュボード/API/NDJSON（プレビューである点・IDEテレメトリ依存を明示） [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [docs.github.com](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption), [github.blog](https://github.blog/changelog/2025-10-28-copilot-usage-metrics-dashboard-and-api-in-public-preview/)
*   参考：ソリューションアクセラレータ（メトリクス可視化） [github.com](https://github.com/microsoft/copilot-metrics-dashboard)

---

## 3. Copilot Metrics（詳細）

GitHub Copilot usage metricsは、Copilotの導入効果を可視化し、採用状況や利用パターンを追跡するデータセットです。以下の詳細情報を参考に、組織の導入効果を測定してください。

### Supported IDEs

Copilot usage metricsはIDEからのテレメトリに基づくため、以下のサポート対象IDEを利用する必要があります：
- **Visual Studio Code**: Version 1.101 以上 + Copilot Chat extension 0.28.0 以上
- **JetBrains IntelliJ**: Version 2024.2.6 以上 + Copilot extension 1.5.52-241 以上
- **Visual Studio**: Version 17.14.13 以上 + Copilot extension 18.0.471.29466 以上
- **Eclipse**: Version 4.31 以上 + Copilot extension 0.9.3.202507240902 以上
- **Xcode**: Version 13.2.1 以上 + Copilot extension 0.40.0 以上

**注意**: テレメトリが有効でないユーザーはメトリクスに計上されません。

### Data Freshness（データの鮮度）

Copilot usage metricsダッシュボードおよびAPIは定期的に更新されます：
- **標準**: データは発生から3暦日以内に利用可能（例：月曜日のデータは木曜日までに表示）
- **遅延**: 週末を跨ぐ場合など、最大4暦日の遅延が生じる可能性があります
- **プレビュー期間中**: 仕様変更の可能性があるため、本番依存には注意が必要です

### What Does the Data Measure?（測定内容）

Copilot usage metricsは、以下の5つの主要カテゴリで構成されます：

**1) Adoption（採用率）**
- Daily Active Users（DAU）: 特定の日にCopilotと相互作用したユニークユーザー数
- Weekly Active Users（WAU）: 週単位のユーザー数
- 初期段階では、この指標が継続的に上昇することが重要です

**2) Engagement（利用頻度・深さ）**
- Average requests per active user: 平均的なユーザーがChat/Completionを利用した頻度
- Breadth across features: 複数の機能（Chat、Completions、Agents など）を利用しているか
- 単なる利用者数ではなく、実際の使用パターンを反映した指標

**3) Acceptance Rate（受入率）**
- Inline suggestions acceptance rate: エディタ提案の受け入れ率
- Chat follow-up rate: Chat回答への追加操作率
- **信頼性の指標**: 提案が実務的に有用かどうかを示す

**4) Lines of Code (LoC)（コード生成量）**
- Lines suggested: Copilotが提案したコード行数
- Lines added: 実際に受け入れられ挿入されたコード行数
- Lines deleted: Copilot支援で削除されたコード行数
- **方向指標**: 生産性への定性的な見方を提供（定量的因果関係は限定的）

**5) Pull Request Lifecycle Metrics（PR関連指標）**
- PR creation count: PR created by Copilot（準備中等）
- PR merge count: マージされたPR数
- Median time to merge: 中央値マージ時間
- Code review suggestion activity: レビュー提案の活動量
- **成果指標**: Copilot活用がデリバリースピード・品質に与える影響を測定

### How Can I Use These Metrics?（活用方法）

これらのメトリクスを組み合わせて、以下の問いに答えることができます：

| 質問 | 参考メトリクス |
|------|---------------|
| チームはCopilotをコンスタントに利用しているか？ | Daily/Weekly Active Users |
| どの機能が最大の価値を提供しているか？ | Requests per feature, Agent adoption |
| 開発者はCopilotの出力を信頼しているか？ | Acceptance rate trends over time |
| トレーニングや施策は効果を上げているか？ | Adoption and engagement growth |
| Copilotはデリバリースピードに影響しているか？ | PR merge counts, median time to merge, cycle time |

**パターン分析のコツ**:
- 単一の数字に注目するのではなく、複数の信号を組み合わせて解釈する
- 例：DAUが安定 + 受入率が上昇 = 信頼度向上 + 実務的価値の確立
- トレンド（方向）を重要視し、絶対値よりも変化率に着目する

### 計測基盤と制限

**公式ツール**:
- **ダッシュボード**: GitHub Enterprise/Organization管理画面で4週間（28日）の傾向を可視化
- **REST API**: プログラマティックアクセスで詳細なイベント テレメトリを取得
- **NDJSON Export**: 生データをBI/分析ツール用に抽出

**重要な制限**:
- **IDE テレメトリ依存**: 他のCopilot surface（Web上のChat、Mobile、CLIなど）は含まれない
- **ライセンス/シート管理データは別**: 計測されるのは「利用活動」のみで、「割り当て」ではない
- **プレビュー状態**: 仕様や保持期間が変更される可能性あり

### 参考資料

詳細については、以下を参照してください：
- [GitHub Copilot usage metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)
- [Viewing the Copilot usage metrics dashboard](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption)
- [Measuring the impact of GitHub Copilot](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

---

## 4. 導入フェーズ（Phases）：GCAFの標準ロードマップ

公式の“adoptionを駆動するプロセス”は段階導入を推奨しているため、GCAFもフェーズ制にします。 [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [samqbush.github.io](https://samqbush.github.io/copilot-adoption/)

### Phase 0：Prepare（準備）

**目的**：導入目的・対象・統制・測定の土台を固める。\n**主タスク** [resources.github.com]

**目的**：導入目的・対象・統制・測定の土台を固める。

**主タスク** [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies), [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)

*   ユースケース選定（テスト生成、定型コード、リファクタなど）
*   ポリシー草案（禁止事項、責任分界、除外、監査） [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies), [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [copilot.gi...trust.page](https://copilot.github.trust.page/faq)
*   KPIとベースライン（PR時間、開発者アンケ、使用率） [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)

**Exit criteria（次へ進む条件）**

*   ポリシー承認（暫定で可）
*   PoC設計（対象チーム、期間、評価方法）

---

### Phase 1：Pilot（小規模実証）

**目的**：安全に試し、学びを“標準”に落とす。

**主タスク** [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [samqbush.github.io](https://samqbush.github.io/copilot-adoption/)

*   小規模チームへ付与、環境セットアップ支援 [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption)
*   トレーニング（プロンプト・レビュー・セキュア） [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering), [learn.microsoft.com](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/), [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/)
*   コンテンツ除外（.env/鍵/契約資料など） [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/cppblog/configure-github-copilot-access-via-content-exclusion/)
*   メトリクス収集開始（usage metrics、アンケ） [copilot-usage-metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

**Exit criteria**

*   “やってよい/悪い”が現場で理解される
*   KPI初期値と改善仮説が立つ

---

### Phase 2：Early Scale（拡大：複数チームへ）

**目的**：Championと標準テンプレで“自走”を作る。

**主タスク** [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/all-things-azure/adopting-github-copilot-at-scale/)

*   Champion育成・コミュニティ化 [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/all-things-azure/adopting-github-copilot-at-scale/)
*   標準プロンプト資産（prompt engineering指針、prompt files） [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering), [code.visua...studio.com](https://code.visualstudio.com/docs/copilot/customization/prompt-files)
*   ルールの明文化（例外/高リスク領域の扱い） [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/), [copilot.gi...trust.page](https://copilot.github.trust.page/faq)
*   ダッシュボードでチーム差を特定し、支援を厚くする [docs.github.com](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption), [github.blog](https://github.blog/changelog/2025-10-28-copilot-usage-metrics-dashboard-and-api-in-public-preview/)

---

### Phase 3：Enterprise Scale（全社展開）

**目的**：統制と可視化を“仕組み化”し、横展開する。

**主タスク** [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies), [copilot-usage-metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [wellarchit...github.com](https://wellarchitected.github.com/features/copilot/)

*   Enterprise AI Controls（ポリシー）を統一 [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies)
*   Content Exclusionの標準テンプレ適用 [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion)
*   運用（ライセンス付与/ヘルプ/FAQ/教育）を定常化 [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption)
*   メトリクス定例（採用率・受入率・PRサイクル） [copilot-usage-metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics), [github.blog](https://github.blog/changelog/2025-10-28-copilot-usage-metrics-dashboard-and-api-in-public-preview/)

---

### Phase 4：Optimize（最適化・定着）

**目的**：測定→改善→再教育のループで効果を伸ばし続ける。

**主タスク** [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [docs.github.com](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption)

*   ESSPの考え方で障壁を特定し改善（品質/速度/幸福） [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)
*   低採用チームへの集中支援（プロンプト/環境/タスク設計）
*   成功パターンをプロンプト資産・テンプレに反映 [code.visua...studio.com](https://code.visualstudio.com/docs/copilot/customization/prompt-files), [github.com](https://github.com/github/awesome-copilot)

---

## 5. ガードレール（GCAF標準ポリシーひな型）

ここは社内の法務/セキュリティと合意しやすいよう、一次情報（Trust Center/公式Docs）を根拠にして構造化します。 [copilot.gi...trust.page](https://copilot.github.trust.page/faq), [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies), [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion)

### 3.1 利用範囲（推奨/条件付き/非推奨）

*   **推奨**：テスト生成、ボイラープレート、リファクタ補助、ドキュメント下書き [docs.github.com](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat), [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)
*   **条件付き**：認可/暗号/決済/安全性クリティカル（必ず人間の設計・レビュー・テスト） [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/), [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)
*   **非推奨（原則禁止）**：秘密情報・個人情報・顧客データを含む入力（必要なら除外/ダミー化） [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [resources.github.com](https://resources.github.com/ja/copilot-trust-center/)

### 3.2 コンテンツ除外（必須設定例）

*   例：`**/.env`、鍵/証明書、契約・要件文書、顧客データスキーマ、認可設定など
*   Content Exclusionは、除外ファイルでの提案無効＋他ファイルへの影響遮断＋Chat/コードレビューにも影響する。 [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/cppblog/configure-github-copilot-access-via-content-exclusion/)

### 3.3 責任分界（必須明記）

*   生成物の最終責任は開発チーム（Copilotは補助）
*   AI生成コードも通常のコードと同等のレビュー・テストを必須とする [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/), [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)

---

## 6. Enablement（教育・定着の標準パッケージ）

公式の“Drive adoption”の流れをベースに、社内運用に落とし込みます。 [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/all-things-azure/adopting-github-copilot-at-scale/)

### 4.1 30/60/90日プラン（例）

*   **30日**：Champion任命、基礎研修、FAQ/Slack/Teams窓口 [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [learn.microsoft.com](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/)
*   **60日**：ユースケース別ワークショップ（テスト/リファクタ/設計相談） [docs.github.com](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat), [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering)
*   **90日**：メトリクスレビュー会、成功事例共有、プロンプト資産化 [docs.github.com](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption), [code.visua...studio.com](https://code.visualstudio.com/docs/copilot/customization/prompt-files)

### 4.2 プロンプト標準（GCAF Prompting Standard）

*   「最初に目的→制約→例→分割→曖昧さ排除」など、GitHub Docsの推奨に沿う [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering), [github.blog](https://github.blog/developer-skills/github/how-to-write-better-prompts-for-github-copilot/)
*   Chat利用の基本（@workspace、#fileなど）を標準化 [docs.github.com](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat), [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering)

---



## 7. 最小実装チェックリスト（MRT：Minimum Required Tasks）

「最初から作り込みすぎない」ために、チェックリストで最低限を定義します。下記は“Minimum Required Tasks for Copilot Adoption”の思想を取り込み、GCAFとして再構成しています。 [samqbush.github.io](https://samqbush.github.io/copilot-adoption/), [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption)

### 7.1 Pilot前に必須（Must）

*   ポリシー（AI Controls）方針がある [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies)
*   Content Exclusion（機密ファイル）設計 [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/cppblog/configure-github-copilot-access-via-content-exclusion/)
*   KPI/ベースライン定義（測定可能な範囲を明確化） [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/), [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)
*   教育（プロンプト・レビュー・セキュリティ） [learn.microsoft.com](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/), [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering), [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/)

### 7.2 Scale前に必須（Must）

*   Champion運用（支援導線） [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [devblogs.m...rosoft.com](https://devblogs.microsoft.com/all-things-azure/adopting-github-copilot-at-scale/)
*   メトリクスダッシュボードで採用状況を確認 [docs.github.com](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption), [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)
*   例外申請・高リスク領域のガードレールが運用されている [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/), [copilot.gi...trust.page](https://copilot.github.trust.page/faq)

---

## 8. 用語リスト（Glossary）

*   **GCAF（GitHub Copilot Adoption Framework）**：本資料で定義した、Copilot導入のための実務フレームワーク。
*   **CAF（Cloud Adoption Framework）**：導入を複数視点で整理する枠組み。本資料では考え方をCopilot導入に適用。
*   **PoC（Proof of Concept）**：本格導入前に有効性やリスクを小規模で検証する実証。
*   **KPI（Key Performance Indicator）**：導入効果を測るための重要指標。
*   **ESSP**：GitHub Resourcesで示される、Copilot効果測定の考え方（段階的に評価・最適化するアプローチ）。
*   **Champion**：現場展開をリードする推進担当者（相談窓口・事例共有・教育支援）。
*   **AI Controls**：GitHub Enterprise/Organizationで設定するCopilotのポリシー制御。
*   **Content Exclusion**：Copilotの提案・Chat文脈から特定コンテンツを除外する機能。
*   **Prompt Engineering**：目的・制約・文脈を明確にして、回答品質を高めるプロンプト設計手法。
*   **prompt files（.prompt.md）**：VS Code等で再利用可能なプロンプトテンプレート資産。
*   **@workspace / #file**：Copilot Chatでワークスペース全体や特定ファイルを文脈指定するための記法。
*   **SAST（Static Application Security Testing）**：静的解析でコードの脆弱性を検出する手法。
*   **Leading Indicators（先行指標）**：導入初期に変化を捉えやすい指標（利用率・受入率など）。
*   **Lagging Indicators（遅行指標）**：結果として現れる指標（PRサイクル・品質指標など）。
*   **NDJSON（Newline Delimited JSON）**：1行1JSONで構成されるデータ形式。メトリクス出力の取り回しに利用。
*   **MRT（Minimum Required Tasks）**：導入時に最低限実施すべき必須タスク群。
*   **Copilot EMU (Enterprise Managed Users)**:
    企業が自社のIDプロバイダー（Okta, Microsoft Entra ID等）を通じて作成・管理する専用アカウントで、GitHub Copilotを利用する運用形態。GitHub Enterprise Cloudの法人向け高度管理機能（EMU）の一部。
    *  主な特徴:
        *  一元的なアイデンティティ管理: 社内アカウントでシングルサインオン（SSO）が可能。退職・異動時のアクセス権削除もIdP側で即座に反映される。
        *  セキュリティの強化: アカウントが企業テナント内に完全に隔離されるため、リポジトリへのアクセス制限やセキュリティポリシーを強力に適用可能。
        *  コンプライアンス管理: 管理者が全ユーザーのCopilot利用状況やポリシー設定（コードスニペットの再利用許可など）を一括で統制できる。
        *  外部との隔離: 原則として個人のGitHubアカウントとは切り離された「企業専用アカウント」として機能し、機密情報の保護を優先した設計。
    *  導入メリット:
    大規模組織におけるライセンス管理の自動化、セキュリティ・ガバナンスの向上、および監査対応の容易化。

*   **GitHub Copilot code review**: 
    GitHub Copilotが提供する、プルリクエスト（PR）やエディタ上のコードに対して、バグの検出、パフォーマンス改善、セキュリティの脆弱性チェックを自律的に行うAIエージェント。
    *  主な特徴:
        *  自律的なレビュー: PR作成時に自動で起動し、変更差分を分析して人間のようなコメント（レビュー）を残す。
        *  リポジトリ全体の理解: 個別のファイルだけでなく、プロジェクト全体のコンテキストに基づいた高度なフィードバックを行う。
        *  カスタム指示: .github/copilot-instructions.md 等のファイルを通じて、プロジェクト固有のコーディング規約や設計ルールを学習させることが可能。
        * マルチプラットフォーム: GitHub.com 上でのPRレビューに加え、VS Code などのIDE上でもコミット前のセルフチェックとして利用できる。
    *  導入メリット:
    レビューサイクルの高速化、人的ミスの削減、およびチーム内のコード品質の標準化。

*   **seat management data（シート管理データ）**:
    GitHub Copilotのライセンス（シート）の割り当て状況や利用状況に関するデータ。管理者がGitHubの管理画面やAPIを通じて確認できる。
    *  主なデータ内容:
        *  割り当て済みのユーザー: 現在誰がシートを保有しているかのリスト。
        *  最終アクティビティ日 (last_activity_at): ユーザーが最後にCopilotを（IDE等で）利用した日時。
        *  利用状況メトリクス: 提案の受け入れ率やチャットの使用回数など、投資対効果（ROI）を測定するための統計データ。
        *  非アクティブなシート: 割り当てられているが一定期間利用がないアカウントの特定。 
    *  活用シーン:
        *  コスト最適化: 利用していないユーザーのシートを回収し、必要なメンバーに再割り当てする。
        *  ガバナンス: 組織全体の利用傾向を把握し、導入の効果測定やセキュリティポリシーの適用状況を確認する。 

*   **SCIM（System for Cross-domain Identity Management）**:
    複数のクラウドサービスやドメイン間で、ユーザーの作成・更新・削除（プロビジョニング）を自動化するためのオープン標準プロトコル。 
    *  GitHub Copilotにおける役割:
        *  自動プロビジョニング: 社内ディレクトリ（IdP）に新入社員を追加すると、GitHubアカウントとCopilotライセンスが自動的に作成・付与される。
        *  自動停止（デプロビジョニング）: 従業員が退職して社内アカウントが無効になると、GitHubのアクセス権やCopilotのシートも即座に自動回収される。
        *  属性同期: 氏名やメールアドレス、所属グループなどの変更がリアルタイムでGitHub側に同期される。 
    *  主なメリット:
        *  運用の効率化: 管理者がGitHubの管理画面で一人ずつユーザーを追加・削除する手間がなくなる。
        *  セキュリティ向上: 退職者のアカウント削除漏れを防ぎ、不要なアクセス権が残るリスクを排除できる。
        *  ライセンスコストの最適化: 利用資格がなくなったユーザーから自動でシートを回収できる。

*   **Git Credential Manager (GCM)**:
    Git操作（clone, push, pullなど）における認証プロセスを簡略化・セキュアにするためのオープンソースの資格情報ヘルパー。
    *  主な特徴:
        *  多要素認証（MFA）のサポート: ブラウザベースのログインを介して、GitHubの2要素認証やSSO（SAML/EMU環境）をスムーズに処理できる。
        *  安全な保存: OS標準のキーチェーン（Windows Credential ManagerやmacOS Keychainなど）に認証情報を暗号化して保存するため、パスワードを平文で管理する必要がない。
        *  個人アクセストークン（PAT）の自動生成: ユーザーが手動でトークンを発行・コピー＆ペーストしなくても、ログイン操作だけで一時的なトークンを自動で取得・利用する。
        *  GitHub Copilotとの親和性: GitHub Enterprise Cloud (EMU) 環境など、高度な認証が求められる環境でGitを操作する際のデファクトスタンダードとなっている。 
    *  導入メリット:
        *  認証エラーによる作業の中断を防ぎ、複雑な認証設定（SSO等）を意識することなくコマンドラインからのGit操作を可能にする。


*   **Copilot Extensions**:
    GitHub Copilot Chatの機能を拡張し、外部サービスと双方向にやり取りすることを可能にするエージェントベースの連携機構。
    *  仕組みの仕組み（アーキテクチャ）:
        *  呼び出し（インテント解析）: ユーザーがChatで @extension-name と入力すると、GitHubがその意図を解釈します。
        *  リクエストの転送: GitHubは、その拡張機能をホストしている外部サーバー（App）に対して、ユーザーの質問や文脈をHTTPSリクエストとして送信します。
        *  外部処理: 拡張機能側（API）で、自社データの検索やツールの操作（例：デプロイ、チケット作成）を実行し、回答を生成します。
        *  回答の表示: 外部サーバーからのレスポンスをGitHub Copilotが受け取り、リッチなテキストやUIとしてユーザーに表示します。
    *  主な特徴:
        *  スキルセットの追加: 「Sentryでエラーログを調べる」「Azureにリソースを作成する」といった、AIモデル単体では不可能な「アクション（実行）」が可能になります。
        *  GitHub Appとしての実装: Extensionsは GitHub App として構築されるため、認証や権限管理が厳格に行われます。
        *  カスタム拡張の作成: 企業は自社専用の拡張機能（Internal Extension）を開発し、社内のドキュメント検索や独自のデプロイフローと連携させることができます。
    *  導入メリット:
        *  コンテキストの切り替え（コンテキストスイッチ）を最小限に抑え、開発に必要なすべての操作をチャットインターフェースに統合できる。

---

# 付録A：参照資料（公式・準公式・ベンダー提供）

## A-1. 公式（GitHub Docs / GitHub Resources / GitHub Blog）

*   **Driving GitHub Copilot adoption in your company**（展開・定着プロセス）  
    <https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption> [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption)
*   **Measuring the impact of GitHub Copilot（ESSP）**（測定フレームワーク）  
    <https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/> [resources.github.com](https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/)
*   **GitHub Well-Architected – Copilot**（設計原則：生産性/ガバナンス/セキュリティ等）  
    <https://wellarchitected.github.com/features/copilot/> [wellarchit...github.com](https://wellarchitected.github.com/features/copilot/)
*   **Managing policies and features for GitHub Copilot in your enterprise**（AI Controls/ポリシー）  
    <https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies> [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies)
*   **Content exclusion for GitHub Copilot**（除外の仕様と制限）  
    <https://docs.github.com/en/copilot/concepts/context/content-exclusion> [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion)
*   **GitHub Copilot usage metrics**（メトリクス：ダッシュボード/API/NDJSON、範囲・制限）  
    <https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics> [docs.github.com](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics)
*   **Viewing the Copilot usage metrics dashboard**（見方・運用）  
    <https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption> [docs.github.com](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/view-usage-and-adoption)
*   **Prompt engineering for GitHub Copilot Chat**（プロンプト指針）  
    <https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering> [docs.github.com](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering)
*   **GitHub Copilot Trust Center（日本語ページ含む）**（セキュリティ/プライバシー/IP/透明性）  
    <https://resources.github.com/ja/copilot-trust-center/>   
    <https://github.blog/news-insights/policy-news-and-insights/how-to-responsibly-adopt-github-copilot-with-the-github-copilot-trust-center/>   
    <https://copilot.github.trust.page/faq> [resources.github.com](https://resources.github.com/ja/copilot-trust-center/) [github.blog](https://github.blog/news-insights/policy-news-and-insights/how-to-responsibly-adopt-github-copilot-with-the-github-copilot-trust-center/) [copilot.gi...trust.page](https://copilot.github.trust.page/faq)
*   **Copilot usage metrics dashboard and API in public preview**（プレビュー告知・範囲）  
    <https://github.blog/changelog/2025-10-28-copilot-usage-metrics-dashboard-and-api-in-public-preview/> [github.blog](https://github.blog/changelog/2025-10-28-copilot-usage-metrics-dashboard-and-api-in-public-preview/)
*   **How to write better prompts for GitHub Copilot**（実例中心のプロンプト改善）  
    <https://github.blog/developer-skills/github/how-to-write-better-prompts-for-github-copilot/> [github.blog](https://github.blog/developer-skills/github/how-to-write-better-prompts-for-github-copilot/)

## A-2. 準公式/コミュニティ（実務者の枠組み）

*   **Minimum Required Tasks for Copilot Adoption**（大規模導入チェックリスト）  
    <https://samqbush.github.io/copilot-adoption/> [samqbush.github.io](https://samqbush.github.io/copilot-adoption/)
*   **Awesome GitHub Copilot**（コミュニティのプロンプト/設定資産）  
    <https://github.com/github/awesome-copilot> [github.com](https://github.com/github/awesome-copilot)

## A-3. ベンダー提供 / 解説記事（参考：非公式）

*   **Atmosera – GitHub Copilot Adoption Framework**（“フレームワーク”を名乗るベンダー資料）  
    <https://www.atmosera.com/accelerate/github-copilot-adoption-framework/> [atmosera.com](https://www.atmosera.com/accelerate/github-copilot-adoption-framework/)
*   **Microsoft Dev Blog：Adopting Copilot at Scale**（大規模導入のTips）  
    <https://devblogs.microsoft.com/all-things-azure/adopting-github-copilot-at-scale/> [devblogs.m...rosoft.com](https://devblogs.microsoft.com/all-things-azure/adopting-github-copilot-at-scale/)
*   **Microsoft Dev Blog：Content Exclusion**（除外機能の解説）  
    <https://devblogs.microsoft.com/cppblog/configure-github-copilot-access-via-content-exclusion/> [devblogs.m...rosoft.com](https://devblogs.microsoft.com/cppblog/configure-github-copilot-access-via-content-exclusion/)
*   **Copilot security controls（TechCommunity）**（導入懸念の説明補助）  
    <https://techcommunity.microsoft.com/blog/azuredevcommunityblog/demystifying-github-copilot-security-controls-easing-concerns-for-organizational/4468193> [techcommun...rosoft.com](https://techcommunity.microsoft.com/blog/azuredevcommunityblog/demystifying-github-copilot-security-controls-easing-concerns-for-organizational/4468193)
*   **Governance Model for Enterprises（解説）**  
    <https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/> [c-sharpcorner.com](https://www.c-sharpcorner.com/article/github-copilot-governance-model-for-enterprises/)
*   **copilot-metrics-dashboard（アクセラレータ）**  
    <https://github.com/microsoft/copilot-metrics-dashboard> [github.com](https://github.com/microsoft/copilot-metrics-dashboard)

---

# 次にできること（おすすめ）

このGCAFを「社内標準」にするなら、次の2点を追加すると一気に実戦投入できます。

1.  **社内向けテンプレ一式**（Word/Confluence想定）

*   利用ポリシーひな型（禁止事項、責任分界、例外手続き）
*   Content Exclusion 推奨パターン集
*   レビュー観点チェックリスト
*   30/60/90日導入計画書

2.  **PowerPoint版（AWS CAF風の構成）**

*   6視点の1枚絵（CAFライク）
*   フェーズ別ロードマップ
*   KPI/ダッシュボード例

---

## 質問（最小限）

GCAFをあなたの組織に合わせて「完成版」にするため、次だけ教えてください。

1.  対象は **Copilot Business** / **Copilot Enterprise** のどちら想定ですか？（ポリシー・機能差があるため） [docs.github.com](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies), [docs.github.com](https://docs.github.com/en/copilot/concepts/context/content-exclusion)
2.  まずの対象は **全社**ですか？それとも \*\*特定部門（例：開発部門のみ）\*\*ですか？ [docs.github.com](https://docs.github.com/en/copilot/tutorials/roll-out-at-scale/enable-developers/drive-adoption), [samqbush.github.io](https://samqbush.github.io/copilot-adoption/)

回答があれば、上記GCAFを **あなたの導入条件に最適化した“社内配布版（章立て・テンプレ付き）”** に仕上げます.
