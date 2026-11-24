# 法律问答与引用评审

`legal-analysis` 是一套中文 Agent Skill，用于评审中国大陆和澳大利亚法律问答。输入一道或多道题、对应回答和原引用，得到一份逐题评审的 Markdown 报告。报告分别说明回答是否成立、原引用实际支持什么，以及新找到的法条或判决如何补充或改变结论。

## 在 Codex 中安装

在准备评审问答的项目目录运行：

```sh
npx skills add HaaaappyDay/legal-analysis --skill legal-analysis --agent codex
```

默认安装到当前项目。要在多个项目中使用，可在命令末尾加 `-g`。安装后，在 Codex 中用 `$legal-analysis` 调用。[skills CLI 安装说明](https://github.com/vercel-labs/skills#install-a-skill)

在线核验法源需要 Agent 具备网页搜索或读取能力，生成报告需要工作目录的写入权限。

## 试一道题

```text
请用 $legal-analysis 评审下面的问答，将报告保存为 legal-qa-review.md。

法域和时间：中国大陆，2023 年。
问题：我签了房屋买卖合同，还没办过户，合同有效吗？
原回答：房屋还没过户，买卖合同无效。
原引用：[1]《中华人民共和国民法典》第209条。
```

读报告时可以核对一个具体区别：第209条讲不动产物权变动的登记原则，原回答用它推断买卖合同无效。第215条直接涉及合同效力，应标为评审补充。报告应说明单凭未过户无法推出合同无效，并保留法律另有规定或当事人另有约定等条件。[《民法典》第209、215条](https://www.court.gov.cn/zixun/xiangqing/233181.html)

默认报告写入当前工作目录的 `legal-qa-review.md`。多道题可以放在同一次输入中，保留题号和原引用编号。已定位材料但只读到摘要时，报告会标明“原文未核”。[报告模板](references/report-template.md)

## 法域与法源

| 法域 | 内容 | 检索 |
|---|---|---|
| 中国大陆 | [《民法典》七编及附则、公司商事、劳动、行政、刑事与程序等](references/mainland-china/index.md) | [查法条、司法解释、案例及历史版本](references/mainland-china/search.md) |
| 澳大利亚 | [联邦、州和领地的法律领域与适用背景](references/australia/index.md) | [查成文法、判决段落、历史版本及后案](references/australia/search.md) |

评审时按问题发生日期核对适用版本。维护领域指南时，附上官方来源、具体条款或裁判段落，并说明哪些事实会改变案例的适用结论。共用的评审标准见 [SKILL.md](SKILL.md)。
