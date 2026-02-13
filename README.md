# MoltNet Project Page

This repository contains the source for the **MoltNet** project website, in the style of [Nerfies](https://github.com/nerfies/nerfies.github.io).

---

## 如何发布出去（让别人 / 组内能看到）

### 方式一：公开页面（任何人通过链接都能看）

1. **在 GitHub 新建仓库**（可先选 Public）
   - 仓库名例如：`MoltNet_Project` 或 `moltnet-page`。
2. **把本地的 MoltNet_Project 推上去**（在终端执行）：
   ```bash
   cd /Users/chenhuang/Desktop/MoltNet_Project
   git init
   git add .
   git commit -m "Initial MoltNet project page"
   git branch -M main
   git remote add origin https://github.com/你的用户名/仓库名.git
   git push -u origin main
   ```
3. **开启 GitHub Pages**
   - 打开该仓库 → **Settings** → 左侧 **Pages**
   - **Build and deployment** 里 **Source** 选 **Deploy from a branch**
   - **Branch** 选 `main`，**Folder** 选 **/ (root)**，点 **Save**
   - 等 1～2 分钟，页面会出现在：
     - **项目页**：`https://你的用户名.github.io/仓库名/`  
     - 例如：`https://isakzhang.github.io/MoltNet_Project/`
4. 把上面的链接发给别人，对方用浏览器打开即可看到。

---

### 方式二：仓库设为 Private，仅组内看代码 + 共享页面链接

- **代码只给组内看**：仓库设为 **Private**，只把需要协作的人加为 **Collaborators**（仓库 **Settings** → **Collaborators**）。
- **页面发布方式不变**：Private 仓库也可以开 GitHub Pages，步骤同上（Settings → Pages → Deploy from branch → main / root）。
- **重要**：用 GitHub 免费账号时，即使用 Private 仓库，**发布出来的网页链接仍是公开的**（任何人拿到链接都能打开）。  
  **“仅组内看”的做法**：不对外公开这个链接，只把 `https://你的用户名.github.io/仓库名/` 发给组内成员；不分享链接的人就看不到。
- 若需要**必须登录或密码才能看页面**，需要用别的服务（例如 Vercel/Netlify 的密码保护、或 GitHub Enterprise 的 private Pages），本仓库目前按「仅分享链接给组内」即可。

---

## 部署为 GitHub Pages（步骤小结）

1. **在 GitHub 上创建仓库**
   - 仓库名建议：`你的用户名.github.io`（个人主页）或 `MoltNet_Project`（项目页）。
   - 若用项目页：部署后地址为 `https://你的用户名.github.io/MoltNet_Project/`。

2. **推送本目录到该仓库**
   ```bash
   cd /Users/chenhuang/Desktop/MoltNet_Project
   git init
   git add .
   git commit -m "Initial project page"
   git remote add origin https://github.com/你的用户名/仓库名.git
   git push -u origin main
   ```

3. **开启 GitHub Pages**
   - 仓库 → **Settings** → **Pages**
   - **Source** 选 **Deploy from a branch**
   - **Branch** 选 `main`，文件夹选 **/ (root)**，保存。
   - 几分钟后访问：`https://你的用户名.github.io/仓库名/`（若仓库名为 `用户名.github.io` 则根路径即可）。

## 本地预览

在项目根目录起一个简单 HTTP 服务即可：

```bash
cd /Users/chenhuang/Desktop/MoltNet_Project
python3 -m http.server 8000
```

浏览器打开：<http://localhost:8000>。

## 修改内容

- **标题、作者、摘要、链接**：编辑 `index.html` 中对应文字和 `href`。
- **视频**：在 `index.html` 里把 YouTube 嵌入链接中的 `YOUR_VIDEO_ID` 换成你的视频 ID。
- **图片**：将 teaser 图放到 `static/images/teaser.png`，结果图放到 `static/images/result1.png`、`result2.png` 等，并在 `index.html` 中引用。
- **样式**：修改 `static/css/style.css`。

## 引用

若 MoltNet 对您的工作有帮助，请引用：

```bibtex
@article{your2025moltnet,
  author  = {Author One and Author Two and Author Three},
  title   = {MoltNet: Your Project Title},
  journal = {Conference or Journal},
  year    = {2025},
}
```

## License

网站采用 [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)。模板参考 [Nerfies project page](https://github.com/nerfies/nerfies.github.io)。
