# 部署说明 / How to publish

这套主页用「**缩略图 + GitHub Pages**」实现首页可视化：首页 README 显示一张图，点击跳转到真正可交互的在线页面。GitHub 的 profile README 不能内嵌可执行的 HTML/JS，所以这是最小成本且标准的做法。

## 一、发布个人主页（profile README）

> ⚠️ GitHub 规则：**承载主页 README 的仓库名必须和你的 GitHub 用户名完全一致**。
> 你的用户名是 `chen-Zhang816`，所以仓库要叫 `chen-Zhang816`（不是 `zhangchen`）。
> 「主页显示的名字」可以另外在 GitHub 个人资料 Settings → Name 里改成你想要的。

1. 新建一个 **public** 仓库，命名为 `chen-Zhang816`。
2. 把本文件夹 `github-profile/` 里的内容（`README.md`、`README.zh-CN.md`、`assets/`）推上去：
   ```bash
   cd github-profile
   git init && git add . && git commit -m "profile homepage"
   git branch -M main
   git remote add origin https://github.com/chen-Zhang816/chen-Zhang816.git
   git push -u origin main
   ```
3. 打开 `https://github.com/chen-Zhang816` 即可看到主页。

## 二、上线 MuseGate 作品集（保持 HTML 原格式不变）

1. 新建 public 仓库 `musegate-portfolio`。
2. 推送本仓库 `musegate-portfolio/index.html`（即你的 portfolio，原样未改）：
   ```bash
   cd musegate-portfolio
   git init && git add . && git commit -m "musegate portfolio"
   git branch -M main
   git remote add origin https://github.com/chen-Zhang816/musegate-portfolio.git
   git push -u origin main
   ```
3. 仓库 **Settings → Pages → Source 选 `main` / `(root)`** → Save。
4. 约 1 分钟后访问 `https://chen-zhang816.github.io/musegate-portfolio/`，主页缩略图就会指向这里。

## 三、Echo Story（semantic-map）—— 已就绪 ✅

`chen-Zhang816/semantic-map` 的 Pages 已上线：
`https://chen-zhang816.github.io/semantic-map/` （含 3D 语义地图、主题网络、数据集下载）。
主页缩略图已直接指向它，无需额外操作。

## 缩略图说明

- `assets/musegate-cover.png` —— MuseGate 作品集封面截图
- `assets/semantic-map-3d.png` —— 3D 语义地图实时截图
- 想让缩略图「动起来」（鼠标拖动旋转 3D 地图的录屏 GIF）效果更好，可以后续替换为 GIF，README 里的引用路径不用改。
