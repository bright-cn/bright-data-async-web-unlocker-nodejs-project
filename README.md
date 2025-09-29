# Bright Data 异步 Web Unlocker Node.js 项目

[![Bright Data Promo](https://github.com/bright-cn/LinkedIn-Scraper/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://www.bright.cn/)

<a href="https://github.com/bright-cn/bright-data-async-web-unlocker-nodejs-project?file=index.js" target="_blank">在 CodeSandbox 打开</a>，使用 GitHub 登录，然后 fork 该仓库开始修改。

## Bright Data 异步 Web Unlocker API 示例

此项目演示如何使用 Bright Data 的异步 [Unlocker API](https://www.bright.cn/products/web-unlocker) 通过 [Bright Data Unlocker API](https://www.bright.cn/products/web-unlocker) 访问带有反爬或验证码保护的网站。

## 概述

该脚本借助 Bright Data 的 Web Unlocker 自动绕过反爬与验证码，帮助你顺利访问目标网站内容。

### 在 StackBlitz 中使用环境变量

1. 选择 `.env` 文件  
2. 添加如下变量：
   - `BRIGHT_DATA_API_TOKEN`：你的 Bright Data [API Token](https://docs.brightdata.com/general/account/api-token)
   - `BRIGHT_DATA_ZONE`：你的 Bright Data [Zone](https://www.bright.cn/cp/zones) 名称（如 `web_unlocker1`）

### 直接配置

或者，直接在脚本中编辑 CONFIG 对象：

```javascript
const CONFIG = {
  apiToken: process.env.BRIGHT_DATA_API_TOKEN || 'YOUR_API_TOKEN', // 替换为你的实际 Token
  zone: process.env.BRIGHT_DATA_ZONE || 'web_unlocker1',           // 替换为你的 Zone
  targetUrl: 'https://geo.brdtest.com/welcome.txt'                 // 替换为你的目标 URL
};
```

## 运行示例

1. 确认已配置好 `API token` 与 `zone`
2. 在终端运行 `node index.js`
3. 在控制台查看结果输出

## 工作原理

1. 脚本向 Bright Data 的 Unlocker API 端点发起 POST 请求  
2. 请求中携带你的认证 Token 与目标 URL  
3. Bright Data 的 Web Unlocker 代表你访问目标 URL  
4. 响应返回至脚本，并在控制台显示

## 故障排查

若遇到错误：

- 检查 API Token 是否正确
- 确认 Zone 名称有效
- 确保目标 URL 格式正确

## 修改示例

如需请求其他 URL：
1. 更新 CONFIG 对象中的 `targetUrl`
2. 重新运行脚本

## 其他资源

- [Bright Data Web Unlocker API](https://docs.brightdata.com/scraping-automation/web-unlocker/introduction)
- [获取 API Token](https://docs.brightdata.com/general/account/api-token)
- [管理 Zones](https://www.bright.cn/cp/zones)

**说明：** 本示例用于学习演示。用于生产时，建议增加更完善的错误处理、日志记录与安全措施。
