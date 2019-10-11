### 什么是BEM
> CSS命名的一种规范，即Block-Element-Modifier, 目的是能够让协同开发时review或者维护代码时候一目了然

### 具体规范写法
> 根据规范名称来看，命名由三个部分组成。

例子
```css
.block { /* styles */ }
.block__element { /* styles */ } 
.block--modifier { /* styles */ }
```

- 块(Block)
  代表该部分在项目中的组成成分。这里的块可以有多重划分方法，可以按照模块划分，比如: header, nav, search, footer等, 也可以按照功能划分, 比如: button, input等
  
```css
.header { /* styles */ }
.button { /* styles */ }
```
  
  
- 元素(Element)
  一个元素是块的一部分，具有某种功能。元素是依赖上下文的：它们只有处于他们应该属于的块的上下文中时才是有意义的。例如一个search块中有输入框input, 还有点击按钮button; 又或者是行或是某个小单元
  
```css
.search__input { /* styles */ }
.search__btn { /* styles */ }
.content__item { /* styles */ }
.content__row { /* styles */ }
```

- 修饰符(Modifier)
  顾名思义，这个主要起到的作用是修饰当前部分。 比如一个button有多种颜色: 默认颜色,提交时颜色, 禁用时颜色等; 还可能有多种尺寸: 大, 中, 小等
  
```css
.button--big { /* styles */ }
.search--default { /* styles */ }
``` 


PS: 这三个组成部分中, 每个部分如果是长单词, 可以用-号隔开, 例如: .search-form__btn--disable


参考资料:

[前端 | BEM规范你应该了解](https://www.jianshu.com/p/99ca15d0c7c7)

[BEM规范入门](https://www.jianshu.com/p/5e018c7f0bc6)

参考项目:

[Tencent-weui](https://github.com/Tencent/weui)
 
