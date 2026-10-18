# Vultr评测：$2.5起的真实价格、国内访问速度和换IP机制，先看这几条再充值

Vultr 在几乎所有“便宜 VPS”的榜单里都会出现，结论可以先放这里：它适合愿意自己动手的开发者和折腾型用户——价格低、机房多、按小时计费、支持支付宝付款；但它全线是普通线路，国内访问速度一般，也不提供任何托管运维。如果你想要的是“开机就能用的建站主机”，这篇文章的后半段会告诉你为什么它可能不适合你。

> **选购速览**：绝大多数个人用户选 Cloud Compute Regular 的 **$5/月**档（1核 1GB 内存、25GB SSD、1TB 月流量）就够了；建站或跑数据库，加 1 美元上主频更高的 High Frequency；想先试再决定的，注册能领最高 **$300 试用金**，按小时扣费，删了就停。👉 [查看 Vultr 当前套餐与试用金活动](https://www.vultr.com/pricing/?ref=7268283)

## Vultr 到底是个什么商家

一句话：美国的 IaaS 云服务商，由 The Constant Company 运营，Vultr 品牌在 2014 年上线（母公司的历史可以追溯到 2008 年），官方称已部署超过 4500 万台云服务器，覆盖六大洲 32 个地区。

产品线比一般 VPS 商家宽：除了 Cloud Compute（也就是大家常说的 VPS），还有专用 vCPU 的 Optimized Cloud Compute、裸金属服务器、Cloud GPU、托管数据库、对象存储和 Kubernetes 等。不过对个人用户来说，95% 的场景只需要关心 Cloud Compute 这一条线。

定位上它是 IaaS，给你一台干净的机器，系统安装、Web 环境、安全补丁、备份全都自己管。英文测评把这个边界划得很清楚：Vultr 只负责基础设施层，往上的每一层都是用户自己的责任。这直接决定了后面所有优缺点的走向。

## 价格与套餐：先分清 Regular、High Performance、High Frequency

入门价 **$2.50/月**起，但注意这是 IPv6-only 档；带独立 IPv4 的最低 $3.50/月，主流的 1核 1GB 档是 $5/月。三条产品线的区别用一句话说清：Regular 最便宜，用上一代 Intel CPU 和普通 SSD；High Performance 换成新一代 AMD EPYC 或 Intel Xeon 加 NVMe 硬盘；High Frequency 主打 3GHz+ 的高主频 CPU 加 NVMe，价格一般比同规格贵 1 美元左右。

"High Performance"和"High Frequency"名字很像，意思不一样：前者给你更新的硬件，后者给你更高的时钟频率。WordPress、Node API、游戏服这类单线程负载，High Frequency 占优；多线程吞吐场景，High Performance 同规格有时还更便宜。

### Cloud Compute Regular 全部档位

| 套餐 | vCPU / 内存 / 存储 | 月流量 | 月价 | 购买 |
| --- | --- | --- | --- | --- |
| Regular（仅IPv6） | 1核 / 0.5GB / 10GB | 0.5TB | $2.50 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular | 1核 / 0.5GB / 10GB | 0.5TB | $3.50 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 1GB | 1核 / 1GB / 25GB | 1TB | $5 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 2GB | 1核 / 2GB / 55GB | 2TB | $10 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 2GB | 2核 / 2GB / 65GB | 3TB | $15 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 4GB | 2核 / 4GB / 80GB | 3TB | $20 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 8GB | 4核 / 8GB / 160GB | 4TB | $40 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 16GB | 6核 / 16GB / 320GB | 5TB | $80 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 32GB | 8核 / 32GB / 640GB | 6TB | $160 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 64GB | 16核 / 64GB / 1280GB | 10TB | $320 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular 96GB | 24核 / 96GB / 1600GB | 15TB | $640 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |

那份 $2.50 的套餐提醒一句：它没有 IPv4 地址，而国内绝大部分网络环境没法直连 IPv6，为了省 1 美元选它基本等于买了个用不了的服务。实际入口是 $3.50 的 0.5GB 档或 $5 的 1GB 档。

### High Performance 常用档位

| 套餐 | vCPU / 内存 / 存储（NVMe） | 月流量 | 月价 | 购买 |
| --- | --- | --- | --- | --- |
| HP 1GB | 1核 / 1GB / 25GB | 2TB | $6 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| HP 2GB | 1核 / 2GB / 50GB | 3TB | $12 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| HP 2GB双核 | 2核 / 2GB / 60GB | 4TB | $18 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| HP 4GB | 2核 / 4GB / 100GB | 5TB | $24 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| HP 8GB | 4核 / 8GB / 180GB | 6TB | $48 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| HP 12GB | 4核 / 12GB / 260GB | 7TB | $72 | [ 购买](https://www.vultr.com/products/cloud-compute/?ref=7268283) |

官网价格页上 High Performance 还有内存更大的档位，High Frequency 的完整档位表也可以在那里查到。👉 [查看 Vultr Cloud Compute 全部档位价格](https://www.vultr.com/products/cloud-compute/?ref=7268283)

### 共享型之外的选项

Regular 和 High Performance 都是共享 vCPU，同物理机上的其他租户吃满 CPU 时你会受影响——英文评测在持续负载测试里确实记录到标准型比专用 CPU 型波动大。对延迟和稳定性敏感的生产服务，要么上 High Frequency，要么直接看 Optimized Cloud Compute（专用 vCPU）和裸金属。裸金属的选择面不大且经常缺货，中文测评记录过 2核 8GB 的独立服务器套餐 $60/月，具体以官网现价为准。

## 按小时计费和“免费换IP”的真实玩法

Vultr 按小时计费，费率是月价的 1/730——$5 的套餐约等于每小时 $0.007，开一周只付一周的钱，把实例删掉计费立刻停止。账户需要先充值，最低 $10，之后创建任意数量的实例都从余额里按小时扣。

很多人冲着“免费换 IP”来，这里说清楚它的机制：所谓免费换 IP，就是销毁当前实例（停止计费）再重新部署一台，新机器会分配新 IP，可以顺便换机房，全程不额外收费。

两个坑要提前知道。一是销毁即清空，磁盘数据一个字节都不剩，换 IP 前先用控制台自带的快照功能备份，重建后再恢复——控制台还有重装系统、防火墙、备份这些常用功能，都免费可用。二是 Vultr 的 IP 库不算大，因为换 IP 太自由，历史上有不少 IP 段被滥用到国内访问不通，你重建之后也可能分到被墙的 IP，有时候得多销毁重建几次。

> 实用建议：先用最低档测试目标机房的 IP 和速度，跑几天没问题再升级配置。👉 [注册 Vultr 领取新用户试用金](https://bit.ly/VulTR)

## 国内访问速度：把预期放低一点

Vultr 全线普通线路，没有针对中国优化，国内访问速度就是“能用但一般”的水平，晚高峰国际带宽拥堵时丢包比较常见。这不是它一家的问题，但选它之前得接受这个现实。

机房选择上，中文主机测评的结论是西雅图、硅谷、洛杉矶、东京这几个点对国内相对快。官方机房覆盖六大洲 32 个地区，北美有西雅图、硅谷、洛杉矶、达拉斯、芝加哥、新泽西、亚特兰大、迈阿密，欧洲有伦敦、巴黎、法兰克福、阿姆斯特丹，亚洲有东京、新加坡、首尔，大洋洲有悉尼，另外还有孟买、多伦多等节点——不同评测统计口径从 11 到 20 多个不等，统计的是数据中心还是网络节点有差异。

选机房的简单规则：主要给国内用户访问，选美西（洛杉矶、硅谷、西雅图）或东京；面向东南亚选新加坡；用户在欧美就选纽约、法兰克福这类近点。实际速度因运营商和时段差异很大，先开一台测速再决定是最稳妥的做法。

性能数据方面，一家做了 12 个月连续监测的英文评测记录到：纽约机房在无 CDN、无缓存的情况下 TTFB 平均 145ms（伦敦 185ms、悉尼 240ms），在线率 99.95%；另一家评测的中位数 TTFB 是 217ms，30 天在线率 100%。压力测试里 100 并发时响应退化约 31%，500 并发时退化到 162%——说明标准共享型在高并发下会明显到瓶颈，生产环境别指望 $5 套餐扛流量。👉 [查看 Vultr 全部机房与当前价格](https://www.vultr.com/pricing/?ref=7268283)

## 第三方评测的口碑分布

各家评分口径不同，但指向一致：基础设施强，服务弱。HostingTweaks 给出综合 76/100，其中性能 99、可靠性 100，但支持只有 50、易用性相关项也偏低；VPSVerdict 打了 9.1/10，称赞它 32+ 地区的覆盖和快速部署，同时指出标准型存在邻居干扰、支持达不到“管家级”；中文测评站同样给了 9.1 分。

售后以工单为主，基础设施类问题响应尚可，应用层的问题不管。有没有在线聊天不同评测记录不一，可以确定的是没有电话支持、没有 24/7 即时响应。出了问题基本靠自己的排障能力和官方知识库。

## 优点和缺点清单

**优点：**

- 起价低，$2.50/$5 档在同类大商家里有竞争力
- 按小时计费，随开随删，试错成本极低
- 机房多、分布广，换机房部署方便
- 销毁重建不收费，可“免费换 IP”
- 支持支付宝、微信、PayPal、信用卡付款
- 控制面板功能全：快照、备份、防火墙、重装都有

**缺点：**

- 普通线路，国内访问速度一般，晚高峰可能丢包
- 部分 IP 段已被墙，换 IP 可能要试几次
- 无托管服务、无邮件托管、无免费迁移，全靠自己
- Windows 加收 $10/月版权费，且要 2GB 内存以上套餐，最低 $20/月
- 客服只有工单，无即时响应

## 适合谁买，谁该绕开

适合的用户画像很清晰：会 Linux 基本操作的开发者，需要完整 root 权限和自定义环境的人；要在全球多地部署、用 API 批量管理实例的团队；想低成本多开小实例跑学习项目或 DevOps 练手的；以及需要频繁更换 IP 的用户。

该绕开的也不少。完全不懂命令行的 WordPress 用户，买回来只会卡在“连面板都没有”这一步——想要面板得自己装 cPanel，一个月还要多花 $15。需要邮件托管的别考虑，得自己配 Postfix 或者用外部服务。要 Windows VPS 的更不建议，加上 $10 版权费后最低 $20/月，中文测评明确建议这类需求去看 Hostwinds 这种性价比更高的 Windows 专门商家。期待一键建站、免费迁移、专人客服的，托管型主机才对路。

## 常见问题

**Vultr 能用支付宝充值吗？**
能。付款方式包括支付宝、微信、PayPal 和信用卡，最低充值 $10。

**新用户有试用金吗？**
有。目前官方推广活动是新用户最高 $300 试用金（早些年的常见活动是 $100），按小时扣费，具体以注册页面显示为准。

**Vultr 换 IP 真的不要钱吗？**
机制上不要钱：销毁实例停止计费，重新部署就分配新 IP。但数据会清空，记得先做快照；而且 IP 库有限，新 IP 也可能在国内不通。

**Vultr 和 DigitalOcean、Hetzner 比怎么选？**
搜索任何 cheap VPS 榜单，这三家基本都排在一起。英文评测给出的选择逻辑是：看重全球机房分布和自动化部署选 Vultr；单纯拼欧洲市场的每核价格，Hetzner 更有优势。三家都是 IaaS，运维负担差不多。

## 按用途给个最终建议

个人小项目和练手，选 $3.50 或 $5 的 Regular，先充 $10 按小时玩，不合适删掉就走。建站、跑数据库这类单线程敏感的应用，多花 1 美元上 High Frequency，主频和 NVMe 的提升是实打实的。跑生产服务、怕邻居干扰，直接看 Optimized 专用 vCPU。国内访问优先的场景，接受普通线路的现实，选美西或东京机房，IP 不通就销毁重建。至于 Windows、托管建站、要客服兜底这三种需求，Vultr 都不是对的答案，不必勉强。

下单前确认两件事：机房在部署时可以随时重选，选错了销毁重建就行；试用金也是按小时扣的，测试用的机器跑完记得及时销毁，别让闲置实例偷偷吃余额。👉 [用 Vultr 试用金先开一台，几小时就有答案](https://bit.ly/VulTR)
