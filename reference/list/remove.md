# remove
* list[meta header]
* std[meta namespace]
* list[meta class]
* function[meta id-type]

```cpp
void remove(const T& value);
```

## 概要
指定された値の要素を全て削除する。


## 効果
コンテナの全ての要素に対する各イテレータ`i`において、`*i == value`による比較が`true`となる要素を削除する。  
削除された要素に対するイテレータおよび参照は無効となる。


## 戻り値
なし


## 例外
型`T`の等値比較が例外を投げなければ、この関数は例外を投げない


## 計算量
ちょうど`x`の要素数回だけ等値比較を行う


## 例
```cpp
#include <iostream>
#include <list>

int main()
{
  std::list<int> ls = {3, 1, 4, 1};

  ls.remove(1); // 値1の要素を全て削除

  for (int x : ls) {
    std::cout << x << std::endl;
  }
}
```
* remove[color ff0000]

### 出力
```
3
4
```


