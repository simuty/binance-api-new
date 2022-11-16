### 问题一

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