## 字符处理

+ 计算字符长度
（中文按两字节算）

```js
/**
 * 计算字符长度
 * @param val {string} 文本
 * @return {number} 文本长度（中文按双字节算）
 */
function getTextLen (val) {
  return (val || '').replace(/[^x00-xff]/gi, '**').length;
}
```

+ 获取 url 参数

```js
/**
 * 获取 url 参数
 * @param name {string} 参数名
 * @return {string} 参数对应的值
 */
function getUrlQuery(name) {
  const reg = new RegExp(`(^|&)${name}=([^&]*)(&|$)`, 'i');
  const r = window.location.search.substr(1).match(reg);
  if (r != null) {
    return unescape(r[2]);
  }
  return null;
},
```
