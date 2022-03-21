# JS 技巧记录

## 判断小数是否相等

```
function epsEqu(x,y) {
  return Math.abs(x - y) < Math.pow(2, -52);
}
// 举例
0.1 + 0.2 === 0.3 // false
epsEqu(0.1 + 0.2, 0.3) // true
```

### 数字格式化

```
(123456789).toLocaleString('en-US')  // 1,234,567,890


(123456789).toLocaleString('zh-hans-CN-u-nu-hanidec',{useGrouping:false})
//"一二三四五六七八九"
(123456789).toLocaleString('zh-hans-CN-u-nu-hanidec',{useGrouping:true})
//"一二三,四五六,七八九"
new Date().toLocaleString('zh-hans-CN-u-nu-hanidec')
//"二〇一八/一/三一 下午八:五四:五一"


export function toThousandslsFilter(num) {
  return (+num || 0).toString().replace(/^-?\d+/g, m => m.replace(/(?=(?!\b)(\d{3})+$)/g, ','))
}
```

### 匹配汉字的正则

```
/\p{Script=Han}/u
```
