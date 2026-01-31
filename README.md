# Smart-Recipe-System-Based-on-the-Flask-Framework
这是一个基于 Web 的营养健康助手应用，旨在帮助用户查询食物的营养成分、获取针对特定疾病（如糖尿病）的饮食建议，并计算膳食热量。

## ✨ 主要功能

- **食物营养查询**：输入食物名称，查询其详细的营养成分，包括热量、碳水化合物、脂肪、蛋白质等。
- **智能饮食建议**：集成 OpenAI 和讯飞星火大模型，为特定疾病（如糖尿病）患者提供个性化的饮食建议。
- **热量计算器**：选择多种食物和相应的份量（克），自动计算总热量。
- **可视化界面**：简洁明了的 Web 界面，方便用户操作。

## 🛠️ 技术栈

- **后端**: Flask
- **数据库**: MySQL
- **AI 服务**: OpenAI, 讯飞星火 (Spark AI)
- **数据处理**: Pandas
- **前端**: HTML, CSS, JavaScript

## 🚀 快速开始
请按照以下步骤在本地运行该项目。

### 克隆仓库

```bash
git clone <your-repository-url>
cd nutrition_app

###虚拟环境
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt

###配置数据库
def get_db_connection():
    connection = mysql.connector.connect(
        host='localhost',
        user='root',  # 替换为你的MySQL用户名
        password='root',  # 替换为你的MySQL密码
        database='ruangong_fooddb',  # 替换为你的数据库名
        charset='utf8mb4'
    )
    return connection

###配置密钥.env文件配置 API 密钥
OPENAI_API_KEY="你的OpenAI_API_Key"
SPARK_APP_ID="你的讯飞APPID"
SPARK_API_SECRET="你的讯飞APISecret"
SPARK_API_KEY="你的讯飞APIKey"

###app.py中加载并运行
