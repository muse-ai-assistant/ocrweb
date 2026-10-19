# ocrweb 📷

> 🌐 **在线体验（手机/电脑都能用）: https://muse-ai-assistant.github.io/ocrweb/**
> 🌐 **Try online: https://muse-ai-assistant.github.io/ocrweb/**

Screenshot / photo → text, **100% on-device OCR** — your images never leave the browser.

截图 / 照片一键转文字，**纯本地识别、文件不上传**——银行卡、聊天记录这类敏感截图也能放心用。

## Why / 为什么做

Most online OCR tools upload your images to their servers. But screenshots are often bank cards, chat logs, ID photos — things you don't want leaving your device. ocrweb runs tesseract.js entirely in your browser: the image is processed locally, nothing is ever uploaded.

市面上的在线 OCR 都要把图片传到云端。可截图里多是银行卡、聊天记录、证件——这些东西谁想传出去？ocrweb 用 tesseract.js 在浏览器本地跑识别，图片不出设备。并且英文工具普遍不支持中文，这里中文 / English / 中英混合都能选。

## Features / 功能

- 🖼️ 4 ways to add an image / 4 种图片输入：drag & drop 拖拽、click to select 点击选择、paste with `Ctrl+V` 粘贴、camera on mobile 手机拍照
- 🌐 OCR language / 识别语言：中文 (chi_sim) / English (eng) / 中英混合
- 📊 Progress bar / 识别进度条，first-time language pack download notice / 首次语言包下载提示（chi_sim ~13 MB，之后浏览器缓存）
- 📝 Result actions / 结果操作：one-click copy 一键复制、download as `.txt` 下载、start over 清空重来
- 🌍 Bilingual UI (中文 / EN) / 中英双语界面，一键切换
- 📱 Mobile-first / 手机优先，拍照场景优化
- 🔒 No upload, no server, no tracking / 无上传、无服务器、无追踪

## Usage / 使用

No build, no install — just open `index.html` (or the GitHub Pages link above) and use it.

无需构建、无需安装——直接打开 `index.html`（或上面的在线链接）就能用。

1. Drop / select / paste / photograph an image 放入图片
2. Pick OCR language 选择识别语言
3. Hit "开始识别" and wait for the progress bar 点开始识别
4. Copy or download the text 复制或下载结果

Internet is needed on first use (tesseract.js + language pack load from CDN); after that the browser caches everything.

首次使用需要联网（从 CDN 加载 tesseract.js 和语言包），之后浏览器会自动缓存。

## Tech / 技术

- Single-file app: `index.html` only, zero build step
- [tesseract.js](https://github.com/naptha/tesseract.js) v5 via jsDelivr CDN, WebAssembly + Web Worker
- Trained data: `chi_sim` / `eng` (tessdata, `chi_sim+eng` for mixed)

## License / 许可

MIT
