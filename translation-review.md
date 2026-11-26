# 法律分析指南中译英审校报告

审校对象为翻译提交 `86147c9` 的 37 份 Markdown 文件，逐项对照其父提交 `d702cd8` 的同路径中文底稿。行号均指 `86147c9`。未发现整份文件、整段正文或表格行漏译。需要修订的是句内丢失的限定、改变法律概念或核查范围的译法，以及翻译后难以复用的原始检索标识。

以下意见针对修订前的译文，所列问题已在工作区英文稿中修订。优先处理了三处会改变判断起点的表述。“2021 年前后”应以《民法典》施行日划界。“赡养”应保留法定亲属范围和给付条件。澳大利亚扣船程序中的 *relevant person* 应保留其假设性责任。查找中国裁判时，还应恢复可复制的原案号与中文查询式。

## 通用指南与模板

| 英文稿位置 | 中文与现译 | 建议英文 | 对使用者的影响 |
|---|---|---|---|
| `README.md:26` | “房屋还没过户”译为 *title to the home has not yet been transferred* | *The sale contract is invalid because the transfer of title has not yet been registered.* | 这是供评审的错误答案，须保留其错误结论。中文以未办过户手续为前提，英文却把物权尚未转移直接当成事实。按建议改写，才能和第 25 行的问题核对同一事实。见[《民法典》第209、215条](https://www.court.gov.cn/zixun/xiangqing/233181.html)。 |
| `SKILL.md:57` | “可交付‘阶段性分析’”译为 *deliver an "interim analysis"* | *If the necessary materials or decisive facts genuinely cannot be obtained, you may provide an interim analysis.* | 现译把准许交付写成指令。后句关于列明待补材料、未定结论和下一步的要求应继续适用于选择交付的情形。 |
| `SKILL.md:89` | “事实发生日期用于选法”译为 *The event date selects the applicable law* | *Use the date of the relevant events to identify the version of the law that applies.* | 本段是在区分事实日期、完成日期和核验日期。现译容易让人以为日期本身即可决定准据法，也掩盖了查明过渡条款的必要性。 |
| `references/search-observations.md:16` | “后案状态仍需另查”译为 *subsequent case history still requires a separate search* | *How later decisions have treated this judgment still needs to be checked.* | 英文法律检索区分同一案件的上诉历程与其他案件后来如何援用、区别或否定其判例命题。此处待查的是后者。见[墨尔本大学法律图书馆的检索工具对照表](https://law.unimelb.edu.au/law-library/research-tools/australian-case-citator-comparison)。 |

**法源名称与标识。** `references/search-observations.md:12` 应与合同编案例和中国大陆检索指南一起保留原案号 `（2019）最高法知民终433号`。可以附英文转写，案号应能与原件“关联索引”直接比对。第 12、14 行等处的 *People's Courts Case Database* 如作为机构网页的专名，建议统一为最高人民法院英文网站栏目所用的 *People’s Court Case Database*。[案例库原件，第3页](https://ipc.court.gov.cn/upload/file/2025/12/01/15/30/20251201153032_81336.pdf) · [最高人民法院英文案例栏目](https://english.court.gov.cn/cases.html)

`README.md:3` 将“一套中文 Agent Skill”改写为 *an English-language Agent Skill*，符合本次英文化的实际情况。交付语言仍由用户指定，见两个回答模板第 3 行。

## 中国大陆法（民法典分编以外）

### 影响法律判断或检索的译法

| 位置 | 中文 → 现译 | 建议英文 | 判断依据 |
|---|---|---|---|
| `references/mainland-china/index.md:16` | “2021 年前后发生的事实” → “Facts arising before or after 2021” | “Facts arising before, on, or after the Civil Code’s entry into force on January 1, 2021” | 英译按年份划界，字面跳过整个 2021 年。时间效力应比较法律事实与施行日，2021 年内发生的事实尤其需要覆盖。[最高法时间效力规定第1条](https://www.court.gov.cn/zixun/xiangqing/282051.html) |
| `references/mainland-china/companies.md:14` | “2024年7月1日前后” → “before or after July 1, 2024” | “Identify when each relevant event occurred in relation to the commencement of the revised Company Law on 1 July 2024.” | 修订法在7月1日施行，恰在当日发生的出资、转让或决议也需选定适用版本。同句所引文号建议附上中文原号 `法释〔2024〕7号`。[最高法关于公司法时间效力的规定](https://www.court.gov.cn/fabu/xiangqing/436481.html) |
| `references/mainland-china/public-law.md:12` | “尤其查2026年8月15日前后持续行为、合同履行或时效届满情况” → “expiry of limitation periods spanning August 15, 2026” | “Check whether the conduct continued across August 15, 2026, when the contract was performed, and whether the limitation period had already expired by that date.” | 若只检查跨越该日的时效期间，会先行排除恰需辨别的情形，即旧法时效在施行时已经届满。合同争议还要看具体履行在何时发生。[最高法时间效力规定第3、5条](https://www.court.gov.cn/fabu/xiangqing/508001.html) |
| `references/mainland-china/social.md:11` | “赡养” → “support of elderly parents” | “maintenance of parents and, where applicable, grandparents” | “elderly”添加年龄门槛，“parents”遗漏法律在一定条件下规定的祖父母、外祖父母。第1067条规定给付请求时采用缺乏劳动能力或生活困难的条件，第1074条另列孙辈赡养情形。[全国人大常委会公报所载条文](https://wb.flk.npc.gov.cn/flfg/PDF/bd53dd912c1048f2aecbaa229238334b.pdf) |
| `references/mainland-china/criminal.md:13` | “拖欠货款……合同与付款证据可以支持民事履行情况” → “owes payment for goods … can establish the state of civil performance” | “The company is overdue in paying for the goods, so the person in charge has already committed fraud.” / “The contract and payment records can support findings about whether the parties performed their contractual obligations.” | 普通未清偿债务可以尚未到期。原例给定了逾期。后句则把证据“支持”有关履行情况的判断升为能“证实”。两处共同改变示例中既有事实与待证事实之间的界线。 |
| `references/mainland-china/search.md:10`、`:14`、`:22`、`:23`、`:31` | “（2019）最高法知民终433号”。可直接执行的 `site:court.gov.cn "第五百六十三条" "合理期限"` 等 → “(2019) Zui Gao Fa Zhi Min Zhong No. 433”。英文关键词并要求读者自行换成中文 | “Case No. （2019）最高法知民终433号”. “Search for `site:ipc.court.gov.cn "最高法知民终433号"`.” “Search for `site:court.gov.cn "第五百六十三条" "合理期限"`.” 同样保留“法释〔年份〕序号”和两组事实关键词。 | 入库编号、案号、文号与引号内查询串是定位原文的数据。可附英文释义。音译不能在中文裁判内逐字定位。原案 PDF 同时列有两个不同编号。[最高法知识产权法庭案例文本](https://ipc.court.gov.cn/upload/file/2025/12/01/15/30/20251201153032_81336.pdf) |
| `references/mainland-china/procedure.md:11`、`:12` | “司法救助”“司法协助安排” → 两处均为 “judicial assistance” | 第11行 “judicial aid for people facing hardship”。第12行 “arrangements for mutual judicial assistance” | 第一项是当事人或受害人的困难救助，第二项指跨法域送达、取证等法院间协作。官方报道有时也将前者译作 judicial assistance，但相邻两行用完全相同的英文，会误指申请主体和受理机制。[最高法有关司法救助的英文说明](https://english.court.gov.cn/2026-08/12/c_1204756.htm) · [最高法司法协助栏目](https://english.court.gov.cn/judicialassistance.html) |
| `references/mainland-china/companies.md:11` | “未作决议，债权人一定不能向公司索赔” → “without a resolution, the creditor can never recover from the company” | “Without a resolution, the creditor can never claim compensation from the company.” | “recover”把提出损害赔偿请求改成任何请求的最终受偿结果，并省去了赔偿。原段随后分别核对担保对公司是否发生效力和是否承担赔偿责任，这里应保留被评审者实际说了什么。[最高法担保制度解释第7条](https://www.court.gov.cn/zixun/xiangqing/282721.html) |
| `references/mainland-china/markets.md:8` | “投诉线索” → “Grounds for a complaint” | “A lead reported in a complaint does not by itself establish entitlement to damages.” | 线索是待调查的信息，grounds 通常指提出投诉的理由或依据。示例意在区分监管线索与支持赔偿的事实。 |
| `references/mainland-china/index.md:37` | “授权” → “statutory authorization” | “the source and scope of the issuing authority’s power” | 原文要求查授权来源和范围。英文限定为 statutory，容易漏查有权机关作出的授权决定。《立法法》第12、13条明确规定授权决定及其内容。[全国人大常委会公报](https://wb.flk.npc.gov.cn/flfg/PDF/e4ab62be00d1476d97f65aaa5b56c336.pdf) |

### 建议澄清的专业术语

| 位置 | 中文 → 现译 | 建议英文 | 判断依据 |
|---|---|---|---|
| `references/mainland-china/criminal.md:7` | “单位犯罪” → “crimes committed by organizations” | “crimes committed by entities under Article 30 of the Criminal Law” | 这是法定犯罪主体类别，含公司、企业、事业单位、国家机关、团体，且法律须规定相应单位犯罪。普通词 organizations 难以提示这两层限定。最高检所载英译用 entity，较早最高法版本也用 unit。同句的“中止”译 voluntary abandonment 有最高检所载第24条用语支持，可保留。[最高检所载《刑法》第24、30条英译](https://en.spp.gov.cn/2020-12/26/c_948417.htm) |
| `references/mainland-china/social.md:8` | “解除、终止” → “Rescission, termination” | “Termination by agreement or on the initiative of a party, and termination by operation of law (including expiry)” | 未作解释的 rescission 容易带出溯及撤销、回复原状等含义。劳动合同法中的解除覆盖协商解除、辞职、解雇，终止另有期满等事由。两者同样可能涉及经济补偿。[《劳动合同法》第36至48条](https://www.samr.gov.cn/zw/zfxxgk/fdzdgknr/bgt/art/2023/art_0abfdd261c03417b949df19d869add8d.html) |
| `references/mainland-china/social.md:3` | “用工单位” → “labor-user entity” | “the entity receiving dispatched workers” | 用人单位和用工单位并列时，明确后者接收被派遣劳动者，可帮助读者识别分别承担劳动合同义务和用工义务的主体。最高法所载英译亦用 receiving unit。[《劳动合同法》第58至59条英译](https://english.court.gov.cn/2015-08/17/c_1170097_9.htm) |
| `references/mainland-china/companies.md:10` | “代表诉讼和个人损害赔偿” → “derivative actions, and compensation for personal loss” | “derivative actions and direct claims for damages suffered by the shareholder” | personal loss 在这里指股东自身利益受到的损害。补出受损主体，可与为公司利益提起的代表诉讼相对应。[《公司法》第189、190条](https://www.samr.gov.cn/xyjgs/flfg/art/2024/art_d4e84936a8a744f8928ac7aec7594345.html) |
| `references/mainland-china/markets.md:8`、`:9` | “虚假宣传” → “false publicity”。“合理使用等抗辩” → “defenses such as permitted reasonable use” | “false or misleading commercial promotion”。“defenses such as use permitted under statutory exceptions” | publicity 可能仅指媒体曝光，未说明经营者商业宣传的行为属性。合理使用涉及具体权利及法定例外，“reasonable”较易使人误以为泛泛的合理性足以成立抗辩。[《反不正当竞争法》第9条](https://www.cnipa.gov.cn/art/2026/5/20/art_104_206437.html) · [《著作权法》第24条英译](https://en.npc.gov.cn.cdurl.cn/2020-11/11/c_674691_2.htm) |
| `references/mainland-china/markets.md:10` | “处理者” → “the processor” | “the personal information processor under the PIPL (the party that determines the purposes and methods of processing)” | 官方英译本身采用 personal information processor。补齐全称并注明职能有助跨法域读者识别与受托处理者的区别。这是消歧建议。[《个人信息保护法》第73条英译](https://en.spp.gov.cn/2021-12/29/c_948419_3.htm) |

## 民法典分编审校

《民法典》法条以[最高人民法院公布的中文全文](https://www.court.gov.cn/zixun/xiangqing/233181.html)核验，英文术语可参看[中国政府网转载全国人大英文译本](https://english.www.gov.cn/archive/lawsregulations/202012/31/content_WS5fedad98c6d0f72576943005.html)。

### 影响法律含义或审查步骤的译文

| 现行位置 | 原文与现译 | 建议英文 | 法律影响 |
|---|---|---|---|
| `references/mainland-china/civil-code/family.md:10` | “赡养” → “support of elderly parents” | “duties to support parents and, where applicable, grandparents” | 加入“年老”门槛，还遗漏在法定情形下的祖父母和外祖父母。第1067条第2款规定父母请求赡养费的条件是缺乏劳动能力或生活困难，第1074条第2款另规定孙辈的义务。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |
| `references/mainland-china/civil-code/family.md:8` | “等事实与举证” → “and the evidence” | “identify the relevant facts, the evidence supporting them, and which party bears the burden of proof” | 现译只指证据材料。第1064条第2款中，超出家庭日常生活需要的个人名义债务，债权人须就法定例外举证。第12行的例子保留了这一点，表格也应保留。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |
| `references/mainland-china/civil-code/general.md:12` | “债权自动消灭”“债权状态” → “the debt is automatically extinguished” / “the status of the debt” | “the creditor’s claim is automatically extinguished” / “whether the creditor’s claim subsists and how the limitation defense affects its enforcement” | 引号内保留待批评的错误命题，只改主体和权利方向。“债权”在债权人一侧，英文落到了债务人所负之债。第192、193条区分义务人的时效抗辩和法院依职权适用的限制。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |
| `references/mainland-china/civil-code/property.md:12` | “买房未过户” → “The house purchase has not been registered” | “The transfer of title to the house has not been registered, so the contract is invalid.” | 示例刻意提出错误推论。“过户”指不动产所有权转移登记。现译容易理解为交易或购房合同未登记，掩盖第209、215条所区分的两个对象。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |
| `references/mainland-china/civil-code/contracts.md:3` | “变更与转让” → “modification and assignment” | “modification and transfer of contractual rights and obligations” | 单用 assignment 容易仅指债权让与。所概括的第六章还涵盖债务转移及经同意的一并转让，见第545、551、555、556条。文件第9行已分别列出相关概念。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |
| `references/mainland-china/civil-code/contracts.md:11` | “为谁管理、真实意思……受益人状态” → “whose affairs were managed, the person's actual wishes … the recipient's state of knowledge” | “whose affairs were managed and the beneficiary’s actual wishes … whether the recipient knew or should have known that the benefit lacked a legal basis, and whether the benefit still exists” | 前半句应明确第979条中意思的主体。后半句将开放性的“状态”限于知情，容易在第986条下漏查善意受领人所获利益是否已不存在，直接影响返还义务。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |

### 法律英语及检索精度

| 现行位置 | 原文与现译 | 建议英文 | 理由 |
|---|---|---|---|
| `references/mainland-china/civil-code/contracts.md:8` | “违约金与定金” → “agreed damages and earnest-money remedies” | “liquidated damages and remedies under an earnest-money clause” | agreed damages 可表达约定赔偿，但第585、588条对应制度在人大参考译本中用 liquidated damages。统一术语可帮助读者查到法院或仲裁机构调整违约金、以及两种条款择一适用的规则。[政府网站转载英译，第585–588条](https://english.taizhou.gov.cn/Government/LawsandRules/art/2023/art_4afa47a964b94a2c8bef075f8b9ade04.html) |
| `references/mainland-china/civil-code/contracts.md:15` | “（2019）最高法知民终433号” → “(2019) Zui Gao Fa Zhi Min Zhong No. 433” | “appellate case no. （2019）最高法知民终433号 (Supreme People’s Court, civil intellectual property appeal no. 433 of 2019)” | 年份、序号正确，纯拼音削弱通过官方案号精确检索的能力。入库编号与二审案号应分别保留。[案例库原文第1页](https://ipc.court.gov.cn/upload/file/2025/12/01/15/30/20251201153032_81336.pdf) |
| `references/mainland-china/civil-code/succession.md:9` | “必要份额” → “required reserved shares” | “the necessary portion to be reserved for an heir who cannot work and has no means of support” | reserved shares 容易让人联想到法定比例的特留份。第1141条按两个并存的资格条件保留必要的遗产份额，无固定比例。属于防误读释译。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |
| `references/mainland-china/civil-code/property.md:10` | “设立时点” → “date of creation” | “the time when the security right arose” | 同一日可能发生多次登记、交付，原文的“时点”比 calendar date 精细。第414、415条以登记或交付的先后确定顺位。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html) |

### 中英文共同的简写或歧义

这些表述在中文底稿中已有歧义，修改英文时宜同时澄清原意。

- `references/mainland-china/civil-code/succession.md:9` 将“见证资格与份数”照字面写成 “witnesses’ eligibility, the number of copies”。第1135–1138条按遗嘱形式规定人数，第1136条要求在每一页签名并注明年月日。法律没有在这里统一规定遗嘱副本份数。建议 “witness eligibility and the number of witnesses required for the relevant form”。如果“份数”意指内容相抵触的多份遗嘱，应另写 “whether there are multiple wills”，对应第1142条。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html)
- `references/mainland-china/civil-code/torts.md:7` 的“经营场所”照字面成了 “business premises”。作为下一句所问“身份及具体义务”的主体，第1198条规定的是经营者、管理者。建议 “operators or managers of business premises”。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html)
- `references/mainland-china/civil-code/temporal.md:8` 的“原判已经终审而申请再审”成为 “a retrial application after a final judgment”。第5条的时间条件是民法典施行前案件已经终审。建议 “For a retrial application in a case finally adjudicated before 1 January 2021, also check Article 5.” 同文件第11行“某期在2021年后履行”译为 “after 2021”，按通常英文指2022年起，中文也能如此理解。如果此例要示范第20条的施行日分界，可写 “one installment was performed after the Civil Code entered into force on 1 January 2021”。[最高法时间效力规定第5、20条](https://www.court.gov.cn/zixun/xiangqing/282051.html)
- `references/mainland-china/civil-code/family.md:7` 的“婚前重大疾病情形”译作 “serious premarital illness”。作为情形概述，两者均未交代第1053条下撤销取决于登记前未如实告知。建议 “failure to disclose a serious illness before registration of the marriage”。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html)
- `references/mainland-china/civil-code/torts.md:9` 的“可能加害人／各自责任”对应 “persons who may have caused the harm … their liability”。第1254条需区分侵权人赔偿、难以确定具体侵权人时可能加害的建筑物使用人依法给予补偿，以及管理人未尽安全保障义务的侵权责任。建议 “the identified tortfeasor, building users who may owe statutory compensation if the tortfeasor cannot be identified, and a manager who may be liable for failing to take safety measures”。[民法典](https://www.court.gov.cn/zixun/xiangqing/233181.html)

`references/mainland-china/civil-code/personality.md` 各行未发现需要单列的实质中英偏差。Rights in rem / real rights、nominate / typical contracts 等均有可理解的体系用法，不宜仅因与某一参考译本不同即判错。

## 澳大利亚

### 建议修订

| 位置 | 中文原文 | 现译 | 建议英文 | 理由 |
|---|---|---|---|---|
| `references/australia/maritime-trade.md:5`、`references/australia/maritime-trade.md:9` | “有关责任人”“责任主体” | “the relevant person liable” / “person liable” | “the ‘relevant person’ (the person who would be liable if the claim succeeded in an action in personam)”。第 9 行沿用 “the relevant person” | **优先修订。** 扣船的管辖判断中，现译把假设性责任读成已成立的责任。《Admiralty Act 1988》第 3(1) 条定义了 relevant person。高院明确区分此处的假设与须证明的所有权、时间等管辖事实。第 9 行底稿本来就用 sister ship，可补法定术语 “the requirements for proceeding against a surrogate ship under s 19”，作为术语校准。[Admiralty Act 1988，第 3、19 条](https://www.legislation.gov.au/C2004A03627/2021-09-01/2021-09-01/text/original/pdf) · [The Iran Amanat [1999] HCA 11，第 16–19 段](https://www.hcourt.gov.au/sites/default/files/eresources/2025-10-28/HCA/Iran%20Amanat%20v%20KMP%20Coastal%20Oil%20Pte%20Limited%20%28S22-1998%29%20%5B1999%5D%20HCA%2011.pdf) |
| `references/australia/business.md:8` | “成立公司或有限责任合伙” | “incorporating a company and forming a limited liability partnership” | “incorporating a company and forming a limited partnership under the applicable state or territory law” | **优先修订。** 中文称谓较宽。英文写成 limited liability partnership 容易让读者按另一法域的 LLP 检索及理解责任。澳洲官方区分 limited partnership 与 incorporated limited partnership，且一般合伙人与有限合伙人的责任有别。证实为后者时可明确加 incorporated。[澳大利亚政府合伙指引](https://business.gov.au/planning/business-structures-and-types/business-structures/partnership) · [新州 Partnership Act 1892，第 3 部](https://legislation.nsw.gov.au/view/whole/pdf/inforce/2024-10-19/act-1892-012) |
| `references/australia/business.md:7` | “公司签署与第三人” | “Execution by companies and third parties” | “Execution by companies and reliance by third parties” | by 同时支配 companies 和 third parties，把第三人写成签署人。本行所核对的第三人地位是交易相对方能否依赖法定假定。[Corporations Act 2001，第 126–129 条](https://www.legislation.gov.au/C2004A00818/2026-09-19/2026-09-19/text/original/epub/OEBPS/document_1/document_1.html) |
| `references/australia/search.md:33` | “查后续上诉及引用它的判决……辨明维持、推翻、限缩、区别适用或单纯提及” | “distinguish affirmation, overruling, limitation, distinguishing and mere mention” | “Check whether the decision was affirmed or reversed on appeal, and whether later courts overruled, limited, distinguished or merely mentioned it.” | 中文“推翻”在同案上诉和另案处理两种语境均适用。现译只留下 overruling，遗漏同案上诉的 reversal，会导致判例效力标签错列。[澳大利亚高校法律检索指南，判例引证部分](https://oercollective.caul.edu.au/legal-research-skills-an-australian-law-guide-2024-edition/open/download?type=pdf) |
| `references/australia/index.md:39` | “受理、上诉、选法” | “Commencing proceedings, appeals, choice of law” | “Which court or tribunal can hear the matter, appeals, choice of law” | commencing proceedings 描述一方启动诉讼，受理关注法院或审裁机构能否接案。若专指立案接收，可写 “acceptance of initiating documents for filing”。联邦法院指引将申请人提交、法院接收及管辖分开说明。[联邦法院启动案件指引](https://www.fedcourt.gov.au/going-to-court/i-am-a-party/court-processes/starting-a-matter) |
| `references/australia/contracts-consumers.md:9`、`references/australia/contracts-consumers.md:14` | 链接标签“ACL 法案与历史版本”“ACL 附表2，第3-2及5-4部分” | “ACL Act and historical versions” / “ACL Schedule 2, Parts 3-2 and 5-4” | “Competition and Consumer Act 2010, including historical versions” / “Competition and Consumer Act 2010 (Cth), sch 2 (Australian Consumer Law), pts 3-2 and 5-4” | 中文标签已有歧义。英文使 ACL 看似独立的 Act 且另有自己的附表 2。本文第 3 行的层级正确，两个标签应与之统一。[联邦立法登记册，Competition and Consumer Act 2010，附表 2](https://www.legislation.gov.au/C2004A00109/2025-02-21/2025-02-21/text/original/epub/OEBPS/document_4/document_4.html) |
| `references/australia/equity.md:9` | “若收款人主张已改变处境，应与原案事实和理由比对” | “If the recipient pleads change of position, compare the facts and reasons of the original case.” | “If the recipient relies on a change of position, compare the circumstances of the present claim with the facts and reasoning of the cited case.” | 现译少了类比的一端，字面要求在原案内部比对事实与理由。pleads 还较“主张”更易限于正式诉答阶段。[Hills Industries [2014] HCA 14](https://www.hcourt.gov.au/sites/default/files/eresources/2014/HCA/14.pdf) |
| `references/australia/migration.md:14` | “要看授权法及错误对结果的影响” | “depends on the enabling legislation and its effect on the outcome” | “depends on the terms of the enabling legislation and the effect of the error on the outcome” | its 的最近先行词是 legislation，造成影响结果的究竟是法律还是错误的实质歧义。中文已清楚指定后者。[Hossain [2018] HCA 34，第 29–31、35–37 段](https://www.hcourt.gov.au/sites/default/files/eresources/2018/HCA/34.pdf) · [LPDT [2024] HCA 12，第 14–16 段](https://www.hcourt.gov.au/sites/default/files/eresources/2024/HCA/12.pdf) |

### 中文底稿中需要澄清的表述

- `references/australia/proceedings.md:8`。中文并列“警方指控、控方案情、证据可采与法院认定的证明门槛”，英文的 *standard of proof* 只明确修饰法院认定。如要与下一行对应，可写 “Distinguish what the police allege, what the prosecution must prove, and the standard for establishing facts on which admissibility depends.” 第141、142条的适用以该法适用于相关程序为前提。[Evidence Act 1995，第141、142条](https://www.legislation.gov.au/C2004A04858/2025-06-10/2025-06-10/text/1/epub/OEBPS/document_1/document_1.html)

- `references/australia/government-rights.md:10`。“受保护行为”直译为 “protected conduct”，会使读者转向当事人受保护的特定行为，尤其是对投诉行为的保护，而本例仅泛指歧视投诉。与本页第 8 行衔接，可写 “the provisions governing the protected attribute and the alleged discriminatory conduct, any applicable exceptions, and the avenues for obtaining a determination”。如原作者本来特指受保护的投诉行为，需在例子里交代这一事实。[澳大利亚人权委员会对歧视投诉和裁判的说明](https://humanrights.gov.au/?a=68594)
- `references/australia/business.md:11`。“债务人”译 debtor 准确。PPSR 登记和检索可能还须区分提供担保财产的 grantor。若本段作为登记核验清单，可在两种语言中都补上，英文写 “the debtor and, if different, the grantor of the security interest”。[澳大利亚 PPSR 术语表，Debtor、Grantor 与 Authorised search purpose 条](https://www.ppsr.gov.au/glossary)
