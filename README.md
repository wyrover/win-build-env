# win-build-env

在 win7 下搭建开发环境

**1. 升级 powershell (Win7AndW2K8R2-KB3191566-x64.zip)** 

```
https://download.microsoft.com/download/6/F/5/6F5FF66C-6775-42B0-86C4-47D41F2DA187/Win7AndW2K8R2-KB3191566-x64.zip
```

**2. 安装 .net framework 4.6**   

```
https://download.microsoft.com/download/F/9/4/F942F07D-F26F-4F30-B4E3-EBD54FABA377/NDP462-KB3151800-x86-x64-AllOS-ENU.exe
```

**3. install scoop**

```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser; 
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

**4. install chocolatey**

```
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

**5. vc 运行时库**

```
choco install vcredist-all -y
```


## basic tools

```
scoop bucket add extras
scoop bucket add versions
scoop install git coreutils curl grep sed 
scoop install concfg
scoop install pshazz
scoop install openssh
```

```
choco install notepadplusplus.install
```


## python 

```
scoop bucket add versions # add the 'versions' bucket if you haven't already

scoop install python27 python
python --version # -> Python 3.6.2

# switch to python 2.7.x
scoop reset python27
python --version # -> Python 2.7.13

# switch back (to 3.x)
scoop reset python
python --version # -> Python 3.6.2

scoop bucket add gvahim https://github.com/gvahim/scoop.git
scoop install visual_cpp_for_python27
scoop install python-packages
```



## vc2013 


```
choco install visualstudiocommunity2013
choco install windows-sdk-7.1
```


## vc2015

```
```

## vc2017


```
```



## msys2



## Qt


## Java

```
scoop install openjdk
scoop install gradle
scoop install maven

```

```
choco install visualstudiocode -y
```


## php

```
scoop install php
```


## node

```
scoop install nodejs
scoop install yarn
```


## database

```
scoop install redis
scoop install mongodb
```


## links

- https://github.com/george-haddad/win-cross-dev