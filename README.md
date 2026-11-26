# Legal Q&A and Citation Review

`legal-analysis` is an English-language Agent Skill primarily for reviewing legal questions and answers concerning mainland China, Australia and New Zealand. It can also answer legal questions directly. Providing a question and answer selects review mode, with citations optional; providing only a question, with or without reference materials, selects direct-answer mode. For multiple questions, the mode is selected individually.

A review separately explains whether each claim is sound, what the original citations support, and how far source verification has progressed. If the original answer is seriously deficient, the review is retained and a fully rewritten answer is supplied. Direct answers and reviews share the same rules for jurisdiction, relevant dates, research and verification of authorities.

## Installation

Run this command in the project directory where you intend to review questions and answers:

```sh
npx skills add HaaaappyDay/legal-analysis --skill legal-analysis
```

Follow the installation prompts to select your agent. Installation is local to the current project by default; append `-g` to make the skill available across projects. [skills CLI installation instructions](https://github.com/vercel-labs/skills#install-a-skill)

Online verification of legal sources requires an agent with web search or webpage-reading capabilities; generating files requires write access to the working directory. If the task has no internet access at all, the agent first explains that it cannot obtain or verify external information and that the result may contain significant errors or omissions, then asks whether to continue. Analysis limited to the available materials begins only after the user gives explicit informed consent, and the limitations are prominently repeated on delivery. Independent review requires an environment that supports a fresh context without inherited history and file handoffs; otherwise, the agent states that review was conducted only within the same context.

## Try a question

```text
Use the legal-analysis skill to review the following question and answer, and save the report as legal-qa-review.md.

Jurisdiction and relevant time: mainland China, 2023.
Question: I have signed a contract to buy a home, but the transfer of title has not yet been registered. Is the contract valid?
Original answer: The sale contract is invalid because the transfer of title has not yet been registered.
Original citation: [1] Article 209 of the Civil Code of the People's Republic of China.
```

When reading the report, check this specific distinction: Article 209 sets out the registration principle for changes in rights in rem over immovable property, whereas the original answer uses it to infer that the sale contract is invalid. Article 215 directly addresses contractual validity and should be identified under supplementary authorities. The report should explain that failure to register the transfer alone does not establish that the contract is invalid, while retaining qualifications such as contrary provisions of law or agreements between the parties. [Civil Code, Articles 209 and 215](https://www.court.gov.cn/zixun/xiangqing/233181.html)

For a direct answer, supply only the question, jurisdiction and relevant time above, without the original answer. You may also provide reference materials. [Direct-answer template](references/answer-template.md)

By default, direct answers are saved as `legal-answer.md` in the current working directory, and reports containing review questions as `legal-qa-review.md`. If the filename already exists and no update has been requested, an incrementing suffix is added. Multiple questions retain their numbering; mixed tasks use the appropriate structure for each question and are combined into one file. Where a source has been located but only a summary read, it is marked "original text not verified". An explicit request for inline text only is honoured. [Review report template](references/report-template.md)

The "Review and verification record" at the end of the document lists the completion date, each source's version and pinpoint reference, actual verification date and scope, subsequent-development searches, and significant outstanding matters. Event dates and verification dates are recorded separately. Sources shared across questions may be combined, and areas not searched or verified remain explicitly identified.

## Independent review and file handoffs

The current agent ordinarily reviews the user's original answer. Newly generated or fully rewritten answers are reviewed in a separate context that does not inherit the generation history. For complex matters involving multiple jurisdictions, transitions between historical versions or substantive conflicts, the reviewer first researches the question independently and then reads the answer and citations for comparison. Typographical or citation-format changes receive a targeted check.

When a handoff is needed, a separate task directory is created under `.legal-analysis/`, with UTF-8 files containing the original question, original answer, citations, draft versions and review findings. Dispatch messages convey file paths, stages and permitted read/write scope; substantive text is not embedded in tool calls or command lines. Files are completed before handoff, original inputs remain unchanged, and drafts are frozen during review. A shared filesystem does not provide access-control isolation. See the [review and file handoff guide](references/review-workflow.md) for reading boundaries, the two-stage sequence and fallback procedures.

## Jurisdictions and legal sources

| Jurisdiction | Coverage | Research |
|---|---|---|
| Mainland China | [The Civil Code's seven Books and supplementary provisions, company and commercial law, employment, administrative law, criminal law, procedure and other subjects](references/mainland-china/index.md) | [Find legislation, judicial interpretations, cases and historical versions](references/mainland-china/search.md) |
| Australia | [Federal, state and territory legal subjects and applicable context](references/australia/index.md) | [Find legislation, judgment paragraphs, historical versions and subsequent cases](references/australia/search.md) |
| New Zealand | [National and local law, Māori land and Treaty issues, specialist courts and tribunals](references/new-zealand/index.md) | [Find dated legislation, judgments and later judicial treatment](references/new-zealand/search.md) |

During review, check the applicable version against the date of the events in question. When maintaining subject guides, include official sources and specific provisions or judgment paragraphs, and explain which facts would change the application of a case. Shared review standards are in [SKILL.md](SKILL.md).
