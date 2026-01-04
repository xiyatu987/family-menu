# 家庭菜单管理工具APP

## 项目概述
一个智能的家庭菜单管理工具，每次打开随机推荐四个菜品（3个蔬菜+1个荤菜），确保营养搭配合理，选择应季食材。

## 功能特性
- 🍽️ 智能菜单推荐：每次打开显示4个菜品
- 🥬 应季蔬菜推荐：根据季节推荐当季蔬菜
- 🥩 营养搭配：荤素搭配，营养均衡
- 🖼️ 直观展示：菜品图片和名称清晰展示
- 🐳 Docker部署：支持NAS等设备的Docker部署
- 📱 响应式设计：支持手机、平板、电脑访问

## 技术栈
- **前端**: React + TypeScript + Tailwind CSS
- **后端**: Node.js + Express + TypeScript
- **数据库**: SQLite (轻量级，适合家庭部署)
- **部署**: Docker + Docker Compose

## 项目结构
```
family-menu-app/
├── backend/                 # 后端服务
│   ├── src/
│   │   ├── controllers/     # 控制器
│   │   ├── models/         # 数据模型
│   │   ├── routes/         # 路由
│   │   ├── services/       # 业务逻辑
│   │   └── database/       # 数据库相关
│   └── Dockerfile
├── frontend/               # 前端应用
│   ├── src/
│   │   ├── components/     # React组件
│   │   ├── pages/         # 页面
│   │   ├── services/      # API服务
│   │   └── types/         # TypeScript类型
│   └── Dockerfile
├── docker-compose.yml     # Docker编排
└── README.md             # 项目文档
```

## 安装和运行

### 开发环境
```bash
# 后端
cd backend
npm install
npm run dev

# 前端
cd frontend
npm install
npm run dev
```

### Docker部署
```bash
# 构建并启动所有服务
docker-compose up -d

# 查看日志
docker-compose logs -f

# 停止服务
docker-compose down
```

## API文档

### 获取菜单推荐
```
GET /api/menu/recommend
Response: {
  "dishes": [
    {
      "id": 1,
      "name": "西红柿炒鸡蛋",
      "image": "https://example.com/tomato-egg.jpg",
      "category": "蔬菜",
      "season": "夏季",
      "nutrition": {
        "calories": 120,
        "protein": "8g",
        "fat": "6g",
        "carbs": "12g"
      }
    }
  ]
}
```

## 开发计划
- [x] 需求分析和技术选型
- [ ] 设计数据库结构和菜谱数据
- [ ] 开发后端API服务
- [ ] 开发前端界面
- [ ] 实现菜单推荐算法
- [ ] Docker容器化配置
- [ ] 测试和优化
- [ ] 部署文档编写

## 许可证
MIT License
