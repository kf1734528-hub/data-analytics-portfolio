# Data Analytics Portfolio

Personal Data Analytics Portfolio

中国地质大学（武汉）经济管理学院应用统计专业硕士研究生的数据分析作品集。网站用于持续记录统计建模、数据处理、空间分析与商业分析项目。

在线地址（首次成功部署后可访问）：

<https://kf1734528-hub.github.io/data-analytics-portfolio/>

## 技术栈

- Quarto：静态网站与分析报告生成
- Markdown / QMD：页面与项目文档
- GitHub：版本管理
- GitHub Pages：网站托管
- Python、SQL、R：后续分析项目所用工具

## 本地运行

需要安装 [Quarto](https://quarto.org/docs/get-started/)。在项目根目录运行：

```bash
quarto preview
```

生成静态网站：

```bash
quarto render
```

构建结果位于 `docs/`。该目录由 Quarto 自动生成并已加入 `.gitignore`，GitHub Actions 会在部署时重新生成。

## 项目结构

```text
.
├── _quarto.yml
├── index.qmd
├── styles.css
├── about/
│   └── profile.qmd
├── projects/
│   ├── index.qmd
│   ├── wuhan-housing/
│   │   └── index.qmd
│   └── hechi-mining/
│       └── index.qmd
├── skills/
│   └── skills.qmd
├── contact/
│   └── contact.qmd
├── assets/
│   └── favicon.svg
└── .github/workflows/
    └── publish.yml
```

## 添加新项目

1. 在 `projects/` 下创建独立目录，例如 `projects/project-name/`。
2. 在目录中创建 `index.qmd`。
3. 在 `projects/index.qmd` 添加项目卡片和链接。
4. 本地运行 `quarto render`，确认页面和链接正常。

项目内容应包含问题定义、数据来源、处理过程、分析方法、经核验的结果和局限性。不要提交个人隐私数据、导师项目原始资料、访问凭据或其他敏感文件。

## GitHub Pages 部署

仓库已配置 `.github/workflows/publish.yml`。推送到 `main` 后，工作流会安装 Quarto、生成 `docs/` 并部署到 GitHub Pages。

首次部署前，在 GitHub 仓库中进入 **Settings → Pages**，将 **Source** 设置为 **GitHub Actions**。如果工作流无法部署，请检查仓库 Actions 是否启用，以及当前账号是否具有 Pages 管理权限。

## 内容状态

已有项目页面只记录当前已确认的信息。数据来源、样本范围、模型结果、图表与成果指标将在核验并确认可公开后补充；规划项目不会预设结果。
