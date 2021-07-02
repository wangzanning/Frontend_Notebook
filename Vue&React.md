- [React / Vue 项目时为什么要在列表组件中写 key](https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/1)***[ ! important ]***

  提高diff速度，复杂模板的情况下

  带key更准确：带key就不是`就地复用`了，在sameNode函数 `a.key === b.key`对比中可以避免就地复用的情况。所以会更加准确。

  利用key的唯一性生成map对象来获取对应节点，比遍历方式更快

- [React Hook](https://segmentfault.com/a/1190000019223106)***[ ! important ]***

  useEffect: **使用 useEffect 完成副作用操作，赋值给 useEffect 的函数会在组件渲染到屏幕之后**。默认情况下，**effect 将在每轮渲染结束后执行**。

- [React useLayoutEffect 和 useEffect 的执行时机](https://www.cnblogs.com/iheyunfei/p/13065047.html)***[ ! important ]***

  useEffect 在渲染时是异步执行，并且要等到浏览器将所有变化渲染到屏幕后才会被执行。

  useLayoutEffect 在渲染时是同步执行，其执行时机与 componentDidMount，componentDidUpdate 一致

- [useMemo与useCallback使用指南](https://blog.csdn.net/sinat_17775997/article/details/94453167)***[ ! important ]***

  useMemo返回缓存的变量，useCallback返回缓存的函数。

  假设有一个父组件，其中包含子组件，子组件接收一个函数作为props；通常而言，如果父组件更新了，子组件也会执行更新；但是大多数场景下，更新是没有必要的，我们可以借助useCallback来返回函数，然后把这个函数作为props传递给子组件；这样，子组件就能避免不必要的更新。

- 

- 

- 

