# 苏米官网 · GitHub Pages

网站域名：`sumi.ppxdesign.icu`

这是可直接部署的静态官网。`index.html` 位于仓库根目录，CSS、JavaScript 与图片均为相对路径。

## GitHub 设置

1. 将本目录的全部内容上传到 `akumazza/sumi-website` 仓库的 `main` 分支根目录。
2. 仓库 Settings → Pages → Source 选择 **Deploy from a branch**。
3. Branch 选择 **main**，文件夹选择 **/ (root)**，保存。
4. Custom domain 填写 **sumi.ppxdesign.icu**，保存。
5. 域名检查和证书签发完成后启用 **Enforce HTTPS**。

`CNAME` 文件已指定域名。`.nojekyll` 用于直接提供静态文件。GitHub 设置中仍应确认 Custom domain 一栏已保存。

## 腾讯云 DNSPod

在腾讯云 DNSPod 的 `ppxdesign.icu` 记录管理中只新增一条：

- 主机记录：`sumi`
- 记录类型：`CNAME`
- 线路：`默认`
- 记录值：`akumazza.github.io`
- TTL：`600` 秒（或控制台默认值）

记录值不要附带仓库名称、https:// 或路径。

用户已确认：`ppxdesign.icu` 上的「裴小勇 — 视觉与三维设计」作品集继续保留。不要修改根域名 `@`、`www`、现有作品集仓库或其他记录。

请先在新网站的 GitHub Pages 设置中绑定 `sumi.ppxdesign.icu`，再添加这条解析。最终以 DNSPod 控制台和权威 DNS 的实时结果为准。

## 验证

打开 `https://sumi.ppxdesign.icu/`，检查首页、产品图片、场景切换、搜索和方案下载。确认 `https://ppxdesign.icu/` 仍展示原有作品集。DNS 缓存和 HTTPS 证书签发可能需要等待。

## 网站内容

Logo 由用户提供。产品资料和图片来自苏米原官网。家居氛围图为 AI 生成的设计示意。场景控制为网页演示；方案需求清单在浏览器本地生成，不会自动提交给公司。

## 官方参考

- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.dnspod.com/dns/a-record-zh/
