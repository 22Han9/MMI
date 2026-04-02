# MMI
A multimodal and multi model AI dialog system supports multi-user and multi round sessions and historical memory persistence.
基于 C++/Linux 平台实现 AI 对话系统，集成多模态多模型接口，支持多用户多轮会话及历史记忆持久化。
1. 高并发 AI 推理服务：依托 Muduo 网络库与线程池实现高并发请求处理，使用 RabbitMQ 消息队列异步执行模型推理与数据库写入，显著提升系统吞吐量和响应性能。
2. 多模型、多模态集成：采用策略+工厂模式设计提高解耦性和扩展性，实现多模型动态切换（百炼、豆包、RAG 等）。基于 ONNXRuntime + OpenCV 部署轻量级图像识别模型，集成百度语音合成 API 实现文本转语音输出（TTS），为系统提供了完整的文本、语音、图像交互能力。
3. 轻量级 MCP 服务设计：封装自定义工具调用机制，实现服务端工具注册、提示词构建与调用流程。
4. 服务化与部署：利用 Docker 构建统一运行环境，整合 MySQL、RabbitMQ 等组件，实现项目一键部署。
