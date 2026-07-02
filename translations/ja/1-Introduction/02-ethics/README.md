# データ倫理入門

|![ スケッチノート by [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/02-Ethics.png)|
|:---:|
| データサイエンス倫理 - _スケッチノート by [@nitya](https://twitter.com/nitya)_ |

---

私たちは皆、データ化された世界に生きるデータ市民です。

市場の動向によると、2022年までに3分の1の大企業がオンラインの[マーケットプレイスおよび取引所](https://www.gartner.com/smarterwithgartner/gartner-top-10-trends-in-data-and-analytics-for-2020/)を通じて自社のデータを売買するようになります。<strong>アプリ開発者</strong>として、データ駆動の洞察やアルゴリズム駆動の自動化を日常のユーザー体験に統合することがより簡単かつ安価になります。しかしAIが普及するにつれて、そのようなアルゴリズムの大規模な[兵器化](https://www.youtube.com/watch?v=TQHs8SA1qpk)によって引き起こされる潜在的な害も理解する必要があります。

傾向は、2025年までに私たちは[180ゼタバイト](https://www.statista.com/statistics/871513/worldwide-data-created/)を超えるデータを生成し消費すると示しています。<strong>データサイエンティスト</strong>にとって、この情報の爆発は個人および行動データへの前例のないアクセスを提供します。それにより詳細なユーザープロファイルを構築し、しばしば[自由な選択の錯覚](https://www.datasciencecentral.com/the-pareto-set-and-the-paradox-of-choice/)を助長する方法で意思決定に微妙に影響を与える力を持ちます。これはユーザーを望ましい結果に促すために使われることもありますが、同時にデータプライバシー、自律性、アルゴリズムの影響の倫理的境界について重要な疑問を提起します。

データ倫理は現在、データサイエンスとエンジニアリングのための_必要なガードレール_であり、私たちのデータ駆動の行動による潜在的な害や意図しない結果を最小限に抑えるのに役立ちます。[GartnerのAIハイプサイクル](https://www.gartner.com/smarterwithgartner/2-megatrends-dominate-the-gartner-hype-cycle-for-artificial-intelligence-2020/)は、デジタル倫理、責任あるAI、AIガバナンスにおける関連トレンドを、大規模なメガトレンドであるAIの_民主化_と_産業化_のキードライバーとして特定しています。

![2020年のGartner AIハイプサイクル](https://images-cdn.newscred.com/Zz1mOWJhNzlkNDA2ZTMxMWViYjRiOGFiM2IyMjQ1YmMwZQ==)

本レッスンでは、データ倫理の魅力的な領域を探究します。基礎概念と課題からケーススタディ、そしてガバナンスなどの応用AI概念まで、データとAIに関わるチームや組織で倫理文化を築くための内容です。




## [事前講義クイズ](https://ff-quizzes.netlify.app/en/ds/quiz/2) 🎯

## 基本定義

まずは基本用語を理解しましょう。

「倫理（ethics）」という言葉は、[ギリシャ語の「ethikos」](https://en.wikipedia.org/wiki/Ethics)（およびその語根「ethos」）に由来し、「性格や道徳的本質」を意味します。

<strong>倫理</strong>とは、社会における私たちの行動を支配する共有価値と道徳原則を指します。倫理は法律に基づくものではなく、「正しい対間違い」とされる広く受け入れられた規範に基づいています。しかし倫理的配慮は、企業統治の施策や遵守を促進するための政府規制に影響を与えることがあります。

<strong>データ倫理</strong>は、「_データ、アルゴリズム、およびそれに対応する慣行_に関連する道徳的問題を研究し評価する」[倫理の新しい分野](https://royalsocietypublishing.org/doi/full/10.1098/rsta.2016.0360#sec-1)です。ここでの<strong>「データ」</strong>は生成、記録、管理、処理、普及、共有、使用に関連する行為を指し、<strong>「アルゴリズム」</strong>はAI、エージェント、機械学習、ロボットに注目し、<strong>「慣行」</strong>は責任あるイノベーション、プログラミング、ハッキング、倫理規範のようなトピックを含みます。

<strong>応用倫理</strong>は、[道徳的考慮の実践的適用](https://en.wikipedia.org/wiki/Applied_ethics)です。これは、_現実の行動、製品、プロセス_の文脈で倫理問題を積極的に調査し、定義された倫理価値に合致し続けるように是正措置を取るプロセスです。

<strong>倫理文化</strong>は、[応用倫理を実行化すること](https://hbr.org/2019/05/how-to-design-an-ethical-organization)に関連し、組織全体で倫理的原則と実践が一貫してスケーラブルに採用されることを確実にします。成功した倫理文化は、組織全体で倫理的原則を定義し、遵守に対して意味のあるインセンティブを提供し、組織のあらゆるレベルで望ましい行動を促進して倫理規範を強化します。


## 倫理の概念

このセクションでは、<strong>共有価値</strong>（原則）や<strong>倫理的課題</strong>（問題）といったデータ倫理の概念について説明し、これらの概念を実社会の文脈で理解できるように<strong>ケーススタディ</strong>を紹介します。

### 1. 倫理原則

あらゆるデータ倫理戦略は、受け入れ可能な行動を説明しデータとAIのプロジェクトにおける遵守行動を導く「共有価値」である_倫理原則_を定義することから始まります。これらは個人やチームレベルで定義できますが、多くの大企業はこれを企業レベルで定義し、すべてのチームに一貫して適用される_倫理的AI_のミッションステートメントやフレームワークで概説しています。

**例:** Microsoftの[責任あるAI](https://www.microsoft.com/en-us/ai/responsible-ai)のミッションステートメントは、_「私たちは人を第一に置く倫理原則に基づいたAIの進歩にコミットしている」_と述べ、以下の6つの倫理原則を示しています。

![Microsoftの責任あるAI](https://docs.microsoft.com/en-gb/azure/cognitive-services/personalizer/media/ethics-and-responsible-use/ai-values-future-computed.png)

これらの原則を簡単に見ていきましょう。_透明性_と_説明責任_は他の原則の基盤となる価値なので、まずここから始めます。

* [<strong>説明責任</strong>](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6)は、実践者に対しデータおよびAIの運用とこれらの倫理原則を遵守する責任を負わせます。
* [<strong>透明性</strong>](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6)は、データやAIの行動がユーザーにとって_理解可能_（解釈可能）であり、判断の背景にある理由が説明されることを保証します。
* [<strong>公平性</strong>](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6)は、AIが_すべての人_を公平に扱うことに焦点を当て、データやシステムにおける体系的または暗黙の社会技術的偏見を解消します。
* [<strong>信頼性と安全性</strong>](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6)は、AIが定義された価値に_一貫して_従い、潜在的な害や意図しない結果を最小限に抑えることを保証します。
* [<strong>プライバシーとセキュリティ</strong>](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6)は、データの由来を把握し、ユーザーに対して_データプライバシーと関連する保護_を提供することに関わります。
* [<strong>包摂性</strong>](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6)は、AIソリューションを意図的に設計し、多様な人間のニーズと能力を満たすよう適応させることを意味します。

> 🚨 あなたのデータ倫理ミッションステートメントはどのようなものになりますか？他の組織の倫理的AIフレームワークを調べてみましょう。例えば、[IBM](https://www.ibm.com/cloud/learn/ai-ethics)、[Google](https://ai.google/principles)、[Facebook](https://ai.facebook.com/blog/facebooks-five-pillars-of-responsible-ai/)の例があります。これらはどのような共有価値を共通して持っていますか？それらの原則は、彼らが運営するAIプロダクトや業界にどのように関連していますか？

### 2. 倫理的課題

倫理原則を定義したら、次は自分たちのデータとAIの行動がこれらの共有価値と一致しているかを評価します。行動を「データ収集」と「アルゴリズム設計」の2つのカテゴリで考えてみましょう。

データ収集では、行動はおそらく識別可能な生存個人に関する<strong>個人データ</strong>や個人識別情報(PII)を含みます。これには個人を_総合的に_特定する[多様な非個人データ項目](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-personal-data_en)も含まれます。倫理的課題は、_データプライバシー_、_データ所有権_、および利用者の_インフォームドコンセント_や_知的財産権_などの関連トピックに関わります。

アルゴリズム設計では、<strong>データセット収集と管理</strong>、それを用いて現実世界の文脈で結果を予測し意思決定を自動化する<strong>データモデル</strong>の訓練と展開を行います。倫理的課題は意図しない不公平や誤解を招きうる_データセットの偏り_、_データ品質_問題、_不公平性_、_誤表現_といったものに由来します。これらには体系的な問題も含まれます。

どちらの場合も、倫理的課題は行動が共有価値と衝突する可能性のある領域を示しています。これらの懸念を検出、軽減、最小化、または排除するには、行動に関する道徳的な「イエス／ノー」の質問をし、必要に応じて是正措置を取る必要があります。以下にいくつかの倫理的課題とそれに関わる道徳的質問を見ていきましょう。


#### 2.1 データ所有権

データ収集はしばしばデータ主体を特定可能な個人データを伴います。[データ所有権](https://permission.io/blog/data-ownership)は、データの作成、処理、および普及に関する_管理_と[_ユーザー権利_](https://permission.io/blog/data-ownership)に関わります。

問うべき道徳的な質問は：
 * データの所有者は誰か？（ユーザーか組織か）
 * データ主体はどのような権利を持つか？（例：アクセス、消去、可搬性）
 * 組織はどのような権利を持つか？（例：悪意あるユーザーレビューの修正）

#### 2.2 インフォームド・コンセント

[インフォームド・コンセント](https://legaldictionary.net/informed-consent/)は、ユーザーが目的、潜在的なリスク、代替案を含む関連情報を十分に理解した上で（データ収集などの）行為に同意する行為を定義します。

検討すべき質問は：
 * ユーザー（データ主体）はデータの取得と利用の許可を与えたか？
 * ユーザーはなぜそのデータが取得されたのか理解しているか？
 * ユーザーは参加による潜在的リスクを理解しているか？

#### 2.3 知的財産権

[知的財産権](https://en.wikipedia.org/wiki/Intellectual_property)は、人間の創造的取り組みによる無形の創作物を指し、それが個人や企業に経済的価値をもたらす場合があります。

検討すべき質問は：
 * 収集されたデータはユーザーまたは企業に経済的価値があったか？
 * <strong>ユーザー</strong>は知的財産権を持つか？
 * <strong>組織</strong>は知的財産権を持つか？
 * これらの権利が存在する場合、それをどのように保護しているか？

#### 2.4 データプライバシー

[データプライバシー](https://www.northeastern.edu/graduate/blog/what-is-data-privacy/)または情報プライバシーは、個人識別情報に関してユーザーのプライバシーの保護とユーザーの身元の保護を指します。

検討すべき質問は：
 * ユーザーの（個人）データはハッキングや漏洩から保護されているか？
 * ユーザーデータは許可されたユーザーと利用状況のみにアクセス可能か？
 * データ共有や配布時にユーザーの匿名性は保たれているか？
 * 匿名化されたデータセットからユーザーの特定は可能か？

#### 2.5 忘れられる権利

[忘れられる権利](https://en.wikipedia.org/wiki/Right_to_be_forgotten)または[消去権](https://www.gdpreu.org/right-to-be-forgotten/)は、特定の状況下でインターネット検索や他の場所からの個人データの削除・除去をユーザーが要求できる個人データ保護の追加権利を与えます。過去の行動を理由に不利益を受けずにオンラインで再出発することが可能になります。

検討すべき質問は：
 * システムはデータ主体が消去を要求できるか？
 * ユーザーの同意撤回が自動的な消去を起動すべきか？
 * 同意なし、または違法な手段でデータが収集されたことはないか？
 * データプライバシーに関する政府規制を遵守しているか？

#### 2.6 データセットの偏り

データセットまたは[収集の偏り](http://researcharticles.com/index.php/bias-in-data-collection-in-research/)は、アルゴリズム開発のために_代表性のない_部分集合を選択することで、多様なグループに対する結果の不公平を生み出す可能性があります。偏りの種類には選択バイアス、ボランティアバイアス、計測機器の偏りなどがあります。

検討すべき質問は：
 * 代表的なデータ主体セットを募集したか？
 * 収集・管理したデータセットを様々な偏りについてテストしたか？
 * 発見された偏りを軽減または除去できるか？

#### 2.7 データ品質

[データ品質](https://lakefs.io/data-quality-testing/)は、アルゴリズム開発に使用する管理済みデータセットの妥当性を検証し、目的に対して特徴や記録が必要な精度と一貫性を満たしているかどうかを評価します。

検討すべき質問は：
 * ユースケースに有効な_特徴_を収集したか？
 * 多様なデータソース間で_一貫した_データ収集が行われたか？
 * 多様な条件やシナリオに対してデータセットは_完全_か？
 * 現実を正確に反映する情報が_正確に_収集されているか？
#### 2.8 アルゴリズムの公平性

[Algorithm Fairness](https://towardsdatascience.com/what-is-algorithm-fairness-3182e161cf9f)は、アルゴリズム設計が特定のデータ主体のサブグループに体系的に差別をもたらし、_割り当て_（そのグループからリソースが拒否または withheld される）や_サービスの品質_（AIがあるサブグループに対して他のグループほど正確でない）に[潜在的な害](https://docs.microsoft.com/en-us/azure/machine-learning/concept-fairness-ml)を生じさせていないかを確認します。

ここで検討すべき質問は次の通りです：
 * 多様なサブグループや条件でモデルの精度を評価しましたか？
 * ステレオタイプ化などの潜在的な害がシステムにないか精査しましたか？
 * 特定された害を軽減するためにデータ修正やモデル再学習が可能ですか？

[AI Fairnessチェックリスト](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE4t6dA)などのリソースを活用して詳細を学びましょう。

#### 2.9 誤った表現

[Data Misrepresentation](https://www.sciencedirect.com/topics/computer-science/misrepresentation)は、意図した物語を支援するために正直に報告されたデータからの洞察を欺瞞的に伝えていないかを問うものです。

ここで検討すべき質問は次の通りです：
 * 不完全または誤ったデータを報告していますか？
 * 誤解を与える結論を導くようなデータの可視化をしていますか？
 * 結果を操作するために選択的な統計手法を使っていますか？
 * 別の結論を示す可能性のある代替説明はありますか？

#### 2.10 自由な選択
[Illusion of Free Choice](https://www.datasciencecentral.com/profiles/blogs/the-illusion-of-choice)は、システムの「選択アーキテクチャ」が、意思決定アルゴリズムを用いて利用者に選択肢とコントロールを持たせているように見せかけつつ、好ましい結果に誘導する現象です。これらの[ダークパターン](https://www.darkpatterns.org/)は、利用者に社会的および経済的な害をもたらす可能性があります。ユーザーの意思決定は行動プロファイルに影響を与えるため、これらの行動は将来の選択に影響し、害を拡大または延長する可能性があります。

ここで検討すべき質問は次の通りです：
 * ユーザーはその選択の意味を理解していましたか？
 * ユーザーは（代替の）選択肢とそれぞれの利点と欠点を認識していましたか？
 * ユーザーは自動化または誘導された選択を後で取り消せますか？

### 3. ケーススタディ

これらの倫理的課題を実際の文脈で理解するためには、倫理違反を見過ごしたときに個人や社会に及ぶ潜在的な害と結果を浮き彫りにするケーススタディを見るのが役立ちます。

いくつかの例を示します：

| 倫理課題 | ケーススタディ | 
|--- |--- |
| <strong>インフォームドコンセント</strong> | 1972年 - [Tuskegee Syphilis Study](https://en.wikipedia.org/wiki/Tuskegee_Syphilis_Study) - 研究に参加したアフリカ系アメリカ人男性は無料の医療を約束されたが、診断結果や治療の有無が被験者に知らせられず欺かれた。多くの被験者が死亡し、パートナーや子供にも影響が及んだ。この調査は40年間続いた。 | 
| <strong>データプライバシー</strong> | 2007年 - [Netflixデータ賞](https://www.wired.com/2007/12/why-anonymous-data-sometimes-isnt/)は、研究者に50,000人の匿名化された映画評価1,000万件を提供し推薦アルゴリズムの改善を助けた。しかし、研究者は匿名化データとIMDbコメントなどの_外部データセット_を照合し、一部のNetflix加入者の匿名性を事実上喪失させた。|
| <strong>収集バイアス</strong> | 2013年 - ボストン市が[Street Bump](https://www.boston.gov/transportation/street-bump)という市民が道路の穴を報告できるアプリを開発し、より良い道路データを入手した。しかし[低所得層の人々は車や電話のアクセスが限定的](https://hbr.org/2013/04/the-hidden-biases-in-big-data)で、そのグループの道路問題はこのアプリで見えなくなった。開発者は学者と協力し、公平なアクセスとデジタル格差の問題に取り組んだ。 |
| <strong>アルゴリズムの公平性</strong> | 2018年 - MITの[Gender Shades Study](http://gendershades.org/overview.html)は性別分類AI製品の精度を評価し、女性や有色人種で精度差を明らかにした。[2019年のApple Card](https://www.wired.com/story/the-apple-card-didnt-see-genderand-thats-the-problem/)は女性に男性よりも少ない信用枠を与えていると見られた。両例はアルゴリズムバイアスが社会経済的害を招く問題を示している。|
| <strong>データの誤表現</strong> | 2020年 - ジョージア州公衆衛生局がリリースしたCOVID-19チャートは、x軸の非時系列順序により確認された症例の傾向について市民を誤解させるものであった。[グラフによる誤表現の例](https://www.vox.com/covid-19-coronavirus-us-response-trump/2020/5/18/21262265/georgia-covid-19-cases-declining-reopening)として挙げられる。 |
| <strong>自由な選択の錯覚</strong> | 2020年 - 学習アプリ[ABCmouseがFTCの訴えで1,000万ドル和解](https://www.washingtonpost.com/business/2020/09/04/abcmouse-10-million-ftc-settlement/)した。親たちは解約できないサブスクリプション料金を支払わされた。これは選択アーキテクチャにおけるダークパターンであり、ユーザーが潜在的に害になる選択に誘導された例である。 |
| <strong>データプライバシーとユーザー権利</strong> | 2021年 - Facebookの[データ漏えい](https://www.npr.org/2021/04/09/986005820/after-data-breach-exposes-530-million-facebook-says-it-will-not-notify-users)により5億3,000万人のデータが漏れ、FTCに50億ドルの和解金を支払った。しかし漏えいをユーザーに通知せず、データ透明性とアクセスに関するユーザー権利を侵害した。 |

さらなるケーススタディを探索したいですか？以下のリソースをチェックしてください：
* [Ethics Unwrapped](https://ethicsunwrapped.utexas.edu/case-studies) - 多様な産業での倫理ジレンマ。
* [Data Science Ethicsコース](https://www.coursera.org/learn/data-science-ethics#syllabus) - 代表的なケーススタディを探求。
* [問題が起きた事例](https://deon.drivendata.org/examples/) - deonチェックリストと例。

> 🚨 ご自身が見たケーススタディについて考えてみてください。あなたの人生で似た倫理的課題を経験したり影響を受けたことがありますか？このセクションで議論した倫理課題のいずれかを示す別のケーススタディを少なくとも一つ思い浮かべられますか？

## 応用倫理

私たちは倫理の概念、課題、現実のケーススタディについて話してきました。しかし、プロジェクトに倫理原則や実践をどのように適用し始めますか？また、より良いガバナンスのためにこれらの実践をどう運用化しますか？実際の解決策を探りましょう：

### 1. プロフェッショナルコード

プロフェッショナルコードは、組織がメンバーに倫理原則と使命を支持させる「動機付け」の一つの方法を提供します。コードは専門的行動のための_道徳的ガイドライン_であり、従業員やメンバーが組織の原則に沿った意思決定をするのを助けます。これはメンバーの自主的遵守に依存しますが、多くの組織はメンバーの遵守を促すための追加の報酬や罰則を設けています。

例：

 * [Oxford Munich](http://www.code-of-ethics.org/code-of-conduct/) 倫理規範
 * [Data Science Association](http://datascienceassn.org/code-of-conduct.html) 行動規範（2013年制定）
 * [ACM Code of Ethics and Professional Conduct](https://www.acm.org/code-of-ethics)（1993年以降）

> 🚨 あなたはプロのエンジニアリングまたはデータサイエンス組織に所属していますか？彼らのサイトを調べて、プロフェッショナルな倫理規範が定義されているか確認してください。それは彼らの倫理原則について何を言っていますか？メンバーが規範を守るようにどう「動機付け」ていますか？

### 2. 倫理チェックリスト

プロフェッショナルコードは実践者に求められる_倫理的行動_を定義しますが、特に大規模プロジェクトでの執行には[既知の限界](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md)があります。代わりに、多くのデータサイエンス専門家は、原則と実践をより決定的かつ実行可能な方法で<strong>結びつける</strong>[チェックリスト](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md)を推奨しています。

チェックリストは質問を「はい/いいえ」のタスクに変換し、標準的な製品リリースのワークフローで追跡可能にします。

例：
 * [Deon](https://deon.drivendata.org/) - [業界推奨](https://deon.drivendata.org/#checklist-citations)に基づく一般用途のデータ倫理チェックリストで、コマンドラインツールによる統合が容易。
 * [Privacy Audit Checklist](https://cyber.harvard.edu/ecommerce/privacyaudit.html) - 法的・社会的リスクの観点から情報取扱慣行の一般的ガイダンス。
 * [AI Fairness Checklist](https://www.microsoft.com/en-us/research/project/ai-fairness-checklist/) - AI実務者が作成した、公平性チェックの導入と統合をサポート。
 * [22 questions for ethics in data and AI](https://medium.com/the-organization/22-questions-for-ethics-in-data-and-ai-efb68fd19429) - 設計、実装、組織の文脈で倫理問題の初期探究に適したより開かれたフレームワーク。

### 3. 倫理規制

倫理は共有価値を定義し、正しいことを_自主的に_行うことです。<strong>コンプライアンス</strong>は、定められた法律を順守することに関わります。<strong>ガバナンス</strong>は組織が倫理原則を実施し、既存の法律に準拠するための運営全般を指します。

今日、ガバナンスは組織内で二つの形態をとっています。第一に、組織内のすべてのAI関連プロジェクトで<strong>倫理的AI</strong>原則を定義し、その導入を運用化する実践を設けること。第二に、運営地域の対象となるすべての政府規制の<strong>データ保護規制</strong>に準拠することです。

主なデータ保護・プライバシー規制の例：

 * `1974`年、[米国プライバシー法](https://www.justice.gov/opcl/privacy-act-1974) - 連邦政府による個人情報の収集、利用、開示を規制。
 * `1996`年、[米国医療保険の携行性と説明責任に関する法律（HIPAA）](https://www.cdc.gov/phlp/publications/topic/hipaa.html) - 個人の健康データを保護。
 * `1998`年、[米国児童オンラインプライバシー保護法（COPPA）](https://www.ftc.gov/enforcement/rules/rulemaking-regulatory-reform-proceedings/childrens-online-privacy-protection-rule) - 13歳未満の児童のデータプライバシーを保護。
 * `2018`年、[一般データ保護規則（GDPR）](https://gdpr-info.eu/) - ユーザー権利、データ保護、プライバシーを提供。
 * `2018`年、[カリフォルニア消費者プライバシー法（CCPA）](https://www.oag.ca.gov/privacy/ccpa) - 消費者に個人データに関する多くの_権利_を付与。
 * `2021`年、中国の[個人情報保護法](https://www.reuters.com/world/china/china-passes-new-personal-data-privacy-law-take-effect-nov-1-2021-08-20/)が成立し、世界で最も厳しいオンラインデータプライバシー規制の一つを作成。

> 🚨 欧州連合のGDPR（一般データ保護規則）は現在も最も影響力のあるデータプライバシー規制の一つです。それが市民のデジタルプライバシーと個人データを保護する[8つのユーザー権利](https://www.freeprivacypolicy.com/blog/8-user-rights-gdpr)も定義していることをご存じでしたか？それらが何か、なぜ重要であるかを学びましょう。

### 4. 倫理文化

「法律の文面」を満たすだけの_コンプライアンス_と、AIの武器化を加速させ得る[システム的問題](https://www.coursera.org/learn/data-science-ethics/home/week/4)（硬直化、情報の非対称性、分配的不公平など）に対処する間には依然として形にしにくいギャップがあります。

後者は[組織間で感情的なつながりと一貫した共有価値を築く](https://towardsdatascience.com/why-ai-ethics-requires-a-culture-driven-approach-26f451afa29f)、産業全体にまたがる倫理文化を定義する[協働的アプローチ](https://www.coursera.org/learn/data-science-ethics/home/week/4)を必要とします。これには、組織内におけるより[形式化されたデータ倫理文化](https://www.codeforamerica.org/news/formalizing-an-ethical-data-culture/)の構築が求められます。誰でも[アンドンコード](https://en.wikipedia.org/wiki/Andon_(manufacturing))（プロセス初期で倫理懸念を提起）を引ける環境とし、AIプロジェクトのチーム形成において_倫理評価_（例：採用時の評価）を主要基準にします。

---
## [講義後クイズ](https://ff-quizzes.netlify.app/en/ds/quiz/3) 🎯
## 復習 & 自習

講座や書籍は主要な倫理概念と課題の理解に役立ち、ケーススタディやツールは現実の文脈での応用倫理実践を支援します。以下は出発点としてのリソースです。

* [Machine Learning For Beginners](https://github.com/microsoft/ML-For-Beginners/blob/main/1-Introduction/3-fairness/README.md) - Microsoftによる公平性のレッスン。
* [Principles of Responsible AI](https://docs.microsoft.com/en-us/learn/modules/responsible-ai-principles/) - Microsoft Learnの無料学習パス。
* [Ethics and Data Science](https://resources.oreilly.com/examples/0636920203964) - O'Reillyの電子書籍（M. Loukides、H. Mason他）
* [Data Science Ethics](https://www.coursera.org/learn/data-science-ethics#syllabus) - ミシガン大学のオンラインコース。
* [Ethics Unwrapped](https://ethicsunwrapped.utexas.edu/case-studies) - テキサス大学のケーススタディ。

# 課題

[Write A Data Ethics Case Study](assignment.md)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**免責事項**：
本書類は AI 翻訳サービス [Co-op Translator](https://github.com/Azure/co-op-translator) を使用して翻訳されています。正確性を期していますが、自動翻訳には誤りや不正確な部分が含まれる可能性があることをご承知おきください。原文の原語版が正式な情報源とみなされるべきです。重要な情報については、専門の人間による翻訳を推奨します。本翻訳の利用により生じたいかなる誤解や解釈違いについても、当方は責任を負いかねます。
<!-- CO-OP TRANSLATOR DISCLAIMER END -->