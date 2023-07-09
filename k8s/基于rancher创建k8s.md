## 部署rancher
```sehll
docker run -d --name rancher --restart=unless-stopped \
  -p 80:80 -p 443:443 \
  --privileged \
  rancher/rancher:stable

```

## 查看rancher默认密码
```shell
docker logs  rancher  2>&1 | grep "Bootstrap Password:"
```

## 查看rancher日志
```shell
docker logs -f rancher
```

## 参考
[使用 Docker 将 Rancher 安装到单个节点中](https://ranchermanager.docs.rancher.com/zh/pages-for-subheaders/rancher-on-a-single-node-with-docker)
