# GIT remote

## View all added remote node

```console
user@hostname# git remote -v
origin https://github.com/kclilepie/kclikepie (fetch)
origin https://github.com/kclilepie/kclikepie (push)
```

## Add new node for extra remote repo.

```
user@hostname# git remote add bar git@git.dc.kaluwa.com.tw:rum/taquila
user@hostname# git remote
bar
origin
user@hostname# git remote -v
bar https://git.dc.kaluwa.com.tw:rum/taquila (fetch)
bar https://git.dc.kaluwa.com.tw:rum/taquila (push)
origin https://github.com/kclilepie/kclikepie (fetch)
origin https://github.com/kclilepie/kclikepie (push)
```
