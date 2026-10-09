# 猫猫打罐罐 · 支持网站

纯静态网页，可直接部署到 GitHub Pages。无需 npm、构建或后台服务。支持页面和隐私政策无需 JavaScript 即可阅读。

## 文件

- `index.html`：支持页面、联系信息和常见问题。
- `privacy.html`：隐私政策，有独立 URL 方便填写 App Store Connect。
- `styles.css`：手机与桌面共用样式。
- `assets/app-icon.png`：现有游戏图标。
- `.nojekyll`：使用静态文件直接发布。

## 发布前填写

在两个 HTML 文件中替换全部 `[待填写支持邮箱]` 和 `[待填写开发者名称]`。

支持页的邮箱建议使用可点击链接，例如：

```html
<p class="email"><a href="mailto:你的真实邮箱">你的真实邮箱</a></p>
```

隐私页最后更新日期按实际发布日期调整。如最终游戏增加联网、SDK、广告或内购，先调整相应页面说明。

## 方式一：随当前项目上传

1. 将此 `docs` 文件夹整体保留在 GitHub 仓库根目录，推送到你的发布分支（通常是 `main`）。
2. 打开仓库 **Settings → Pages**。
3. 在 **Build and deployment → Source** 选择 **Deploy from a branch**。
4. **Branch** 选择上传文件所在分支，文件夹选择 **/docs**，点击 **Save**。
5. 等待部署完成，使用 Pages 页面显示的实际网址访问。

普通项目仓库的地址通常为：

```text
支持URL：https://你的GitHub用户名.github.io/仓库名/
隐私政策URL：https://你的GitHub用户名.github.io/仓库名/privacy.html
```

以 GitHub Pages 显示的实际网址为准；如使用用户名主页仓库或自定义域名，地址可能不同。

## 方式二：只上传网页

如果不需要上传游戏源代码，新建一个网页仓库，将此目录里的 `index.html`、`privacy.html`、`styles.css`、`assets/` 和 `.nojekyll` 上传到仓库根目录。

在 Pages 设置中选择对应分支与 **/(root)** 文件夹即可。

## 本地预览

在 `docs` 目录运行：

```sh
python3 -m http.server 8080
```

然后访问 `http://localhost:8080/`，隐私政策地址为 `http://localhost:8080/privacy.html`。结束预览时按 Ctrl+C。

## 官方参考

- [GitHub Pages 发布源配置](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Pages 数据收集说明](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection)
