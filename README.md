# 生词大师 · 全功能测验版

一个支持 **Excel/JSON/CSV 导入、错题本、连对隐藏、手机/电脑两用** 的 4 选 1 词汇测验网页。  
> 在线演示地址（开通 GitHub Pages 后替换）：https://<YOUR_USERNAME>.github.io/<YOUR_REPO>/

---

## 一、如何注册 GitHub（没有用户名的同学先看这里）
1. 打开 https://github.com 注册账号。
2. 选择一个 **用户名（username）**，将出现在你的个人主页 URL 和 Pages 域名里（建议简短、好记）。
3. 注册完成后，登录到 GitHub。

---

## 二、如何部署到 GitHub Pages（永久免费）
> 只需上传一个 `index.html`，几分钟就能上线。

1. **创建仓库**
   - 右上角 **New repository**
   - 仓库名：`<YOUR_REPO>`（例如 `vocab-quiz`）
   - 选择 **Public** → 点击 **Create repository**

2. **上传文件**
   - 进入仓库 → **Add file → Upload files**
   - 上传 `index.html`（本仓库已附带），然后点击 **Commit changes**

3. **开启 GitHub Pages**
   - 进入仓库 **Settings → Pages**
   - **Source** 选择 **Deploy from a branch**
   - **Branch** 选择 `main`，**Folder** 选择 `/ (root)` → **Save**
   - 等待 1–2 分钟，页面会显示你的网站地址：  
     `https://<YOUR_USERNAME>.github.io/<YOUR_REPO>/`

4. **添加到手机主屏（可选）**
   - iPhone（Safari）：分享按钮 → **添加到主屏幕**
   - Android（Chrome）：右上角菜单 → **添加到主屏幕**

---

## 三、电脑上传生词 → 手机做题（推荐流程）
1. 在**电脑端**打开网站或本地 HTML：导入你的 Excel（需包含列：单词、词性、中文含义、例句/来源可选）。
2. 点击 **“导出题库（JSON）”**，下载 `vocab-quiz-dataset.json`。
3. 在**手机端**打开网站 → 点击 **“粘贴导入（JSON/CSV）”**，将 `vocab-quiz-dataset.json` 的内容复制进去即可。

> 进度与错题本使用 **localStorage** 保存在浏览器本地：同一设备同一浏览器会自动记住；清理浏览器数据或更换设备会丢失。

---

## 四、功能亮点
- 4 选 1 随机出题，**同词性干扰项**优先，选项不明显
- **选对：绿色加粗**；**选错：错误项红色 + 正确项绿色加粗**
- **错题本**统计与排序；**连对达到阈值**可自动隐藏该词
- **支持导入**：Excel（.xlsx）/ JSON / CSV
- **导出进度**（错误/连对/次数等）与 **导出题库（JSON）**
- 手机端优化：更大点按区域、无高亮、手感流畅

---

## 五、题库模板（Excel 列名建议）
- `word`（或 “单词”）
- `pos`（或 “词性”）
- `meaning`（或 “中文含义（句子中）/中文含义/释义”）
- `example`（或 “原文引用/例句/PPT中原文引用（生词加粗）”）
- `source`（或 “来源”）

> 不同列名也可自动识别，以上是建议名称。

---

## 六、常见问题（FAQ）
**Q：我在手机上只有一个 HTML 文件，怎么打开？**  
A：用浏览器打开即可（iPhone “文件”里长按 → 共享 → Safari；Android 选择 Chrome）。打开一次后，建议 **添加到主屏幕**。

**Q：会记住我上次做题的错题和进度吗？**  
A：会，只要是同一设备同一浏览器。换设备或清除浏览器数据会丢失。

**Q：想跨设备同步错题？**  
A：可接入 Firebase / Supabase（有免费额度），实现登录与云端同步。

---

## 七、更新方法
- 直接在 GitHub 仓库网页里 **Upload files** 覆盖 `index.html` 即可，几秒后自动生效。

---

## Screenshot（可替换）
> 在此处放几张使用截图，或一张动图（GIF）。

---

## License
本项目仅供个人学习与使用，禁止商业用途。如需二次开发，请注明来源。
