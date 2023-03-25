# v2ray
最好用的 V2Ray 一键安装脚本 &amp; 管理脚本

使用 root 用户输入下面命令安装或卸载

```bash
bash <(curl -s -L https://git.io/v2ray.sh)
```
## 快速管理
- v2ray info 查看 V2Ray 配置信息
- v2ray config 修改 V2Ray 配置
- v2ray link 生成 V2Ray 配置文件链接
- v2ray infolink 生成 V2Ray 配置信息链接
- v2ray qr 生成 V2Ray 配置二维码链接
- v2ray ss 修改 Shadowsocks 配置
- v2ray ssinfo 查看 Shadowsocks 配置信息
- v2ray ssqr 生成 Shadowsocks 配置二维码链接
- v2ray status 查看 V2Ray 运行状态
- v2ray start 启动 V2Ray
- v2ray stop 停止 V2Ray
- v2ray restart 重启 V2Ray
- v2ray log 查看 V2Ray 运行日志
- v2ray update 更新 V2Ray
- v2ray update.sh 更新 V2Ray 管理脚本
- v2ray uninstall 卸载 V2Ra

## 配置文件路径
```bash
V2Ray 配置文件路径：/etc/v2ray/config.json
Caddy 配置文件路径：/etc/caddy/Caddyfile
脚本配置文件路径: /etc/v2ray/233blog_v2ray_backup.conf
```
## WS+TLS / HTTP2
如果你使用了这两个协议，那么就会使用了脚本自带的 Caddy 集成
不管如何，不建议直接去更改 Caddy 的配置：/etc/caddy/Caddyfile
如果你需要配置其他网站相关，请将网站的配置文件放到 /etc/caddy/sites 目录下，然后重启 Caddy 进程即可，脚本默认生成的 Caddy 的配置会加载 /etc/caddy/sites 这个目录下的所有配置文件。
所以，请将你的网站配置文件放到 /etc/caddy/sites 目录下，完完全全不需要去更改 /etc/caddy/Caddyfile
记得重启 Caddy进程：
```bash
service caddy restart
```
## Caddy 插件相关

本脚本集成了 Caddy，但不集成任何 Caddy 插件，如果你需要安装某些 Caddy 插件，你可以使用官方的 Caddy 安装脚本来一键安装。
本人的脚本集成的 Caddy 的安装路径，跟 Caddy 官方的安装脚本是一致的。所以可以直接安装，不会有任何问题

举个例子，安装包含 http.filebrowser 插件的 Caddy，执行如下命令即可
```bash
curl https://getcaddy.com | bash -s personal http.filebrowser
```
## 备份
为了避免由于不可抗拒的原因所造成本人主动删除脚本，所以建议请将本脚本 Fork 一份
备份地址： https://github.com/233boy/v2ray/fork
安装方法，确保你已经 Fork 了脚本，将 233boy 修改成你的 Github 用户名

```bash
git clone https://github.com/233boy/v2ray -b master
cd v2ray
chmod +x install.sh
./install.sh local
```

## 脚本说明
[V2Ray 一键安装脚本](https://github.com/233boy/v2ray/wiki/V2Ray%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E8%84%9A%E6%9C%AC)

## 搭建教程
[V2Ray搭建详细图文教程](https://github.com/233boy/v2ray/wiki/V2Ray%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E5%9B%BE%E6%96%87%E6%95%99%E7%A8%8B)


## 更多 V2Ray 教程文章
https://github.com/233boy/v2ray/wiki
