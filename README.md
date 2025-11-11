# AI智能平台

一个完整的AI智能对话服务平台，支持用户注册登录、邮箱验证、AI对话、个人中心和管理后台等功能。

## 🌟 功能特性

### 用户功能
- 🔐 用户注册登录（邮箱验证码）
- 👤 个人信息管理（姓名、性别、头像、个人介绍）
- 💬 AI智能对话（支持DeepSeek和ChatGPT）
- 📱 响应式设计，支持移动端

### 管理员功能
- 👥 用户管理（查看、封禁、解封）
- 🔍 IP地址追踪
- 📊 系统统计
- 🔧 后台管理面板

### 技术特性
- ⚡ 前后端分离架构
- 🔒 JWT身份认证
- 📧 SMTP邮箱验证
- 💾 MySQL数据库
- 🎨 Tailwind CSS样式

## 🚀 快速开始

### 环境要求
- Node.js >= 16.0.0
- MySQL >= 5.7
- npm >= 7.0.0

### 安装步骤

1. **克隆项目**
```bash
git clone <repository-url>
cd ai-platform
```

2. **安装依赖**
```bash
npm run install:all
```

3. **配置环境变量**

创建 `backend/.env` 文件：
```env
# 数据库配置
DB_HOST=localhost
DB_PORT=3306
DB_NAME=ai_platform
DB_USERNAME=root
DB_PASSWORD=your_password

# JWT配置
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=7d

# 邮箱配置
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_email_password

# AI API配置
DEEPSEEK_API_KEY=your_deepseek_api_key
CHATGPT_API_KEY=your_chatgpt_api_key

# 服务器配置
PORT=3001
NODE_ENV=development
CORS_ORIGIN=http://localhost:5173
```

创建 `frontend/.env` 文件：
```env
VITE_API_BASE_URL=http://localhost:3001/api
```

4. **初始化数据库**
```bash
npm run db:migrate
```

5. **启动开发服务器**
```bash
npm run dev
```

访问地址：
- 前端：http://localhost:5173
- 后端：http://localhost:3001

## 📁 项目结构

```
ai-platform/
├── backend/                 # 后端服务
│   ├── src/
│   │   ├── config/         # 配置文件
│   │   ├── models/         # 数据模型
│   │   ├── routes/         # API路由
│   │   ├── services/       # 业务服务
│   │   ├── middleware/     # 中间件
│   │   └── utils/          # 工具函数
│   ├── migrations/         # 数据库迁移
│   └── package.json
├── frontend/               # 前端应用
│   ├── src/
│   │   ├── components/     # 公共组件
│   │   ├── pages/          # 页面组件
│   │   ├── store/          # 状态管理
│   │   ├── services/       # API服务
│   │   └── utils/          # 工具函数
│   └── package.json
└── package.json           # 根包配置
```

## 🔧 开发指南

### 后端开发
```bash
cd backend
npm run dev
```

### 前端开发
```bash
cd frontend
npm run dev
```

### 数据库迁移
```bash
npm run db:migrate
```

### 生产构建
```bash
npm run build
```

## 📚 API文档

### 认证接口
- `POST /api/auth/send-verification-code` - 发送验证码
- `POST /api/auth/register` - 用户注册
- `POST /api/auth/login` - 用户登录
- `GET /api/auth/me` - 获取当前用户

### 用户接口
- `PUT /api/user/profile` - 更新用户信息
- `PUT /api/user/password` - 修改密码

### 聊天接口
- `POST /api/chat/message` - 发送消息
- `GET /api/chat/history` - 获取对话历史

### 管理接口
- `GET /api/admin/users` - 获取用户列表
- `PUT /api/admin/users/:id/ban` - 封禁用户
- `PUT /api/admin/users/:id/unban` - 解封用户

## 🛡️ 安全性

- 密码使用bcrypt加密
- JWT token认证
- IP地址追踪
- 邮箱验证码
- SQL注入防护
- XSS攻击防护

## 🤝 贡献指南

1. Fork 项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🙏 致谢

- [React](https://reactjs.org/) - 前端框架
- [Express](https://expressjs.com/) - 后端框架
- [Tailwind CSS](https://tailwindcss.com/) - CSS框架
- [Sequelize](https://sequelize.org/) - ORM工具
- [DeepSeek](https://deepseek.com/) - AI服务
- [ChatGPT](https://openai.com/) - AI服务

## 📞 联系我们

如有问题或建议，请通过以下方式联系我们：

- 邮箱：support@aiplatform.com
- 项目地址：[GitHub Repository]

---

**AI智能平台** © 2024 - 让AI对话更智能、更便捷！