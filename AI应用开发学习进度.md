# AI 应用开发学习进度

> 学习方向：Java 后端开发工程师 → AI 应用开发工程师  
> 最近更新：2026-08-19  
> 维护方式：每次课后更新勾选、课程记录、练习结果和下一课。

## 总体路线

`LLM 基础 → LLM API 开发 → Embedding/向量数据库 → RAG 深入 → Tool Calling → AI Agent → 工程化与生产实践`

## 阶段列表

### 1. LLM 基础
- [x] LLM、ChatGPT / API 基本工作方式
- [x] Context、Chat History
- [x] 每次请求将之前聊天内容重新传给模型
- [ ] Token
- [ ] Temperature / Top-P
- [ ] System / User / Assistant 消息角色
- [ ] Context Window、多轮对话机制

### 2. LLM API 开发
- [ ] API Key 与安全管理、Chat API、流式输出
- [ ] Structured Output、JSON Schema
- [ ] Function / Tool Calling、多模型调用
- [ ] 错误处理、超时、重试、Token / 成本统计

**项目 1：AI Chat** — 用 Spring Boot 实现可多轮对话的 AI 后端。

### 3. Embedding 与向量数据库
- [x] RAG 基本机制
- [ ] Embedding、向量、余弦相似度
- [ ] Chunk（文档切分）、Vector Database
- [ ] Milvus / pgvector / Elasticsearch
- [ ] 文档 → Chunk → Embedding → Vector DB
- [ ] Query → Embedding → Similarity Search

**项目 2：企业 AI 知识库** — 文档解析、切分、向量检索与 LLM 问答。

### 4. RAG 深入
- [ ] Naive RAG、Hybrid Search、Metadata Filter、Rerank
- [ ] Query Rewrite、Multi Query、Context Compression
- [ ] 命中率、幻觉、RAG Evaluation

### 5. Tool Calling
- [ ] Tool Schema、工具选择与执行、工具结果回传、多工具调用、错误处理

### 6. AI Agent
- [ ] Agent 循环与规划、Memory、ReAct / Plan-and-Execute、多 Agent、可靠性与安全

### 7. 工程化与生产实践
- [ ] Prompt 管理、评测与回归测试、Tracing、数据安全、成本控制、部署与性能优化

## 当前进度

**当前阶段：LLM 基础**  
**下一课：Token**

已理解：模型请求本身无状态，应用需在每次请求中携带必要的历史消息。  
已理解：RAG 从外部知识检索相关内容，再作为上下文交给 LLM 回答。

## 已掌握知识

| 知识点 | 掌握情况 | 备注 |
| --- | --- | --- |
| 聊天历史重新传递 | 已理解 | 历史由应用组装并随请求携带。 |
| RAG 基本机制 | 已理解 | 检索相关资料，再交给模型辅助回答。 |

## 待学习知识

1. **Token**：Token 切分、输入/输出 Token、费用与上下文窗口。
2. **生成参数与角色消息**：Temperature、Top-P、System/User/Assistant。
3. **RAG 前置能力**：Embedding、Chunk、余弦相似度、向量数据库。

## 每课学习记录

| 日期 | 课次 | 学习主题 | 要点/结论 | 状态 |
| --- | --- | --- | --- | --- |
| 2026-08-19 | 0 | 多轮聊天上下文 | 每次请求由应用携带必要的历史消息。 | 已完成 |
| 2026-08-19 | 0 | RAG 基本机制 | 检索外部知识后，将相关内容提供给模型回答。 | 已完成 |
| 待开始 | 1 | Token | Token、计费、上下文窗口及 Java 开发中的影响。 | 下一课 |

## 练习 / 测验结果

| 日期 | 主题 | 形式 | 结果 | 待巩固点 |
| --- | --- | --- | --- | --- |
| 暂无 | — | — | — | 每次练习后追加。 |

## 项目进度

| 项目 | 当前状态 | 下一步 |
| --- | --- | --- |
| AI Chat（Spring Boot） | 未开始 | 学完阶段 1 的关键概念后，完成最小对话 API。 |
| 企业 AI 知识库 | 未开始 | 学完 Embedding、Chunk 和向量检索后启动。 |

## 下一课建议：Token（20–30 分钟）

1. Token 不是“字数”，而是模型处理文本的基本片段。
2. 输入/输出 Token 与 API 成本的关系。
3. Token 如何限制聊天历史和 RAG 检索内容。
4. Java 后端中何时截断或摘要历史、控制检索片段数量。

完成标志：能解释很长的聊天历史为何影响请求成本、速度和可用上下文。

## 追加模板

```md
| YYYY-MM-DD | N | 主题 | 关键结论 / 易错点 | 已完成 / 待复习 |
| YYYY-MM-DD | 主题 | 练习或测验形式 | 得分 / 结论 | 下一步复习点 |
```
