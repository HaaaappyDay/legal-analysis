# 澳大利亚立法与判决检索

## 有正文链接，先用 fetch 直读

将用户提供的官方正文 URL 直接传给 fetch，核对法域、版本或判决身份，再定位相关条款或段落。以下为 2026-11-24 在当前 Agent 环境中成功直读的两个样本。

| 官方材料 | 实际读到的位置与核验边界 |
|---|---|
| [《Competition and Consumer Act 2010》(Cth) 附表2，联邦登记册 HTML](https://www.legislation.gov.au/C2004A00109/2025-02-21/2025-02-21/text/original/epub/OEBPS/document_4/document_4.html) | 2025年2月21日版 s 260(1)，能核对货物不符合保证时构成 major failure 的条件。仅用于该历史版本；评价退款权还需读相应救济条款。 |
| [ACCC v TPG Internet Pty Ltd [2013] HCA 54，高等法院判决 PDF](https://www.hcourt.gov.au/sites/default/files/eresources/2013/HCA/54.pdf) | 第45段，可读到多数意见对广告主要信息的分析；结合同一意见第46–53段评价原回答。需要评价判例后续效力时另查后案。 |

## 缺少链接或直读失败，用 search 定位

查联邦法可搜 `site:legislation.gov.au "Competition and Consumer Act 2010" "259" "260" 2025-02-21`。若只读到目录或 latest/details 页，继续找日期版正文和对应卷册。查判决可搜 `site:hcourt.gov.au "TPG" "[2013] HCA 54"`，按案名与 `judgment PDF` 定位裁判理由；只有 catchwords、摘要或当事人提交书时标明材料类型。

**NSW 历史法例：从搜索结果打开索引副本。** 直接读取抽查的新州租赁法现行 HTML 和历史 PDF 时，工具返回 403。改搜 `site:legislation.nsw.gov.au "Residential Tenancies Act 2010" "urgent repairs" April 2025`，从工具返回的搜索结果打开官方 PDF 的索引副本，在文内找 `Landlord’s general obligation`、`Urgent repairs to residential premises` 和页脚的版本区间。实测从结果打开可读到第48–50页的 ss 62–64，页脚标明适用期为2024年12月13日至2025年5月18日；把同一 URL 直接交给 fetch 仍返回 403。仅在工具实际提供连续正文和版本信息时使用这条路径。只有摘要时，记“已定位，原文未核”；州政府办事说明可单独列为说明性材料。[已定位的官方历史 PDF](https://legislation.nsw.gov.au/view/whole/pdf/inforce/2025-04-25/act-2010-042)

**后案。** LawCite 查询入口在本工具中返回 403。Agent 默认搜“中立引注＋后案案名或争点”，再打开法院判决理由，核对法院怎样处理原案。首项可能是当事人提交书，要看文书首部。仅就实际读到的后案报告核验结果。

## 找规定及适用版本

1. **拆解引文。** 例如 `Competition and Consumer Act 2010 (Cth) sch 2 s 259(3)` 中，Cth 是联邦，sch 2 是附表2，最后才是条款。联邦立法在 Federal Register of Legislation 按正式名称查，以事实日期选 point in time / compilation；打开相应卷册、附表和 subsection，检查 commencement、application 和 transitional provisions。对 NSW、Vic 等标识，改从当地法规库找历史版本；统一立法还要查当地采纳和变更。[联邦登记册检索帮助](https://www.legislation.gov.au/help-and-resources/using-the-legislation-register/how-to-use-browse-search-and-advanced-search) · [各州及领地法规入口](https://www.opc.gov.au/links/legislation-states-territories-and-new-zealand)
2. **只有中文问题时换成当地术语。** 例如“瑕疵商品是否一定能退款”可查 `Australian Consumer Law goods "major failure" supplier refund`。从结果回到附表2，分别核对保证内容（如 s 54）、向供应商主张救济（s 259）、重大故障（s 260）及拒收限制与后果（ss 262–263）。报告保留英文法名、法域、版本和具体条款。下列历史文本用于演示版本定位。[2025年2月21日版，附表2](https://www.legislation.gov.au/C2004A00109/2025-02-21/2025-02-21/text/original/epub/OEBPS/document_4/document_4.html)

## 找判决和后续处理

| 手头线索 | 检索路径 |
|---|---|
| 有中立引注 | 如 `[2013] HCA 54`，优先按完整引注或案名在 High Court Judgments 查；FCA、FCAFC 查 Federal Court Judgments；如 NSWCA 则查 NSW Caselaw。按案件页进入 reasons for judgment，核对法院、日期、意见作者、段落与最终 orders。案件进度页和律师提交的 submissions 可帮助找到案件，不能单独证明法院接受了该论点。[High Court Judgments](https://www.hcourt.gov.au/cases-and-judgments/judgments) · [Federal Court Judgments](https://www.fedcourt.gov.au/digital-law-library/judgments) · [NSW Caselaw](https://www.caselaw.nsw.gov.au/) |
| 只有案名、授权判例集卷页或争点 | 以一方或双方当事人名、年份、法院或卷页检索。按争点找案例时用当地法律术语、条款号和决定性事实筛选，例如 `"dominant message" broadband misleading advertising`。较早判例可能只有判例集卷页，保留其页码定位。跨库可用 AustLII 发现候选，再与法院文本或授权报告核对。[联邦法院引注说明](https://www.fedcourt.gov.au/law-and-practice/practice-documents/practice-notes/gpn-auth) · [AustLII](https://www.austlii.edu.au/) |
| 需要知道判决还能支持什么 | 用中立引注、报告引注和案名查后续上诉及引用它的判决；具备可用的交互式引证数据库时还可查 citing cases。打开后案，辨明维持、推翻、限缩、区别适用或单纯提及；再查涉案法条是否修订。案件记录可确认程序进展，后续法律处理应定位到裁判理由。对尚未核到的后续状态保留说明。[联邦法院检索 FAQ](https://www.fedcourt.gov.au/digital-law-library/judgments/judgments-faq) · [悉尼大学法律资料检索说明](https://www.library.sydney.edu.au/support/searching/understanding-legal-sources) |

**试查示例。** 搜索 `"[2013] HCA 54" TPG`，进入 *ACCC v TPG Internet Pty Ltd* 的判决全文。第45–53段是多数意见对广告整体印象及其呈现方式的分析。若原引只是案件页列出的 catchwords，应以这些段落核验回答；该案也不能单凭关键词支持消费者退货退款的结论。[高等法院案件页](https://www.hcourt.gov.au/cases-and-judgments/judgments/judgments-1998-current/australian-competition-and-consumer-commission-v-tpg-internet-pty-ltd) · [判决全文](https://www.hcourt.gov.au/sites/default/files/eresources/2013/HCA/54.pdf)

法院站检索无命中时，换法院、案名拼写、旧报告引注或跨库查找。记录哪些资料确实读到了；只有 headnote、摘要或当事人材料时，明确相应局限。数据库未显示新的引用，不足以证明判决此后一直获遵循。
