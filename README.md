# 陆壹AI工具导航

一个精美、轻量、开箱即用的 AI 工具导航站。收录全球优质 AI 工具，助力探索 AI 无限可能。

![Tech](https://img.shields.io/badge/HTML5-纯静态-orange) ![Tailwind](https://img.shields.io/badge/TailwindCSS-3.x-38bdf8) ![License](https://img.shields.io/badge/License-MIT-green)

## ✨ 特性

- **纯静态单页**：仅一个 `index.html`，无需后端、无需构建工具，双击即可运行
- **暗色/亮色主题**：一键切换，自动跟随系统偏好，选择持久化到 localStorage
- **实时搜索**：根据工具名称与描述即时过滤，无需回车刷新
- **分类筛选**：内置 10 个分类，点击分类按钮快速定位
- **大模型直达**：首页收录 DeepSeek、豆包、通义千问、Kimi、ChatGPT、Gemini、Grok、Claude 等常用入口
- **精美 UI**：TailwindCSS + Font Awesome，磨砂玻璃卡片、动态渐变背景、卡片浮入动画
- **响应式布局**：适配手机、平板、桌面，网格自适应 1/2/4 列
- **回到顶部**：滚动超过 300px 后显示悬浮按钮，平滑滚动

## 📂 分类一览

| 分类 | 收录内容示例 |
| --- | --- |
| 常用工具 | Gamma（AI PPT）、腾讯朱雀 AI 生成检测、建筑提示词 |
| AI 对话 | ChatGPT、Claude、Gemini、DeepSeek、Grok、智谱清言、Perplexity、秘塔 AI 搜索 |
| AI 写作 | NotebookLM、WPS AI、Kimi、Notion AI、Copy.ai |
| AI 绘图 | Midjourney、通义万相、Liblib、Flux AI、Civitai、Recraft |
| AI 视频 | 即梦 AI、可灵 Kling、海螺 AI、Runway、Luma Dream、腾讯混元 |
| AI 音乐 | Suno、Udio、ElevenLabs、Stable Audio、AIVA |
| AI 编程 | Cursor、Trae、Claude Code、Windsurf、Bolt.new、v0.dev、HuggingFace |
| 本地/桌面 | LM Studio、Ollama、CherryStudio |
| 模型排行 | LMSYS Arena、Open LLM Leaderboard |

## 🚀 快速开始

无需安装任何依赖，任选其一：

```bash
# 方式一：直接打开
双击 index.html 用浏览器打开

# 方式二：本地服务（推荐）
cd nav
python -m http.server 8080
# 或
npx serve .
```

然后访问 `http://localhost:8080`。

## 🔧 如何添加工具

编辑 `index.html` 中的 `TOOLS` 数组，按以下格式追加即可：

```js
{
  name:  '工具名称',
  desc:  '一句话描述',
  cat:   'chat',                                  // 分类 id，见 CATS 数组
  url:   'https://example.com',
  icon:  'fa-robot',                              // Font Awesome 图标类名
  color: 'text-blue-500 dark:text-blue-400',      // 图标颜色（Tailwind 类）
}
```

如需新增分类，在 `CATS` 数组中添加 `{ id, name, icon, color }`，并在顶部"常用大模型直达"对应修改 `HERO` 数组。

## 🛠️ 技术栈

- **HTML5 + 原生 JavaScript**：零依赖渲染逻辑
- **TailwindCSS 3.x**（CDN 引入，darkMode: class）
- **Font Awesome 6.4**（CDN 引入）
- **localStorage**：主题状态持久化

## 📄 许可证

本项目基于 [LICENSE](LICENSE) 开源。
