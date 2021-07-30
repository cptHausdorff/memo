Promise
=======

参考
----

- [Using Promises/MDN Web Docs][1]


[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises

- 非同期処理の完了もしくは失敗を表すオブジェクト

関数が返す Promise の使い方
-----------------------

- `Promise` はコールバックを関数に渡すかわりに、関数が返したオブジェクトに対してコールバックを登録する
- 非同期関数呼び出し(asynchronnous function call)

Promise チェーン
-------------

```javascript
doSomething()
.then(result => doSomethingElse(result))
.then(newResult => doThirdThing(newResult))
.then(finalResult => {
  console.log(`Got the final result: ${finalResult}`);
})
.catch(failureCallback);
```

- 例外が発生すると、ブラウザーはチェーンをたどって `.catch()` ハンドラーか `onRejected` を探す
- ECMAScript 2017 の糖衣構文 `async/await`

```javascript
async function foo() {
  try {
    const result = await doSomething();
    const newResult = await doSomethingElse(result);
    const finalResult = await doThirdThing(newResult);
    console.log(`Got the final result: ${finalResult}`);
  } catch(error) {
    failureCallback(error);
  }
}
```

古いコールバック API をラップする Promise の作成
------------------------------------

```javascript
const wait = ms => new Promise(resolve => setTimeout(resolve, ms));

wait(10*1000).then(() => saySomething("10 seconds")).catch(failureCallback);
```

