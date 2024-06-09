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