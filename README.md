# DDNS Client
`DDNS Client` 是一个运行在用户机上的 `Dynamic DNS` 客户端更新器，主要原理是利用 `DDNS` 提供商所支持的 `HTTP/HTTPS` 域名解析修改链接来定时对本地路由的外网动态 `IP` 地址进行更新，这样我们就不用担心本地动态 `IP` 地址的问题了。
`DDNS Client` is a client or an updater for `Dynamic DNS` that running on the user computer, The principle is using modifiable `HTTP/HTTPS` URL of DDNS Provider to periodically update specific domain matching to dynamic public ip address of the local router , so there will be no longer worry about the dynamic public ip problems.

## 描述
`DDNS Client` 主要利用 `Python` 编写，会涉及到其 `requests` 模块来进行发送 `HTTP/HTTPS` 请求，利用 `ifconfig.me` 来获取本地路由的外网动态 `IP` 地址，然后每隔 `300` 秒反复进行更新操作。
`DDNS Client` written by Python, Involving `requests` module to send `HTTP/HTTPS` request, and using `ifconfig.me` to fetch dynamic public address of local router, then every `300s` to refresh `DNS`.

# 运行 / Running
我们有两种方式运行此程序，一是部署在容器中进行运行，二是可以直接利用本机 `python` 环境进行运行，推荐第一种。
We have two ways to run this program , First is throughout `Docker Container`, Second is we can directly run on the local pc that must have `python` environment installed, First solution is recommended/

## 容器方式 / Docker Container (Recommended)
```
docker run -d -t caryyu/ddns-client
--hostname=domain
--username=u
--password=p
--template="https://api.dynu.com/nic/update?
hostname=__HOSTNAME__&myip=__MYIP__&username=__USERNAME__&password=__PASSWORD__"
```

## 直接运行 / Python 
```
python runner.python
--hostname=domain
--username=u
--password=p
--template="https://api.dynu.com/nic/update?
hostname=__HOSTNAME__&myip=__MYIP__&username=__USERNAME__&password=__PASSWORD__"
```

# 贡献 / Contribution
All of contributions are welcomed.
