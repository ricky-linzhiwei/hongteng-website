# 仙游县鸿腾财务咨询服务中心 · 静态官网

> 最低成本官网方案：纯静态 HTML/CSS/JS，零框架、零后端、零月费。按 GEO 诊断建议建设，内置 EEAT 内容与 FAQ 结构化数据，直接提升 AI 搜索可见度。

## 文件结构
```
hongteng-website/
├── index.html            # 主页面（含 LocalBusiness + FAQPage 结构化数据）
├── assets/
│   ├── css/style.css     # 样式（响应式，蓝金信任色）
│   └── js/main.js        # 移动端菜单交互
├── robots.txt            # 爬虫规则（上线前改域名）
├── sitemap.xml           # 站点地图（上线前改域名）
└── README.md
```

## 上线前必改项（3 处）
1. ~~**联系电话/微信**~~ ✅ 已填：统一热线 0594-8666880、微信/手机 18965579740（渠道变更时同步更新 `index.html` 与 JSON-LD）。
2. **客户评价**：`#reviews` 区块的 3 条见证为占位文案，请替换为**真实客户授权案例/实名评价**（EEAT 关键）。
3. **域名替换**：`robots.txt`、`sitemap.xml` 中的 `your-domain.example.com` 改为你的正式域名。
4. ~~**百度站长验证标签**~~ ✅ 已预埋：`<meta name="baidu-site-verification" content="【粘贴百度站长平台验证代码】">`，登录 ziyuan.baidu.com 添加网站后，把百度给的验证代码填进 content 即可。

## 最低成本部署方案

| 方案 | 托管 | 费用 | 适合 |
|---|---|---|---|
| A 免费预览 | GitHub Pages / Cloudflare Pages / Netlify | **0 元** | 先验证效果；国内访问偏慢，长期运营需备案 |
| B 国内合规（推荐） | 腾讯云/阿里云 对象存储(COS/OSS)+CDN + 域名 + ICP 备案 | **约 ¥150–260/年** | 合规国内官网，AI 与百度可正常抓取 |

**方案 B 成本拆解（年）**
- 域名：.cn ≈ ¥29，.com ≈ ¥60
- 对象存储+CDN（纯静态流量极小）：≈ ¥50–100
- ICP 备案：免费（需有国内接入，可绑一台轻量服务器 ¥60–100/年 同时满足备案与接入）
- 合计 ≈ **¥150–260/年**，即拥有合规、可被 AI 与搜索引擎正常收录的官网

> 备案提示：国内服务器/存储是备案接入前提；纯静态也可走 Cloudflare Pages（免费）+ 自定义域名，但若面向国内访客顺畅访问仍需国内备案接入。

## GEO / EEAT 已内置的优化
- `<title>` + `meta description` 含"仙游代理记账/公司注册/工商代办"本地意图词
- **LocalBusiness JSON-LD**：名称、成立时间、地址、TSC5级奖项、企查查/爱企查 sameAs
- **FAQPage JSON-LD**：10 条仙游本地意图问答，直接被 AI 搜索（DeepSeek/豆包/元宝等）引用
- 资质公示（代理记账许可号、TSC5级、双备案、信用代码、林志伟15年、10人团队）
- 语义化标题层级 + 移动端响应式

## 后续（配合 GEO 诊断建议）
- ✅ **15 篇仙游本地意图 EEAT 长文已发布**：见 `blog/` 目录与首页"财税科普"板块，全部含合法 FAQPage JSON-LD，直接喂给 AI 搜索。
- 每周在官网/公众号/百家号/知乎围绕 15 个本地意图问题持续更新，拉升 8 平台提及率。
- 补全企查查/爱企查词条字段，更新知乎陈旧信息。
- 部署后提交百度/必应收录，并用 15 问 × 8 平台看板月度监测 AIVO 变化。

## 百度收录操作（当前进度）
> 站点已部署在 GitHub Pages，线上地址：https://ricky-linzhiwei.github.io/hongteng-website/
> 百度/必应收录**必须由你本人用个人百度账号完成站点验证**（同 GitHub，我无法代为注册个人账号）。其余我已做好。

**你只需做 1 步：**
1. 浏览器打开 https://ziyuan.baidu.com/site （百度搜索资源平台 → 站点管理 → 添加网站）
2. 输入站点地址 `https://ricky-linzhiwei.github.io/hongteng-website/` → 选择"HTML 标签验证"
3. 复制百度给的 `content` 验证码（形如 `abcdefg123456`），发给我
4. 我把它填进 `index.html` 的 `baidu-site-verification` 标签并重新推送；你再在百度后台点"完成验证"

**验证通过后（我可代执行的）：**
- 站点地图提交：`sitemap.xml` 已在 https://ricky-linzhiwei.github.io/hongteng-website/sitemap.xml
- 主动推送：拿到百度"接口调用地址/站点 token"后，我可写脚本批量推送 URL 加速收录
- 必应收录：https://www.bing.com/webmasters 同样添加站点（支持 XML 提交）

> 注意：GitHub Pages 的 `github.io` 域名在国内访问偏慢，且不利于长期 SEO/GEO。建议按上面"方案 B"换国内合规域名+备案，百度收录与 AI 抓取会更稳。
