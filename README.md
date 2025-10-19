基于 Spring Boot 3 + Spring AI + RAG + Tool Calling + MCP 的AI考研/考公辅导智能体，为用户提供学习指导服务。具备多轮对话、记忆持久化、RAG 知识库检索等能力，通过 ReAct 模式能够自主思考并调用工具来完成复杂任务，比如利用网页搜索、资源下载和 PDF 生成工具，实现从知识问答到工具协同。
1.对话记忆持久化：自主实现了基于文件系统的 ChatMemory，结合 Kryo 高性能序列化库保存对话历史数据，解决了服务重启后对话记忆丢失的问题，增强了系统稳定性。
2.结构化输出：基于 Spring AI 的结构化输出特性实现了恋爱报告生成功能，将 AI 的回复精准转换为结构化 Java 对象，便于后续的数据处理和展示。
3.RAG向量存储：自定义VectorStore实现，结合EmbeddingModel将文本转换为语义向量并存储到PGvector向量数据库，支持语义相似度搜索和多维度过滤，提高了检索精准度。
4.AI工具调用：利用Spring AI的工具调用注解实现了多种工具调用功能，包括文件操作、联网搜索、网页抓取、终端操作、资源下载和PDF生成，扩展了AI的能力边界。
整体架构：
<img width="1038" height="1239" alt="image" src="https://github.com/user-attachments/assets/8838a966-8bcd-439f-aef2-b465a9ce6fe6" />
