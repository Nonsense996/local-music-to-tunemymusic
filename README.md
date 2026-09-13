# 本地音乐 → TuneMyMusic 导入工具

一个纯网页小工具,帮你把本地音乐文件夹里的歌曲信息导出成 [TuneMyMusic](https://www.tunemymusic.com/) 能识别的文件,方便把本地音乐一键导入 Spotify(或其他流媒体平台)。

**在线使用:https://nonsense996.github.io/local-music-to-tunemymusic/**

## 特点

- 🔒 **全程本地处理**,音乐文件不会上传到任何服务器,标签解析完全在你的浏览器里完成
- 📁 支持整个文件夹递归扫描,自动识别子文件夹里的音乐
- 🎵 支持 MP3 / FLAC / M4A / WAV / OGG 五种常见格式
- ✅ 扫描完先预览,分别列出识别成功、标签缺失、解析失败的文件,心里有数再导出
- 📄 支持导出 CSV(推荐,匹配更准)或 TXT 两种格式
- 🚫 不依赖任何第三方 JS 库或 CDN,单文件运行,打开即用

## 怎么用

1. 打开上面的在线链接(推荐用 Chrome 浏览器)
2. 点击"选择音乐文件夹",选中你存放本地音乐的文件夹
3. 等待扫描完成,看一眼预览结果
4. 点击"下载 CSV"(或 TXT),把下载好的文件上传到 [tunemymusic.com](https://www.tunemymusic.com/),选择导入到 Spotify 即可

## 技术说明

标签读取部分是手写的二进制解析(ID3v2/ID3v1、Vorbis Comment、RIFF INFO、MP4 atom 结构),没有使用 music-metadata、jsmediatags 等第三方库,避免依赖不稳定的 CDN。

## 反馈

用起来有问题或者某些歌曲识别不出来,欢迎提 [Issue](../../issues)。
