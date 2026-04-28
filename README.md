# 🖼️ 画廊 - 流欺

一个优雅的瀑布流画廊，支持图片分类、懒加载、背景图动态切换，纯HTML/CSS/JS实现，无需任何依赖。

## ✨ 特性

- 🎨 **瀑布流布局** - 自动适配不同尺寸图片，支持宽高比分类
- 🖱️ **图片分类** - 横图(horizontal)/竖图(vertical)/方图(square)一键筛选
- 🌄 **动态背景** - 背景图定时轮播，支持8种平移入场动效
- 💾 **图片预览** - 点击放大预览，支持下载原图/新窗口打开
- 📱 **响应式设计** - 手机/平板/PC自适应列数(2/3/4列)
- ⚡ **懒加载** - 滚动时按需加载，性能友好
- 🎯 **返回顶部** - 一键返回，体验顺滑

## 🚀 快速开始

### 1. 准备图片列表

在项目根目录创建 `img.txt` 文件，每行一个图片URL：
https://example.com/images/photo1.jpg

https://example.com/images/photo2.png

https://example.com/images/photo3.webp

### 2. 目录结构
project/
├── index.html # 主文件
├── img.txt # 图片URL列表
└── README.md # 说明文档

### 3. 运行

直接双击 `index.html` 或在本地服务器中打开即可。

## 📝 图片分类规则

系统根据URL路径自动判断图片类型：

| 类型 | URL规则 | 示例 |
|------|---------|------|
| 横图 | 包含 `/h/` | `https://cdn.com/h/sunset.jpg` |
| 竖图 | 包含 `/s/` | `https://cdn.com/s/portrait.jpg` |
| 方图 | 包含 `/f/` | `https://cdn.com/f/avatar.jpg` |

> 💡 如果想自定义分类规则，可以修改 `getImageTypeFromUrl()` 函数。

## ⚙️ 配置说明

在 `index.html` 的 `<script>` 中可以调整以下参数：

```javascript
const BATCH_SIZE = 28;        // 每次滚动加载的图片数量
bgInterval = setInterval(...); // 背景切换间隔(默认5000ms)
🎨 背景图API
默认使用 https://api.lqay.cn/api/zxsjt/?cat=heng 获取随机背景图。

如需更换背景源，修改 BG_API_URL 变量即可。

📄 许可证
MIT © 2026 [你的名字]

🙏 致谢
图片源：[你的CDN仓库链接]

API提供：[你的博客/API地址]

📮 联系
博客：blog.lqay.cn
