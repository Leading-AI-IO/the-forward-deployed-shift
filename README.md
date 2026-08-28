# The Forward Deployed Shift

**成果実装 ── FDEが示す、AIで「作る」が終わった世界の価値のありか / The Forward Deployed Shift — Where Value Survives When "Building" Is Over**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Language](https://img.shields.io/badge/Language-Japanese%20%7C%20English-blue)](docs/)

<p align="left">
  <img src="./assets/ogp_design.png" width="90%">
</p>

*Read this in other languages: [English](README_en.md)*

---

> **定義｜What is The Forward Deployed Shift**
>
> **本書とは**、山内怜史（Satoshi Yamauchi）による、2026年5月の同じ週に
> AnthropicとOpenAIがそれぞれエンタープライズAI実装企業を設立した事実を
> 起点に、AIによって「作る」がコモディティ化した結果、価値が「顧客の
> 最前線で一次情報を掴み、個別解を再現可能な資産に変えて成果に変える力」
> ＝「成果実装」という一点に集約したことを論じた構造分析である。終章の
> 言葉：「作ることは、終わった。届けることが、いま始まった。」
>
> **This book** is a structural analysis by Satoshi Yamauchi examining how
> Anthropic and OpenAI both launched enterprise AI deployment ventures in
> the same week (May 2026), arguing value has consolidated into "outcome
> implementation" — the ability to capture non-synthesizable first-hand
> information at the customer frontline.
>
> *著者・全書籍一覧 / Author & full catalog: [github.com/Leading-AI-IO](https://github.com/Leading-AI-IO)*

---

## 📖 概要

2026年5月、わずか1週間の間に、AI業界の二大巨頭がほとんど同じ賭けに出た。Anthropicは Blackstone・Hellman & Friedman・Goldman Sachs と組んで新しいエンタープライズAIサービス会社を設立し、OpenAIは初期投資40億ドル超・19パートナーで「The Deployment Company」を立ち上げた。世界最高のモデルを持つ企業群が、同じタイミングで同じ結論に達した——**より賢いモデルを「作る」だけでは、もう足りない。**

その象徴が、求人需要が前年比で数百%規模に急増した職種、**Forward Deployed Engineer（FDE）**だ。だが本書は、FDEを「新しい高給エンジニア職」としては扱わない。FDEとは、AIによって「作る（BUILD）」がコモディティ化した結果、価値が**「成果実装」という一点に集約した構造的現象**の現れである。

本書はこの構造変化を一語で捉える。**「成果実装」**——AIを作るのではなく、顧客の最前線で一次情報を掴み、個別解を再現可能な資産へ変えて、実際の事業成果に変える力だ。MIT NANDAの調査では、生成AIに投じられた推定300〜400億ドルに対し約95%の組織がP&Lに効果を出せていない。その95%が死ぬ場所は、AIを作る研究室ではなく、AIを届ける顧客の最前線——**「死の谷」**である。

本書は、AIで「作る」が工業化された構造、Palantirが20年前に発明した成果実装の原型、合成できない一次情報（discovery）という最後の希少資源、受託と事業を分ける productization、そして D&V による方法論までを、一次データと現場の構造から一本の線でつなぐOSS書籍である。価値は「作ること」から「成果に変えること」へ、完全に移った。

**［2026年7月更新］** 本書の公開後、わずか3か月で、この構造はさらに検証された。6月30日にAWSが10億ドル、7月2日にMicrosoftが25億ドル規模の実装組織を設立し、7月22日にはa16zがFDE育成プログラムの初回65名を発表——その多くがPalantir出身者だった。第8章として、この3か月の記録を追記している。

---

## 📄 ドキュメント

| ファイル | 言語 | 内容 |
| --- | --- | --- |
| [the-forward-deployed-shift_JP.md](./docs/jp/the-forward-deployed-shift_JP.md) | 🇯🇵 日本語 | 本文（日本語版） |
| [the-forward-deployed-shift_EN.md](./docs/en/the-forward-deployed-shift_EN.md) | 🇺🇸 English | 本文（英語版） |

---

## 📑 目次

- **序章:** 作る時代の終わり
- **第1章:** 95%はなぜ現場で死ぬのか
- **第2章:** BUILDの工業化 — なぜ「作れること」は価値でなくなったのか
- **第3章:** 成果実装とは何か — Palantirが20年前に発明していた構造
- **第4章:** discoveryは合成できない — 一次情報という、唯一の希少資源
- **第5章:** 受託と資産化を分けるもの — productizationという分岐点
- **第6章:** 成果実装の方法論 — D&Vを現場へ適用する
- **第7章:** 既存事業の非連続成長 — 成果はモデルでなく、最後の1マイルから
- **第8章:** 作る側は、全員降りてきた — 2026年6-7月、レイヤーが垂直に埋まった
- **終章:** あなたが成果実装者になる

---

## 🔗 Related Projects

本書は、以下のOSSプロジェクトと相互に接続されている。

| プロジェクト | 概要 | リンク |
| --- | --- | --- |
| **Depth & Velocity**                | 成果実装のOSとなる、生成AI時代の新規事業開発方法論                  | [GitHub](https://github.com/Leading-AI-IO/depth-and-velocity)             |
| **The Palantir Impact**             | 成果実装の発祥。Palantir Foundryのオントロジー戦略を解剖。産業構造の解剖シリーズ第1弾 | [GitHub](https://github.com/Leading-AI-IO/palantir-ontology-strategy)     |
| **The 10:80:10 Principle**          | 判断の両端を握る思考のOS。人とAIの共創黄金比「10:80:10」の法則      | [GitHub](https://github.com/Leading-AI-IO/the-10-80-10-principle)  |
| **The Orchestrator**                | AI時代に最も希少な人材像「オーケストレーター」を世界で初めて定義            | [GitHub](https://github.com/Leading-AI-IO/the-orchestrator-in-the-ai-era) |
| **The Structural Shift from SaaS**  | SaaSからService-as-a-Softwareへの構造的転換。成果課金への移行。      | [GitHub](https://github.com/Leading-AI-IO/saas-is-dead-the-next-ai-business-model)  |
| **The AI Organization**             | AI導入が失敗する本質は技術ではなく組織にある。AI時代の組織論      | [GitHub](https://github.com/Leading-AI-IO/the-ai-organization)  |
| **The Agentic Commerce Economy**    | AIエージェントが購買を代行する時代、広告モデルの構造的変化            | [GitHub](https://github.com/Leading-AI-IO/agentic-commerce-economy)       |
| **The AI Strategist**               | AIストラテジストという職業を定義し、BTC交差点で戦うための実践的フレームワーク    | [GitHub](https://github.com/Leading-AI-IO/the-ai-strategist)              |
| **The Silence of Intelligence**     | Anthropic CEO ダリオ・アモディの思想を体系化。産業構造の解剖シリーズ第2弾 | [GitHub](https://github.com/Leading-AI-IO/the-silence-of-intelligence)    |
| **The Anatomy of Anthropic**        | Anthropicの戦略・製品・研究・安全性を包括的に解剖                | [GitHub](https://github.com/Leading-AI-IO/the-anatomy-of-anthropic)       |
| **The Growth Engine of Anthropic**  | Anthropicの1兆ドル到達の構造解剖                          | [GitHub](https://github.com/Leading-AI-IO/the-growth-engine-of-anthropic) |
| **What They Won't Teach You**       | AIに有利な世代が教えない、AIの使い方と"思考のOS"                 | [GitHub](https://github.com/Leading-AI-IO/what-they-wont-teach-you)       |
| **The Edge of Intelligence**        | AIがあなたのデバイスで動く時代：クラウドの終わりと、エッジの始まり           | [GitHub](https://github.com/Leading-AI-IO/edge-ai-intelligence)           |
| **The Redesign of Design Strategy** | デザイン戦略の再定義。IDEO崩壊の構造分析を含む                    | [GitHub](https://github.com/Leading-AI-IO/design-strategy-in-the-ai-era)  |
| **Advertising, Redesigned**         | AI時代の広告の未来を、7社の戦略と構造分析から描くOSS書籍              | [GitHub](https://github.com/Leading-AI-IO/advertising-redesigned)         |
| **A Trillion Dollars and a Firebomb** | 1兆ドルと火炎瓶。AI時代の同時加速する現実。 | [GitHub](https://github.com/Leading-AI-IO/a-trillion-and-a-firebomb)  |
| **The Attention Economy Is Over**   | アテンション・エコノミーの終わり。次世代SNSの設計条件。 | [GitHub](https://github.com/Leading-AI-IO/the-attention-economy-is-over)  |
| **Will AI Break the Planet?**       | 数十兆円のAIインフラ投資と、地球温暖化の「不可逆ライン」 | [GitHub](https://github.com/Leading-AI-IO/will-ai-break-the-planet)  |
| **Frontier-Grade Open Weights** | フロンティア級のオープンウェイトモデルは、開かれたのか。 | [GitHub](https://github.com/Leading-AI-IO/frontier-grade-open-weights)  |
| **Earned-ai-model-optionality** | AIモデルは選べる。選べるのは、選べるようにした企業だけだ。 | [GitHub](https://github.com/Leading-AI-IO/earned-ai-model-optionality)  |
| **Us-china-ai-competition** | 米中AI競争の多層構造 ── 決めているのは、強さではなく条件である。 | [GitHub](https://github.com/Leading-AI-IO/us-china-ai-competition)  |
| **The China AI Registry** | あなたが名前を言える5つの中国AIモデルは、中国が数えているものの1%に満たない。 | [GitHub](https://github.com/Leading-AI-IO/the-china-ai-registry)  |

---

## 👤 著者

**Satoshi Yamauchi** (山内 怜史)

* **AI Strategist & Business Designer at Sun Asterisk Inc.**

* **Founder / AI Strategist at [Leading.AI](https://www.leading-ai.io/)**

* 15年以上にわたりBusiness・Technology・Creativeの3領域を越境。フューチャーアーキテクトでITコンサルタントとして40案件のPL/PMを推進後、リクルートで事業戦略・新規事業開発に従事。Sun Asteriskでビジネスデザイナー兼AIストラテジストとして、新規事業×生成AIの方法論「Depth & Velocity」を体系化。

* This project is part of the research by Leading.AI.

* [📒 Read my insights on Note](https://note.com/satoshi_yamauchi)

* [🌐 Visit Leading.AI Official Website](https://www.leading-ai.io/)

---

## 🤝 Contributing

Issues and Pull Requests are welcome. 本書の構造分析に対するフィードバック、FDE・エンタープライズAI導入・成果実装の最新事例の追加情報、誤字脱字の修正など、皆様からのContributeを歓迎します。

---

## 📝 License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).<br>
© 2026 Satoshi Yamauchi / [Leading AI](https://www.leading-ai.io/) — Licensed under CC BY 4.0
