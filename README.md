# MetaCode · Discord Token 助手（dc-ex）

> Chrome 浏览器扩展：在你已登录的 Discord 网页上，读取**你自己**账号的 token 和已加入的服务器列表，方便粘贴到 [MetaCode](https://metacode.top/data/discord) 使用。
>
> *English: a Chrome extension for [MetaCode](https://metacode.top/data/discord) users. On the Discord web app you are logged in to, it shows your own account token and the servers you have joined, so you can paste the token into MetaCode. Download the zip from [Releases](../../releases).*

本仓库只发布打包好的扩展，不包含源码。

## 下载与安装

1. 到 [**Releases**](../../releases) 下载最新版本的 `.zip` 文件，**解压到一个固定的文件夹**（装好后不要删除或移动它）。
2. 在 Chrome 地址栏打开 `chrome://extensions`。
3. 打开右上角的「**开发者模式**」。
4. 点「**加载已解压的扩展程序**」，选择第 1 步解压出来的文件夹（里面直接能看到 `manifest.json`）。
5. 安装成功后，点工具栏的拼图图标，把「MetaCode · Discord Token 助手」固定到工具栏，用起来更方便。

Edge 等基于 Chromium 的浏览器步骤类似（地址是 `edge://extensions`）。

## 使用

1. 用浏览器打开 [Discord 网页版](https://discord.com/app)，并**登录你的账号**，停留在这个页面。
2. 点击工具栏里的扩展图标。
3. **首次使用**需要验证：输入你在 MetaCode 网站上使用的**钱包地址**（Discord 登录的用户填 `discord:` 开头的那串，和网站里显示的一致），点「确认」。已被开通「Discord 自动化」权限的用户会通过验证。
4. 通过后，弹窗里会显示这个账号的 token，点右边的按钮即可复制；下方列出这个账号加入的所有 Discord 服务器。
5. 把复制的 token 粘贴到 MetaCode 网站的账号库里使用。

之后每次点击扩展图标，都会自动用保存的地址重新验证一次；点弹窗底部的「切换账号」可以换一个地址。

## 隐私与安全

- **token 只在你自己的浏览器里显示，不会发送给 MetaCode，也不会发给任何第三方服务器。**
- 扩展只会访问两个地址：
  - `discord.com`：用你的 token 请求你自己的服务器列表；
  - `metacode.top`：把你输入的钱包地址发过去，查询它是否已开通权限。
- 钱包地址保存在扩展自己的本地存储里，不上传别处。
- **token 等同于你的账号密码。** 拿到它的人可以直接操作你的 Discord 账号，不要发给别人，不要贴到公开的地方。
- 钱包地址验证只是一个使用门槛，不是严格的身份认证。请不要把自己的钱包地址随便告诉别人。

## 常见问题

**提示「该地址没有使用权限」？**
请确认地址和你在 MetaCode 网站上使用的完全一致（建议直接从网站复制）；还没有开通 Discord 自动化权限的，请联系我们开通。

**提示「无法连接 MetaCode」？**
说明网络没通。检查网络或代理后重试，网络不通时扩展不会放行。

**弹窗里显示「未找到token字段」或没有 token？**
请确认当前标签页是**已登录**的 Discord 网页版（`discord.com/app`），不是登录页，也不是 Discord 桌面客户端；刷新页面后再点一次扩展图标。

**服务器列表显示获取失败？**
一般是 token 已失效，或者网络访问 Discord 有问题。重新登录 Discord 网页后再试。

**为什么提示「开发者模式」「已停用开发者模式的扩展」？**
这个扩展不是从 Chrome 应用商店安装的，所以是以开发者模式加载。Chrome 重启后可能弹出提示，选择保留即可。如果扩展被停用，到 `chrome://extensions` 重新启用。

**怎么更新？**
下载新版本的 zip，覆盖解压到原来的文件夹，然后在 `chrome://extensions` 里点这个扩展的「重新加载」按钮。

## 联系我们

使用中遇到问题，请通过 [MetaCode 网站](https://metacode.top) 上的联系方式找到我们。
