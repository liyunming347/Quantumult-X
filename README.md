# 一、Quantumult X  自用资源汇总
---
[一个资源比较全的大佬Quantumult X资源库](https://github.com/deezertidal/QuantumultX-Rewrite?tab=readme-ov-file)

[loon插件发布资源地址,也适用Quantumult X](https://getupnote.com/share/notes/zSn1ShBmzNYISKcTgjXE5oHMrNf2/4a3b6152-3dd3-46da-b479-8c30ef6ef8d1)

---
## 1、Quantumult X 一些配置介绍。
**1、Quantumult X 策略组是什么？**
- 策略组可以实现 自动切换节点、节点筛选、是否走代理等。
- 策略组 需要配合 分流规则 使用。
- 策略组 可包含多个节点和策略组。

**2、Quantumult X 自带 3 种策略。**
- PROXY （代理）
- DIRECT（直连）
- REJECT（拒绝）

**3、Quantumult X 策略组类型。**
- static 静态策略-手动选择节点
- available 健康检查-自动选择节点，从第一个节点开始检查是否可用，直到选择可用节点。
- round-robin 负载均衡-轮询调度，轮流调用节点使用，IP可能会一直变。
- dest-hash 随即调整负载均衡
- url-latency-benchmark 自动测速-自动选择延迟低的节点

**4、Quantumult X 手动添加。**

在配置文件中的[general]下面添加以下内容

</span>

    用于节点延迟测试
    server_check_url=
    http://www.gstatic.com/generate_204
    #用于节点测试geo_location_checker=http://ip-api.com/json/?lang=zh-CN, https://raw.githubusercontent.com/I-am-R-E/Functional-Store-Hub/Master/GeoLocationChecker/QuantumultX/IP-API.js
    服务器测试超时时间 (毫秒)
    server_check_timeout = 3000
    功能强大的解析器，用于引用资源的转换resource_parser_url=https://cdn.jsdelivr.net/gh/KOP-XIAO/QuantumultX@master/Scripts/resource-parser.js
    下列路径将不经过QuanX的处理
    excluded_routes=239.255.255.250/32, 
    24.105.30.129/32, 185.60.112.157/32, 
    185.60.112.158/32, 182.162.132.1/32
    udp_whitelist=1-442, 444-65535

在配置文件中的[filter_remote]下粘贴以下内容

</span>

    FILTER_LAN, tag=LAN, force-
    policy=direct, enabled=true
    FILTER_REGION, tag=CN, force-
    policy=direct, enabled=true

## 2、Quantumult X 分流规则。
- Spotify分流 
</span>

    https://whatshub.top/rule/Spotify.list
- Copilot分流
</span>

    https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Microsoft/Microsoft.list
- 国际网络分流
</span>

    https://raw.githubusercontent.com/kjfx/QuantumultX/main/country/filter.list
- Twitter分流
</span>

    https://whatshub.top/rule/Twitter.list
- 国内媒体分流
</span>

    https://whatshub.top/rule/ChinaMedia.list
- YouTube Music分流
</span>

    https://whatshub.top/rule/YouTubeMusic.list
- YouTube分流
</span>

    https://whatshub.top/rule/YouTube.list
- 抖音IP分流
</span>

    https://raw.githubusercontent.com/im-dashan/proxy-plugin/main/loon/DouYin.list
- 抖音IP分流最新群友给的
</span>

    https://whatshub.top/rule/DouYin.list
- 微博分流
</span>

    https://whatshub.top/rule/Weibo.list
- 国内直连
</span>

    https://whatshub.top/rule/China.list
- Telegram分流
</span>

    https://whatshub.top/rule/Telegram.list
- ChatGPT分流
</span>

    https://whatshub.top/rule/ChatGPT.list

## 3、Quantumult X 重写资源。
- 小红书净化
</span>

    https://github.com/ddgksf2013/Rewrite/raw/master/AdBlock/XiaoHongShu.conf
- 喜马拉雅净化vip
</span>

    https://raw.githubusercontent.com/WeiGiegie/666/main/xmly.js
- 知乎净化
</span>

    https://gist.githubusercontent.com/ddgksf2013/d43179d848586d561dbb968dee93bae8/raw/zhihu.js
- 什么值得买净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/smzdm_remove_ads.plugin
- 酷安净化
</span>

    https://github.com/ddgksf2013/Scripts/raw/master/coolapk.js
- 百度网盘净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/BaiduNetDisk_remove_ads.plugin
- 阿里云盘净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/AliYunDrive_remove_ads.plugin
- 起点读书净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/QiDian_remove_ads.plugin
- 12406净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/12306_remove_ads.plugin
- 淘宝净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/Taobao_remove_ads.plugin
- 京东净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/JD_remove_ads.plugin
- 微博净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/Weibo_remove_ads.plugin
- YouTube净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/YouTube_remove_ads.plugin
- 百度地图净化
</span>

    https://gist.githubusercontent.com/ddgksf2013/beec132ca0c3570ffa0cf331bce8f82a/raw/baidumap.adblock.conf
- 高德地图净化
</span>

    https://github.com/ddgksf2013/Rewrite/raw/master/AdBlock/Amap.conf
-  Spotify净化
</span>

    https://gitlab.com/lodepuly/vpn_tool/-/raw/master/Tool/Loon/Plugin/Spotify_remove_ads.plugin
- vvwbo修复主页
</span>

    https://raw.githubusercontent.com/bin64/Scripts/main/QuantumultX/vvebo.js
- 最美证件照VIP
</span>

    https://raw.githubusercontent.com/WeiGiegie/666/main/zjzxg.js
- 喜马拉雅净化VIP
</span>

    https://raw.githubusercontent.com/WeiGiegie/666/main/xmly.js

- 山丘阅读VIP
</span>

    https://raw.githubusercontent.com/chxm1023/Rewrite/main/shanqiuyuedu.js
- 酷我音乐VIP
</span>

    https://raw.githubusercontent.com/Yuheng0101/X/main/Scripts/kuwo.js
- 酷我音乐净化
</span>

    https://napi.ltd/script/Worker/KuWo.js
- 读不舍手VIP
</span>

    https://gist.githubusercontent.com/ddgksf2013/dbb1695cd96743eef18f3fac5c6fe227/raw/revenuecat.js
- 山丘阅读VIP
</span>

    https://raw.githubusercontent.com/chxm1023/Rewrite/main/shanqiuyuedu.js

- 韩小圈VIP
</span>

    https://gist.githubusercontent.com/Yu9191/35453bcc1df1fd21febed34eb078c7e9/raw/Hanxiaoquan.sgmodules
- 驾考宝典微信小程序净化VIP
</span>

    https://raw.githubusercontent.com/Yu9191/Rewrite/main/kjzbd.js
