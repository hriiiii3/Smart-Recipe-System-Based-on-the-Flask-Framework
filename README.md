下面这一大段内容，你直接全选、复制，粘贴到你的 README.md 文件中即可，格式会自动渲染正确：
plaintext
# Smart-Recipe-System-Based-on-the-Flask-Framework
这是一个基于 Web 的营养健康助手应用，旨在帮助用户查询食物的营养成分、获取针对特定疾病（如糖尿病）的饮食建议，并计算膳食热量。

## ✨ 主要功能
- 食物营养查询：输入食物名称，查询其详细的营养成分，包括热量、碳水化合物、脂肪、蛋白质等。
- 智能饮食建议：集成 OpenAI 和讯飞星火大模型，为特定疾病（如糖尿病）患者提供个性化的饮食建议。
- 热量计算器：选择多种食物和相应的份量（克），自动计算总热量。
- 可视化界面：简洁明了的 Web 界面，方便用户操作。

## 🛠️ 技术栈
- 后端: Flask
- 数据库: MySQL
- AI 服务: OpenAI, 讯飞星火 (Spark AI)
- 数据处理: Pandas
- 前端: HTML, CSS, JavaScript

## 🚀 快速开始

### 环境要求
- Python ≥ 3.8
- MySQL ≥ 8.0
- 网络通畅（用于调用OpenAI和讯飞星火API）

### 1. 克隆仓库
```bash
git clone [你的仓库完整地址，比如https://github.com/你的用户名/你的仓库名.git]
cd nutrition_app
````
### 2.创建虚拟环境
```bash
# 创建虚拟环境
python -m venv venv
````
### 3.激活虚拟环境
```bash
# Windows 系统
.\venv\Scripts\activate
````

### 4.安装项目依赖
```bash
pip install -r requirements.txt
````
### 5. 配置数据库
#打开 MySQL，在命令行或 Navicat 中执行下面的语句创建数据库：
```bash
sql
CREATE DATABASE ruangong_fooddb CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
````
```bash
import mysql.connector

def get_db_connection():
    connection = mysql.connector.connect(
        host='localhost',
        user='[你的MySQL用户名，一般默认是root]',
        password='[你的MySQL密码，比如123456]',
        database='ruangong_fooddb',
        charset='utf8mb4'
    )
    return connection
````
### 6. 配置 API 密钥（.env 文件）
#在你的项目文件夹根目录，新建一个文件，文件名直接叫「.env」（前面有个点，没有后缀）
#打开这个.env 文件，粘贴下面的内容，修改 [] 里的密钥：
```bash
OPENAI_API_KEY="[你的OpenAI API密钥]"
SPARK_APP_ID="[你的讯飞星火APPID]"
SPARK_API_SECRET="[你的讯飞星火APISecret]"
SPARK_API_KEY="[你的讯飞星火APIKey]"
````
### 7. 启动项目
#在项目文件夹的命令行里，输入下面的命令，按回车：
```bash
运行
python app.py
````
### 8. 访问项目
#打开你的浏览器（比如 Chrome），在地址栏输入本地地址
