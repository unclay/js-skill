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