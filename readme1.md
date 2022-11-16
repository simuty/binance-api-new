### 问题一

单元测试，在本地总是无法运行，在服务器上`npm run test`, 如果需要单独执行某个测试，加only.
返回数据错误，其实只需要在返回的时候，`sendResult`中将，`// return res.text().then(text => JSONbig.parse(text))` 改为`return res.json()`即可; 

关于原作者用`JSONbig`，可能是感觉返回的大数据问题，其实返回的是字符串。

```
返回值，这个样子，应该是返回数据格式的时候有问题
const list = await client.futuresAllBookTickers()
[
  [Object: null prototype] {
    symbol: 'ALICEUSDT',
    bidPrice: '1.220',
    bidQty: '1072.4',
    askPrice: '1.221',
    askQty: '3674.1',
    time: 1668516703672
  }
]
```