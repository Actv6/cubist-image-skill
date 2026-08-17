# cubist-image

一个可复用的 Codex Skill，用于把人物、建筑、街景和风景照片转换为强烈解构的原创立体主义图像。

## 特点

- 默认采用强烈几何解构，而不是轻微滤镜
- 支持人物、建筑、街景、物体和风景
- 保留主体数量、主要姿势、轮廓与关键颜色锚点
- 自动避免额外人物、可读水印、品牌文字和签名
- 内置五种视觉预设：`fractured-primary`、`analytical-ochre`、`paper-collage`、`blue-expression`、`rose-stage`

## 安装

把整个仓库目录复制到 Codex Skills 目录，并确保入口文件路径为：

```text
<skills-directory>/cubist-image/SKILL.md
```

重新打开一个 Codex 会话后即可调用。

## 使用示例

上传一张图片，然后输入：

```text
使用 cubist-image，把这张照片做成强烈解构的立体主义作品。
```

也可以指定预设和强度：

```text
使用 cubist-image 的 blue-expression 预设，强度 extreme。
```

## 文件结构

```text
cubist-image/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── presets.md
```

生成图片时使用 Codex 内置图像生成能力，不需要在仓库中配置 API Key。
