# 第八届 “强网杯” 全国网络安全挑战赛

**附件存放在本仓库的 Github Release 中**

## Misc

### pickle_jail

> Break this pickle jail to get the flag! (flag格式为 flag{UUID4})

```Dockerfile

FROM python@sha256:c38ead8bcf521573dad837d7ecfdebbc87792202e89953ba8b2b83a9c5a520b6

RUN pip install -i https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple Faker

```

### Master of DFIR - Coffee

> 随着调查的深入你发现情况比你预想得要复杂很多,你逐步发现了更多入侵的痕迹
>
> "看起来不能这么早就休息了" 于是你继续投身于下一步的调查中
>
> 你需要继续完成题目帮助饥渴C猫发掘所有的真相

### Master of DFIR - Phishing

> 饥渴C猫是一个刚刚入职的员工，但是最近他发现自己的电脑变得越来越奇怪。可能由于是之前他接受的一封奇怪的邮件，于是饥渴C猫找到了你,他希望你作为取证-应急响应大师可以帮忙。你可以完成调查到底发生了什么并且填写相关的调查报告。

Hint: 第六问指得是解密完载荷后可以看到一个s******s的函数(*不代表正确长度) 然后你需要去提交该函数的参数,这个参数是需要解字符串混淆后的一段字符串 并且将这段字符放到cyberchef MD5一下

Hint: 第12问的最终载荷指得是RAT的载荷 java的马和本题目毫无关系

1. 攻击者的邮箱是什么? (注意:MD5(攻击者邮箱),以cyberchef的为准) 示例:9b04d152845ec0a378394003c96da594

```plaintext
a8cd5b4ba47e185d4a69a583fde84da5
```

2. 攻击者所投放的文件md5是什么? (注意:以md5sum的结果为准) 示例:33ec9f546665aec46947dca16646d48e

```plaintext
f436b02020fa59f3f71e0b6dcac6c7d3
```

2. 攻击者所投放文件的密码是什么? 示例:000nb

```plaintext
2024qwbs8
```

3. 攻击者所使用的攻击载荷后缀是什么？ 示例:lnk

```plaintext
msc
```

4. 攻击者所投放样本的初始执行语句在该攻击载荷文件的第几行? 示例:20

```plaintext
97
```

5. 经过初始执行后,攻击者所加载的第二部分载荷所使用的语言是什么? 示例:javascript

```plaintext
VBScript
```

6. 攻击者所进行的第二部分载荷其将白EXE存在了什么地方? (注意:需要提供完成的解混淆后的第二部分载荷s*******s函数的参数) 提交需要MD5(参数内容) 以Cyberchef结果为准 示例:9b04d152845ec0a378394003c96da594

```plaintext
69b23cfd967d07c39d1517e2a3c37e34
```

7. 攻击者使用的这个白EXE加载黑DLL的手法所对应的MITRE ATT&CK ID是什么? (注意:请注意示例的提示提交大类即可不需要细化到分项) 示例: T1000

```plaintext
T1574
```

8. 攻击者所使用的黑DLL劫持了原始DLL的哪个函数? 示例: main

```plaintext
curl_easy_init
```

9. 攻击者所使用的黑DLL解密下一阶段载荷所使用的算法是什么? 示例:chacha20

```plaintext
RC4
```

9. 攻击者所使用的黑DLL解密下一阶段载荷所使用的Key是什么? (注意:请提交一段小写的十六进制字符串) 示例:1122334455

```plaintext
f21a9d8b1e5d
```

10. 攻击者所使用的下一阶段载荷的回连C2是什么? (注意:需要提供ip地址:端口的形式) 示例:127.0.0.1:5100

```plaintext
192.168.57.119:6000
```

11. 攻击者所使用最终阶段载荷所使用的加密算法是什么? 示例:DES

```plaintext
AES
```

12. 攻击者所使用最终阶段载荷所使用的密钥的MD5是什么? (注意:MD5(密钥内容),以cyberchef的为准) 示例:9b04d152845ec0a378394003c96da594

```plaintext
a524c43df3063c33cfd72e2bf1fd32f6
```

13. 攻击者使用了什么家族的C2? 示例:PoshC2

```plaintext
OrcaC2
```

### AbstractMaze

> I like maze. Give me a maze.

新增附件：`strategy.py`

### 谍影重重5.0

> 我国某部门已经连续三年对间谍张纪星进行秘密监控，最近其网络流量突然出现大量的神秘数据，为防止其向境外传送我国机密数据，我们已将其流量保存，请你协助我们分析其传输的秘密信息。

## Crypto

### traditional_game

> Since you've made it here, let's now play a Traditional Game from 1997.

### homomor_game

> It seems that you enjoy this homomorphic game...Don't you?

### electronic_game

> After finishing traditional cigarettes, let's try vaping some electronic cigarettes.

### ECRandom_game

> easy密码游戏

### EasyRSA

> easy的RSA。

### 21_steps

> weight it in 21 steps!

### apbq

> I obtained several sets of ap + bq through channel measurement. Can you solve it?

## Reverse

### boxx

> 迷宫重重，尝试走出你的地图吧！

Hint: 字符为最后四张图的影像图

### remem

> None

### 斯内克

> 我不希望我的蛇被人捡到能直接使用。

Hint: 赛题附件已更新，总体算法并未修改。对于解决此赛题，需关注以下内容：

1. 需要选手的操作序列最短

2. 赛题内设用于触发验证的轮次减少

3. 选手可忽略由蛇的身体长度引起的可能

蛇要最优走好每一步；蛇不应该直接调头(如当蛇往右走时，不能直接转变方向为左)，否则会咬伤自己。

### mips

> Someone has found the mips binary, along with an emulator to execute it. What can you find in them?
>
> USAGE：./emu ./mips_bin

### solve2-apk

> None

### ez_vm

> ez_vm

## Pwn

### chat_with_me

> None

### qroute

> None

### prpr

> NOne

### expect_number

> 积小成多。看看你能用0，1，2构造出那些数字呢？

### baby_heap

> None

### old_fashion_apache

> 对外只开放赛题环境映射的一个端口

## Web

### PyBlockly

> 积木编程

### Playground

> Go playground designed for newbie

### Proxy

> Proxy what you want

### EzCalc

> Yet another calculator

### Proxy_revenge

> Proxy what you want but encrypted
