# 魔塔AI智能助手 - 快速启动指南

## 🚀 快速运行

本项目已配置好魔塔社区的GLM-4.5模型，可以直接运行！

### 前置要求

1. **安装依赖**：
   ```bash
   uv sync --frozen
   ```

2. **激活环境**：
   ```bash
   # Windows
   .venv\Scripts\activate
   
   # Linux/Mac
   source .venv/bin/activate
   ```

### 🎯 直接运行方式

#### 方式一：完整服务（推荐）

1. **启动后端服务**：
   ```bash
   python src/run_service.py
   ```
   - 服务地址：http://localhost:8080
   - API文档：http://localhost:8080/docs

2. **启动前端界面**（新终端）：
   ```bash
   streamlit run src/streamlit_app.py
   ```
   - 界面地址：http://localhost:8501

#### 方式二：命令行客户端

```bash
python src/run_client.py
```
- 直接在命令行与AI对话
- 需要先启动后端服务

#### 方式三：LangGraph代理

```bash
python src/run_agent.py
```
- 直接运行LangGraph代理
- 无需启动后端服务

### 📋 配置说明

项目已预配置魔塔社区模型：
- **模型**：ZhipuAI/GLM-4.5
- **API地址**：https://api-inference.modelscope.cn/v1
- **配置文件**：`.env`（已包含在版本控制中）

### 🛠️ 可用的智能助手

1. **研究助手** (research-assistant) - 默认
   - 网络搜索功能
   - 数学计算能力

2. **聊天机器人** (chatbot)
   - 基础对话功能

3. **RAG助手** (rag-assistant)
   - 文档检索问答

4. **命令代理** (command-agent)
   - 系统命令执行

5. **后台任务代理** (bg-task-agent)
   - 后台任务处理

6. **交互式代理** (interrupt-agent)
   - 支持中断的对话

### 🔧 故障排除

1. **端口占用**：
   - 确保8080和8501端口未被占用
   - 或修改`.env`文件中的`PORT`配置

2. **依赖问题**：
   ```bash
   uv sync --frozen --reinstall
   ```

3. **模型连接问题**：
   - 检查网络连接
   - 确认魔塔社区API服务状态

### 📁 项目结构

```
src/
├── run_service.py      # FastAPI后端服务
├── run_client.py       # 命令行客户端
├── run_agent.py        # LangGraph代理
├── streamlit_app.py    # Streamlit前端界面
├── agents/             # 各种智能助手
├── client/             # 客户端库
└── core/               # 核心配置
```

### 🌟 特色功能

- ✅ 完全中文化界面
- ✅ 魔塔社区GLM-4.5模型
- ✅ 流式对话输出
- ✅ 多种智能助手模式
- ✅ 对话历史管理
- ✅ 分享和恢复功能
- ✅ 开箱即用配置

---

**快速体验**：直接运行 `python src/run_service.py` 和 `streamlit run src/streamlit_app.py` 即可开始使用！
