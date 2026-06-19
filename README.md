# WaterKit Support · 技术支持站

WaterKit 的 App Store「技术支持网址」所用静态站。
纯静态 HTML + CSS，无依赖，托管在 GitHub Pages。

- **线上地址**：<https://jusuoli.github.io/WaterKit-support>
- **语言**：中文 / English（页面右上角切换）

## 页面结构

```
WaterKit-support/
├── index.html              # 支持首页（关于 / 联系 / FAQ / 隐私条款入口）
├── privacy-policy.html     # 隐私政策（中英双语）
├── terms.html              # 服务条款（中英双语）
├── assets/
│   └── app-icon.png        # App 图标（来自项目 AppIcon）
└── .github/workflows/
    └── deploy.yml          # 推送到 main 自动发布 Pages
```

## 部署方式

采用 GitHub Actions 部署（最稳定，不依赖本地 `gh-pages` 分支）：

1. 仓库 Settings → Pages → **Source = GitHub Actions**
2. 每次 push 到 `main`，`.github/workflows/deploy.yml` 会自动构建并发布。

## 本地预览

```bash
cd WaterKit-support
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 更新内容

- 改完 HTML 后 `git add . && git commit -m "update support" && git push`
- 等 Actions 跑完（约 30 秒），刷新线上地址即可。

## 同步 App 图标

```bash
cp ../DrinkingPanda/Resources/Assets.xcassets/AppIcon.appiconset/icon_1024.png assets/app-icon.png
```

---

© 2026 WaterKit · jusuoli
