# Python 
```
python runner.python 
--hostname=domain 
--username=u 
--password=p 
--template="https://api.dynu.com/nic/update?
hostname=__HOSTNAME__&myip=__MYIP__&username=__USERNAME__&password=__PASSWORD__"
```

# 运行容器
```
docker run -d -t caryyu/ddns-client 
--hostname=domain 
--username=u 
--password=p 
--template="https://api.dynu.com/nic/update?
hostname=__HOSTNAME__&myip=__MYIP__&username=__USERNAME__&password=__PASSWORD__"
```