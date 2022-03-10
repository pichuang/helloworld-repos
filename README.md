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

### (Optional) GitHub Packages Support
```bash
$ export USER=pichuang
$ export TOKEN=ghp_pichuang_is_handsome_man
$ echo "$TOKEN" | helm registry login -u $USER --password-stdin https://ghcr.io
Login Succeeded

$ helm push online-helmchart-0.1.0.tgz oci://ghcr.io/pichuang/helloworld-repos
Pushed: ghcr.io/pichuang/helloworld-repos/online-helmchart:0.1.0
Digest: sha256:db95f68f21ef82d7514c1ee427f68074e556178067bc459721a617c59e3e527b
```

- Connect Package

![](/images/github-package.png)

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
- https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
- https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry
- https://docs.aws.amazon.com/AmazonECR/latest/userguide/push-oci-artifact.html
