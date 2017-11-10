#####  promise

    异步问题，解决回调函数的问题
    
##### 浏览器的history
    push push一个新的entry到history stack
    history stack :所有的浏览记录都存放在history stack里面，它就相当于一个数组
    
    entry:
        每一个访问的页面（访问过的路径）
        
    每点击了一次a链接，就push了一个新页面
    
    点击一下a链接，就是往历史堆里面增加一个地址
    
##### BrowserRouter
    使用 browerHistory
    放在最顶层 把其他的组件作为 children 
    
    
##### Route
    path的属性：如果地址匹配到了这个路径，就会显示
    
    exact属性：只会在path匹配 lication.pathName 时才匹配 
    
    render:接收一个回调函数，和component的第二点一样
    
    children:和render一样，不过，它无论如何都会被匹配到 不管path是什么
    
    component属性：
    1. 接收一个组件变量，会自动往组件里传入三个值 props:location match history
    2. 可以接受一个回调函数，会往回调函数里面传一个对象作为参数，
    3. 不可以在里面嵌套元素
        如果是平级的元素的话，会报一个错，告诉你要single React Element
        
    Route会往匹配的组件里传入三个组件：history match location
    
    
##### link
    最后会被渲染成 a 链接
    to的属性：跳转到哪里
        接收字符串：'./rus',一个rule的地址
    
    replace:bool
        true 跳转视图的时候，替换掉浏览器 history stack 里面 当前的 entry
        false 跳转视图的时候，往history stack 里面 push 一个新的entry


###### React某组件
    react组件帮助我们实现setState 只不过被routerdown隐藏起来了
    
###### location   history.location（self）
    props.location 是传入props的时候的location的值
    history.location 是实时变化的 随着地址的变化而变化
    
##### 传入的三个属性
    history
    location
        history里面的location是可变的 是实时的，不稳定的，如果你想要location，直接读取此 location，而不是从history里面拿到
    match

##### NavLink
    activeClassName
    activeObject
##### Readirect
    to的属性 如果他被渲染的时候，会重新向到一个新的地方
##### Switch
    一旦匹配到一个 就不再继续往下匹配
##### withRouter
    一个高阶组件，接收一个组件作为参数（比如Aac），然后导出一个组件，这个时候Aac组件的props就有了那三个属性
    
        