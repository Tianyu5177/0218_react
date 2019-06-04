##React面试题：
###1.说说你对React的基本理解
   动态构建用户界面的JS库

###2.React的特点
   1. Declarative(声明式编码)
   2. Component-Based(组件化编码)
   3. 高效
   
###3.React高效的原因
   1. 虚拟(virtual)DOM, 不总是直接操作真实DOM(批量更新, 减少更新的次数) 
   2. 高效的DOM Diff算法, 最小化DOM更新

###4.说说react的jsx
1. JSX 是一个看起来很像 XML 的 js 语法扩展
2. 作用: 简化创建虚拟DOM的语法
3. 浏览器不能直接运行, 需要使用babel转换成纯JS语法: React.createElement()
5. 注意: JSX标签必须有结束；组件标签首字母必须大写；必须只有一个根标签；

###5.说说你对模块与模块化, 组件与组件化的理解？
1. 模块: 具有特定功能的js文件。
1. 模块化: 如果项目的JS编写是以多模块编写组合使用的, 那这个项目就是一个模块化的项目, 也就是模块化的编码方式。
1. 组件: 实现局部功能界面的所有代码的集合。
1. 组件化: 如果项目的功能界面是由多个组件组合编写实现的, 那这个项目就是一个组件化的项目, 也就是组件的编码方式。

###6.定义组件的2种方式？
1. 方式1: 工厂函数(简单/无状态组件)

	   function MyComponent1(props) {
	      return <h1>自定义组件标题11111</h1>
	   }
		ReactDOM.render(<MyComponent1/>, domContainer)
2. 方式2: ES6类(复杂/有状态组件)

	   class MyComponent2 extends React.Component {
	      render () { // 回调函数, 为组件对象提供虚拟DOM
	        return <h1>自定义内容</h1>
	      }
	   }
	ReactDOM.render(<MyComponent2/>, domContainer)

###7.说说类组件和工厂函数式组件的区别？
1. 类组件: 使用class定义的组件, 会产生组件对象, 可以有自身的状态和生命周期勾子
2. 函数组件: 使用function定义的组件, 不会产生组件对象, 没有自身的状态和生命周期勾子
3. 区别组件对象的3大属性
4. state: 值为容器对象, 保存的是组件内可变的数据,组件根据state中的数据显示, 要更新界面只要更新state即可 
5. props: 值为容器对象, 保存的是从组件外传递过来的数据, 当前组件只读, 父组件修改了自动显示新数据
6. refs: 值为容器对象, 保存的是n个有ref属性的dom元素对象, 属性名是ref指定的标识名称, 值为对应的dom元素
