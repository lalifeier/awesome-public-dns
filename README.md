# 🌍 Awesome Public DNS

📖 **全球公共 DNS 服务器合集，提供 iOS/macOS 描述文件 (`.mobileconfig`) 便捷配置。**

---

## ⚠️ 注意事项

🔹 **DoH3 性能优于 DoT**
谷歌的[官方文章](https://security.googleblog.com/2022/07/dns-over-http3-in-android.html)指出，在支持 HTTP/3 的设备上，DNS over HTTP/3 (DoH3) 比 DoT 表现更佳。

🔹 **iOS/macOS 的加密 DNS 限制**
自 iOS/iPadOS 15.5 起，苹果优化了公共 Wi-Fi（如咖啡厅、机场）的[强制登录门户](https://zh.wikipedia.org/wiki/%E5%BC%BA%E5%88%B6%E9%97%A8%E6%88%B7)，加密 DNS 规则有所调整。然而，仍存在一些限制，苹果尚未修复：

- **无法启用加密 DNS**：
  - [Little Snitch & Lulu](https://github.com/paulmillr/encrypted-dns/issues/13)
  - [VPN 连接](https://github.com/paulmillr/encrypted-dns/issues/18)
- **部分流量绕过加密 DNS**：
  - [终端和 App Store](https://github.com/paulmillr/encrypted-dns/issues/22)
  - [Chrome 浏览器](https://github.com/paulmillr/encrypted-dns/issues/19)

🔹 **进一步的隐私保护**
如果你希望获得更高级的隐私防护，可参考 [基于 Tor 网络的加密 DNS](https://github.com/alecmuffett/dohot)。

## 📌 公共 DNS 列表

### 🇨🇳 中国公共 DNS

以下是中国大陆可用的公共 DNS 服务器，适用于加速国内网站访问。

| 提供商 | IPv4 地址 | IPv6 地址 | DoH 地址 | DoT 地址 | 备注 |
| ----------------------------------- | ------------------- | ---------------------- | --------------------------- | ------------------------------ | ------------------------- |
| [阿里 DNS](https://www.alidns.com/) | 223.5.5.5<br />223.6.6.6 | 2400:3200::1<br />2400:3200:baba::1 | `https://dns.alidns.com/dns-query`<br />`https://223.5.5.5/dns-query`<br />`https://223.6.6.6/dns-query`<br />`https://2400:3200::1/dns-query`<br />`https://2400:3200:baba::1/dns-query` | `dns.alidns.com` | - |
| [腾讯 DNS](https://www.dnspod.cn/Products/Public.DNS) | 119.29.29.29<br />182.254.116.116<br />119.28.28.28<br />182.254.118.118 | 2402:4e00:: | `https://doh.pub/dns-query`<br />`https://1.12.12.12/dns-query`<br />`https://120.53.53.53/dns-query` | `dot.pub`<br />`1.12.12.12`<br />`120.53.53.53` | - |
| [360 DNS](https://sdns.360.net/index.html) | 101.226.4.6<br />218.30.118.6 | - | `https://doh.360.cn` | dot.360.cn | - |
| [114 DNS](http://www.114dns.com/) | 114.114.114.114<br />114.114.115.115 | - | ❎ | ❎ | - |
| [百度 DNS](https://dudns.baidu.com/) | 180.76.76.76 | 2400:da00::6666 | ❎ | ❎ | - |
| 字节跳动火山引擎 DNS | 180.184.1.1<br />180.184.2.2 | - | ❎ | ❎ | - |
### 🌎 全球公共 DNS

以下是全球通用的公共 DNS 服务器，适用于加速国际网站访问。

| 提供商 | IPv4 地址 | IPv6 地址 | DoH 地址 | DoT 地址 | 备注 |
| ----------------------------------- | ------------------- | ---------------------- | --------------------------- | ------------------------------ | ------------------------- |
| [Google Public DNS](https://developers.google.com/speed/publics) | 8.8.8.8<br />8.8.4.4 | 2001:4860:4860::8888<br />2001:4860:4860::8844 | `https://dns.google/dns-query`<br />`https://8.8.8.8/dns-query`<br />`https://8.8.4.4/dns-query`<br />`https://[2001:4860:4860::8888]/dns-query`<br />`https://[2001:4860:4860::8844]/dns-query`<br />`https://[2001:4860:4860::64]/dns-query`<br />`https://[2001:4860:4860::6464]/dns-query` | `dns.google` | 高速、可靠的DNS服务 |
| [Cloudflare DNS](https://developers.cloudflare.com/1.1.1.1/) | 1.1.1.1<br />1.0.0.1 | 2606:4700:4700::1111<br />2606:4700:4700::1001 | `https://cloudflares.com/dns-query`<br />`https://1.1.1.1/dns-query`<br />`https://1.0.0.1/dns-query`<br />`https://[2606:4700:4700::1111]/dns-query`<br />`https://[2606:4700:4700::1001]/dns-query`<br />`https://[2606:4700:4700::64]/dns-query`<br />`https://[2606:4700:4700::6464]/dns-query` | `one.one.one.one`<br />`1dot1dot1dot1.cloudflares.com` | 强调隐私和安全 |
| [OpenDNS](https://www.opendns.com/) | 208.67.222.222<br />208.67.220.220 | 2620:119:35::35<br />2620:119:53::53 | `https://doh.opendns.com/dns-query` | `doh.opendns.com` | 具有内容过滤功能 |
| [Quad9](https://www.quad9.net/) | 9.9.9.9<br />149.112.112.112 | 2620:fe::fe<br />2620:fe::fe:9 | `https://dns.quad9.net/dns-query` | `dns.quad9.net` | 集成安全过滤功能 |
| [Quad101](https://101.101.101.101/) | 101.101.101.101<br />101.102.103.104 | 2001:de4::101<br />2001:de4::102 | `https://dns.twnic.tw/dns-query`<br />`https://101.101.101.101/dns-query` | 101.101.101.101<br />`dns.twnic.tw` | 台湾网络资讯中心公共 DNS |
###  🚫 去广告 DNS

以下是提供广告拦截功能的公共 DNS 服务器，可用于屏蔽网页广告、跟踪器和恶意网站。

| 提供商 | IPv4 地址 | IPv6 地址 | DoH 地址 | DoT 地址 | 备注 |
| ----------------------------------- | ------------------- | ---------------------- | --------------------------- | ------------------------------ | ------------------------- |
| [18bit DNS](https://18bit.cn/) | - | - | `https://doh.18bit.cn/dns-query` | `dns.18bit.cn` | 提供广告过滤功能 |
| [AdGuard DNS](https://adguard.com/en/adguards/overview.html) | 94.140.14.14<br />94.140.15.15 | 2a0d:2a00:1::<br />2a0d:2a00:2:: | `https://dns.adguard.com/dns-query` | `dns.adguard.com` | 提供广告过滤和隐私保护功能 |
| [NextDNS](https://nextdns.io/) | - | - | `https://dns.nextdns.io/{id}` | `dot.nextdns.io` | 自定义过滤规则，支持广告拦截 |
| [OpenDNS FamilyShield](https://www.opendns.com/setupguide/#familyshield) | 208.67.222.123<br />208.67.220.123 | - | `https://doh.familyshield.opendns.com/dns-query` | `familyshield.opendns.com` | 提供广告和恶意软件过滤功能 |
| [CleanBrowsing](https://cleanbrowsing.org/) | 185.228.168.9<br />185.228.169.9 | - | `https://dns.cleanbrowsing.org/dns-query` | `dns.cleanbrowsing.org` | 提供广告和恶意软件过滤功能 |


## 📜 iOS/macOS 描述文件

| 提供商 | 备注 | DoH | DoT | 安装链接 |
| ------ | ---- | ---- | ---- | -------- |
| Ali DNS | 阿里云公共 DNS | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/aliyun.mobileconfig) |
| DNSPod | 腾讯旗下 DNS | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/dnspod.mobileconfig) |
| 360 Secure DNS | 360 安全DNS | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/360.mobileconfig) |
| Google DNS | 全球通用，高稳定性 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/google.mobileconfig) |
| Cloudflare DNS | 1.1.1.1，隐私保护强 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/cloudflare.mobileconfig) |
| Quad9 | 强调安全性，拦截恶意网站 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/quad9.mobileconfig) |
| Quad101 | 台湾 TWNIC 提供，去广告 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/quad101.mobileconfig) |
| AdGuard | 强力去广告，保护隐私 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/adguard.mobileconfig) |
| CleanBrowsing | 适合家长控制，过滤成人内容 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/CleanBrowsing.mobileconfig) |
| OpenDNS | 思科旗下 DNS，可定制过滤规则 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/opendns.mobileconfig) |
| 18Bit | 去广告 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/18bit.mobileconfig) |
| EasyMosdns | 去广告 | ✅ | ❎ | [安装描述文件](https://lalifeier.github.io/dns/profiles/easyMosdns.mobileconfig) |
| 清风云 DNS | 去广告 | ✅ | ✅ | [安装描述文件](https://lalifeier.github.io/dns/profiles/ipv4dns.mobileconfig) |

### 📱 iOS / iPadOS
1. **使用 Safari 浏览器**（⚠ 其他浏览器仅会下载文件，不会弹出安装提示）打开 GitHub 上的 `.mobileconfig` 文件。
2. 点击 **“允许”** 按钮，完成描述文件下载。
3. 打开 **“设置” → “通用” → “VPN、DNS 与设备管理”**。
4. 选择已下载的描述文件，点击 **“安装”** 并按照提示完成设置。

---

### 💻 macOS（[官方文档](https://support.apple.com/zh-cn/guide/mac-help/mchl54d25c17/mac)）
1. 下载并保存 `.mobileconfig` 文件，**确保文件扩展名为 `.mobileconfig`，而不是 `.txt` 等其他格式**。
2. **打开“系统设置”**（ 苹果菜单 → “系统设置”）。
3. 在左侧边栏选择 **“隐私与安全性”**，然后在右侧找到 **“描述文件”**（可能需要向下滚动）。
4. 在 **“已下载”** 部分，**双击** 描述文件。
5. 查看描述文件内容后，点击 **“继续” → “安装”**（安装过程中可能需要输入密码）。
6. **如果 Mac 上已有旧版本的描述文件**，新的描述文件将自动覆盖旧的设置。

---

## 📝 创建新描述文件

你可以使用这个[工具](https://dns.notjakob.com/tool.html)在线创建你自己的描述文件。

描述文件本质上是 XML 文本文件，如果你有兴趣提交新的描述文件，将现有的描述文件复制一份并修改其 UUID 即可，请确保在本 README 文件中更新描述文件的相关信息。

随机 UUID 除了可以通过网站在线生成，还有很多其他获取方法：

- 在浏览器中按下 `F12` 打开“开发人员工具”，在控制台中运行这段代码

```javascript
crypto.randomUUID();
```

- 在 macOS / Linux 终端中运行此命令

```sh
# 适用于 macOS 和 Linux
uuidgen

# 适用于 Linux
cat /proc/sys/kernel/random/uuid
```

- 在 Powershell 中运行此命令

```powershell
New-Guid
```

## 🔗 相关资源

- [DNS 提供商](https://adguards.io/kb/general/dns-providers/)
- [Cloudflare DNS](https://developers.cloudflare.com/1.1.1.1/)
- [Google Public DNS](https://developers.google.com/speed/publics/docs/using?hl=zh-cn)
- [Quad9 DNS](https://docs.quad9.net/services/)
- [OpenDNS](https://www.opendns.com/)

## 🙌 特别感谢

本项目参考并借鉴了以下优秀的开源项目，在此表示感谢：

- [rockyou/dns-mobileconfig](https://github.com/rockyou/dns-mobileconfig)
- [paulmillr/encrypted-dns](https://github.com/paulmillr/encrypted-dns)
- [bamf2077/secure-dns](https://github.com/bamf2077/secure-dns)

## 📢 欢迎贡献！

如果你发现了新的 DNS 服务器或有更好的 `.mobileconfig` 描述文件，欢迎提交 PR！💡 让我们一起优化 DNS 体验！ 🚀
