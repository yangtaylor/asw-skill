---
description: 使用架构解决方案编写助手，通过交互式问答生成符合TOC-AAM-T001模板格式的完整架构解决方案文档
argument-hint: [项目名称]
tools: Read,Write,AskUserQuestion
---

# 架构解决方案编写

项目名称：$ARGUMENTS

请使用 architecture-solution-writer 技能，为"$ARGUMENTS"项目编写架构解决方案文档。

## 执行步骤

1. 加载 architecture-solution-writer 技能
2. 读取技能中的参考文件（references/）了解模板结构
3. 按照技能工作流程执行：
   - 收集并读取用户提供的材料文件
   - 分阶段向用户提问收集项目信息
   - 判断各章节适用性
   - 使用 docx-js 生成完整的 .docx 文档
   - 执行自动化完整性检查
4. 输出最终文档到工作区
