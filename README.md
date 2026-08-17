# cubist-image

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

一个可复用的 Codex Skill，用于把人物、建筑、街景、物体和风景转换为强烈解构的原创立体主义图像。

它不是简单地给照片套滤镜，而是通过多重视角、错位五官、交错几何平面、拼贴色块和绘画纹理重新构造画面。

## 特点

- 默认采用强烈几何解构，而不是轻微滤镜
- 支持照片风格转换和纯文字生成
- 支持人物、建筑、街景、物体和风景
- 保留主体数量、主要姿势、轮廓与关键颜色锚点
- 自动避免额外人物、可读水印、品牌文字和签名
- 内置五种视觉预设
- 使用 Codex 内置图像生成能力，无需在仓库中配置 API Key

## 视觉预设

| 预设 | 适合场景 | 视觉特点 |
| --- | --- | --- |
| `fractured-primary` | 肖像、社交媒体视觉 | 蓝、红、黄高对比色块，默认预设 |
| `analytical-ochre` | 建筑、物体、复杂构图 | 赭石、棕色与灰色的密集切面 |
| `paper-collage` | 海报、平面设计 | 撕纸、拼贴与炭笔线条 |
| `blue-expression` | 独处人物、情绪画面 | 深蓝色调与安静沉重的氛围 |
| `rose-stage` | 群像、表演、柔和肖像 | 玫瑰色、陶土色与柔化轮廓 |

## 安装

### 手动安装

克隆仓库：

```bash
git clone https://github.com/Actv6/cubist-image-skill.git
```

把仓库目录复制到你的 Codex Skills 目录，并确保入口文件路径为：

```text
<skills-directory>/cubist-image/SKILL.md
```

重新打开一个 Codex 会话后即可调用。

## 使用方法

上传一张图片，然后输入：

```text
使用 cubist-image，把这张照片做成强烈解构的立体主义作品。
```

指定预设和强度：

```text
使用 cubist-image 的 blue-expression 预设，强度 extreme。
```

纯文字生成：

```text
使用 cubist-image，以 paper-collage 预设创作一幅立体主义城市夜景。
```

### 强度选项

- `moderate`：更重视主体辨识度
- `strong`：默认；保留轮廓并强烈重构内部结构
- `extreme`：优先视觉冲击和抽象程度

## 文件结构

```text
cubist-image/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── presets.md
```

## 隐私与安全

- 不要把 API Key、Token、个人凭据或私密照片提交到仓库
- 本 Skill 默认调用 Codex 内置图像生成工具，仓库本身不读取环境变量
- 编辑本地照片时，请确认你有权处理和分享相关图片
- 输出应保持原创，不应复刻或临摹特定现有艺术作品

## 贡献

欢迎提交 Issue 或 Pull Request，包括：

- 新的配色预设
- 更稳定的主体保留规则
- 针对不同场景的提示词改进
- 文档与兼容性修正

提交贡献即表示你同意按照本仓库的 MIT License 发布相关内容。

## License

本项目采用 [MIT License](LICENSE)。
