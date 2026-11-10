单词桥 · 发布包说明
====================

这个文件夹里就是全部需要上传的内容，一共 5 个文件 + 4 张图标，不用改任何东西。

  index.html            ← 程序本体（改好的发布版）
  manifest.webmanifest  ← 让浏览器知道“这是个 App”（名字、图标、全屏打开）
  sw.js                 ← 离线缓存，装到桌面后断网也能打开
  icon-180 / 192 / 512 / 1024 .png  ← 桌面图标
  README.txt            ← 本说明，可以不传

—— 第一次上传（GitHub Pages）——
1. github.com 注册 → 右上 + → New repository → 名字随意（如 word-bridge）→ 选 Public → Create。
2. 点 “uploading an existing file”，把本文件夹里的所有文件一起拖进去（不要只拖 index.html）。
3. Commit changes。
4. Settings → Pages → Source 选 Deploy from a branch → Branch 选 main / (root) → Save。
5. 等 1–2 分钟，Pages 顶部出现 “Your site is live at https://用户名.github.io/word-bridge/” ，
   这个地址就是发给别人用的链接。

—— 以后每次更新 ——
1. 用新的 index.html 覆盖仓库里的 index.html（Add file → Upload files → 拖进去 → Commit）。
2. 顺手把 sw.js 里的 `const CACHE = 'wordbridge-1'` 改成 'wordbridge-2'（往后递增），
   否则已经“装到桌面”的设备可能还在用旧缓存。
3. 等 1 分钟左右，刷新页面即可。

—— 手机上“装成 App”——
· 安卓 / Chrome：打开链接 → 右上角菜单 → 安装应用 / 添加到主屏幕。
· iPhone / Safari：打开链接 → 分享 → 添加到主屏幕。
装好后桌面出现“单词桥”图标，点开是全屏，没有地址栏；装过一次后断网也能打开
（只是发音需要联网）。

—— 关于数据 ——
每个孩子的头像、桥、薄弱词、记录都存在“这台设备 + 这个浏览器”里，不上传。
家长中心 →「存档备份」可以导出 .json 文件，换设备或换浏览器时在那里导入恢复。
留意：微信里打开的页面和 Safari/Chrome 打开的页面是两个独立的存储，
建议固定一种打开方式（都用桌面图标最稳）。
