# helloworld-repos

## For Chart Owner
### Create the Helm chart package
```
$ helm create helloworld-repos
$ helm package helloworld-repos
Successfully packaged chart and saved it to: /home/pichuang/code/helloworld-repos/online-helmchart-0.1.0.tgz
```

### Create Helm Chart Repository Index
```bash
$ helm repo index --url https://pichuang.github.io/helloworld-repos .
```

### Setup GitHub Page

![](/images/github-page.png)


## For User

### Configure helm client
```bash
$ helm repo add helloworld-repos https://blog.pichuang.com.tw/helloworld-repos/
"helloworld-repos" has been added to your repositories

$ helm search repo helloworld
NAME                                    CHART VERSION   APP VERSION     DESCRIPTION
helloworld-repos/online-helmchart       0.1.0           1.16.0          A Helm chart for Kubernetes
```

## References
- https://docs.bitnami.com/tutorials/create-your-first-helm-chart/
- https://ithelp.ithome.com.tw/articles/10239692
