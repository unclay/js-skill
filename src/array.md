## 对象数组处理

+ 计算某个字段之和

```js
/**
 * 计算字符长度
 * @return {number} 字段之和
 */
const data = [
  {
    amount: 10
  },
  {
    amount: 20
  }
];
// 求amount之和
const amount = data.reduce((total, a) => total + a.amount, 0);
```
