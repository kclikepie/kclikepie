# GIT remote

## View all added remote node

```console
user@hostname# git remote -v
origin https://github.com/kclilepie/kclikepie (fetch)
origin https://github.com/kclilepie/kclikepie (push)
```

## Add new node for extra remote repo.

```console
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

## Merge to local working copy.

```console
# Move to working dir
cd $working directory/

# Fetch remote source code in bar
git fetch bar

# merge bar/master to local
git merge bar/master

## if there's other branch for merge, replace master by the branch name.
```

