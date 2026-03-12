# 🫀 Pediatric Cardiac Surgery Assistant
## 婴幼儿心外科智能辅助系统

[![Netlify Status](https://api.netlify.com/api/v1/badges/your-badge-id/deploy-status)](https://app.netlify.com/sites/your-site-name/deploys)

一个专为临床婴幼儿心外科医生设计的智能辅助系统，提供AI咨询、医学术语翻译和患者随访管理功能。

## ✨ 功能特性

### 1. 🤖 AI智能助手
- **语音输入**: 支持语音提问，自动转换为文字
- **语音播放**: AI回复支持TTS语音播放
- **专业咨询**: 基于DeepSeek大语言模型，提供专业医学建议
- **上下文对话**: 保持对话历史，提供连贯的交流体验

### 2. 📚 医学辞典
- **三语翻译**: 支持中文、英文、德文互译
- **专业术语**: 专注于小儿心脏外科医学术语
- **详细释义**: 提供术语的医学含义和临床应用

### 3. ⏰ 随访提醒
- **患者管理**: 记录患者信息和手术类型
- **日期提醒**: 自动标记过期和即将到期的随访
- **本地存储**: 数据保存在浏览器本地，保护隐私
- **桌面通知**: 支持浏览器通知提醒

### 4. 🔗 参考资源
- 集成全球顶尖儿童心脏中心链接
- 包括德国、美国和中国的主要医疗机构

## 🚀 部署指南

### 前置要求
- [Netlify](https://www.netlify.com/) 账号
- [DeepSeek API](https://platform.deepseek.com/) 密钥

### 方法一：通过Netlify UI部署（推荐）

1. **Fork或下载此仓库**

2. **在Netlify创建新站点**
   - 登录 [Netlify](https://app.netlify.com/)
   - 点击 "Add new site" → "Import an existing project"
   - 连接你的Git仓库（GitHub/GitLab/Bitbucket）

3. **配置构建设置**
   - Build command: (留空)
   - Publish directory: `.`
   - Functions directory: `netlify/functions`

4. **设置环境变量**
   - 进入 Site settings → Environment variables
   - 添加新变量:
     - Key: `DEEPSEEK_API_KEY`
     - Value: 你的DeepSeek API密钥

5. **部署**
   - 点击 "Deploy site"
   - 等待部署完成

### 方法二：通过Netlify CLI部署

1. **安装Netlify CLI**
   ```bash
   npm install -g netlify-cli
   ```

2. **登录Netlify**
   ```bash
   netlify login
   ```

3. **初始化项目**
   ```bash
   cd pediatric-cardiac-surgery-assistant
   netlify init
   ```

4. **设置环境变量**
   ```bash
   netlify env:set DEEPSEEK_API_KEY "your-deepseek-api-key"
   ```

5. **部署**
   ```bash
   netlify deploy --prod
   ```

### 方法三：一键部署

点击下方按钮直接部署到Netlify：

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/yourusername/pediatric-cardiac-surgery-assistant)

部署后记得在Netlify设置中添加 `DEEPSEEK_API_KEY` 环境变量！

## 🔑 获取DeepSeek API密钥

1. 访问 [DeepSeek Platform](https://platform.deepseek.com/)
2. 注册或登录账号
3. 进入 API Keys 页面
4. 创建新的API密钥
5. 复制密钥并保存（只会显示一次）

## 📝 配置说明

### 环境变量

| 变量名 | 说明 | 必需 |
|--------|------|------|
| `DEEPSEEK_API_KEY` | DeepSeek API密钥 | ✅ 是 |

### 文件结构

```
.
├── index.html                    # 主页面
├── netlify.toml                  # Netlify配置
├── package.json                  # 项目依赖
├── README.md                     # 说明文档
└── netlify/
    └── functions/
        ├── chat.js              # AI对话API
        └── translate.js         # 翻译API
```

## 🛠️ 本地开发

1. **克隆项目**
   ```bash
   git clone https://github.com/yourusername/pediatric-cardiac-surgery-assistant.git
   cd pediatric-cardiac-surgery-assistant
   ```

2. **安装依赖**
   ```bash
   npm install
   ```

3. **配置环境变量**
   创建 `.env` 文件：
   ```
   DEEPSEEK_API_KEY=your_api_key_here
   ```

4. **启动开发服务器**
   ```bash
   npm run dev
   ```

5. **访问应用**
   打开浏览器访问 `http://localhost:8888`

## ⚠️ 免责声明

本系统提供的信息仅供临床婴幼儿心外科医生参考，不能代替专业医疗判断。所有临床决策必须结合患儿的具体情况、最新医学证据和医生的专业经验综合判断。

**The information provided by this system is for reference by clinical pediatric cardiac surgeons only and cannot replace professional medical judgment. All clinical decisions must be made based on the specific conditions of the patient, latest medical evidence, and professional experience of physicians.**

## 🔒 隐私与安全

- **数据存储**: 随访提醒数据仅存储在用户浏览器本地
- **API安全**: DeepSeek API密钥存储在Netlify环境变量中，不会暴露给前端
- **HTTPS**: 通过Netlify自动启用HTTPS加密传输

## 🌐 参考医疗机构

### 国际顶尖儿童心脏中心

- 🇩🇪 [Deutsches Herzzentrum der Charité (DHZC)](https://www.dhzc.charite.de/en/)
- 🇩🇪 [Deutsches Herzzentrum Berlin (DHZB)](https://www.dhzb.de)
- 🇩🇪 [Heidelberg University Hospital](https://www.heidelberg-university-hospital.com)
- 🇩🇪 [LMU Klinikum München](https://www.lmu-klinikum.de)
- 🇺🇸 [Texas Children's Heart Center](https://www.texaschildrens.org/heart)
- 🇺🇸 [Children's Hospital of Philadelphia - Cardiac Center](https://www.chop.edu/centers-programs/cardiac-center)
- 🇺🇸 [Boston Children's Hospital - Heart Center](https://www.childrenshospital.org/centers/heart-center)

### 中国主要儿童心脏中心

- 🇨🇳 [上海儿童医学中心 - 心胸外科](https://www.scmc.com.cn/list/1404/2617.html)
- 🇨🇳 [阜外医院 - 小儿心脏外科中心](https://www.fuwaihospital.org/Departments/Main/Detail/60)
- 🇨🇳 [解放军总医院 - 小儿心脏外科](https://www.301hospital.com.cn/hospital/sixth/xexzwk.html)

## 🐛 问题反馈

如遇到问题，请通过以下方式反馈：
- 提交 GitHub Issue
- 发送邮件至项目维护者

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交Pull Request或Issue来改进此项目！

---

**注意**: 使用前请确保已正确配置DeepSeek API密钥，否则AI功能将无法使用。
