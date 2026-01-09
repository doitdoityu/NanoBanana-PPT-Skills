# PPT Generator Skill

> 基于文档内容使用 Google Nano Banana Pro 自动生成高质量 PPT 图片的 Claude Code Skill

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Claude](https://img.shields.io/badge/Claude-Code%20Skill-orange.svg)

**创作者**: [歸藏](https://github.com/op7418)

[功能特性](#-功能特性) • [一键安装](#-一键安装-claude-code) • [使用指南](#-使用指南) • [风格库](#-风格库) • [常见问题](#-常见问题)

</div>

---

## 📖 简介

PPT Generator 是一个强大的 Claude Code Skill，能够智能分析文档内容，自动生成专业的 PPT 图片。使用 Google 最新的 Nano Banana Pro 图像生成模型，支持多种视觉风格，生成 16:9 高清 PPT，并附带优雅的 HTML5 播放器。

### 🎨 视觉效果预览

**风格1: 渐变毛玻璃卡片风格**
- 高端未来科技感
- 3D玻璃物体 + 霓虹渐变
- 电影级光照效果
- 适合：科技产品、商务演示、品牌展示

**风格2: 矢量插画风格**
- 温暖可爱的扁平化设计
- 黑色轮廓线 + 复古配色
- 玩具模型般的几何化处理
- 适合：教育培训、创意提案、品牌故事

---

## ✨ 功能特性

### 核心能力

- 🤖 **智能文档分析** - 自动提取核心要点，规划 PPT 内容结构
- 🎨 **多风格支持** - 内置2种专业风格，可无限扩展
- 🖼️ **高质量输出** - 16:9 比例，2K/4K 分辨率可选
- 📊 **智能布局** - 封面页、内容页、数据页自动识别
- 🎬 **HTML5 播放器** - 支持键盘导航、全屏、自动播放
- ⚡ **快速生成** - 2K 约 30 秒/页，5 页 PPT 约 2.5 分钟

### 技术亮点

- ✅ 基于 Google Nano Banana Pro (Gemini 3 Pro Image Preview)
- ✅ 完整的提示词工程和风格管理系统
- ✅ 模块化设计，易于扩展新风格
- ✅ 安全的环境变量管理
- ✅ 详细的文档和使用指南

---

## 🚀 一键安装 (Claude Code)

### 方法一：自动化安装（推荐）

**复制以下提示词，发送给 Claude Code，即可完成全自动安装：**

```
请帮我安装 PPT Generator Skill：

1. 从 GitHub 克隆项目：
   git clone https://github.com/op7418/NanoBanana-PPT-Skills.git
   cd NanoBanana-PPT-Skills

2. 创建 Python 虚拟环境：
   python3 -m venv venv
   source venv/bin/activate

3. 安装依赖：
   pip install google-genai pillow

4. 配置系统环境变量（请将 YOUR_API_KEY_HERE 替换为我的实际 API 密钥）：

   对于 zsh 用户（macOS 默认）：
   echo 'export GEMINI_API_KEY="YOUR_API_KEY_HERE"' >> ~/.zshrc
   source ~/.zshrc

   对于 bash 用户：
   echo 'export GEMINI_API_KEY="YOUR_API_KEY_HERE"' >> ~/.bashrc
   source ~/.bashrc

5. 验证安装：
   ./run.sh --help

6. 运行测试（如果有 test_slides_plan.json）：
   ./run.sh --plan test_slides_plan.json --style styles/gradient-glass.md --resolution 2K

完成后，告诉我安装结果和如何使用。

我的 API 密钥是：YOUR_API_KEY_HERE
（请在执行前帮我替换所有 YOUR_API_KEY_HERE）
```

**使用步骤**：
1. 复制上面的提示词
2. 将 `YOUR_API_KEY_HERE` 替换为你的实际 [Google AI API 密钥](https://makersuite.google.com/app/apikey)
3. 发送给 Claude Code
4. 等待自动安装完成

### 方法二：直接使用（如果已克隆）

如果你已经克隆了仓库，直接发送：

```
我想使用 PPT Generator 生成一个演示文稿。

项目路径：NanoBanana-PPT-Skills/

请基于我提供的文档内容，生成一个 [5/10/15/20] 页的 PPT，
使用 [渐变毛玻璃卡片风格/矢量插画风格]，分辨率 2K。

我的文档内容是：
[在这里粘贴你的文档内容或提供文档路径]
```

---

## 📋 手动安装步骤

如果你想手动安装，按照以下步骤操作：

### 前置要求

- Python 3.8+
- Git
- Google AI API 密钥 ([获取地址](https://makersuite.google.com/app/apikey))

### 安装步骤

#### 1. 克隆项目

```bash
git clone https://github.com/op7418/NanoBanana-PPT-Skills.git
cd NanoBanana-PPT-Skills
```

#### 2. 创建虚拟环境

```bash
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

#### 3. 安装依赖

```bash
pip install google-genai pillow
```

#### 4. 配置 API 密钥

**推荐方式：系统环境变量**

编辑你的 shell 配置文件：

```bash
# zsh 用户 (macOS 默认)
echo 'export GEMINI_API_KEY="your-api-key-here"' >> ~/.zshrc
source ~/.zshrc

# bash 用户
echo 'export GEMINI_API_KEY="your-api-key-here"' >> ~/.bashrc
source ~/.bashrc

# fish 用户
set -Ux GEMINI_API_KEY "your-api-key-here"
```

**替代方式：.env 文件**

```bash
cp .env.example .env
# 编辑 .env 文件，填入你的 API 密钥
```

#### 5. 验证安装

```bash
./run.sh --help
```

应该显示：
```
✅ 使用系统环境变量中的API密钥
usage: generate_ppt.py [-h] --plan PLAN --style STYLE ...
```

---

## 💡 使用指南

### 在 Claude Code 中使用

#### 基础用法

直接告诉 Claude Code 你的需求：

```
我想基于以下文档生成一个 5 页的 PPT：

[文档标题]
[文档内容...]

使用渐变毛玻璃卡片风格，2K 分辨率。
```

#### 指定风格和页数

```
帮我生成一个关于"AI产品设计"的 10 页 PPT，
使用矢量插画风格，4K 分辨率。

主要内容包括：
1. 现状分析
2. 设计原则
3. 案例研究
4. 未来展望
```

#### 从文件生成

```
基于 my-document.md 文档，生成一个 15 页的 PPT，
使用渐变毛玻璃卡片风格。
```

### 命令行使用

#### 准备 slides 规划文件

创建 `slides_plan.json`：

```json
{
  "title": "你的演示标题",
  "total_slides": 5,
  "slides": [
    {
      "slide_number": 1,
      "page_type": "cover",
      "content": "标题：演示主题\n副标题：演示描述"
    },
    {
      "slide_number": 2,
      "page_type": "content",
      "content": "核心要点1\n- 子要点1\n- 子要点2"
    }
  ]
}
```

#### 生成 PPT

```bash
./run.sh --plan slides_plan.json \
         --style styles/gradient-glass.md \
         --resolution 2K
```

#### 查看结果

生成完成后：

```bash
open outputs/TIMESTAMP/index.html
```

---

## 🎨 风格库

### 已内置风格

#### 1. 渐变毛玻璃卡片风格 (`gradient-glass.md`)

**视觉特点**：
- Apple Keynote 极简主义
- 玻璃拟态效果
- 霓虹紫/电光蓝/珊瑚橙渐变
- 3D 玻璃物体
- 电影级体积光照

**适用场景**：
- 🚀 科技产品发布
- 💼 商务演示
- 📊 数据报告
- 🏢 企业品牌展示

#### 2. 矢量插画风格 (`vector-illustration.md`)

**视觉特点**：
- 扁平化矢量设计
- 统一黑色轮廓线
- 复古柔和配色
- 几何化简化
- 玩具模型感

**适用场景**：
- 📚 教育培训
- 🎨 创意提案
- 👶 儿童相关
- 💖 温暖品牌故事

### 添加自定义风格

1. 在 `styles/` 目录创建新的 `.md` 文件
2. 按照模板编写风格定义（参考现有风格）
3. 直接使用新风格生成 PPT

---

## 🎮 播放器功能

生成的 HTML5 播放器支持：

| 功能 | 快捷键 | 说明 |
|------|--------|------|
| 下一页 | `→` `↓` | 切换到下一张 |
| 上一页 | `←` `↑` | 切换到上一张 |
| 首页 | `Home` | 跳到第一页 |
| 末页 | `End` | 跳到最后一页 |
| 全屏 | `ESC` | 切换全屏模式 |
| 自动播放 | `空格` | 暂停/继续 |
| 隐藏控件 | `H` | 隐藏/显示 |
| 触摸滑动 | - | 移动设备支持 |

---

## 📚 项目结构

```
NanoBanana-PPT-Skills/
├── README.md                 # 本文件
├── ENV_SETUP.md              # 环境变量配置指南
├── SECURITY.md               # 安全最佳实践
├── QUICKSTART.md             # 5分钟快速上手
├── generate_ppt.py           # 核心生成脚本
├── run.sh                    # 启动脚本
├── ppt-generator.md          # Skill 定义文件
├── .env.example              # 环境变量模板
├── .gitignore                # Git 忽略规则
├── styles/                   # 风格库
│   ├── gradient-glass.md     # 渐变毛玻璃卡片风格
│   └── vector-illustration.md # 矢量插画风格
├── templates/                # HTML 模板
│   └── viewer.html           # PPT 播放器
└── outputs/                  # 生成结果（自动创建）
```

---

## 🔧 配置选项

### 分辨率选择

| 分辨率 | 尺寸 | 文件大小 | 生成速度 | 推荐场景 |
|--------|------|----------|----------|----------|
| 2K | 2752x1536 | ~2.5MB/页 | ~30秒/页 | 日常演示、在线分享 ✅ |
| 4K | 5504x3072 | ~8MB/页 | ~60秒/页 | 打印输出、大屏展示 |

### 页数建议

| 页数范围 | 演讲时长 | 适用场景 |
|----------|----------|----------|
| 5 页 | 5 分钟 | 电梯演讲、快速介绍 |
| 5-10 页 | 10-15 分钟 | 标准演示、产品介绍 |
| 10-15 页 | 20-30 分钟 | 深入讲解、培训课程 |
| 20-25 页 | 45-60 分钟 | 完整培训、研讨会 |

---

## 🎯 使用示例

### 示例 1：快速生成

**需求**：基于会议纪要生成 5 页快速回顾 PPT

**Claude Code 提示词**：
```
我需要基于这份会议纪要生成一个 5 页的 PPT，使用矢量插画风格：

会议主题：Q1 产品路线图规划
时间：2026-01-09
参与人：产品团队

讨论内容：
1. 用户反馈汇总
2. 新功能优先级
3. 技术可行性评估
4. Q1 里程碑
5. 下一步行动项

请生成 PPT，2K 分辨率。
```

### 示例 2：教育内容

**需求**：制作编程教学 PPT

**Claude Code 提示词**：
```
帮我创建一个 15 页的 Python 基础教程 PPT，使用矢量插画风格：

第1章：Python 简介
第2章：变量和数据类型
第3章：控制流程
第4章：函数
第5章：实践项目

每章 3 页，包括概念讲解、代码示例和练习题。
分辨率 2K。
```

### 示例 3：商业演示

**需求**：投资人路演 PPT

**Claude Code 提示词**：
```
基于我们的商业计划书，生成一个 20 页的投资路演 PPT，
使用渐变毛玻璃卡片风格：

1. 问题与机会
2. 解决方案
3. 市场规模
4. 商业模式
5. 竞争分析
6. 团队介绍
7. 财务预测
8. 融资需求

4K 分辨率（准备打印）。
```

---

## ❓ 常见问题

### Q: 如何获取 Google AI API 密钥？

**A**: 访问 [Google AI Studio](https://makersuite.google.com/app/apikey)，登录后即可创建 API 密钥。

### Q: 生成失败怎么办？

**A**: 检查以下几点：
1. API 密钥是否正确配置
2. 网络连接是否正常
3. Python 依赖是否完整安装
4. 查看详细错误信息

### Q: 可以生成中文内容吗？

**A**: 完全支持！Nano Banana Pro 支持多语言，中文生成效果很好。

### Q: 如何导出为 PDF？

**A**:
1. 在浏览器中打开生成的 `index.html`
2. 按 `Cmd+P` (Mac) 或 `Ctrl+P` (Windows)
3. 选择"另存为 PDF"

### Q: 单页生成失败会影响其他页吗？

**A**: 不会。每页独立生成，可以单独重新生成失败的页面。

### Q: 是否支持自定义字体？

**A**: 当前由 Nano Banana Pro 自动选择字体。可以在风格提示词中指定字体风格偏好。

### Q: 生成的图片可以商用吗？

**A**: 请查阅 [Google AI 使用条款](https://ai.google.dev/terms)。一般情况下，你拥有生成内容的权利。

---

## 🛡️ 安全说明

### API 密钥安全

- ✅ 使用系统环境变量存储（推荐）
- ✅ .env 文件已在 .gitignore 中
- ✅ 代码中无硬编码密钥
- ✅ 可安全提交到 GitHub

详细说明请查看：
- **ENV_SETUP.md** - 环境变量配置指南
- **SECURITY.md** - 安全最佳实践

### 提交前检查

```bash
# 验证没有密钥泄露
grep -r "AIzaSy" --exclude-dir=.git --exclude-dir=venv .
# 应该无输出

# 检查 Git 状态
git status
# 确认无敏感文件
```

---

## 🤝 贡献指南

### 添加新风格

1. Fork 本项目
2. 在 `styles/` 创建新风格文件
3. 参考现有风格编写提示词
4. 测试生成效果
5. 提交 Pull Request

### 报告问题

在 [GitHub Issues](https://github.com/op7418/NanoBanana-PPT-Skills/issues) 提交问题，请包含：
- 错误信息
- 操作步骤
- 系统环境
- 日志文件（如有）

---

## 📝 更新日志

### v1.0.0 (2026-01-09)

- ✨ 首次发布
- 🎨 内置 2 种专业风格
- 🖼️ 支持 2K/4K 分辨率
- 🎬 HTML5 播放器
- 📊 智能文档分析
- 🔐 安全的环境变量管理

---

## 📄 许可证

MIT License

Copyright (c) 2026 歸藏

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 🙏 致谢

- **Google Gemini Team** - 提供强大的 Nano Banana Pro 图像生成模型
- **Claude Code** - 优秀的 AI 编程助手平台
- **开源社区** - 提供的各种工具和灵感

---

## 📞 联系方式

- **创作者**: 歸藏
- **GitHub**: [@op7418](https://github.com/op7418)
- **Issues**: [GitHub Issues](https://github.com/op7418/NanoBanana-PPT-Skills/issues)

---

<div align="center">

**⭐ 如果这个项目对你有帮助，请给一个 Star！**

Made with ❤️ by 歸藏 | Powered by Claude Code & Google Nano Banana Pro

</div>
