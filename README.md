# 🍅 Tomato BookStore Frontend

一个基于 Vue 3 + TypeScript 构建的现代化在线书店前端应用，提供完整的图书购买和管理体验。

![Vue.js](https://img.shields.io/badge/Vue.js-3.5.13-4FC08D?style=flat&logo=vue.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.0-3178C6?style=flat&logo=typescript)
![Vite](https://img.shields.io/badge/Vite-6.2.1-646CFF?style=flat&logo=vite)
![Element Plus](https://img.shields.io/badge/Element_Plus-2.9.7-409EFF?style=flat&logo=element)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📖 项目简介

Tomato BookStore 是一个功能完善的在线书店系统前端，为用户提供图书浏览、购买、评价等全方位服务，同时为管理员提供商品、订单、优惠券等后台管理功能。

## ✨ 主要功能

### 👥 用户功能

- **用户认证**：注册、登录、安全设置
- **图书浏览**：分类浏览、搜索、详情查看
- **购物车**：添加商品、数量调整、批量操作
- **订单管理**：下单、支付、订单查询、物流跟踪
- **评价系统**：商品评价、星级评分、评价管理
- **个人中心**：账户设置、订单历史、个人信息
- **优惠券**：领取和使用优惠券
- **AI 聊天**：智能客服助手

### 👨‍💼 管理员功能

- **商品管理**：添加、编辑、删除商品信息
- **广告管理**：轮播图和推广内容管理
- **评价管理**：用户评价审核和管理
- **优惠券管理**：创建、编辑优惠券活动
- **数据统计**：销售数据和用户行为分析

## 🛠️ 技术栈

### 核心框架

- **Vue 3** - 渐进式 JavaScript 框架
- **TypeScript** - 类型安全的 JavaScript 超集
- **Vite** - 下一代前端构建工具

### 状态管理

- **Pinia** - Vue 3 官方推荐状态管理库

### 路由

- **Vue Router 4** - Vue.js 官方路由管理器

### UI 框架

- **Element Plus** - 基于 Vue 3 的桌面端组件库
- **Element Plus Icons** - 丰富的图标库

### 网络请求

- **Axios** - Promise 基于的 HTTP 库

### 工具库

- **Marked** - Markdown 解析器
- **DOMPurify** - DOM XSS 防护
- **UUID** - 唯一标识符生成

### 开发工具

- **Vue DevTools** - Vue 开发者工具
- **ESLint + Prettier** - 代码规范和格式化

## 🚀 快速开始

### 环境要求

- Node.js >= 18.0.0
- pnpm >= 8.0.0 (推荐) 或 npm >= 9.0.0

### 安装依赖

```bash
# 使用 pnpm (推荐)
pnpm install

# 或使用 npm
npm install
```

### 开发环境运行

```bash
# 启动开发服务器
pnpm dev

# 或
npm run dev
```

访问 `http://localhost:5173` 查看应用

### 构建生产版本

```bash
# 类型检查 + 构建
pnpm build

# 或
npm run build
```

### 预览生产构建

```bash
# 预览构建结果
pnpm preview

# 或
npm run preview
```

## 📁 项目结构

```text
src/
├── assets/           # 静态资源
│   ├── images/      # 图片资源
│   ├── icons/       # 图标资源
│   └── css/         # 样式文件
├── components/       # 可复用组件
│   └── icons/       # 图标组件
├── pages/           # 页面组件
├── views/           # 视图组件
│   ├── AccountSettings/     # 账户设置相关
│   ├── AdminProductManagement/  # 商品管理相关
│   ├── AdminAdverManagement/    # 广告管理相关
│   ├── AdminCouponManagement/   # 优惠券管理相关
│   ├── AdminEvaluationManagement/ # 评价管理相关
│   ├── Detail/              # 商品详情相关
│   ├── HomePage/            # 首页相关
│   └── Evaluation/          # 评价相关
├── router/          # 路由配置
├── stores/          # 状态管理
├── api/            # API 接口
└── main.ts         # 应用入口
```

## 🔧 开发配置

### IDE 推荐

- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)
- 禁用 Vetur 插件以避免冲突

### TypeScript 支持

项目使用 `vue-tsc` 进行类型检查，确保 `.vue` 文件的类型安全。

### 代理配置

开发环境已配置 API 代理：

```typescript
server: {
  proxy: {
    '/api': {
      target: 'http://tomatomallapi.yunshangmalan.online',
      changeOrigin: true
    }
  }
}
```

## 🌟 核心特性

- **📱 响应式设计**：适配各种设备屏幕
- **🎨 现代化 UI**：基于 Element Plus 的精美界面
- **⚡ 高性能**：Vite 构建，快速的热更新
- **🔒 类型安全**：全面的 TypeScript 支持
- **🛡️ 安全防护**：XSS 防护和输入验证
- **♿ 无障碍访问**：遵循 Web 无障碍标准
- **🔄 状态管理**：Pinia 实现的响应式状态管理

## 📚 页面路由

| 路径 | 页面 | 描述 |
|------|------|------|
| `/` | 登录页 | 用户登录入口 |
| `/register` | 注册页 | 用户注册 |
| `/homepage` | 首页 | 商品展示和分类 |
| `/detail/:id` | 商品详情 | 商品详细信息 |
| `/cart` | 购物车 | 购物车管理 |
| `/order` | 订单页 | 订单确认和支付 |
| `/payment-success` | 支付成功 | 支付完成页面 |
| `/myorders` | 我的订单 | 订单历史查询 |
| `/myevaluation` | 我的评价 | 评价管理 |
| `/account-settings` | 账户设置 | 个人信息设置 |
| `/admin/*` | 管理后台 | 各种管理功能页面 |

## 🤝 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交变更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢

- [Vue.js](https://vuejs.org/) - 优秀的前端框架
- [Element Plus](https://element-plus.org/) - 精美的 UI 组件库
- [Vite](https://vitejs.dev/) - 快速的构建工具

## 📞 联系方式

如有问题或建议，请通过以下方式联系：

- 提交 [Issue](https://github.com/Meiyuan-Zhu/Tomato-BookStore-Frontend/issues)
- 发送邮件到项目维护者

---

⭐ 如果这个项目对你有帮助，请给我们一个 Star！
