# win-build-env

在 win7 下搭建开发环境

**1. 升级 powershell (Win7AndW2K8R2-KB3191566-x64.zip)**
**2. install scoop**

```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser; 
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

**3. install chocolatey**

```
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

**4. vc 运行时库**

```
choco install vcredist-all -y
```


## basic tools

```
scoop bucket add extras
scoop bucket add versions
scoop install git coreutils curl grep sed 
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
