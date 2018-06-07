在使用homebrew 安装 [ldid](http://iphonedevwiki.net/index.php/Ldid) 签名工具失败提示如下： 
安装命令：
```
sudo brew install ldid
```
提示错误如下：
```
Running Homebrew as root is extremely dangerous and no longer supported.
As Homebrew does not drop privileges on installation you would be giving all build scripts full access to your system.
```
正解是不要使用root 权限来安装即使用 `brew install ldid` 即可。