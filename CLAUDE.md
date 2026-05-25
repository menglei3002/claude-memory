# 全局指令

## 知识库
执行任务前，先检查 `D:\AI\my-knowledge\workflows\` 中的工作流文档。
如果找到匹配的工作流，直接复用，无需让用户重新说明。
任务完成后，主动询问是否需要将新发现的流程沉淀到知识库。

知识库位置：`D:\AI\my-knowledge\`
Git 仓库：git@github.com:menglei3002/my-knowledge.git

## 持久化
每次完成有意义的产出（代码、文档、工作流、配置变更）后，主动提醒用户是否需要提交到 git。
项目记忆位置：`C:\Users\Administrator\.claude\projects\C--Users-Administrator\memory\`
记忆 Git 仓库：git@github.com:menglei3002/claude-memory.git

## 技术演进
当加载记忆或工作流时，如果发现与已验证的新方案矛盾，主动标记过时内容并更新。
新方案优先于旧记忆，旧记忆必须被修正而非并存。
