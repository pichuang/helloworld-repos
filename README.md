# helloworld-repos

## Create the Helm chart package
```
$ helm create helloworld-repos
$ helm package helloworld-repos
Successfully packaged chart and saved it to: /home/pichuang/code/helloworld-repos/online-helmchart-0.1.0.tgz
```

## Create Helm Chart Repository Index
```bash
$ helm repo index --url https://pichuang.github.io/helloworld-repos .
```


## Configure helm client
```bash
helm repo add helloworld-repos http://blog.pichuang.com.tw/helloworld-repos/
helm search helloworld
```

## References
- https://docs.bitnami.com/tutorials/create-your-first-helm-chart/
- https://ithelp.ithome.com.tw/articles/10239692
