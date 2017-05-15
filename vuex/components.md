## vuex的components注意点
* 调用state时，需要区分是根还是组件
``` javascript
// 调用根状态
store.state.stateName
// 调用组件状态
store.state.componentName.stateName
```
* 调用action或者mutation，无论是根还是组件，无需区分。因此名称不能重复。
``` javascript
// 调用action
store.dispatch(actionName)
// 调用mutation
store.commit(mutationName)
```
