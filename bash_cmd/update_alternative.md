# Briefing for update-alternative
For more detail, you man check man 8 update-alternative

##  This application is to manage multiple version of specific application.

### cmd/how to
Take python as an example: 

1. Check status
```console
user@ubuntu# update-alternatives --display python
python - manual mode
 link best version is /usr/bin/python2.7
 link currently points to /usr/bin/python2.7
 link python is /usr/bin/python
/usr/bin/python2.7 - priority 1
/usr/bin/python3.6 - priority 1
```

2. setup option
```console
user@ubuntu# update-alternatives --install $targetSymbolicLinkFullPath $targetBinaryTheSameAsSymboliclink $binaryRealPath #priorityValue
user@ubuntu# update-alternatives --install /usr/bin/python python /usr/bin/python2.7 200 --slave python-config x86_64-linux-gnu-python2.7-config
user@ubuntu# update-alternatives --install /usr/bin/python python /usr/bin/python3.7 300 --slave python-config x86_64-linux-gnu-python3.6-config
```

3. Switching version
```console
user@ubuntu# update-alternatives --config python
There are 2 choices for the alternative python (providing /usr/bin/python).

  Selection    Path                Priority   Status
------------------------------------------------------------
  0            /usr/bin/python3.6   300       auto mode
  1            /usr/bin/python2.7   200       manual mode
* 2            /usr/bin/python3.6   300       manual mode

Press <enter> to keep the current choice[*], or type selection number:
```

## Ref:
[SUSE] (https://documentation.suse.com/zh-tw/sles/15-GA/html/SLES-all/cha-update-alternative.html "SUSE reference website")
