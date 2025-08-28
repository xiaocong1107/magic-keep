# 魔法笔记MagicKeep

![Screenshot]([https://github.com/user-attachments/assets/cc03dd25-072b-4766-b788-971aeda609f3](https://img.bornforai.cn/articlePicture/2025/magickeep/maigckeep1.jpg))

魔法笔记MagicKeep是一款现代化的笔记应用，具有简洁界面和强大功能。该应用采用前沿的Web技术栈构建，提供Markdown编辑、清单管理、图片附件、标签分类、色彩主题、暗黑模式、拖拽排序、数据导入导出、用户认证等核心功能。

项目最大的亮点是集成了AI分析功能，用户可以对笔记内容进行AI智能分析，自动生成内容摘要、要点整理、改进建议等，极大地提升了笔记的价值和用户体验。

## ✨ 核心功能

- **用户认证与多用户支持**
  - 用户注册、登录（用户名+密码）
  - 秘钥恢复功能，支持通过秘钥登录
  - 多用户隔离，每个用户只能看到自己的笔记

- **笔记管理**
  - 支持文本笔记，内置Markdown编辑器
  - 清单功能（可添加项目、标记完成状态、行内编辑）
  - 智能回车键（自动继续列表或在空行时退出）
  - 格式化工具栏（编辑器内和模态编辑模式）
  - 链接在新标签页中打开

- **图片管理**
  - 支持多图片附件（客户端压缩）
  - 网格缩略图显示和大图模态查看
  - 全屏查看器支持前后导航和图片下载

- **组织与布局**
  - 笔记置顶/取消置顶功能
  - 标签作为标签芯片显示
  - 标签侧边栏/抽屉，显示所有标签及数量
  - 快速筛选：所有笔记和所有图片
  - 每个笔记支持自定义颜色主题
  - 全文搜索功能
  - 拖拽重新排序
  - 网格卡片显示截断内容和标签芯片

- **AI智能分析功能（核心亮点）**
  - 用户可对笔记启用AI分析，提供智能内容处理
  - 支持多种预设提示模板，也可自定义提示语
  - AI分析在后台异步进行，不阻塞用户操作
  - 实时状态显示（分析中、完成、失败）
  - 失败重试机制
  - 生成内容以Markdown格式展示

- **实时协作功能**
  - 清单实时协作：多人可同时添加/标记项目，实时查看更新
  - 笔记协同编辑：多人可共同编辑Markdown笔记，变更实时同步

- **批量操作功能**
  - 支持多选笔记进行批量下载、置顶/取消置顶、删除或更改颜色

- **数据管理**
  - 导出所有笔记（JSON格式）和导入（合并模式，保留现有笔记）
  - 单笔记下载为.md文件
  - 支持从Google Keep导入（Google Takeout）

- **渐进式Web应用(PWA)**
  - 支持在桌面和移动设备上安装

- **界面与主题**
  - 使用Tailwind CSS (v4)构建，具有玻璃态效果
  - 支持暗黑/明亮模式，并持久化保存用户选择
  - 响应式设计，适配各种屏幕尺寸

## 🚀 快速开始

### 在线体验

访问我们的在线演示站点：[https://app.bornforai.cn](https://app.bornforai.cn)

### 本地部署

1. 克隆仓库：
   ```bash
   git clone https://github.com/your-username/magic-keep.git
   cd magic-keep
   ```

2. 安装依赖：
   ```bash
   npm install
   ```

3. 启动开发服务器：
   ```bash
   npm run dev
   ```

4. 访问应用：
   在浏览器中打开 http://localhost:5173

## 🛠 技术栈

- **前端**: React 18+, Vite 4+, Tailwind CSS 4+
- **状态管理**: React Hooks
- **拖拽功能**: @dnd-kit库
- **图标库**: Lucide React
- **动画库**: Framer Motion
- **Markdown解析**: Marked
- **PWA支持**: vite-plugin-pwa
- **后端**: Express.js + SQLite

## 📦 部署

### Docker部署

```bash
# 拉取最新镜像
docker pull nikunjsingh/magic-notes:latest

# 创建数据目录
mkdir -p ~/.magic-notes

# 运行容器
docker run -d \
  --name magic-notes \
  --restart unless-stopped \
  -p 8080:8080 \
  -e NODE_ENV=production \
  -e API_PORT=8080 \
  -e JWT_SECRET="replace-with-a-long-random-string" \
  -e DB_FILE="/app/data/notes.db" \
  -e ADMIN_EMAILS="your-admin-username" \
  -v ~/.magic-notes:/app/data \
  nikunjsingh/magic-notes:latest
```

访问地址：http://localhost:8080

### 静态文件部署

```bash
# 构建静态文件
npm run build:out

# 部署 out 目录到任何静态文件服务器
```

## 🤝 贡献

欢迎提交Issue和Pull Request来帮助我们改进项目。

1. Fork本仓库
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个Pull Request

## 📄 许可证

本项目采用MIT许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 📧 联系我们

如有任何问题或建议，请通过以下方式联系我们：

- 提交Issue
- 发送邮件至：[your-email@example.com](mailto:your-email@example.com)

---

© 2025 魔法笔记MagicKeep. 保留所有权利。
