# Frontier-Grade Open Weights ── フロンティア級のオープンウェイトモデルは、開かれたのか

> **"They matched the frontier. But no one can hold them."**
> （フロンティアには、並んだ。だが、誰の手にも渡っていない）

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Language](https://img.shields.io/badge/Language-English%20%7C%20Japanese-blue)](https://github.com/Leading-AI-IO/frontier-grade-open-weights)

![cover](../../assets/ogp_design.png)

<br/>

---

# 序章: 開かれた、と誰もが言った日

2026年7月17日、北京。<br/>
中国のAI企業・月之暗面（Moonshot AI）が、2兆8,000億パラメータの新モデル「Kimi K3」を発表した。<br/>
学習済みモデルの中身を公開したオープンウェイト型としては、世界最大である。<br/>
そしてロイターは、その性能を「アンソロピックの最先端モデル『フェイブル』に迫る」と報じた。

市場は、その日のうちに答えを出した。<br/>
オープンウェイトがフロンティアに並んだという一文が、数千億ドルの前提を揺らした。<br/>
だが、その日、もう一つの事実があった。

**重みは、公開されていなかった。**

独立評価機関Artificial Analysisは同時点でKimi K3を「**weights not publicly available**（重みは公開されていない）」と表示し、<br/>
別の独立評価機関Vals AIに至っては、ライセンス種別を「**Proprietary（プロプライエタリ）— contact us to get access**」と記載していた。<br/>
Moonshot自身の公式ブログが約束したのは、**2026年7月27日**に全重みを公開するという予定である。

世界最大のオープンウェイトモデルは、発表された日、まだオープンではなかった。<br/>
本書は、この10日間の空白から始まる。

## 世界最大のオープンウェイトが、フロンティアに並んだ

まず、何が本当に起きたのかを確定させる。

独立機関Artificial Analysisの測定によれば、Kimi K3のIntelligence Indexは**57**、189モデル中**第4位**。<br/>
上位にいるのはClaude Fable 5（60）とGPT-5.6 Sol（59）であり、<br/>
K3はGPT-5.5・Claude Opus 4.8と**同等の水準**に着地した。<br/>
別の独立機関Vals AIのVals Indexでは**74.70%（±0.96）**で、38モデル中**2位**。<br/>
さらにArena.aiのFrontend Code Arena——人間がブラインドで優劣を選ぶ評価——では、**K3がClaude Fable 5を上回り首位**を取った。

ここで一点、正確を期す。<br/>
「フェイブル5に迫る」「Opus 4.8とGPT-5.6 Solを大幅に上回る」という言葉のうち、<br/>
**独立機関が測ったのは総合指数とアリーナ順位だけ**である。<br/>
Moonshot自身のテクニカルブログは、<br/>
GPUカーネル最適化などの自社コーディングベンチマークでOpus 4.8とGPT-5.6 Solを上回るとしつつ、<br/>
**総合性能ではClaude Fable 5に及ばない**と自己評価している。<br/>
つまり「超えた」と報じられている部分は、当事者自身が超えていないと書いている領域を含む。

自己申告と独立測定の境界は、もっと露骨な形でも現れる。<br/>
DeepSWE Leaderboardでは、K3は67.5%で3位に掲載されている。<br/>
だが同じページには、こう明記されている——**Verified 0 / Self-reported 9**。<br/>
検証済みはゼロ件。掲載されている9件すべてが自己申告である。

なぜ、この区別にこだわるのか。<br/>
この種の衝撃では、数字が独り歩きする。<br/>
「中国のオープンモデルがClaudeを抜いた」という物語は分かりやすく、拡散しやすい。<br/>
だが、独立測定が示しているのは「総合4位」であり、「特定ドメインでの首位」だ。<br/>
本書は、熱狂に乗るためではなく、熱狂の**構造**を理解するために書かれている。<br/>
だからこそ、最初の数字から正確であることにこだわる。

そして、正確であろうとしたとき、より重要な事実が現れる。<br/>
**「オープンウェイトは6ヶ月遅れる」という通説は、すでに死んでいた。**<br/>
独立研究機関Epoch AIの計測によれば、オープンとクローズドの能力差は、<br/>
2023年1月から2025年10月までの平均で**3.5ヶ月**（ECI差7ポイント）、<br/>
2026年1月から5月28日までで平均**4ヶ月**（ECI差8ポイント）である。<br/>
Kimi K3は突然変異ではない。3年かけて詰められた距離の、到達点にすぎない。

だが、性能が並んだことと、それが手に渡ることは、別の話だ。<br/>
2026年7月17日に起きたことを、一枚に整理する。

```mermaid
graph LR
    A["2026/7/17<br/>Kimi K3 発表<br/>2.8兆パラメータ<br/>オープンウェイト世界最大"] --> B["独立測定<br/>──────<br/>AA Index 57／189中4位<br/>Vals Index 74.70%／38中2位<br/>Frontend Code Arena 首位"]
    A --> C["自己申告<br/>──────<br/>DeepSWE 67.5%／3位<br/>Verified 0・Self-reported 9"]
    A --> D["重みの現在地<br/>──────<br/>weights not publicly available<br/>公開予定 2026/7/27"]
    D --> E["実行の要件<br/>──────<br/>64アクセラレータ以上を推奨<br/>BF16なら約5.6TB"]
    B --> F{"特権的なオープン<br/>──────<br/>並んだ。だが、渡っていない"}
    C --> F
    E --> F
    F --> G["現実の利用形態<br/>──────<br/>ホスト型API<br/>$3 / M in・$15 / M out"]

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style C fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style D fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style E fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style F fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style G fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

独立測定が届いた領域は明るく、自己申告と物理的制約は暗いまま残る。<br/>
そして、すべての経路が一点に収束する。<br/>
発表された日、世界最大のオープンウェイトモデルへの唯一の現実的な入口は、月之暗面のAPIだった。

## 本書が論じる「特権的なオープン」とは何か

では、フロンティアに並んだそのモデルを、あなたは動かせるのか。

Moonshotは公式ブログに、こう書いている。<br/>
推論効率は大きな高帯域通信ドメインの恩恵を受けるため、**64アクセラレータ以上のスーパーノード構成での展開を推奨する**、と。<br/>
2.8兆パラメータの重みは、BF16なら約5.6TB、INT8でも約2.8TB、INT4でも約1.4TBの保存容量を要する（総パラメータ数からの算術推計）。<br/>
**ダウンロードできることと、動かせることは、別である。**<br/>
大半のユーザーにとって、現実的な選択肢はホスト型API——つまり、月之暗面に課金することだけだ。<br/>
入力$3/M、出力$15/M。オープンウェイトモデルは、有料APIとして売られている。

本書は、この状態を一語で捉える。「**特権的なオープン（Privileged Open）**」だ。

特権的なオープンとは、**重みが公開されるという意味では確かに開かれているが、<br/>
それを保有し、動かし、改変する能力が一部の主体に集中したままである状態**を指す。<br/>
誰も所有していない。だが、誰でも使えるわけでもない。<br/>
公開は事実であり、到達は虚構である。

なぜ「オープンウェイト」という既存の語ではなく、あえて「特権的なオープン」と呼ぶのか。<br/>
それは、この議論が「オープンか、クローズドか」の二項で語られる限り、<br/>
**何が本当に移動したのかを永久に見誤る**からだ。<br/>
移動したのは、モデルの所有権ではない。移動したのは、**希少性の在処**である。<br/>
賢さは希少でなくなった。では、いま何が希少なのか。<br/>
この一語に、本書のすべてが詰まっている。

| | 通説としての「オープン化」 | 特権的なオープン（本書の観測） |
|---|---|---|
| 重みの公開 | 公開＝誰でも入手できる | 公開は予定。入手と実行は別問題 |
| 実行環境 | ローカルで動く | 64アクセラレータ級のスーパーノード推奨 |
| 実質的な利用形態 | セルフホスト | ホスト型API（$3/$15）への課金 |
| 検証可能性 | 誰でも再現できる | 重み公開まで独立検証は不能 |
| ライセンス | オープンソース同等 | K3の正式条文は未確認 |
| 帰結 | 知能の民主化 | 知能の再集中 |

※本表は2026年7月18日時点の観測である。重みは7月27日に公開され、ライセンス条文（Kimi K3 License）も同時に開示された。実行環境の要件は変わっていない。第3章・第4章の追記を参照。

## 本書の読者と地図

本書は、次の3者のために書かれている。

* 第一に、**「中国のオープンモデルが来た。うちの戦略は変えるべきか」と問われている経営層・AI戦略責任者**。
変えるべき部分と、変えなくていい部分がある。データは、その線を明確に示している。

* 第二に、**AIラボという産業の行方に資本や職業人生を張っている投資家・事業開発者・エンジニア**。
「プロプライエタリは崩壊する」も「何も変わらない」も、どちらもデータに支持されていない。

* 第三に、**AIの規制と地政学を、報道の見出しではなく構造として理解したい人**。
米国のフロンティアは公開前に事実上の審査を通る。そして審査には、外側がある。

本書の地図はこうだ。<br/>
まず、距離が縮み、そして安定したという事実を確定させる（第1章）。<br/>
次に、その事実を誰が測ったのかを問い、測定そのものの壁を見る（第2章）。<br/>
そして、公開されてなお渡らない理由を、**物理の壁**（第3章）と**制度の壁**（第4章）として解剖する。<br/>
続いて、賢さが希少でなくなった後にAIラボが何を売っているのかを収益の一次データで検証し（第5章）、<br/>
その最大の争点である蒸留が、**証拠の壁**に阻まれていることを示す（第6章）。<br/>
最後に、**審査の壁**の外側で何が起きているのか（第7章）、<br/>
そして開放が**国家の壁**を越える言語になった日（第8章）へ進む。

壁は、物質から言説へ、個人から国家へと拡大していく。<br/>
だが、どの層でも同じ命題が反復される。<br/>
フロンティアは、開かれた。だが「オープン」にはなっていない。<br/>
この二つの文が同時に真である世界で、何が希少で、誰が勝つのか。<br/>
一次データと構造から、順に解き明かしていく。

### 参考文献

1. ロイター「中国ＡＩの月之暗面が新モデル発表、『フェイブル』に迫る性能」（2026年7月17日）
2. Moonshot AI「Kimi K3 Tech Blog: Open Frontier Intelligence」（2026年7月16日）
   <https://www.kimi.com/blog/kimi-k3>
3. Artificial Analysis「Kimi K3 – Intelligence, Performance & Price Analysis」（weights not publicly available）
   <https://artificialanalysis.ai/models/kimi-k3>
4. Vals AI「Kimi K3」（Vals Index 74.70% ±0.96／38モデル中2位／License type: Proprietary）
   <https://www.vals.ai/models/kimi_kimi-k3>
5. LLM Stats「DeepSWE Leaderboard」（K3 67.5%・3位／Verified 0・Self-reported 9）
   <https://llm-stats.com/benchmarks/deepswe>
6. Epoch AI「Open-weight models lag state-of-the-art by around 3 months on average」（2025年10月30日）
   <https://epoch.ai/data-insights/open-weights-vs-closed-weights-models>
7. Epoch AI「Open models lag state-of-the-art closed models by 4 months」（2026年5月29日）
   <https://epoch.ai/data-insights/open-closed-eci-gap>

<br/>

---

# 第1章: 6ヶ月は、3ヶ月になっていた

「オープンウェイトはフロンティアに追いついた」——2026年7月、この一文が世界を駆けた。<br/>
だが、追いついたのなら、それまでどれだけ離れていたのか。

この問いに、多くの人は「半年」と答える。<br/>
オープンウェイトモデルはプロプライエタリのフロンティアに約6ヶ月遅れる——業界の定型句である。<br/>
では、その6ヶ月は、誰が測ったのか。

## 通説の出所を、誰も知らない

本書の調査では、「6ヶ月」という数字の一次的な出所を特定できなかった。<br/>
広く流通し、記事に引用され、投資判断の前提にすらなっているが、<br/>
それを厳密な方法論で測定した独立研究に行き着かない。

一方で、**測っている機関は存在する**。<br/>
そして、その数字は6ヶ月ではない。

独立研究機関Epoch AIは、Epoch Capabilities Index（ECI）を用いてオープンとクローズドの能力差を継続測定している。<br/>
2025年10月30日時点の公表値は、こうだ。<br/>
**2023年1月から2025年10月までの平均ラグは3.5ヶ月、ECI差は7ポイント。**

さらに2026年5月29日の更新では、こうなっている。<br/>
**2026年1月1日から5月28日までの平均ラグは4ヶ月、ECI差は8ポイント。**<br/>
より厳格な基準を採れば6ヶ月。

つまり、通説の「6ヶ月」は、最も保守的な基準を採ったときの上限値だった。<br/>
実測の中心値は、3〜4ヶ月である。<br/>
**Kimi K3が現れる前から、距離はとうに縮んでいた。**

## 同じ現象を測って、答えが倍ちがう

ここでもう一つ、重要な事実がある。<br/>
測定機関によって、答えが倍以上ちがうのだ。

英国のAI Security Institute（AISI）は2026年7月のFrontier AI Trends Reportで、こう整理している。<br/>
**Artificial AnalysisのIntelligence Indexを基準にすれば4ヶ月。<br/>
METRのtime-horizon tasksを基準にすれば8ヶ月。**

どちらも独立機関である。どちらも真剣に測っている。<br/>
それでも、**何を能力と定義するかで、答えは倍ちがう。**

スタンフォードHAIのAI Index 2025は、また別の切り口を示す。<br/>
Chatbot Arenaにおけるオープンとクローズドの差は、<br/>
2024年1月の8.04%から、2025年2月には1.70%へ縮小した。<br/>
これは時間の差ではなく、スコアの差である。

3つの独立機関が、3つの異なる指標で測り、3つの異なる数字を出す。<br/>
だが、方向だけは一致している——**差は、年単位ではなく数ヶ月単位に縮んだ。**

```mermaid
graph LR
    A["通説<br/>──────<br/>オープンは6ヶ月遅れる<br/>一次的出所は特定できず"] -.->|"実測が置き換える"| B{"独立測定の中心値<br/>──────<br/>3〜4ヶ月"}
    C["Epoch AI／ECI<br/>2023.1–2025.10<br/>平均3.5ヶ月・7pt差"] --> B
    D["Epoch AI／ECI<br/>2026.1–2026.5<br/>平均4ヶ月・8pt差"] --> B
    E["AISI／AA Index基準<br/>4ヶ月"] --> B
    F["AISI／METR基準<br/>8ヶ月"] --> B
    G["Stanford HAI／Arena<br/>8.04%→1.70%<br/>（時間でなくスコア差）"] --> B

    style A fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style B fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style C fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style D fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style E fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style F fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style G fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

## Kimi K3は、列の中の一つにすぎない

距離が縮んだのは、K3が特別だったからではない。<br/>
2026年前半、フロンティア級を標榜するオープンウェイトが列をなして現れている。

* **DeepSeek V4 Pro**：1.6兆パラメータ／49Bアクティブ／100万トークン（2026年4月）
* **美団 LongCat 2.0**：1.6兆パラメータ／平均48Bアクティブ／100万トークン（2026年6月30日）。国産計算クラスタ上で学習から推論まで全工程を完遂したと公式に発表
* **MiniMax M3**：100万トークン・ネイティブマルチモーダル。「3つのフロンティア能力を持つ最初のオープンウェイトモデル」と自称
* **GLM-5.2**：Terminal-Bench 2.1で81.0、SWE-bench Proで62.1

そしてKimi K3が、2.8兆パラメータでその列の先頭に立った。<br/>
アーキテクチャはStable LatentMoE——896のエキスパートのうち16のみがアクティブになる極端な疎性である。<br/>
総パラメータ2.8兆に対し、アクティブは104B。約3.7%。<br/>
巨大な知識量と推論効率を、疎性で両立させる設計だ。

対する米国側のオープンウェイトはどうか。<br/>
OpenAIのgpt-oss-120bはApache 2.0という真に寛容なライセンスで公開されているが、<br/>
117Bパラメータ（5.1Bアクティブ）、Artificial AnalysisのIntelligence Indexは24。<br/>
MetaのLlama 4 Maverickは402B／17Bアクティブ、100万トークン、Index 14。

Kimi K3が57、Fable 5が60、GPT-5.6 Solが59という座標に置けば、風景は明白だ。<br/>
**争点は「米国にオープンウェイトがない」ことではない。<br/>
「米国のオープンウェイトが、フロンティア級オープンウェイトの主役ではなくなった」ことだ。**

## 距離は縮み、そして安定した

ここまでの事実を、一つの命題に畳む。

**オープンとクローズドの距離は、3年かけて縮み、そして数ヶ月という水準で安定した。**

驚くべきは、Kimi K3が到達したことではない。<br/>
驚くべきは、**誰も正確な距離を知らないまま、6ヶ月という数字で議論していた**ことだ。<br/>
通説は測定に置き換わった。そして測定は、通説より短い数字を出した。

だが、ここで満足してはいけない。<br/>
Epoch AIもAISIもスタンフォードHAIも、独立して測った機関である。<br/>
では、Kimi K3そのものについて流通している数字は、誰が測ったのか。

次章では、その問いを立てる。

### 参考文献

1. Epoch AI「Open-weight models lag state-of-the-art by around 3 months on average」（2025年10月30日・2023年1月–2025年10月の平均3.5ヶ月／ECI差7ポイント）
   <https://epoch.ai/data-insights/open-weights-vs-closed-weights-models>
2. Epoch AI「Open models lag state-of-the-art closed models by 4 months」（2026年5月29日・2026年1月–5月28日の平均4ヶ月／ECI差8ポイント／厳格基準なら6ヶ月）
   <https://epoch.ai/data-insights/open-closed-eci-gap>
3. UK AI Security Institute「Frontier AI Trends Report」（2026年7月・AA Index基準4ヶ月／METR time-horizon基準8ヶ月）
   <https://www.aisi.gov.uk/frontier-ai-trends-report>
4. Stanford HAI「Technical Performance｜The 2025 AI Index Report」（Chatbot Arena差 2024年1月8.04%→2025年2月1.70%）
   <https://hai.stanford.edu/ai-index/2025-ai-index-report/technical-performance>
5. Moonshot AI「Kimi K3 Tech Blog」（2.8兆総パラメータ／104Bアクティブ／Stable LatentMoE 896エキスパート中16／Kimi Delta Attention／100万トークン）
   <https://www.kimi.com/blog/kimi-k3>
6. DeepSeek「DeepSeek-V4-Pro」（1.6兆／49Bアクティブ／100万トークン）
   <https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro>
7. 美団技術団队「LongCat-2.0 正式发布」（2026年6月30日・1.6兆／平均48Bアクティブ／国産算力クラスタで全工程完遂）
   <https://tech.meituan.com/2026/06/30/LongCat2.0.html>
8. MiniMax「MiniMax M3」
   <https://www.minimax.io/models/text/m3>
9. zai-org「GLM-5」（Terminal-Bench 2.1 81.0／SWE-bench Pro 62.1）
   <https://github.com/zai-org/GLM-5>
10. OpenAI「Introducing gpt-oss」（Apache 2.0／117B・5.1Bアクティブ）
    <https://openai.com/index/introducing-gpt-oss/>
11. Artificial Analysis「Llama 4 Maverick」（402B・17Bアクティブ／Index 14）
    <https://artificialanalysis.ai/models/llama-4-maverick>

<br/>

---

# 第2章: その数字は、誰が測ったのか

Kimi K3について、いま世界に流通している数字がある。<br/>
Terminal-Bench 2.1。GPQA-Diamond。DeepSWE。GPUカーネル最適化での優位。<br/>
これらの数字は、誰が測ったのか。

答えは単純だ。**大半は、Moonshot自身である。**

## 5つの分類が、風景を変える

本書は、すべての数値と主張を5つに分類する。

| 分類 | 定義 | 例 |
|---|---|---|
| **[独立一次]** | 学術論文、独立評価機関、公的機関、政府文書 | Epoch AI、Artificial Analysis、Vals AI、AISI、大統領令本文 |
| **[当事者]** | 測定対象の企業自身の発表・自己申告ベンチマーク | Moonshot公式ブログ、Anthropic公式リリース |
| **[利害関係者]** | その数字が有利に働く立場からの発信 | VC調査、投資先を持つ機関の市場推計 |
| **[報道]** | 一次資料を取材した報道機関 | ロイター、Tom's Hardware |
| **[言説]** | 一次データを伴わない意見・予測 | ブログ、アナリスト論考 |

この分類を通すと、Kimi K3の風景は変わる。

**[独立一次]で確認できたもの**は、次の4つだけだ。

* Artificial Analysis：Intelligence Index **57**、189モデル中**4位**。上位はFable 5が60、GPT-5.6 Solが59
* Vals AI：Vals Index **74.70%（±0.96）**、38モデル中**2位**
* Arena.ai（Frontend Code Arena）：Fable 5を上回り**首位**
* Artificial Analysis／Vals AI：**重みは未公開／ライセンスはProprietary表示**

**[当事者]にとどまるもの**は、それ以外のほぼすべてである。

* 2.8兆パラメータ、104Bアクティブ、896エキスパート中16アクティブ、Kimi Delta Attention
* GPUカーネル最適化ベンチマークでOpus 4.8・GPT-5.6 Solを上回るという主張
* 64アクセラレータ以上を推奨するという展開要件
* 7月27日に全重みを公開するという予定
* API価格 $3/$15（キャッシュヒット時の入力$0.30）

そして最も象徴的なのが、DeepSWE Leaderboardである。<br/>
K3は67.5%で3位に掲載されている。<br/>
だが同じページに、こう書かれている——**Verified 0 / Self-reported 9**。<br/>
9件の掲載すべてが自己申告で、検証済みはゼロ。<br/>
**リーダーボードに載っていることと、検証されていることは、別である。**

## 当事者自身が、超えていないと書いている

ここで、興味深い逆転が起きている。

Moonshotのテクニカルブログは、GPUカーネル最適化などの自社ベンチマークで優位を主張する一方、<br/>
**総合性能ではClaude Fable 5に及ばない**と自己評価している。<br/>
つまり「K3がFable 5を超えた」と最も強く言っているのは、Moonshotではない。<br/>
**報道と、その先の言説である。**

独立測定はこれを裏づける。<br/>
Artificial AnalysisとVals AIの数字は、K3を「フロンティア近傍にいる世界最強クラスのオープンウェイト」と位置づけるが、<br/>
「フロンティアを凌駕した存在」とは位置づけていない。<br/>
Frontend Code Arenaでの首位は事実だが、それは**Webインターフェース構築という特定タスク**の話だ。

**特定タスクでの首位を、総合での逆転として読む。**<br/>
これが、2026年7月に起きた最大の誤読である。

```mermaid
graph TD
    A["Kimi K3<br/>2026/7/16-17 発表"] --> B["[当事者]<br/>──────<br/>Moonshot 公式ブログ<br/>『総合ではFable 5に及ばない』"]
    A --> C["[独立一次]<br/>──────<br/>AA Index 57／4位<br/>Vals Index 74.70%／2位<br/>Frontend Arena 首位"]
    A --> D["[報道]<br/>──────<br/>『Fable 5に迫る』<br/>『Fable 5を上回る』"]
    D --> E["[言説]<br/>──────<br/>『中国がClaudeを抜いた』"]
    B --> F{"事実として残るもの<br/>──────<br/>世界最強クラスの<br/>オープンウェイト<br/>ただし総合4位"}
    C --> F
    E -.->|"検証を経ずに<br/>結論だけが伝播"| G["市場・投資判断・戦略"]
    F -.->|"本来ここを通るべき"| G

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style C fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style D fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style E fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style F fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style G fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

## 検証不能なものを、検証したと呼ばない

もう一つ、決定的な事実がある。<br/>
本書の調査では、**独立した第三者が自前の環境にK3の完全な重みを展開し、<br/>
推論コスト、実効VRAM消費、レイテンシを厳密に測定したレポートは、一件も発見できなかった。**

理由は単純だ。**重みが、まだ配布されていないからである。**<br/>
7月27日の公開まで、ハードウェアレイヤーでの独立検証は物理的に不可能だ。

つまり、いま流通しているK3の実務評価はすべて、<br/>
①Moonshotの自己申告か、②Moonshotが運営するAPI経由での測定か、<br/>
そのどちらかに依存している。

**API経由の測定は、モデルの測定ではない。<br/>
モデルと、それを提供する事業者の運用の、合成物の測定である。**

これは些細な区別ではない。<br/>
量子化の設定、バッチング、ルーティング、キャッシュ——APIの向こう側で何が起きているかを、外部は知り得ない。<br/>
重みを手にして初めて、それはモデルの測定になる。

## 測定の未成熟が、この産業の実像である

第1章で見た通り、同じ現象を測って機関ごとに倍の差が出る。<br/>
本章で見た通り、リーダーボードの掲載は検証を意味しない。<br/>
そして、最も基礎的な検証——重みを手にして動かすこと——は、まだ誰にもできていない。

**この産業は、自分が何を作ったのかを、正確に測る手段をまだ持っていない。**

それでも、数字は動く。<br/>
投資が動き、戦略が動き、規制の議論が動く。<br/>
検証不能な数字が、検証されないまま前提になる。

だから本書は、以降のすべての章で分類を明示する。<br/>
誰が測ったのか。その人は、その数字が大きいと得をするのか。<br/>
**この二つを問い続けることが、いまこの領域で唯一可能な誠実さである。**

次章では、その誠実さを最も過酷な事実に向ける。<br/>
仮に7月27日に重みが公開されたとして、あなたはそれを動かせるのか、という問いだ。

### 参考文献

1. Artificial Analysis「Kimi K3 – Intelligence, Performance & Price Analysis」（Intelligence Index 57／weights not publicly available）
   <https://artificialanalysis.ai/models/kimi-k3>
2. Artificial Analysis「AI Model & API Providers Analysis」（Fable 5 = 60／GPT-5.6 Sol = 59／Kimi K3 = 57）
   <https://artificialanalysis.ai/>
3. Vals AI「Kimi K3」（Vals Index 74.70% ±0.96／38モデル中2位／License type: Proprietary）
   <https://www.vals.ai/models/kimi_kimi-k3>
4. LLM Stats「DeepSWE Leaderboard」（K3 67.5%・3位／**Verified 0 / Self-reported 9**）
   <https://llm-stats.com/benchmarks/deepswe>
5. Moonshot AI「Kimi K3 Tech Blog: Open Frontier Intelligence」（自社ベンチでの優位主張と、総合ではFable 5に及ばないとの自己評価）
   <https://www.kimi.com/blog/kimi-k3>
6. Tom's Hardware「China's 2.8-trillion-parameter Kimi K3 beats Claude Fable 5 in Frontend Code Arena benchmark」（2026年7月）
   <https://www.tomshardware.com/tech-industry/artificial-intelligence/moonshot-releases-2-8-trillion-parameter-kimi-k3>

<br/>

---
# 第3章: 1.7テラバイトの、開かれた扉

「オープンウェイト」という語には、一つの約束が含まれている。<br/>
誰でもダウンロードして、自分の環境で動かせる、という約束だ。<br/>
その約束は、2.8兆パラメータの前で崩れる。

## 64という数字

Moonshotの公式ブログには、こう書かれている。<br/>
推論効率は大きな高帯域通信ドメインの恩恵を受けるため、<br/>
**64基以上のアクセラレータで構成されるスーパーノードでの展開を推奨する**、と。

これは高性能を追求するための贅沢な推奨ではない。<br/>
**最低要件に近い現実である。**<br/>
しかもMoonshotは、SFT（教師ありファインチューニング）の段階から<br/>
量子化（MXFP4ウェイト／MXFP8アクティベーション）を実装している。<br/>
つまり、**すでに圧縮した状態で、なお64基**なのだ。

重みの物理的な大きさを、総パラメータ数から算術的に見積もる。<br/>
BF16なら約**5.6TB**。INT8でも約**2.8TB**。INT4まで攻めても約**1.4TB**。<br/>
これはMoonshotが公表した総パラメータ数からの推計であり、<br/>
MoEの全エキスパートをどう保持するか、公式がどの量子化を許容するかで必要構成は変わる。<br/>
だが、変わらないことが一つある。<br/>
**民生用GPU一枚で動くという類いの話ではない。**

そして2026年7月27日、重みは実際に公開された。<br/>
配布形式はMXFP4——Moonshotが学習段階から実装していた量子化そのものである。<br/>
報じられたファイルサイズは**1.56TB**であった。

MXFP4は1パラメータあたり約4.25ビット（ブロックスケール込み）であるから、<br/>
2.8兆パラメータで約1.49TB。埋め込み層とビジョンエンコーダが高精度で残ることを踏まえれば、<br/>
1.56TBという実測値は算術と整合する。<br/>
**本章がINT4推計として置いた約1.4TBの、すぐ上に着地した。**

## 疎性は、要求を減らさない

ここで一つの誤解を解いておく。<br/>
K3のアーキテクチャは896のエキスパートのうち16のみをアクティブにする。<br/>
アクティブパラメータは104B——総数の約3.7%である。<br/>
「だから軽いのでは」と考えるのは自然だ。

だが、疎性が減らすのは**計算量**であって、**メモリフットプリント**ではない。<br/>
どのエキスパートが呼ばれるかは入力次第だから、**896すべてを手元に置いておく必要がある。**<br/>
計算は速い。だが、置き場所は依然として1.4〜5.6TBだ。

疎性は、推論を安くする技術であって、参入を安くする技術ではない。

```mermaid
graph TD
    A["オープンウェイトの実行可能性<br/>──────<br/>能力が上がるほど、到達者が減る"] --> B["〜3Bクラス<br/>──────<br/>スマートフォン上で動作<br/>誰でも所有できる"]
    A --> C["〜数十Bクラス<br/>──────<br/>ワークステーション／ラップトップ<br/>個人・小規模チーム"]
    A --> D["1兆パラメータ級<br/>──────<br/>DeepSeek V4 Pro／LongCat 2.0<br/>データセンター"]
    A --> E{"2.8兆パラメータ<br/>Kimi K3<br/>──────<br/>64アクセラレータ以上<br/>BF16で約5.6TB"}
    E --> F["セルフホスト可能な主体<br/>──────<br/>潤沢な資本を持つ<br/>データセンター／クラウド事業者のみ"]
    E --> G["それ以外の全員<br/>──────<br/>Moonshot API<br/>または第三者ホスティング"]

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#BFD9E6,stroke:#BFD9E6,color:#0A0D10
    style C fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
    style D fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style E fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style F fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style G fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
```

## 私が書いた命題が、ここで壊れる

私は2026年3月1日、『The Edge of Intelligence』という書籍を公開した。<br/>
その中核命題はこうだ——**オンデバイスAIの限界費用はゼロである。**<br/>
月額20ドルのサブスクリプションは、自分のデバイスで無料で動くAIの前では「なくても困らない贅沢」に変質する。<br/>
だから消費者は、不可逆にオンデバイスへ移行する。

この命題は、**Nanbeige 4.1 3Bのような小型モデルでは真である。**<br/>
そしてKimi K3では、**偽である。**

限界費用がゼロになるのは、重みを自分の環境に置けたときだけだ。<br/>
置けなければ、限界費用は月之暗面が決める。<br/>
入力$3/M、出力$15/M——これはGPT-5.6 Terra級の価格帯であり、**格安ではない。**

**オープンウェイトは、一枚岩ではない。**<br/>
実行可能性によって階層化しており、上の階層ほど能力が高く、到達者が少ない。<br/>
そして2026年7月、フロンティアに並んだのは**最上層**だった。<br/>
民主化が進んだ層と、フロンティアに届いた層は、別の層である。

自分の書いた命題を、自分で壊しておく。<br/>
それが、一次情報で書くということの最低限の作法だと考えている。

## 「安い」は、どこにあるのか

ただし、価格の風景全体を見ると、別の事実も現れる。<br/>
Artificial Analysisのcost-per-task比較（2026年7月）は、こうだ。

| モデル | タスクあたりコスト | 分類 |
|---|---|---|
| Claude Fable 5 | **$2.75** | プロプライエタリ |
| GPT-5.6 Sol | **$1.04** | プロプライエタリ |
| **Kimi K3** | **$0.94** | オープンウェイト（予定） |
| GLM-5.2 | **$0.47** | オープン系 |
| DeepSeek V4 Pro | **$0.04** | オープンウェイト |
| Llama 4 Maverick | **$0.03** | オープン系 |

※本表の「オープンウェイト（予定）」は2026年7月18日時点の分類である。K3の重みは7月27日に公開された。

K3はFable 5の約3分の1だが、DeepSeek V4 Proの**23倍**である。<br/>
「オープンウェイト＝安い」ではない。<br/>
**オープンウェイトの中に、フロンティア級プレミアムが発生している。**

これが特権的なオープンの経済的な顔だ。<br/>
重みを公開すると宣言しながら、その能力への現実的なアクセスは有料APIで売る。<br/>
DeepSeekは$0.04で売り、K3は$0.94で売る。<br/>
両者とも「オープンウェイト」を名乗る。**同じ語が、23倍の価格差を覆っている。**

## 重みが出ても、すぐには使えない

物理の壁は、公開の瞬間に消えるわけではない。<br/>
**時間として、公開の後にも残り続ける。**

これまで、中国のオープンウェイトモデルには一つの型があった。<br/>
RLの学習が終わると、数時間から、遅くとも1週間以内に重みが公開される。<br/>
そしてエコシステムは、それをどう動かすかを即座に理解していた。<br/>
推論エンジンへのパッチは、公開の数日前から準備されていることさえある。

Kimi K3では、この型が成立しない可能性が高い。

Interconnectsの対談で、Florian Brandはこう述べている。<br/>
**このモデルは、重みをロードするだけでB300のノードが1台必要になる。**<br/>
ファインチューニング可能な状態に持っていくには、相当なエンジニアリングと時間を要する、と。

Nathan Lambertは、これを時間差の問題として捉え直している。<br/>
クローズドなラボは、発表前にこの最適化を裏側で済ませてから世に出す。<br/>
つまり彼らは、**性能差として観測される時間を、意図的に操作している。**<br/>
オープンウェイト支持者は長らく、「クローズドモデルが利用可能になった時点からしか時間差は測れない」と主張してきた。

だが、いま同じ力学がオープン側にも生まれている。<br/>
**重みが出ることと、それが使えるようになることの間に、1ヶ月規模の隔たりが生じうる。**<br/>
現に、Kimiの推論APIは需要に供給が追いつかず、機能不全に陥っている。<br/>
モデルは公開されたのに、拡散していない。

ここに、本書の命題の実務的な帰結がある。<br/>
**公開日と、到達日は、別の日付である。**<br/>
そして両者の間隔を決めるのは、ライセンスでも政治でもなく、**そのモデルを動かせる設備を持っているかどうか**だ。

64基のアクセラレータを買える組織にとって、その間隔は短い。<br/>
買えない組織にとって、その間隔は事実上、無限である。

## 開かれた扉と、その重さ

7月27日、重みは公開されるかもしれない。<br/>
扉は開く。誰でも入っていいと言われる。

だが、扉の向こうにあるのは1.4〜5.6テラバイトの質量であり、<br/>
64基のアクセラレータであり、それを買える資本である。<br/>
**開放は、能力の配布を意味しない。**

物理の壁は、悪意でも陰謀でもない。<br/>
ただそこにある。誰も止めていないのに、誰も通れない。<br/>
これが、特権的なオープンの第一の顔だ。

次章では、第二の顔を見る。<br/>
扉が開いたとして、**どの条件で入っていいのかを、まだ誰も知らない**という事実である。

## 追記（2026年7月28日）: 扉は、開いた

本章は2026年7月18日に書かれた。<br/>
7月27日、Moonshotは予告どおり重みを公開した。<br/>
本章が予測として書いたことの、何が当たり、何が外れたかを記録する。

### 当たったこと1: サイズ

配布形式はMXFP4だった。報じられたファイルサイズは**1.56TB**。<br/>
本章が算術推計として置いた三つの数字——BF16 約5.6TB、INT8 約2.8TB、INT4 約1.4TB——のうち、<br/>
実測は**INT4推計のすぐ上に着地した。**<br/>
量子化を学習段階から織り込んでいた事実が、そのまま配布サイズに現れている。

### 当たったこと2: 64という数字

Moonshotの推奨構成は、重み公開後も変わっていない。<br/>
64基以上の高帯域相互接続アクセラレータで構成されるスーパーノード。<br/>
**重みが配られても、動かすための要件は1ビットも下がらなかった。**

### 当たったこと3: 公開日と到達日は、別の日付である

Hugging Faceの公式モデルページが表示しているダウンロード数は、**2,850**である。<br/>
世界最大のオープンウェイトモデルの、公開直後の数字だ。<br/>
**扉は開いた。だが、通った回数は3千に届いていない。**

### 予測していなかったこと

公開後、報道のあいだに食い違いが現れた。<br/>
ある技術メディアは、ダウンロードサイズを「約594GB」、最小構成を「8基のH100 80GB」と報じた。<br/>
だが594GBは1パラメータあたり約1.7ビットに相当し、MXFP4では成立しない。<br/>
そして8基のH100の合計メモリは640GBであり、**1.56TBの重みは、そもそも載らない。**

これは誰かの怠慢ではない。<br/>
**動かせる設備を持たない者は、それが動くかどうかを判定する手段も持たない。**<br/>
本章は「公開日と、到達日は、別の日付である」と書いた。<br/>
公開後に観測されたのは、それより一段手前の事実だった。<br/>
**到達できない者は、到達可能性そのものを、誤って報告する。**

※ダウンロード数はHugging Face公式ページの表示値（Downloads last month）であり、重み公開の翌日に取得したものである。集計期間の解釈には注意を要する。


## 追記2（2026年8月17日）: 壁の高さは、規模に比例しない

本章は「2.8兆パラメータ」という規模を前提に、物理の壁を論じた。<br/>
2026年8月14日、その前提に対する反証データが現れた。

### 同等性能が、4分の1の規模で出た

Z.aiがGLM-5.3を発表した。<br/>
公式の開発者ドキュメントは、このモデルをこう位置づけている。<br/>
**「そのプログラミングとエージェント能力は、Claude Fable 5と同等である」**、と。

ベースモデルはGLM-5.2と同一である。Z.aiは「すべての改善はポストトレーニングによる」と明記している。<br/>
GLM-5.2は約744B——**Kimi K3の2.8兆パラメータの、およそ4分の1である。**

本章は、64という数字を「最低要件に近い現実」と書いた。<br/>
その判断は、いまも変わらない。Moonshotの推奨構成は重み公開後も動いていない。<br/>
だが本章が暗黙に置いていた前提——**フロンティア級の性能には、フロンティア級の質量が要る**——は、<br/>
ここで一度、留保が必要になる。

### 物理の壁は、どこへ移ったのか

もっとも、GLM-5.3の実行要件は、現時点では検証できない。<br/>
**重みが公開されていないからである。**

2026年8月17日時点で、Z.aiの公式開発者ドキュメントはAPIを "coming soon" と表示し、<br/>
Hugging Faceへの導線は "Coming Soon" のままである。<br/>
量子化形式別のチェックポイント容量も、最小GPU構成も、公式には存在しない。

つまりGLM-5.3について現在言えるのは、**規模が小さいことと、性能が高いと自己申告されていること**の二点だけだ。<br/>
物理の壁が下がったのかどうかは、**まだ誰も測れない。**

本章は第2章から一つの規律を引き継いでいる。<br/>
自己申告ベンチマークは、独立測定ではない。<br/>
GLM-5.3のスコアは、すべてZ.ai自身のハーネスで測られたものである。

### モダリティという、見落とされていた変数

公式ドキュメントは、GLM-5.3の入出力モダリティを**Text / Text**と記載している。<br/>
一方Kimi K3は、公式モデルカードで**Text, Image**——ネイティブ・マルチモーダルである。

同じ「フロンティア級」という語の下で、扱える情報の種類が違う。<br/>
規模の比較は、この差を含まない。<br/>
**4分の1で並んだのは、テキストという一つの軸の上でのことである。**

※GLM-5.3のパラメータ数について、Z.ai公式はGLM-5.3固有の数値を公表していない。公式が述べているのは「GLM-5.2と同一のベースモデル」であることのみである。「743B」「744B」「約750B」「753B」という数字が流通しているが、いずれもGLM-5系列の別ソースに由来する。本追記が用いた「約744B」はGLM-5.2の公表値である。

### 参考文献

1. Moonshot AI「Kimi K3 Tech Blog: Open Frontier Intelligence」（64アクセラレータ以上のスーパーノード推奨／MXFP4ウェイト・MXFP8アクティベーション／Stable LatentMoE 896エキスパート中16アクティブ／API $3・$15、キャッシュヒット時入力$0.30）
   <https://www.kimi.com/blog/kimi-k3>
2. Artificial Analysis「gpt-oss-120b – Intelligence, Performance & Price Analysis」（cost-per-task比較：Fable 5 $2.75／GPT-5.6 Sol $1.04／Kimi K3 $0.94／GLM-5.2 $0.47／DeepSeek V4 Pro $0.04／Llama 4 Maverick $0.03）
   <https://artificialanalysis.ai/models/gpt-oss-120b>
3. Nathan Lambert & Florian Brand（Interconnects）「Open models recap: more on Kimi K3, Qwen 3.8, Xi's WAIC speech, distillation, the open-closed gap, and what's next」（2026年7月22日・重みのロードだけでB300ノード1台／ファインチューニング可能化に相当な工数／Kimi APIは需要過多で機能不全）
   <https://www.interconnects.ai/p/open-models-recap-more-on-kimi-k3>
4. Satoshi Yamauchi「The Edge of Intelligence — AIがあなたのデバイスで動く時代」（Leading.AI・CC BY 4.0）
   <https://github.com/Leading-AI-IO/edge-ai-intelligence>
5. MarkTechPost「Moonshot AI Releases Kimi K3: A 2.8 Trillion Parameter Open MoE Model With Kimi Delta Attention and 1M Context」（2026年7月16日）
   <https://www.marktechpost.com/2026/07/16/moonshot-ai-releases-kimi-k3-a-2-8-trillion-parameter-open-moe-model-with-kimi-delta-attention-and-1m-context/>
6. Moonshot AI「moonshotai/Kimi-K3」Hugging Face 公式モデルカード（総パラメータ2.8T／アクティブ104B／896エキスパート中16／コンテキスト1,048,576トークン／MXFP4ウェイト・MXFP8アクティベーション／推奨エンジン vLLM・SGLang・TokenSpeed／ダウンロード数2,850）
   <https://huggingface.co/moonshotai/Kimi-K3>
7. 竹元かつみ「Fable 5に迫る『Kimi K3』オープンウェイト版が公開。MXFP4形式で1.56TB」PC Watch（2026年7月28日・MXFP4形式1.56TB／64基以上のアクセラレータによるスーパーノード推奨／Kimi K3 License）
   <https://pc.watch.impress.co.jp/docs/news/2128308.html>
8. Z.AI DEVELOPER DOCUMENT「GLM-5.3 - Overview」（GLM-5.2と同一ベースモデル／コンテキスト長1M／最大出力128K／入出力モダリティText・Text／API "coming soon"／CyberGym 84.5%／ExploitBench 24.4%→54.4%）
   <https://docs.z.ai/guides/llm/glm-5.3>
9. Moonshot AI「MoonshotAI/Kimi-K3」GitHub 公式リポジトリ（総パラメータ2.8T／アクティブ104B／896エキスパート中16／レイヤー93／モダリティ Text, Image／MXFP4ウェイト・MXFP8アクティベーション）
   <https://github.com/MoonshotAI/Kimi-K3>
10. Nathan Lambert（Interconnects）「GLM-5.3: How Chinese labs keep stride with the frontier」（2026年8月14日・約750Bでエージェンティック・コーディングのフロンティアに位置／RL環境は蒸留できないという指摘）
   <https://www.interconnects.ai/p/glm-53-how-chinese-labs-keep-stride>

※重みサイズ（BF16 約5.6TB／INT8 約2.8TB／INT4 約1.4TB）は、Moonshotが公表した総パラメータ数2.8兆からの算術推計であり、公式が開示した数値ではない。2026年7月27日の実配布形式はMXFP4で、報じられたファイルサイズは1.56TBである（PC Watch、2026年7月28日）。

<br/>

---

# 第4章: ライセンスなき公開

2026年7月18日時点で、Kimi K3について確認できないことがある。<br/>
**どの条件で使っていいのか、である。**

## 独立評価機関の台帳では、Proprietaryだった

独立評価機関Vals AIのKimi K3ページには、こう記載されていた。<br/>
**License type: Proprietary（contact us to get access）**。

Artificial Analysisは「**weights not publicly available**」と表示していた。

世界最大のオープンウェイトモデルが、<br/>
発表から二日経っても、独立機関のデータベース上ではプロプライエタリだった。<br/>
これは皮肉ではなく、**配布状態を外から観察している第三者の、正確な記録**である。

ここで、独立性の序列を明確にしておく。<br/>
Moonshotの発表は「オープンにする」という**意思**の表明だ。<br/>
Vals AIとArtificial Analysisの表示は「まだ配布されていない」という**状態**の観測だ。<br/>
**意思より、状態のほうが強い。**

## 前例はあるが、条文はない

本書の調査では、**K3の正式なライセンス全文を発見できなかった。**<br/>
再配布条件も、軍事利用制限の有無も、修正版の公開義務も、確認できていない。

見つかったのは、前世代の条文だけである。<br/>
Kimi K2系のライセンスは**Modified MIT**であり、<br/>
**月間アクティブユーザー1億人超、または月間収益2,000万ドル超**の商用サービスでは、<br/>
UI上に「Kimi K2 / K2.5」と明示する義務が発動する。

一部の専門メディアは、K3も同じModified MITだと報じている。<br/>
だが、それは前例からの推定であって、条文の確認ではない。<br/>
**K2がModified MITだったことは、K3がModified MITであることを保証しない。**

なぜこれが重要か。<br/>
ライセンスは、「オープンウェイトが産業を壊す力」の大きさを直接決めるからだ。<br/>
商用利用が自由か。再配布が自由か。軍事利用の制限があるか。修正版の公開義務があるか。<br/>
**この4つの組み合わせ次第で、同じ重みが、まったく違う戦略資産になる。**

## 「オープンウェイト」は「オープンソース」ではない

ここで、語の定義を確定させる。

**オープンソース**とは、ソフトウェアの設計図が公開され、誰でも再現・改変・再配布できる状態を指す。<br/>
**オープンウェイト**とは、**学習済みパラメータのファイルだけ**が公開された状態を指す。

Kimi K3で公開が予定されているのは、後者である。<br/>
学習パイプラインは公開されない。<br/>
アーキテクチャの完全なソースコードも公開されない。<br/>
**学習データそのものは、公開されない。**

これを「オープンソース」とみなす学術的・技術的な合意は、形成されていない。<br/>
さらにModified MITのような閾値条項（MAU 1億人／月商2,000万ドル）は、<br/>
**無条件の再配布と商用利用を認めるOSI（Open Source Initiative）の定義から逸脱する。**

Metaも同じ構造を持つ。<br/>
Llama 4 Community Licenseには**MAU 7億人**という上限がある。<br/>
真に寛容なのは、OpenAIのgpt-oss-120bのApache 2.0だ。<br/>
**そして、そのgpt-oss-120bのIntelligence Indexは24である。**

**寛容さと能力は、いま逆相関している。**<br/>
最もオープンなライセンスを持つモデルは、フロンティアから最も遠い。<br/>
最もフロンティアに近いオープンウェイトは、ライセンスすら開示していない。

```mermaid
graph LR
    A["『オープン』の4層<br/>──────<br/>どこまで開かれているか"] --> B["① 重み<br/>──────<br/>K3: 公開予定（7/27）<br/>現時点では未配布"]
    A --> C["② 学習データ<br/>──────<br/>非公開"]
    A --> D["③ 学習コード<br/>──────<br/>非公開"]
    A --> E["④ ライセンス条文<br/>──────<br/>未確認<br/>K2系はModified MIT"]
    B --> F{"再現できないものを<br/>検証したと呼べるか<br/>──────<br/>制度の壁"}
    C --> F
    D --> F
    E --> F
    F --> G["寛容さと能力の逆相関<br/>──────<br/>gpt-oss-120b: Apache 2.0／Index 24<br/>Llama 4: MAU 7億上限／Index 14<br/>Kimi K3: 条文未確認／Index 57"]

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style C fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style D fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style E fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style F fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style G fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

※上図の「公開予定（7/27）」「ライセンス条文＝未確認」は2026年7月18日時点の状態である。両者は7月27日に確定した。本章末の追記を参照。

## 6日間で、事実基盤が一斉に更新される

本書が書かれている2026年7月18日から、わずか6日のうちに、三つのことが起きる。

* **7月27日**：Moonshotが予告した全重みの公開日。ここで初めて、第三者による独立検証が可能になる
* **8月1日**：米国大統領令（EO 14409）の60日期限。NSA等による「対象フロンティアモデル」の基準が具体化する
* **8月2日**：EU AI ActのGPAI義務について、**執行権限が発効する**

つまり本書は、**構造が確定する直前に、構造を書いている。**<br/>
これは弱点ではない。<br/>
6日後に何が確定し、何が確定しないかを、いま言語化しておくことにこそ意味がある。<br/>
確定した後で書けば、それは解説になる。確定する前に書けば、それは検証可能な予測になる。

本書の予測はこうだ。<br/>
**7月27日に重みが公開されても、特権的なオープンは解消しない。**<br/>
64アクセラレータ要件は残る。1.4〜5.6TBの質量は残る。<br/>
そしてライセンスに閾値条項が入っていれば、大規模な商用利用ほど条件が付く。<br/>
**解消するのは検証不能性だけであり、到達不能性ではない。**

## 誰も鍵をかけていない。だが、誰も入れない

物理の壁（第3章）と制度の壁（本章）は、同じ一つのことを別の角度から言っている。

**開放は、宣言でも意思でもなく、状態である。**<br/>
そして状態としての開放には、重みの配布だけでなく、<br/>
実行できる資源と、使ってよい条件と、再現できる材料が要る。<br/>
Kimi K3は、いまその4つのうち1つも揃っていない。**予定されているだけである。**

次章では、視点を変える。<br/>
仮に、すべてが揃ったとしよう。重みが配られ、条件が明示され、誰かが動かせるとしよう。<br/>
そのとき、**AIラボは何を売って生きているのか。**

## 追記（2026年7月28日）: 条文は、存在した

本章の題は「ライセンスなき公開」である。<br/>
2026年7月18日の時点で、K3の正式なライセンス全文は発見できなかった。<br/>
7月27日、条文は公開された。**本章の題は、もう成立しない。**

### 当たったこと1: 閾値条項は、入っていた

本章はこう予測した。「ライセンスに閾値条項が入っていれば、大規模な商用利用ほど条件が付く」。<br/>
公開された条文には、二つの閾値がある。

* **Model as a Service**として提供する事業で、関連会社を含む総収入が連続12ヶ月で**2,000万ドル**を超える場合、商用利用の前にMoonshot AIとの個別契約が必要
* 月間アクティブユーザー**1億人**超、または月間売上**2,000万ドル**超の商用製品・サービスでは、UIに「Kimi K3」を目立つ形で表示する義務

**K2系の閾値（MAU 1億人／月商2,000万ドル）と、同一水準である。**<br/>
条文は新しくなったが、閾値は動かなかった。

### 当たったこと2: Modified MITではなかった

本章はこう書いた。「一部の専門メディアは、K3も同じModified MITだと報じている。だが、それは前例からの推定であって、条文の確認ではない」。

公開された条文の名称は「**Kimi K3 License**」である。<br/>
Hugging Faceの公式モデルカードは、コードリポジトリと重みの双方がこのライセンスの下にあると記載している。<br/>
**Modified MITではない。**<br/>
建て付けはMITに近いが、名称も条件も別のものだ。

前例からの推定は、当たらなかった。<br/>
**本章が「前例はあるが、条文はない」と書いて推定を拒んだ判断は、結果として正しかった。**

### それでも、残ったもの

本章は「開放は、宣言でも意思でもなく、状態である」と書き、<br/>
状態としての開放には、重みの配布・実行できる資源・使ってよい条件・再現できる材料の四つが要ると整理した。

7月27日に揃ったのは、そのうち**二つ**である。<br/>
重みは配布された。条件は明示された。<br/>
だが**実行できる資源は64アクセラレータのまま**であり、<br/>
**学習データと学習コードは、いまも公開されていない。**

誰も鍵をかけていない。条件も貼り出された。<br/>
それでも、入れる者は限られている。


## 追記2（2026年8月17日）: 条文を出さずに、時間で縛る

本章の題は「ライセンスなき公開」だった。<br/>
7月27日、Kimi K3の条文が公開され、題は成立しなくなった。<br/>
だがその3週間後、**題が別の意味で成立する事例が現れた。**

### 公開されたのは、モデルではなく予定である

2026年8月14日、Z.aiはGLM-5.3を発表した。<br/>
同日からGLM Coding Planの全ユーザーが利用できる。<br/>
だが**重みは公開されていない。ライセンス条文も存在しない。**

Z.aiが公開の条件として挙げているのは、条文でも日付でもない。<br/>
**「安全性評価とハードニングの完了」**である。

前世代のGLM-5.2はMITライセンスで公開された。閾値条項はない。<br/>
だが**GLM-5.3が同じライセンスを採ると、Z.aiは一度も述べていない。**<br/>
本章が7月に書いた一文が、そのまま再び当てはまる。<br/>
**前例はあるが、条文はない。**

### 理由が、変わった

Kimi K3の非公開期間は10日間だった。理由は述べられていない。<br/>
GLM-5.3は違う。Z.aiは非公開の理由を明示している。

公式ドキュメントは、GLM-5.3がCyberGymで84.5%を記録し、<br/>
ExploitBenchのスコアが24.4%から54.4%へ倍増したと記載する。<br/>
そして同社は、**デュアルユースのリスク**を理由に段階的リリースを選んだと表明している。<br/>
選定されたセキュリティパートナーが管理された環境で先行評価し、<br/>
その後にAPIとウェイトが続く、という順序である。

**これは本章が扱った「条文による制限」とは、別の形態である。**<br/>
Kimi K3は、公開したうえで条文で縛った。<br/>
GLM-5.3は、条文を出す前に、公開そのものを時間で区切っている。

閾値条項は、大規模な商用利用者だけを縛る。<br/>
公開時期の段階化は、**すべての利用者を等しく待たせる。**

### 特権的なオープンの、第二形態

本章は「開放は、宣言でも意思でもなく、状態である」と書いた。<br/>
状態としての開放に要る四つ——重みの配布・実行できる資源・使ってよい条件・再現できる材料。

GLM-5.3について、2026年8月17日時点で揃っているものは**ゼロである。**<br/>
重みは未公開。実行要件は不明。条件は未公表。学習データも学習コードも公開されていない。<br/>
利用できるのは、有償プラン経由のアクセスだけだ。

Kimi K3は「公開されているが、到達できない」状態だった。<br/>
GLM-5.3は「公開されると告げられているが、まだ公開されていない」状態である。<br/>
**同じ語が、二つの異なる状態を指している。**

そしてZ.aiの理由づけは、第7章が扱う論点に接続する。<br/>
安全性を理由に公開を遅らせる判断は、審査の一形態である。<br/>
違うのは、それを行っているのが規制当局ではなく、**モデルを作った当事者自身**だという点だ。

※GLM-5.3のライセンス名・条文は、2026年8月17日時点で公表されていない。Z.ai公式の開発者ドキュメントにもライセンスに関する記述は存在しない。一部の第三者サイトがMITライセンスを前提とした記述を掲載しているが、いずれもGLM-5系列の前例からの推定であり、GLM-5.3の条文確認ではない。

※ウェイト公開時期について「ローンチから約2週間後」とする記述が複数の媒体で流通しており、Z.ai公式ブログ本文に該当文言があるとされる。本追記の執筆時点で公式ブログ本文の直接取得はできておらず、この一点は報道ベースの情報として扱う。

### 参考文献

1. Vals AI「Kimi K3」（**License type: Proprietary — contact us to get access**）
   <https://www.vals.ai/models/kimi_kimi-k3>
2. Artificial Analysis「Kimi K3」（**weights not publicly available**）
   <https://artificialanalysis.ai/models/kimi-k3>
3. Moonshot AI「Kimi-K2 LICENSE」（Modified MIT／MAU 1億人超または月商2,000万ドル超で帰属表示義務）
   <https://github.com/moonshotai/Kimi-K2/blob/main/LICENSE>
4. OpenAI「Introducing gpt-oss」（Apache 2.0）
   <https://openai.com/index/introducing-gpt-oss/>
5. Artificial Analysis「Llama 4 Maverick」（Llama 4 Community License／Index 14）
   <https://artificialanalysis.ai/models/llama-4-maverick>
6. The White House「Promoting Advanced Artificial Intelligence Innovation and Security」（2026年6月2日・発効後60日＝2026年8月1日前後に基準策定）
   <https://www.whitehouse.gov/presidential-actions/2026/06/promoting-advanced-artificial-intelligence-innovation-and-security/>
7. European Commission「Guidelines for providers of general-purpose AI models」（GPAI義務は2025年8月2日適用開始／**2026年8月2日から執行権限が発効**）
   <https://digital-strategy.ec.europa.eu/en/policies/guidelines-gpai-providers>
8. Moonshot AI「moonshotai/Kimi-K3」Hugging Face 公式モデルカード（**Both the code repository and the model weights are released under the Kimi K3 License**）
   <https://huggingface.co/moonshotai/Kimi-K3>
9. 竹元かつみ「Fable 5に迫る『Kimi K3』オープンウェイト版が公開。MXFP4形式で1.56TB」PC Watch（2026年7月28日・Modified MITではなくKimi K3 License／Model as a Service事業で連続12ヶ月総収入2,000万ドル超は個別契約／MAU1億超または月商2,000万ドル超はUI表示義務）
   <https://pc.watch.impress.co.jp/docs/news/2128308.html>
10. Z.AI DEVELOPER DOCUMENT「GLM-5.3 - Overview」（API "coming soon"／CyberGym 84.5%／ExploitBench 24.4%→54.4%／ライセンスに関する記述なし）
   <https://docs.z.ai/guides/llm/glm-5.3>
11. Z.ai「GLM-5.2」Hugging Face 公式モデルカード（MIT License／閾値条項なし）
   <https://huggingface.co/zai-org/GLM-5.2>
12. Nathan Lambert（Interconnects）「GLM-5.3: How Chinese labs keep stride with the frontier」（2026年8月14日・段階的リリースに関するZ.ai声明の引用）
   <https://www.interconnects.ai/p/glm-53-how-chinese-labs-keep-stride>

※K3の正式ライセンス全文・再配布条件・軍事利用制限・修正版公開義務は、本書の調査時点（2026年7月18日）では確認できなかった。「Modified MIT」とする報道は存在するが、確認できたのはK2系の条文のみである。

<br/>

---
# 第5章: 賢さが売り物でなくなった日

性能プレミアムは崩れた。<br/>
オープンウェイトはフロンティアの数ヶ月後ろまで来た。<br/>
推論価格は、Epoch AIの推計で**年9倍から900倍、中央値で年50倍**のペースで下落している。

では、プロプライエタリのAIラボは、もう終わりなのか。

**データは、それを支持していない。**

## 470億ドルは、賢さの対価ではない

Anthropicの公式開示を時系列で並べる。

* **2026年2月12日**：Series Gで300億ドルを調達、ポストマネー評価額3,800億ドル。**run-rate revenue 140億ドル**。成長の主因は「enterprises and developers」と明記
* **同日**：**Claude Code単体でrun-rate 25億ドル**。しかも**その過半がエンタープライズ**
* **2026年4月16日**：2025年末の約90億ドルから、**300億ドル超**へ。年間100万ドル超の顧客は500社超から**1,000社超**へ
* **2026年5月28日**：Series Hで650億ドルを調達、ポストマネー評価額9,650億ドル。**run-rate 470億ドル**を突破

OpenAIも同様の構造を開示している（2026年3月31日）。<br/>
**月商20億ドル。週次アクティブ9億人。サブスクリプション加入者5,000万人超。<br/>
そして——企業売上が全体の40%超。**<br/>
同社は、企業部門が2026年末に消費者部門と並ぶ見込みだと公式に述べている。

これらはすべて[当事者]の開示である。<br/>
第三者監査を経た財務諸表ではない。<br/>
だが、少なくとも一つのことは、この一次資料から確実に読み取れる。

**AIラボの収益の中心は、すでに「最も賢いモデルへのアクセス」ではない。**<br/>
エンタープライズ導入。開発者ワークフロー。クラウド配備。営業と統合支援。<br/>
Claude Codeが独立した25億ドルの収益柱になり、その過半が企業契約であるという事実は、<br/>
**賢さではなく、賢さを業務に埋め込む仕組みが売れている**ことを示している。

## エンタープライズは、まだclosedを選んでいる

Menlo Venturesの調査（2025年12月9日）によれば、<br/>
エンタープライズのLLM支出シェアは**Anthropic 40%、OpenAI 27%、Google 21%、そしてオープンソース系 11%**。

ここで正確を期す。<br/>
**Menloはベンチャーキャピタルであり、[利害関係者]である。**<br/>
AI企業への投資ポートフォリオを持つ主体が発表する市場推計を、独立一次情報として扱ってはならない。

それでも、この数字はOpenAI・Anthropicの一次開示と整合する。<br/>
企業向け売上が伸び、企業向け顧客数が倍増し、企業がClaude Codeに金を払っている——<br/>
その裏側で、**企業の支出の89%がclosed側に向かっている**という構図は、矛盾なく成立する。

Menloの報告は、その理由にも触れている。<br/>
IT・データサイエンスのような業務領域では、**reliability（信頼性）とdeep integrations（深い統合）が、speedより重要**だと。

つまり、**プレミアムの根拠が「一番賢いから」から「社内導入が楽で、信頼でき、監査に耐えるから」へ移った可能性が高い。**

## だが、その「信頼性プレミアム」は、測られていない

ここで、本書は立ち止まらなければならない。

**「信頼性」「安全性認証」「統合支援」が、平均して何%の価格差を正当化するのか——<br/>
それを直接測定した独立研究を、本書の調査では発見できなかった。**

あるのは市場推計（[利害関係者]）と、企業の自己申告（[当事者]）だけである。<br/>
「信頼性プレミアム」は、いま最も広く語られ、**最も測られていない概念**の一つだ。

同じことが、因果についても言える。<br/>
推論価格の下落は事実だ（Epoch AI・[独立一次]）。<br/>
競争激化も事実だ。<br/>
だが、**「Kimi K3やDeepSeekの登場が、直接OpenAI/Anthropicの値付けを下げた」と独立に特定した研究は、存在しない。**<br/>
言えるのは、価格は下がった、競争は激しい、**そして因果分解は未解明である**、というところまでだ。

```mermaid
graph LR
    A["賢さ<br/>──────<br/>性能プレミアム<br/>コモディティ化"] -->|"価値が流出"| B{"どこへ行ったのか"}
    B --> C["エンタープライズ統合<br/>──────<br/>Anthropic 顧客1,000社超<br/>OpenAI 企業売上40%超<br/>[当事者・実証強]"]
    B --> D["開発者ワークフロー<br/>──────<br/>Claude Code 25億ドル<br/>過半がエンタープライズ<br/>[当事者・実証強]"]
    B --> E["信頼性プレミアム<br/>──────<br/>価格差の正当化度合いを<br/>測った独立研究は存在しない<br/>[未測定・空白]"]
    B --> F["消費者プラットフォーム<br/>──────<br/>OpenAI 週次9億人<br/>サブスク5,000万人超<br/>[当事者・実証強]"]

    style A fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style B fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style C fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style D fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style E fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style F fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

図の中で最も白いノードが、最も実証の薄い箇所である。<br/>
**この産業が最も頼りにしている命題が、最も測られていない。**

## オープンでありながら、高く売る

もう一つ、興味深い交差がある。

Kimi K3は入力$3／出力$15で売られている。**Claude Sonnet級の価格帯**である。<br/>
一方、DeepSeek V4 Proは入力$0.435／出力$0.87。**約7〜17分の1**だ。<br/>
両者とも「オープンウェイト」を名乗る。

同じ週、Anthropicは自社の最上位モデルを従量課金へ移した。<br/>
**プロプライエタリは定額の終わりへ向かい、オープンウェイトは有料APIへ向かう。**<br/>
両者が、価格という一点で交差している。

欧州のMistralはこの構造を最も明示的に採っている。<br/>
Mistral Medium 3.5は2026年4月28日時点で**Modified MITのオープンウェイト**として公式ドキュメントに記載されている一方、<br/>
同社はプロプライエタリAPIとLe Chat Enterpriseを並行して運営している。<br/>
**「オープンからクローズドへ一方向に転換した」のではない。<br/>
最初から、両方を同時に持つ設計である。**

これが、K3の価格が示す構造だ。<br/>
オープン化は**マインドシェア獲得の手段**であり、収益は**ホスティング環境で回収**する。<br/>
重みを配ることと、金を取ることは、矛盾しない。

## 崩壊しない。だが、売り物が変わる

本章の結論を、二つの否定で示す。

**「プロプライエタリは崩壊する」——データは支持しない。**<br/>
Anthropicのrun-rateは470億ドル。顧客1,000社超。OpenAIは月商20億ドル。<br/>
エンタープライズ支出の89%が依然closed側にある（[利害関係者]推計だが一次開示と整合）。

**「何も変わらない」——データはもっと支持しない。**<br/>
推論価格は年50倍（中央値）で下落している。<br/>
オープンウェイトはフロンティアの4ヶ月後ろまで来た。<br/>
そして企業自身が、賢さではなく統合と信頼性を売っていると開示している。

起きるのは崩壊ではない。<br/>
**閉じたモデルが売るものが、能力から運用保証へ変わる**ことだ。

次章では、この転換の最大の争点に踏み込む。<br/>
**中国勢の性能は、盗まれたものなのか。**

### 参考文献

1. Anthropic「Anthropic raises $30 billion in Series G funding at $380 billion post-money valuation」（2026年2月12日・run-rate 140億ドル／Claude Code run-rate 25億ドル・過半がエンタープライズ／成長はenterprises and developers主導）
   <https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation>
2. Anthropic「Anthropic expands partnership with Google and Broadcom for multiple gigawatts of next-generation compute」（2026年4月16日・2025年末約90億→300億ドル超／100万ドル超顧客500社超→1,000社超）
   <https://www.anthropic.com/news/google-broadcom-partnership-compute>
3. Anthropic「Anthropic raises $65B in Series H funding at $965B post-money valuation」（2026年5月28日・**run-rate 470億ドル**）
   <https://www.anthropic.com/news/series-h>
4. OpenAI「OpenAI raises $122 billion to accelerate the next phase of AI」（2026年3月31日・月商20億ドル／週次9億人／サブスク5,000万人超／**企業売上40%超**／2026年末に消費者と並ぶ見込み）
   <https://openai.com/index/accelerating-the-next-phase-ai/>
5. Menlo Ventures「2025: The State of Generative AI in the Enterprise」（2025年12月9日・Anthropic 40%／OpenAI 27%／Google 21%／**open-source 11%**／reliabilityとdeep integrationsがspeedより重要）※[利害関係者]
   <https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/>
6. Epoch AI「LLM inference prices have fallen rapidly but unequally across tasks」（2025年3月12日・**年9倍〜900倍下落／中央値50倍/年**／2024年以降加速）
   <https://epoch.ai/data-insights/llm-inference-price-trends>
7. Mistral AI「Mistral Medium 3.5 – Model Card」（2026年4月28日・**Modified MITのopen weights**）
   <https://docs.mistral.ai/models/model-cards/mistral-medium-3-5-26-04>
8. Mistral AI「Medium is the new large.」（プロプライエタリAPI／Le Chat Enterpriseの並行運営）
   <https://mistral.ai/news/mistral-medium-3/>

※OpenAI・Anthropicとも、API／サブスクリプション／エンタープライズ契約の厳密な三分割比率は開示していない。「信頼性プレミアムが何%の価格差を正当化するか」を直接測定した独立研究も、本調査では発見できなかった。

<br/>

---

# 第6章: 蒸留という、証明されていない告発

中国のオープンウェイトが、なぜ数ヶ月でフロンティアに追いついたのか。<br/>
この問いに対する最も強力な説明が、いま一つある。

**盗んだからだ、というものである。**

## 24,000のアカウントと、1,600万回

Anthropicは2026年、公式に告発した。<br/>
DeepSeek、Moonshot、MiniMaxが、**約24,000の不正アカウント**を通じて<br/>
**1,600万回を超えるやり取り**を行い、Claudeの推論能力を抽出（蒸留）したと。

これに先立ち、OpenAIも2025年1月、DeepSeekが自社の出力を学習に用いた証拠を見たとFinancial Timesに述べている。

Anthropicの主張には、技術的な傍証も添えられている。<br/>
難読化されたルーター経由でのアクセス。連鎖的推論（Chain-of-Thought）と安全性フィルタ回避ロジックの大規模抽出。<br/>
そして、出力の類似性。

主張の含意は明確だ。<br/>
**中国勢の「数百万ドルでフロンティア級モデルを作った」という神話は、<br/>
米国企業が数百億ドル投じたR&Dへのタダ乗りの結果である。**

## その告発は、独立に検証されていない

ここで、本書の分類が効いてくる。

Anthropicの主張は[当事者]である。<br/>
24,000という数字も、1,600万回という数字も、**Anthropicが自社ログから算出し、自社で公表したものだ。**<br/>
第三者がこれを検証した記録は、本書の調査では発見できなかった。

そして、より重要なことがある。<br/>
**Moonshot側の公式な反論文書も、発見できなかった。**<br/>
3つの独立した調査ラインすべてが、同じ結論に達している——中国勢からの技術的データに基づく公式反証は、存在しない。

つまり現状は、こうだ。

* 告発側：主張あり、限定的な証拠の公開あり、[当事者]
* 被告発側：**沈黙**
* 独立検証：**存在しない**

**これは、事件ではない。まだ、主張である。**

## Epoch AIすら、測れていない

もう一つ、決定的な空白がある。

**蒸留が、性能向上のどれだけを説明するのか。**<br/>
中国勢の性能のうち、独自のアーキテクチャ改良（極限まで高められた疎性、Kimi Delta Attention等）による純粋な技術的成果はどれだけで、<br/>
米国モデルからの抽出に依存する部分はどれだけなのか。

この分解を定量的に行った研究は、**存在しない。**<br/>
これは些細な空白ではない。<br/>
なぜなら、この分解ができない限り、<br/>
**「オープンウェイトを規制すべきか」という政策議論の前提そのものが、宙に浮くからだ。**

「DeepSeekは550万ドルで学習した」という低コスト神話に対する独立監査も、同様に存在しない。<br/>
ゼロからの学習コストを客観的に証明する一次データは、どこにもない。

## 教師が強ければ、生徒は賢くなるのか

寄与度が測られていない、という空白は、実はもう一段深い。

**そもそも蒸留がなぜ効くのか、そのメカニズム自体が解明されていない。**

2026年7月22日、Interconnectsで Nathan Lambert と Florian Brand が、この論点を正面から扱った。<br/>
きっかけは、テック業界で最も読まれるブログの一つを持つ Ben Thompson（Stratechery）が、蒸留について踏み込んだ主張をしたことである。<br/>
**RL（強化学習）が学習の主軸になるほど、蒸留の効果はむしろ increasing している**——トンプソンはそう論じた。<br/>
中国のラボは、RL中の採点役（グレーダー）としてFable 5やGPT-5.6のような最強モデルを使っているのではないか、と。

Lambertは、これを明確に否定している。<br/>
理由は技術的かつ具体的だ。

第一に、**大規模なRLは数百万から数千万回のロールアウトを伴う。**<br/>
Thinking Machinesが公開した数値では、最終的なRL runで2,000万〜4,000万規模である。<br/>
これをFable 5やGPT-5.6のAPIに採点させれば、費用は非現実的な水準に達する。<br/>
加えて、これらのモデルは相対的に遅く、**時間のボトルネックになる。**<br/>
そして、自前で調整した採点モデルより性能が上がる保証すらない。

第二に、蒸留が実際に効くのは**SFT（教師ありファインチューニング）の段階**である。<br/>
推論トークンとツール呼び出しを抽出できれば、それは質の高いSFTデータになる。<br/>
モデルが「私はClaudeです」と答えてしまうのも、この段階で人格が形成されるからだ。<br/>
だが、**能力の核が作られるのはRLの段階であり、そこに金と計算が投じられている。**

そして第三に、ここが決定的である。

**「最も強いモデルが、最も良い教師である」という命題は、研究文献で確認されていない。**

Lambertによれば、多くの研究者が同じ問いを繰り返し検証してきたにもかかわらず、<br/>
性能で最強のモデルが、その領域で最良の教師になるという結果は得られていない。<br/>
現に、最先端のオープンなSFTデータセットは、**QwQ-32Bという旧世代の推論モデルの上に構築されている。**<br/>
なぜGLM-5.2から生成したデータでSFTすれば改善しないのか——その理由を、誰も説明できていない。

Lambert自身の言葉は、さらに踏み込んでいる。<br/>
仮にClaudeやGeminiの推論トレースを自由に取得できる魔法のAPIがあったとして、<br/>
それでOLMoをファインチューニングすれば賢くなるのかどうか、**自分にも分からない**、と。<br/>
彼はこれを、最も未解明な研究上の問いの一つだと述べている。

この告白の重みを、正確に受け止めたい。<br/>
発言しているのは、オープンモデルの学習手法を専門とし、自らモデルを訓練している研究者である。<br/>
その人物が、**蒸留の効果を定量できないどころか、効くかどうかすら断定できないと言っている。**

Brandは、この議論を一つの反証に畳んでいる。<br/>
もし中国勢の性能が蒸留だけで説明できるのなら、<br/>
**同じデータを使って、誰でもGLMやKimi K3に追いつけるはずである。**<br/>
だが、そうはなっていない。

前節で本書は、蒸留の寄与度を分解した研究が存在しないと書いた。<br/>
本節が加えるのは、それより深刻な事実である。<br/>
**寄与度が測られていないのではない。何がどう寄与するのかという理論そのものが、まだ無い。**

その上に、制度が築かれようとしている。

## 立場は、1年で反転した

ここで、Dario Amodeiの発言を時系列に置く。

Amodeiは、2023年7月の米上院証言以来、オープンソースAIの危険性を一貫して警告してきたと広く伝えられている。<br/>
（※ただし本書の調査では、この証言の逐語を一次資料で確認できていない。<br/>
確認できたのは、複数の二次的言及のみである。**ここは断定を避ける。**）

一次資料として確認できるのは、2026年のエッセイ『The Adolescence of Technology』である。<br/>
そこでAmodeiは、チップの輸出管理について**「great example ... mostly just work（好例だ……おおむね機能している）」**と記している。<br/>
**規制は効く、という立場だ。**

そして2026年、Anthropicは蒸留攻撃を公表し、規制強化の必要性を主張する側に立った。

## regulatory capture という批判

この構図に、独立系研究者から猛烈な反発が起きている。

Interconnectsの Nathan Lambert は2026年7月12日、こう論じた。<br/>
**オープンモデル禁止は安全をもたらさず、善意の側だけを損なう。**<br/>
蒸留論争は**偽の問題**であり、その正体は**Anthropic主導のregulatory capture**（**規制の虜**）である、と。

彼らの主張の骨格はこうだ。<br/>
APIの利用規約違反は、あくまでサービス上の問題である。<br/>
それを根拠にオープンウェイトモデル全体を法的に規制しようとするのは、<br/>
**安価な代替手段を潰し、自社の高額なAPI収益を守るための政治活動にすぎない。**

では、この批判は立証されているか。<br/>
**されていない。**<br/>
OpenAIとAnthropicがNTIAに公式コメントを提出していることは確認できる（2024年3月）。<br/>
両社がオープンウェイトのCBRN・サイバー攻撃リスクを指摘し、厳格な安全性テストを要求したことも確認できる。<br/>
だが、**「競合を締め出すためのcaptureだ」と断定できるだけの一次証拠——資金の流れ、内部の草案要求文書——は、発見できなかった。**

```mermaid
graph TD
    A["蒸留論争<br/>──────<br/>中国勢はなぜ数ヶ月で追いついたのか"] --> B["告発側<br/>──────<br/>Anthropic: 24,000不正アカウント<br/>1,600万回超のやり取り<br/>OpenAI: DeepSeekが出力を使用<br/>[当事者]"]
    A --> C["批判側<br/>──────<br/>Lambert: 偽の問題<br/>regulatory capture<br/>[言説]"]
    A --> D{"独立検証<br/>──────<br/>存在しない"}
    B -.->|"第三者による<br/>全容検証なし"| D
    C -.->|"資金の流れ・内部文書<br/>などの一次証拠なし"| D
    E["被告発側<br/>──────<br/>Moonshot・DeepSeek・MiniMax<br/>公式な技術的反証: 発見できず"] -.-> D
    D --> F["政策議論の前提が<br/>宙に浮いている<br/>──────<br/>蒸留の寄与度は<br/>誰も定量化していない"]

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style C fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style D fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style E fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style F fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

## 断じない、という判断

本書は、どちらが正しいかを断じない。<br/>
**断じられるだけの独立データが、存在しないからだ。**

これは中立を気取っているのではない。<br/>
むしろ逆で、**最も強い主張をしている。**

一方には、世界最高水準のAI企業が、自社ログを根拠に告発している。<br/>
他方には、独立研究者が、その告発の動機を疑っている。<br/>
そして中央には、**誰も測っていない空白がある。**

この空白の上で、政策が決まろうとしている。<br/>
8月1日に、米国のフレームワークが具体化する。<br/>
**証明されていない告発が、証明されないまま、制度の根拠になる。**

これが、特権的なオープンの第三の顔——**証拠の壁**である。

次章では、その制度そのものを見る。

### 参考文献

1. Anthropic「Detecting and preventing distillation attacks」（DeepSeek・Moonshot・MiniMaxによる約24,000の不正アカウント／1,600万回超のやり取り）※[当事者]
   <https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks>
2. Forbes「OpenAI Believes DeepSeek 'Distilled' Its Data For Training」（2025年1月29日）
   <https://www.forbes.com/sites/siladityaray/2025/01/29/openai-believes-deepseek-distilled-its-data-for-training-heres-what-to-know-about-the-technique/>
3. Dario Amodei「The Adolescence of Technology」（2026年・チップ輸出管理は "a great example … mostly just work"）
   <https://darioamodei.com/essay/the-adolescence-of-technology>
4. Nathan Lambert（Interconnects）「6 Months to Live for Open Models」（2026年7月12日・オープンモデル禁止は善意の側だけを損なう／蒸留論争＝regulatory capture）
5. Nathan Lambert & Florian Brand（Interconnects）「Open models recap: more on Kimi K3, Qwen 3.8, Xi's WAIC speech, distillation, the open-closed gap, and what's next」（2026年7月22日・RL段階の蒸留は費用と速度の両面で非現実的／最強モデルが最良の教師であることは文献で未確認／最先端オープンSFTデータセットはQwQ-32Bベース）
   <https://www.interconnects.ai/p/open-models-recap-more-on-kimi-k3>
6. Paddo「Distillation Is Not Scraping: Why the Internet's Favourite Take Is Wrong」（2026年7月）
   <https://paddo.dev/blog/distillation-is-not-scraping/>
7. OpenAI「OpenAI's comment to the NTIA on open model weights」（2024年3月提出）
   <https://openai.com/global-affairs/openai-s-comment-to-the-ntia-on-open-model-weights/>
8. Anthropic「Final Anthropic Response to Docket Number NTIA-2023-0009」（2024年3月提出）
   <https://downloads.regulations.gov/NTIA-2023-0009-0233/attachment_1.pdf>
9. Lawfare「Responding to AI Distillation Without Panic」
   <https://www.lawfaremedia.org/article/responding-to-ai-distillation-without-panic>

※本書の調査では、①Anthropicの告発を第三者が検証した記録、②Moonshot・DeepSeek・MiniMaxによる技術的データに基づく公式反証、③蒸留が性能向上に占める寄与度の定量分解、④「DeepSeekは550万ドルで学習した」という主張の独立監査——のいずれも発見できなかった。Amodeiの2023年上院証言については、一次資料での逐語確認ができていないため、内容の断定を避けた。また、Ben Thompsonの主張とLambertの反論は、いずれも公開された言説であり、どちらの立場も実験的に検証されたものではない。本書は、両者の対立そのものが「メカニズムが未解明である」ことの証拠だと位置づけている。

<br/>

---
# 第7章: 審査には、外側がある

2026年6月12日、Claude Fable 5が世界中で使えなくなった。<br/>
Amazonの報告に基づくサイバーセキュリティ上の懸念により、米国政府の輸出管理指令が発動したためである。<br/>
復帰したのは6月30日。Anthropicが「Redeploying Claude Fable 5」を公開したのは7月1日だった。

**約3週間。世界最高性能とされたモデルが、市場から消えた。**

同じ頃、OpenAIのGPT-5.6は一般公開が遅れ、政府承認済みの限られたパートナーへのプレビューに切り替わった。

そしてKimi K3は、**1日も止まっていない。**

## 法的には、審査は存在しない

ここで、法文を正確に読む必要がある。

2026年6月2日に署名された米国大統領令（EO 14409）は、こう命じている。<br/>
発効後**60日以内**に、機密ベンチマークを整備すること。<br/>
そして、リリース**最大30日前**の政府アクセスを含む**任意（voluntary）の枠組み**を設計すること。

同時に、同じ大統領令にこう明記されている。

> **"Nothing … shall be construed to authorize … mandatory governmental licensing, preclearance, or permitting"**
> （本令のいかなる規定も、義務的な政府ライセンス、事前許可、または許認可を認めるものと解釈してはならない）

**強制ライセンスは、明示的に否定されている。**<br/>
法文上、「公開前に政府の審査を通らなければならない」という制度は、存在しない。

それでも、Fable 5は3週間止まった。<br/>
GPT-5.6は延期された。

**法文と運用は、別である。**<br/>
これが、私が「見えない審査」と呼んできた構造だ。<br/>
誰も承認していない。誰も従うことを義務づけられていない。**それでも、誰も従わないわけではない。**

## 審査の外側は、法文にすら書かれていない

ここに、本章の核心がある。

EO 14409は、オープンウェイトを**明示的に除外していない。**<br/>
対象は "new AI models, including frontier models" の development / publication / release / distribution と読める。<br/>
つまり、法文上はオープンウェイトも射程に入り得る。

だが、実効性はどうか。

**Fable 5の一時停止が証明したのは、APIモデルであれば政府がキルスイッチを引けるということだ。**<br/>
Anthropicは自社のサーバーでモデルを動かしている。だから止められる。

Kimi K3の重みが、7月27日に公開されたとする。<br/>
その瞬間、それはインターネット上に無数に複製される。<br/>
**誰のサーバーにもない。誰にも止められない。**

これが、半導体との決定的な違いだ。<br/>
物理的なチップは港で止められる。<br/>
**重みファイルは、光の速度で国境を越える。**

本書の調査では、**重みファイルの流通を輸出管理でどこまで実効的に封じ込められるかを数量化した政府・独立研究を、発見できなかった。**<br/>
AISI（英国AI Security Institute）は「オープンモデルは安全装置の除去が**quickly and cheaply**に行える」と評価しているが、<br/>
**「配布そのものを止められるか」までは評価していない。**

```mermaid
graph LR
    A["EO 14409（2026/6/2）<br/>──────<br/>60日以内に機密ベンチマーク<br/>最大30日前の政府アクセス<br/>ただし任意枠組み"] --> B["法文<br/>──────<br/>『強制ライセンス・事前許可を<br/>認めるものと解釈してはならない』<br/>審査は存在しない"]
    A --> C["運用<br/>──────<br/>Fable 5: 6/12–6/30 停止（約3週間）<br/>GPT-5.6: 一般公開を延期<br/>審査は機能している"]
    B --> D{"見えない審査<br/>──────<br/>誰も承認していない<br/>誰も従わないわけでもない"}
    C --> D
    D --> E["審査の内側<br/>──────<br/>自社サーバーで動くモデル<br/>＝キルスイッチが効く"]
    D --> F["審査の外側<br/>──────<br/>Kimi K3: 停止 0日<br/>重みは光の速度で国境を越える"]
    F --> G["規制は、規制に従う者にしか効かない"]

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style C fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style D fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style E fill:#2E4756,stroke:#5B8FA8,color:#E8F1F5
    style F fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
    style G fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
```

## 善意の側だけが、損なわれる

Nathan Lambertの命題——**オープンモデル禁止は安全をもたらさず、善意の側だけを損なう**——は、ここで実証される。

止められるのは、止められる場所にいる者だけだ。<br/>
Anthropicは止められた。OpenAIは延期した。<br/>
**協力した者が、遅れた。**

そしてこの構造は、予期せぬ帰結を生んでいる。<br/>
**制裁リスクを嫌う非米中圏の国家や企業が、外部から遮断できないオープンウェイトへ向かう。**<br/>
Fable 5の3週間は、AI主権という概念に、これ以上ない説得力を与えてしまった。

「うちの基幹業務が、他国の政府判断で3週間止まるのか」——<br/>
この問いに、いま「止まらない」と答えられるのは、オープンウェイトだけである。

そして2026年7月、この構造はもう一段、具体的な形で現れた。

Hugging Faceが報告した事例である。<br/>
自社のシステムに対する攻撃エージェントを検知し、その挙動を解析しようとした。<br/>
**GPTとClaudeで解析を試みたが、いずれもガードレールに阻まれ、実行できなかった。**<br/>
攻撃コードの解析という行為そのものが、安全機構によって拒否されたのである。

結果、彼らはGLMを使った。<br/>
能力は劣るが、この種の防御的な解析にガードレールを設けていないモデルだった。

**米国の企業が、自社を防御するために、劣ったモデルに依存せざるを得ない。**

Lambertは、これを禁止論に対する最も強い反論として提示している。<br/>
仮に中国製オープンウェイトの利用を米国企業に禁じれば、どうなるか。<br/>
防御側は改善の手段を失い、攻撃側は世界中で改善を続ける。<br/>
**構造として、防御が改善せず攻撃だけが改善する設計を、自ら選ぶことになる。**<br/>
そのとき初めて、サイバーリスクは現実のものになる、と。

彼はまた、いま検討されている規制の形式そのものにも警告している。<br/>
明確な法的経路を示さないまま、法的措置の可能性をちらつかせる——<br/>
**実質的な「シャドウバン」**である。<br/>
何が禁じられているのかが定義されないため、企業は自主的に萎縮する。

第6章で見たとおり、蒸留の寄与度は測られておらず、そのメカニズムすら解明されていない。<br/>
その上で、定義されない禁止が、実務の現場に作用し始めている。

## 欧州も、無条件には開けない

EUは異なるアプローチを採る。

EU AI ActのGPAI（汎用AI）義務は2025年8月2日に適用開始され、**2026年8月2日から執行権限が発効する。**<br/>
欧州委員会のガイドラインは、**オープンソース提供者が一定の義務を免除される**と明示している。

だが、**これは無条件の免除ではない。**<br/>
計算量が10^25 FLOPsを超えるなどの「システミックリスク」を持つモデルは、**オープンソースであっても免除が取り消される。**<br/>
届出義務も、遵守義務も、執行の枠組みも残る。

つまり、EUにおいて「オープンだから自由」は成立しない。<br/>
フロンティア級オープンウェイトがEUでどう扱われるかは、**ライセンス形態とシステミックリスク判定次第**である。

## 8月1日に、何が確定するのか

EO 14409の60日期限は、2026年8月1日前後に到来する。<br/>
そこでNSA等が策定する「対象フロンティアモデル（covered frontier models）」の閾値が具体化する。

**その具体的な基準——サイバー能力の閾値、判定に用いる計算量（FLOPs）——は、現在プロセスが機密とされており、本書の調査では発見できなかった。**

だから、本書はこう書くしかない。<br/>
**8月1日に、この産業の制度的分水嶺が引かれる。だが、どこに引かれるかを、いま誰も知らない。**

一つだけ、断定できることがある。<br/>
**米国はオープンウェイトを即時全面禁止したわけではないが、フロンティアモデルを国家安全保障の枠組みへ引き寄せる方向に舵を切った。**<br/>
これはEOの文言から直接導ける。

そして、断定できないことがある。<br/>
**8月以降の枠組みで、フロンティア級オープンウェイトの一般公開が法的に禁止されるか否か。**<br/>
現状の枠組みは任意協力を基本としており、**物理的拡散を完全に阻止する法的・技術的手段は、確立されていない。**

次章では、その外側で何が起きているかを見る。<br/>
**Kimi K3が発表されたのと同じ日に、開放が国家の言葉になった。**

### 参考文献

1. The White House「Promoting Advanced Artificial Intelligence Innovation and Security」（2026年6月2日・EO 14409・60日以内の機密ベンチマーク／最大30日前の政府アクセス／任意枠組み／**"Nothing … shall be construed to authorize … mandatory governmental licensing, preclearance, or permitting"**）
   <https://www.whitehouse.gov/presidential-actions/2026/06/promoting-advanced-artificial-intelligence-innovation-and-security/>
2. Anthropic「Redeploying Claude Fable 5」（2026年7月1日・6月12日〜30日のグローバル提供停止）
   <https://www.anthropic.com/news/redeploying-fable-5>
3. The White House「White House Launches Gold Eagle Initiative for Unprecedented Cybersecurity Vulnerability Coordination」（2026年7月）
   <https://www.whitehouse.gov/releases/2026/07/white-house-launches-gold-eagle-initiative-for-unprecedented-cybersecurity-vulnerability-coordination/>
4. UK AI Security Institute「Frontier AI Trends Report」（2026年7月・オープンモデルは安全装置の除去が **quickly and cheaply** に可能／クローズドの方が監視・執行しやすい）
   <https://www.aisi.gov.uk/frontier-ai-trends-report>
5. European Commission「Guidelines for providers of general-purpose AI models」（GPAI義務は2025年8月2日適用／**2026年8月2日から執行権限が発効**／オープンソースは一部義務を免除されるが全面除外ではない）
   <https://digital-strategy.ec.europa.eu/en/policies/guidelines-gpai-providers>
6. NTIA「Dual-Use Foundation Models with Widely Available Model Weights」（2024年7月30日）
   <https://www.ntia.gov/programs-and-initiatives/artificial-intelligence/open-model-weights-report>
7. NTIA「Policy Approaches」（配布禁止・輸出管理・ライセンス・API制限の各オプションを議論）
   <https://www.ntia.gov/programs-and-initiatives/artificial-intelligence/open-model-weights-report/policy-approaches-recommendations/policy-approaches>
8. Council on Foreign Relations「Assessing Trump's Executive Order on AI Oversight」
   <https://www.cfr.org/articles/assessing-trumps-executive-order-on-ai-oversight>
9. Nathan Lambert & Florian Brand（Interconnects）「Open models recap: more on Kimi K3, Qwen 3.8, Xi's WAIC speech, distillation, the open-closed gap, and what's next」（2026年7月22日・Hugging Faceの攻撃解析がGPT/Claudeのガードレールに阻まれGLMを使用／禁止は防御側のみを劣化させる／「シャドウバン」型規制への警告）
   <https://www.interconnects.ai/p/open-models-recap-more-on-kimi-k3>

※Hugging Faceの事例は、Interconnects対談内での言及に基づく。本書の調査では、Hugging Face自身による一次的な報告文書を特定できていない。事例の存在と詳細については、追加の一次確認が必要である。
※EO 14409に基づき2026年8月1日を期限として策定中の「対象フロンティアモデル」のサイバー能力閾値・計算量基準は、プロセスが機密とされているため、本書の調査では確認できなかった。また、重みファイルの流通を輸出管理でどこまで実効的に封じ込められるかを数量化した研究も発見できなかった。

<br/>

---

# 第8章: 開放が、国家の言葉になった日

2026年7月17日。<br/>
Kimi K3が発表された、その同じ日。

北京のWAIC（世界人工知能大会）開幕式で、習近平は演説した。<br/>
そこにこの一節がある。

> **"encourage open source, openness, collaboration and sharing"**
> （オープンソース、開放、協働、共有を奨励する）

そして同じ演説で、こう約束した。<br/>
今後5年で、発展途上国に対し**5,000のAI研修・セミナーの機会**を提供する、と。

**同じ日である。**<br/>
世界最大のオープンウェイトが出た日に、開放が国家の言葉になった。

## 開発者エコシステムの重心は、すでに移っていた

これは象徴の話ではない。数字がある。

arXivで公開された**ATOMレポート**（The ATOM Report: Measuring the Open Language Model Ecosystem）は、<br/>
Hugging Faceにおけるモデルのダウンロード数を追跡している。

その結論はこうだ。<br/>
**2025年8月、中国製モデルのダウンロード数が米国製を逆転した。**<br/>
そして2026年3月時点で、**中国 11.5億回に対し、米国 7.23億回。**

これは、Kimi K3以前の話である。<br/>
**開発者エコシステムの重心は、フロンティア級オープンウェイトが登場する前に、すでに移動していた。**

つまり順序が逆だ。<br/>
中国がフロンティアに追いついたから世界が中国モデルを使い始めたのではない。<br/>
**世界がすでに中国モデルの上でアプリケーションを作っていたところに、フロンティア級が降ってきた。**

## なぜ、開くのか

天文学的なR&Dコストをかけて開発したモデルを、なぜ無償で公開するのか。<br/>
仮説は複数ある。

* **エコシステム支配**：世界中の開発者が中国製モデルの上に構築すれば、標準が握れる
* **ソフトパワー**：グローバルサウスにおけるAIインフラの標準化
* **米国規制の迂回**：チップ禁輸下で、開放によって影響力を確保する
* **半導体制約の裏返し**：限られた計算資源で効率を極限まで高めた成果を、公開で最大化する
* **マインドシェア獲得**：オープンはロスリーダーであり、収益はハイエンドAPIとソブリンAI案件で回収する

米国のシンクタンク（RAND／CSET）は、これを**米国の輸出管理を迂回し、非米同盟国においてAIインフラの標準とソフトパワーを掌握する国家戦略**と分析している。

ここで慎重に書く。<br/>
**「中国が技術的に余裕がないから開いている」という説明を直接支持する国家文書は、本書の調査では見つからなかった。**<br/>
一方、「意図的に開いている」という説明には、習近平演説という**一次的な政治的裏づけがある。**

だが、それでもなお、個々の企業が開く理由は、採用促進・API送客・開発者囲い込み・国際市場浸透など複数である。<br/>
**単一の動機には還元できない。**<br/>
そして、**国家が個々の企業のリリース判断をどこまで直接指揮しているかを示す一次資料も、発見できなかった。**

## 資本構造は、一次資料で追えない

Moonshotの資本構造については、報道が語ることと、確認できることに大きな差がある。

[報道]レベルでは、Alibaba・Tencentからの出資、評価額約300億ドル、20億ドルの新規調達、香港上場観測が伝えられている。<br/>
Zhipu AIは香港上場済み（時価総額約75億ドル）、MiniMaxも香港上場。

だが、**これらを裏づける会社自身の一次文書や目論見書を、本書の調査では発見できなかった。**<br/>
同様に、**AlibabaやTencentの民間出資の背後に中国政府の戦略ファンドがどれだけ流入し、意思決定に影響しているかを示す透明な財務証拠も、確認できない。**

これは本テーマの重要な空白である。<br/>
「国家戦略としてのオープンウェイト」という物語は魅力的だが、<br/>
**その物語を財務レベルで裏づける一次データは、いま存在しない。**

```mermaid
graph TD
    A["2026/7/17<br/>同じ一日"] --> B["Kimi K3 発表<br/>──────<br/>2.8兆パラメータ<br/>オープンウェイト世界最大"]
    A --> C["習近平 WAIC演説<br/>──────<br/>『open source, openness,<br/>collaboration and sharing』<br/>途上国へ5年で5,000研修枠"]
    D["ATOMレポート<br/>──────<br/>2025年8月: 中国製DLが米国製を逆転<br/>2026年3月: 中国11.5億 vs 米国7.23億"] --> E{"重心は、すでに移っていた<br/>──────<br/>フロンティア到達より前に<br/>エコシステムが移動していた"}
    B --> E
    C --> E
    E --> F["確認できないこと<br/>──────<br/>企業の資本構造の一次文書<br/>国家の関与を示す財務証拠<br/>グローバルサウスの実配備データ"]

    style A fill:#0A0D10,stroke:#2E4756,color:#E8F1F5
    style B fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style C fill:#5B8FA8,stroke:#8FB8CC,color:#0A0D10
    style D fill:#8FB8CC,stroke:#BFD9E6,color:#0A0D10
    style E fill:#FFFFFF,stroke:#FFFFFF,color:#0A0D10
    style F fill:#1C2A33,stroke:#2E4756,color:#BFD9E6
```

## ダウンロード数は、採用ではない

ここで、もう一つの空白を明記する。

**中国オープンウェイトのグローバルサウスにおける実配備データ——国別利用比率、ソブリンAI案件での採用件数——を、本書の調査では発見できなかった。**

習近平演説が約束したのは研修枠であり、実配備の定量データではない。<br/>
ATOMレポートが測ったのはダウンロード数であり、本番環境での採用ではない。

**ダウンロードは、意図の指標である。採用は、成果の指標である。**<br/>
この二つを混同すれば、第2章で解体した誤読を、地政学のレイヤーで繰り返すことになる。

## DeepSeekショックが教えたこと

最後に、この構図に一つの反証を置く。

2025年1月、DeepSeekが数百万ドルでフロンティア級を学習したと発表したとき、市場はパニックに陥った。<br/>
**「莫大な計算資源はもう不要になる」——Nvidiaの時価総額は1日で約6,000億ドル失われた。**

その後の現実は、逆だった。<br/>
トークン単価の下落は、**ジェボンズのパラドックス**を完全に実証した。<br/>
安くなったことで、1回のタスクの背後で数万回のループを回すエージェント型AIが爆発的に普及し、<br/>
**データセンターの総計算需要と電力消費は、以前を遥かに凌ぐ規模へ膨らんだ。**

**オープンウェイトの普及は、ハードウェア需要の破壊ではなく、創出だった。**

同じことが、いま繰り返されようとしている。<br/>
「Kimi K3が来た。プロプライエタリは終わりだ」——<br/>
2025年1月に同じことを言った人々が、6,000億ドルを失った。

そして安全性の側でも、慎重さが要る。<br/>
独立評価機関METRの最新レポート（2026年5月19日）によれば、<br/>
**現在のフロンティアモデルであっても、AIエージェントが人間の監視を逃れて自律的に自己複製したり、深刻なサイバー攻撃を完遂したりする能力は、人間の専門家に遠く及ばない。**<br/>
同時に、能力向上の曲線は極めて急峻であり、各国の評価機関は警戒を続けている。

**熱狂も、恐怖も、いまは実証を追い越している。**

### 参考文献

1. CGTN「Full text: Xi's keynote speech at the 2026 WAIC opening ceremony」（2026年7月17日・**"encourage open source, openness, collaboration and sharing"**／今後5年で発展途上国へ**5,000のAI研修・セミナー機会**）
   <https://news.cgtn.com/news/2026-07-17/Full-text-Xi-s-keynote-speech-at-the-2026-WAIC-opening-ceremony-1OQSfeoRvUs/p.html>
2. arXiv「The ATOM Report: Measuring the Open Language Model Ecosystem」（Hugging Faceダウンロード数：**2025年8月に中国製が米国製を逆転**／2026年3月時点で中国11.5億回 vs 米国7.23億回）
   <https://arxiv.org/html/2604.07190v2>
3. RAND / CSET「Open Models, Soft Power, and the Spectrum of U.S.-China Artificial Intelligence Competition」
   <https://cset.georgetown.edu/wp-content/uploads/RAND_PEA4686-1.pdf>
4. METR「Frontier Risk Report (February to March 2026)」（2026年5月19日・自律的な破壊活動・監視逃れの能力は人間の専門家に遠く及ばない）
   <https://metr.org/blog/2026-05-19-frontier-risk-report/>
5. PIIE「How the AI boom shrugged off the DeepSeek shock and keeps gaining steam」（2026年）
   <https://www.piie.com/blogs/realtime-economics/2026/how-ai-boom-shrugged-deepseek-shock-and-keeps-gaining-steam>
6. Stanford Cyber Policy Center「Taking Stock of the DeepSeek Shock」
   <https://cyber.fsi.stanford.edu/publication/taking-stock-deepseek-shock>
7. Red Hat「Why agentic AI needs an open inference stack」（推論コスト低下とエージェント需要の拡大）
   <https://www.redhat.com/en/blog/why-agentic-ai-needs-open-inference-stack>

※Moonshot・Zhipu・MiniMaxの資本構造（Alibaba/Tencent出資・評価額300億ドル・香港上場観測）は[報道]レベルの言及にとどまり、会社自身の一次文書での確証は本調査では得られなかった。中国政府の戦略ファンドの流入・意思決定への影響を示す財務証拠、およびオープンウェイトのグローバルサウスにおける実配備データ（国別利用比率・ソブリンAI採用件数）も発見できなかった。

<br/>

---

# 終章: 特権的なオープンの、その先へ

## 8つの壁が、一つのことを言っている

本書は、8つの章で8つの壁を見てきた。

| 章 | 壁 | 何が渡らないのか |
|---|---|---|
| 第1章 | 距離の壁（崩れた） | 通説の6ヶ月は、実測で3〜4ヶ月だった |
| 第2章 | 測定の壁 | 数字の大半は自己申告。Verified 0 / Self-reported 9 |
| 第3章 | 物理の壁 | 64アクセラレータ、1.4〜5.6TB。開いた扉は、重すぎる |
| 第4章 | 制度の壁 | ライセンス条文が未確認。再現できないものを検証と呼べない |
| 第5章 | 収益の壁 | 賢さは売り物でなくなったが、崩壊はしていない |
| 第6章 | 証拠の壁 | 蒸留は最も語られ、最も検証されていない |
| 第7章 | 審査の壁 | 法文に審査はない。それでも3週間止まった。外側は止まらない |
| 第8章 | 国家の壁 | 開放が国家の言葉になった。だが実配備は誰も測っていない |

壁は物質から言説へ、個人から国家へと拡大する。<br/>
だが、どの層でも同じ命題が反復される。

**フロンティアは、開かれた。だが「オープン」にはなっていない。**

## 想定される、3つの反論

### 反論1：「7月27日に重みが公開されれば、特権的なオープンは解消する」

解消しない。<br/>
重みが配られても、64アクセラレータ要件は残る。1.4〜5.6TBの質量は残る。<br/>
ライセンスに閾値条項が入っていれば、大規模な商用利用ほど条件が付く。<br/>
**解消するのは検証不能性であって、到達不能性ではない。**

むしろ7月27日以降、議論は精密になる。<br/>
Artificial Analysis、Vals AI、METR、AISIが追試を始めれば、いまの論争の半分は片づく。<br/>
**本書が主張しているのは「開かれない」ではない。「開くことと渡ることは別だ」である。**

### 反論2：「これは中国の宣伝にすぎない」

ちがう。<br/>
Artificial AnalysisはIntelligence Index 57、189モデル中4位と測定した。<br/>
Vals AIはVals Index 74.70%、38モデル中2位と測定した。<br/>
Arena.aiは、人間のブラインド選好でK3を首位に置いた。<br/>
**これらはすべて、Moonshotと利害関係のない独立機関である。**

事実は事実だ。<br/>
過小評価は、過大評価と同じだけ、判断を誤らせる。

### 反論3：「プロプライエタリはもう終わりだ」

データが支持しない。<br/>
Anthropicのrun-rateは470億ドル、年間100万ドル超の顧客は1,000社超。<br/>
OpenAIは月商20億ドル、企業売上が40%超。<br/>
エンタープライズのLLM支出は、依然として89%がclosed側にある。

そして何より、2025年1月に同じことを言った人々が、**6,000億ドルを失った。**<br/>
ジェボンズのパラドックスは、オープンウェイトの普及がハードウェア需要を破壊するのではなく、創出することを示した。

**起きるのは崩壊ではない。閉じたモデルが売るものが、能力から運用保証へ変わることだ。**

## 移動したのは、希少性の在処である

本書の中核命題を、最後にもう一度置く。

**移動したのは、モデルの所有権ではない。希少性の在処である。**

賢さは希少でなくなった。<br/>
Epoch AIが測った通り、フロンティアとの距離は3〜4ヶ月。あと数ヶ月待てば、誰でも同等の重みを手にできる。<br/>
では、いま何が希少なのか。

**重みでは代替できない文脈である。**

Kimi K3は2.8兆のパラメータを持つ。あなたの会社の業務プロセスを、一つも知らない。<br/>
Fable 5は世界最高のIntelligence Indexを持つ。あなたの顧客が何に困っているかを、一つも知らない。<br/>
**モデルが持っていないものだけが、これから希少になる。**

## D&Vの再定義

私は『Depth & Velocity』という方法論を書いてきた。<br/>
特権的なオープンの時代に、その2軸を定義し直す。

**Depthの再定義。**<br/>
かつてDepthとは、最も賢いモデルを選ぶ目利きだった。<br/>
いまDepthとは、**公開された重みの上に載せる、自社固有の文脈**である。<br/>
一次情報。業務の構造。判断の基準。これらは重みには入っていない。<br/>
**モデルが民主化されるほど、モデルに入っていないものの価値が上がる。**

**Velocityの再定義。**<br/>
かつてVelocityとは、最新APIへの追随速度だった。<br/>
いまVelocityとは、**審査の内側と外側を、同時に設計できる速度**である。<br/>
Fable 5は3週間止まった。GPT-5.6は13日遅れた。Kimi K3は1日も止まらなかった。<br/>
**片方だけに賭ける設計は、もう成立しない。**

そして、10:80:10の法則が、ここでも作動する。<br/>
最初の10%——どの推論をどこで動かし、何を自社の文脈として持つかを決める判断。<br/>
真ん中の80%——モデルが担う。もはやオープンでもクローズドでも、ほぼ同じ品質で。<br/>
最後の10%——その数字を、誰が測ったのかを問う判断。<br/>
**本書がしてきたことは、まさにこの最後の10%である。**

## 6日後に、確定するもの

本書は2026年7月18日に書かれた。<br/>
6日後、三つのことが起きる。

* **7月27日**：Kimi K3の重みが公開される（予定）。独立検証が初めて可能になる
* **8月1日**：EO 14409の60日期限。「対象フロンティアモデル」の閾値が具体化する
* **8月2日**：EU AI ActのGPAI義務の執行権限が発効する

**この6日間で、本書の事実基盤の半分は更新される。**

> **追記（2026年7月28日）**<br/>
> 7月27日、重みは予告どおり公開された。ライセンスも同時に開示され、名称は「Kimi K3 License」。<br/>
> 配布形式はMXFP4、報じられたファイルサイズは1.56TB。64アクセラレータ推奨は変わっていない。<br/>
> 詳細は第3章・第4章の追記に記した。<br/>
> 8月1日（EO 14409）と8月2日（EU AI Act）は、この追記の時点で未到来である。

だが、更新されないものがある。<br/>
**「誰が測ったのか」を問い続ける態度である。**

いま、この領域では、検証されていない数字が、検証されないまま前提になる。<br/>
[ベンダー]でも、[当事者]でも、[報道]でもない場所に立てる者だけが、その連鎖の外に出られる。

私は、その場所に立ってこの本を書いた。<br/>
Kimi K3を売る立場にない。プロプライエタリAPIを売る立場にもない。<br/>
GEOツールも、コンサルティング契約も、この結論には紐づいていない。<br/>
**だから、こう書ける。**

**フロンティアは、開かれた。だが「オープン」にはなっていない。**<br/>
そして、その二つが同時に真である世界で、希少なのは重みではない。<br/>
**重みが持っていない、あなたの文脈である。**

<br/>

---

## 📩 お仕事のご依頼

新規事業伴走 / AI戦略策定 / 講演・ワークショップ をお受けしています。<br/>
30分の無料初回MTGからスタートできます。

**山内怜史（Satoshi Yamauchi）**<br/>
Business Designer & AI Strategist at Sun Asterisk / Founder & CEO at Leading.AI

* [📒 note](https://note.com/satoshi_yamauchi)
* [🌐 Leading.AI](https://www.leading-ai.io/)

---

## Related Projects

本書は、著者のオープンソース知識リポジトリエコシステムの一作として位置づけられる。

| プロジェクト | 概要 | リンク |
|---|---|---|
| **The Edge of Intelligence** | AIがあなたのデバイスで動く時代。本書は、その命題が2.8兆パラメータで反転することを示す | [GitHub](https://github.com/Leading-AI-IO/edge-ai-intelligence) |
| **The Silence of Intelligence** | Dario Amodeiの思想を体系化。産業構造の解剖シリーズ第2弾 | [GitHub](https://github.com/Leading-AI-IO/the-silence-of-intelligence) |
| **The Anatomy of Anthropic** | Anthropicの戦略・製品・研究・安全性を包括的に解剖 | [GitHub](https://github.com/Leading-AI-IO/the-anatomy-of-anthropic) |
| **The Growth Engine of Anthropic** | Anthropicの1兆ドル到達の構造解剖 | [GitHub](https://github.com/Leading-AI-IO/the-growth-engine-of-anthropic) |
| **The Palantir Impact** | Palantir Foundryのオントロジー戦略を解剖。産業構造の解剖シリーズ第1弾 | [GitHub](https://github.com/Leading-AI-IO/palantir-ontology-strategy) |
| **Depth & Velocity** | 生成AI時代の新規事業開発方法論 | [GitHub](https://github.com/Leading-AI-IO/depth-and-velocity) |
| **The 10:80:10 Principle** | 人とAIの共創黄金比。AI時代の思考のOS | [GitHub](https://github.com/Leading-AI-IO/the-10-80-10-principle) |
| **The AI Strategist** | AIストラテジストという職業の定義 | [GitHub](https://github.com/Leading-AI-IO/the-ai-strategist) |
| **A Trillion Dollars and a Firebomb** | 1兆ドルと火炎瓶。AI時代の同時加速する現実 | [GitHub](https://github.com/Leading-AI-IO/a-trillion-and-a-firebomb) |
| **The Forward Deployed Shift** | 成果実装 ── FDEが示す、AIで「作る」が終わった世界の価値のありか | [GitHub](https://github.com/Leading-AI-IO/the-forward-deployed-shift) |

---

## 📝 License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).<br/>
© 2026 Satoshi Yamauchi / Leading AI — Licensed under CC BY 4.0

