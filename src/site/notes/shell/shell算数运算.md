---
{"dg-publish":true,"permalink":"/shell/shell算数运算/","dgPassFrontmatter":true,"noteIcon":""}
---

```bash
i=0
((i++))
echo $i
let i++
expr $i + 1
echo $i 1 | awk '{printf $1+$2}'
```
求模运算
```bash
expr 5 % 2
let i=5%2
((i=5%2))
```
求幂
```bash
let i=5**2
((i=5**2))
```
进制转换
```bash
echo $((8#11)) # 8进制11 = 9
echo $((16#11)) # 16进制11 = 17
```
ascii字符编码
```bash
root@localhost:~# echo -n "$IFS" | od -b
0000000 040 011 012
0000003
root@localhost:~# echo -n "$IFS" | od -c
0000000      \t  \n
0000003
```
浮点运算
```bash
echo "1 13" | awk '{printf("%.3f",$1/$2)}'
echo 0.996293 | awk '{ printf("%s\n", atan2(sqrt(1-$1^2),$1)*180/3.1415926535);}'
```
随机数
```bash
echo $RANDOM
echo "" | awk '{srand();printf("%f",rand());}'
```
序列数
```bash
seq 5 # 1~5数字
seq 1 5 # 1~5数字
seq 1 2 5 # 1 3 5数字
seq -s: 1 2 5 # 1:3:5
seq -w 1 2 14 # 宽度2个
seq -s: -w 1 2 14 # 01:03:05:07:09:11:13
seq -f "0x%g" 1 5
```