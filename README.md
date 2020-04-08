## QuantumultX-Tutorial

    建筑学的纯小白,学习QuantumultX的经历与总结的QuantumultX的教程

- 教程地址 : https://github.com/WyattIsaac/QuantumultX-Tutorial/wiki

## QuantumultX-官方配置文件
官方链接地址: https://github.com/crossutility/Quantumult-X/blob/master/sample.conf

![](https://tva1.sinaimg.cn/large/00831rSTgy1gdm6kjhtbrj30uz0u0tms.jpg)

### 第一部分 General

```
;server_check_url=http://www.google.com/generate_204
;geo_location_checker=http://www.example.com/json/, https://www.example.com/script.js
dns_exclusion_list=*.cmpassport.com, *.jegotrip.com.cn, *.icitymobile.mobi, id6.me
;ssid_suspended_list=LINK_22E174, LINK_22E175
;udp_whitelist=53, 123, 1900, 80-443
;excluded_routes= 192.168.0.0/16, 172.16.0.0/12, 100.64.0.0/10, 10.0.0.0/8
;icmp_auto_reply=true

```

### 第二部分 DNS

```
server=223.5.5.5
server=114.114.114.114
server=119.29.29.29
server=8.8.8.8
;server=8.8.4.4:53
;server=/example0.com/system
;server=/example1.com/8.8.4.4
;server=/*.example2.com/223.5.5.5
;server=/example4.com/[2001:4860:4860::8888]:53
;address=/example5.com/192.168.16.18
;address=/example6.com/[2001:8d3:8d3:8d3:8d3:8d3:8d3:8d3]

```

### 第三部分 Policy

```
;static=policy-name-1, Sample-A, Sample-B, Sample-C, img-url=http://example.com/icon.png
;available=policy-name-2, Sample-A, Sample-B, Sample-C
;round-robin=policy-name-3, Sample-A, Sample-B, Sample-C
;ssid=policy-name-4, Sample-A, Sample-B, LINK_22E171:Sample-B, LINK_22E172:Sample-C
```

### 第四部分 server_remote

```
[server_remote]
;https://raw.githubusercontent.com/crossutility/Quantumult-X/master/server.txt, tag=Sample-01
;https://raw.githubusercontent.com/crossutility/Quantumult-X/master/server-complete.txt, tag=Sample-02, as-policy=static, img-url=http://example.com/icon.png, enabled=false
```

### 第五部分 filter_remote

```
[filter_remote]
;https://raw.githubusercontent.com/crossutility/Quantumult-X/master/filter.txt, tag=Sample, force-policy=your-policy-name, enabled=true
```

### 第六部分 rewrite_remote

```
[rewrite_remote]
;https://raw.githubusercontent.com/crossutility/Quantumult-X/master/sample-import-rewrite.txt, tag=Sample, enabled=true
```

### 第七部分 server_local

```
;shadowsocks=example.com:80, method=chacha20, password=pwd, obfs=http, obfs-host=bing.com, obfs-uri=/resource/file, fast-open=false, udp-relay=false, server_check_url=http://www.apple.com/generate_204, tag=ss-01
;shadowsocks=example.com:80, method=chacha20, password=pwd, obfs=http, obfs-host=bing.com, obfs-uri=/resource/file, fast-open=false, udp-relay=false, tag=ss-02
;shadowsocks=example.com:443, method=chacha20, password=pwd, obfs=tls, obfs-host=bing.com, fast-open=false, udp-relay=false, tag=ss-03
;shadowsocks=example.com:443, method=chacha20, password=pwd, ssr-protocol=auth_chain_b, ssr-protocol-param=def, obfs=tls1.2_ticket_fastauth, obfs-host=bing.com, tag=ssr
;shadowsocks=example.com:80, method=aes-128-gcm, password=pwd, obfs=ws, fast-open=false, udp-relay=false, tag=ss-ws-01
;shadowsocks=example.com:80, method=aes-128-gcm, password=pwd, obfs=ws, obfs-uri=/ws, fast-open=false, udp-relay=false, tag=ss-ws-02
;shadowsocks=example.com:443, method=aes-128-gcm, password=pwd, obfs=wss, obfs-uri=/ws, fast-open=false, udp-relay=false, tag=ss-ws-tls-01
;shadowsocks=example.com:443, method=aes-128-gcm, password=pwd, obfs=wss, obfs-uri=/ws, tls13=true, fast-open=false, udp-relay=false, tag=ss-ws-tls-02

---

;vmess=example.com:80, method=none, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, fast-open=false, udp-relay=false, tag=vmess-01
;vmess=example.com:80, method=aes-128-gcm, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, fast-open=false, udp-relay=false, tag=vmess-02
;vmess=example.com:443, method=none, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=over-tls, fast-open=false, udp-relay=false, tag=vmess-tls-01
;vmess=192.168.1.1:443, method=none, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=over-tls, obfs-host=example.com, fast-open=false, udp-relay=false, tag=vmess-tls-02
;vmess=192.168.1.1:443, method=none, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=over-tls, obfs-host=example.com, tls13=true, fast-open=false, udp-relay=false, tag=vmess-tls-03
;vmess=example.com:80, method=chacha20-poly1305, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=ws, obfs-uri=/ws, fast-open=false, udp-relay=false, tag=vmess-ws-01
;vmess=192.168.1.1:80, method=chacha20-poly1305, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=ws, obfs-host=example.com, obfs-uri=/ws, fast-open=false, udp-relay=false, tag=vmess-ws-02
;vmess=example.com:443, method=chacha20-poly1305, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=wss, obfs-uri=/ws, fast-open=false, udp-relay=false, tag=vmess-ws-tls-01
;vmess=192.168.1.1:443, method=chacha20-poly1305, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=wss, obfs-host=example.com, obfs-uri=/ws, fast-open=false, udp-relay=false, tag=vmess-ws-tls-02
;vmess=192.168.1.1:443, method=chacha20-poly1305, password=23ad6b10-8d1a-40f7-8ad0-e3e35cd32291, obfs=wss, obfs-host=example.com, obfs-uri=/ws, tls13=true, fast-open=false, udp-relay=false, tag=vmess-ws-tls-03

---

;http=example.com:80,fast-open=false, udp-relay=false, tag=http-01
;http=example.com:80, username=name, password=pwd, fast-open=false, udp-relay=false, tag=http-02
;http=example.com:443, username=name, password=pwd, over-tls=true, tls-host=example.com, tls-verification=true, fast-open=false, udp-relay=false, tag=http-tls-01
;http=example.com:443, username=name, password=pwd, over-tls=true, tls-host=example.com, tls-verification=true, tls13=true, fast-open=false, udp-relay=false, tag=http-tls-02

---

;trojan=example.com:443, password=pwd, over-tls=true, tls-verification=true, fast-open=false, udp-relay=false, tag=trojan-tls-01
;trojan=example.com:443, password=pwd, over-tls=true, tls-verification=true, tls13=true, fast-open=false, udp-relay=false, tag=trojan-tls-02
;trojan=192.168.1.1:443, password=pwd, over-tls=true, tls-host=example.com, tls-verification=true, fast-open=false, udp-relay=false, tag=trojan-tls-03
;trojan=192.168.1.1:443, password=pwd, over-tls=true, tls-host=example.com, tls-verification=true, tls13=true, fast-open=false, udp-relay=false, tag=trojan-tls-04

```

### 第八部分 filter_local

```
[filter_local]
;user-agent, ?abc*, proxy
;host, www.google.com, proxy
;host-keyword, adsite, reject
;host-suffix, googleapis.com, proxy
ip-cidr, 10.0.0.0/8, direct
ip-cidr, 127.0.0.0/8, direct
ip-cidr, 172.16.0.0/12, direct
ip-cidr, 192.168.0.0/16, direct
ip-cidr, 224.0.0.0/24, direct
geoip, cn, direct
final, proxy
```

### 第九部分 rewrite_local

```

[rewrite_local]
;^http://example\.com/resource1/1/ url reject
;^http://example\.com/resource1/2/ url reject-img
;^http://example\.com/resource1/3/ url reject-200
;^http://example\.com/resource1/4/ url reject-dict
;^http://example\.com/resource1/5/ url reject-array
;^http://example\.com/resource2/ url 302 http://example.com/new-resource2/
;^http://example\.com/resource3/ url 307 http://example.com/new-resource3/
;^http://example\.com/resource4/ url request-header ^GET /resource4/ HTTP/1\.1(\r\n) request-header GET /api/ HTTP/1.1$1
;^http://example\.com/resource4/ url request-header (\r\n)User-Agent:.+(\r\n) request-header $1User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/71.0.3578.98 Safari/537.36$2
;^http://example\.com/resource5/ url request-body "info":\[.+\],"others" request-body "info":[],"others"
;^http://example\.com/resource5/ url response-body "info":\[.+\],"others" response-body "info":[],"others"
;^http://example\.com/resource6/ url script-response-body response-body.js
;^http://example\.com/resource7/ url script-echo-response script-echo.js
;^http://example\.com/resource8/ url script-response-header response-header.js
;^http://example\.com/resource9/ url script-request-header request-header.js
;^http://example\.com/resource10/ url script-request-body request-body.js

```

### 第九部分 task_local

```
[task_local]
;* * * * * sample-task.js

```

### 第十部分 MitM

```
[mitm]
;passphrase =
;p12 =
;skip_validating_cert = false
;force_sni_domain_name = false
;hostname = *.example.com, *.sample.com

```
