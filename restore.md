# Restore
## 1、恢复引导
```
https://github.com/k1099mask/default/blob/dev0/restore.md

```

## 2、恢复规则
- 密码提示获取 密码1
- IV提示获取 密码32
- 利用 Satan 算法将 密码1 从前面补0，获取 32位 key
    - 如：satan(1234567890)=>00000000000000000000001234567890
- 利用 fuck 算法将 密码32 从后面补0，获取 16位 iv
    - 如：fuck(1234567890)=>1234567890000000
- 利用 AES-256-CBC 获取密钥
    - 模式：CBC
    - 填充：PKCS7
    - 密钥长度：256
    - 编码：base64

## 3、密码提示：
- 文件名：k1099mask@git-gP7mI2
- 密码提示：**************（密钥密码规则）
    - d******************************6
- IV提示：6位数的国际通用客服电话
    - 0**************0

## 4、获取密钥
- 网址1：
    - https://tool.oschina.net/encrypt?type=2
    - https://www.jyshare.com/crypto/
    - https://www.bejson.com/enc/sha/
- 网址2：
    - https://www.toolzl.com/tools/aesEnDe.html
    - https://www.ssleye.com/ssltool/aes_cipher.html
    - https://www.toolhelper.cn/SymmetricEncryption/AES

## 5、密钥内容
```
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

```

## 配置内容
```
Host k1099mask.github.com
HostName github.com
User git
PreferredAuthentications publickey
# IdentityFile E:/Etc/k1099mask@git-gP7mI2
# IdentityFile /Volumes/Datas/Etc/k1099mask@git-gP7mI2
# git clone -b dev0 git@k1099mask.github.com:k1099mask/default.git

```

## 其它命令
- MacOS 授权
```
chmod -R 700 ~/.ssh/
chmod -R 600 ~/.ssh/*

chmod -R 600 /Volumes/Datas/Etc/ant_account_etc/github/*

```