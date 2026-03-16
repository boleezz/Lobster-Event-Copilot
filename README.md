
# 🦞币安活动规则编译器与参与转化引擎

币安生态首个大模型驱动的「活动规则编译器与决策引擎」。将冗长复杂的活动规则，瞬间转化为千人千面的、可执行的参与策略与任务清单。

## 🧩 极简复现路径 (Dual-Track Reproducibility)

为了让基础设施真正触达每一个用户，Lobster 提供了**开发者代码流**与**普通用户零代码流**双轨复现路径：

### 路径 A：零代码开箱即用 (Prompt-as-Code 模式)
无需配置任何代码环境。任何用户只需获取本仓库中的核心认知引擎指令，即可瞬间在任意大模型（ChatGPT/Claude/Gemini）中拉起你的专属活动副驾。
1. 打开本仓库中的 `system_prompt.md` 文件。
2. 将全文复制并粘贴到你常用的 AI 对话框（或作为 System Prompt / Custom Instruction 填入）。
3. 直接向 AI 发送币安活动链接或长图，Agent 将自动进入标准解析工作流。

### 路径 B：开发者本地容器部署 (API 模式)
面向需要批量处理或接入自动化工作流的开发者：
```bash
git clone [https://github.com/boleezz/Lobster-Event-Copilot](https://github.com/boleezz/Lobster-Event-Copilot)
cd Lobster-Event-Copilot
pip install -r requirements.txt
# 在 .env 中填入大模型 API Key 后运行
python agent_core.py --url "输入币安活动的真实链接"
