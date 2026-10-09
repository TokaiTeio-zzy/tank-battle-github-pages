# 坦克大战 · GitHub Pages 部署包

这是一个可直接部署到 GitHub Pages 的静态游戏站点。入口文件已命名为 `index.html`，无需构建步骤或外部依赖。

## 方式一：上传文件到 GitHub（适合新手）

1. 登录 GitHub，创建一个新仓库，例如 `tank-battle`。
2. 将本压缩包解压。
3. 将解压后文件夹里的**所有内容**上传到仓库根目录（要能直接看到 `index.html` 和 `.github` 文件夹）。
4. 打开仓库的 **Settings → Pages**。
5. 在 **Build and deployment → Source** 中选择 **GitHub Actions**。
6. 打开 **Actions** 标签页，等待 `Deploy Tank Battle to GitHub Pages` 工作流完成。
7. 回到 **Settings → Pages**，点击 **Visit site**。首次发布可能需要几分钟。

## 方式二：使用 Git 命令

在解压目录打开终端，执行（把 `YOUR-USERNAME` 和仓库名换成自己的）：

```bash
git init
git add .
git commit -m "Deploy Tank Battle game"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/tank-battle.git
git push -u origin main
```

然后在仓库的 **Settings → Pages** 中把 Source 设为 **GitHub Actions**。

## 游戏说明

- 电脑：方向键或 WASD 移动，空格开火，Esc 暂停。
- 手机：使用游戏页面上的触控按钮。
- 排行榜：当前为浏览器本地排行榜；不会跨设备或跨玩家同步。
- 游戏完全静态，不需要服务器、数据库、API 密钥或编译。

## 文件结构

```text
tank-battle-github-pages/
├── index.html
├── .nojekyll
├── README.md
└── .github/
    └── workflows/
        └── pages.yml
```

注意：GitHub Pages 网站通常是公开可访问的。发布前请确认仓库中没有私人信息。
