redux notes
======


```javascript
import { createStore } from "redux";

// state 必须提供默认参数
function productsReducer(state=[], action) {
  return state;
}

function cartReducer(state=[], action) {
  return state;
}


const allReducers = {
  products: productsReducer,
  shoppingCart: cartReducer
}

const rootReducer = combineReducers(allReducers);


const store = createStore(rootReducer);
```


让我解释一下上面的代码：

1. 首先，我们从redux包中引入createStore()方法。
2. 我们创建了一个名为reducer的方法。第一个参数state是当前保存在store中的数据，第二个参数action是一个容器，用于：
    type - 一个简单的字符串常量，例如ADD, UPDATE, DELETE等。
    payload - 用于更新状态的数据。
3. 我们创建一个Redux存储区，它只能使用reducer作为参数来构造。存储在Redux存储区中的数据可以被直接访问，但只能通过提供的reducer进行更新。            

