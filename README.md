# 我的前端自学指南

本文档记录我在自学前端过程中对前端的理解, 知识体系搭建的过程，以及相关学习资源的收录。

## Prerequisites

- You **CAN'T** learn something just by watching and copy, you need to do it by yourself!
- Think frequently! ask youself `why`, `how` and `what`

## HTML

### 1. 熟悉各种常用标签

**Resources List:**

- [MDN HTML tutorial](https://developer.mozilla.org/en-US/docs/Learn/HTML).

### 2. 懂得如何使用合适的标签写出简洁明了的页面框架

**Resources List:**

- [HTML Best Practices: How to Build a Better HTML-based Website](https://www.freecodecamp.org/news/html-best-practices/)

## CSS

### 1. 建立`CSS知识体系`

**Resources List:**

- [MDN CSS tutorial](https://developer.mozilla.org/en-US/docs/Learn/CSS).

### 2. 熟练使用常用属性

没有捷径，多多练习

Resources List:

- [Brad Traversy's 50 projects 50 days](https://www.udemy.com/course/50-projects-50-days)
- [Jonas Schmedtmann's Advanced CSS and Sass](https://www.udemy.com/course/advanced-css-and-sass)

### 3. 掌握常见功能的实现，熟悉`Patterns`

没有捷径，多多练习

**Resources List:**

- [Jonas Schmedtmann's Advanced CSS and Sass](https://www.udemy.com/course/advanced-css-and-sass)

## JavaScript

### 1. 熟悉 `基本语法` 和 `常用内置对象`

### 2. 了解 `ojbect` 和 `function` 及其背后的 `Scope`, `Prototype chain`, `Clousre` 等核心概念

**Resources List:**

- [You don't know JS yet](https://github.com/getify/You-Dont-Know-JS)

### 3. 熟练使用 `ES6`

**Resources List:**

- [Understanding ECMAScript 6: The Definitive Guide for JavaScript Developers](https://www.amazon.com/gp/product/1593277571)

### 4. 使用 `TypeScirpt`

#### 4.1 入门，花个`10-20`分钟学习基本用法，然后开始上手，在实践中学习

**Resources List:**

- [Documentation - TypeScript for JavaScript Programmers](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
- [Documentation - TypeScript Tooling in 5 minutes](https://www.typescriptlang.org/docs/handbook/typescript-tooling-in-5-minutes.html)

#### 4.2 学习如何将 `TypeScript` 在项目中使用

**Resources List:**

- [How to Set Up a Node Project With TypeScript](https://www.digitalocean.com/community/tutorials/setting-up-a-node-project-with-typescript)
- [TypeScript tsconfig tutorial](https://www.youtube.com/watch?v=dPgAXFcFHCM)

#### 4.3 学习如何配置 `tsconfig.json`

**Resources List:**

- [TSconfig Reference](https://www.typescriptlang.org/tsconfig)
- [TypeScript 配置文件该怎么写？](https://zhuanlan.zhihu.com/p/197425558)

#### 4.4 如何在编译 `ts` 文件时一起将其他 `assets` 拷贝到 `output` 目录下

**Resources List:**

- [tsc: How to copy non-TypeScript files when building](https://vccolombo.github.io/blog/tsc-how-to-copy-non-typescript-files-when-building/)

## 框架

### 1. 掌握框架的组成部分

了解框架的各个 `组成部分`，懂得每个部分要解决的 `问题` 是什么？进而发现前端框架的`共通点`，在这个过程中可以与 `原生开发` 进行对比学习，了解 `原生开发基本原理` 和其 `痛点`

#### 1.1 框架的组成部分

现阶段主要以 `React` 为研究对象，后续会加入对 `Vue` 的学习研究

**Resources List:**

- [Framework main features](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Main_features)

#### 1.2 `DOM` 操作

在不使用框架的年代，浏览器提供的 `DOM API` 使用起来超级繁琐。
虽然 `JQuery` 的出现简化了很多操作，且磨平了各大浏览器之间的差异。
但是，还是很麻烦。
直到 `MVVM` 这一类框架的出现，直接把`DOM`给 `屏蔽` 了，大大提高了开发效率。
为了更好的使用框架，因此，很有必要研究框架是如何做到 `屏蔽DOM` 的，其背后做了哪些牺牲？在写 `UI` 的过程中，有哪些方面是开发者可以进行优化的？

**Resources List:**

- [What is Virtual DOM? And Why is it faster?](https://dev.to/karthikraja34/what-is-virtual-dom-and-why-is-it-faster-14p9)

#### 1.3 `Event System`

在我的理解中，前端很多代码的存在都是为了处理交互，而交互基于事件系统。
因此，学习了解事件系统有助于写出更优雅的代码。

`React`并没有直接使用浏览器提供的原生 `Event System`, 而是使用了 `SyntheticEvent`, 其目的主要是为了兼容性，保持 `Consistency`。
我猜测其实现应该和 `JQuery` 对于 `DOM` 的封装类似，在原生事件上进行了一层封装，从而保持一致性。

**Resources List:**

- [Handling Events](https://reactjs.org/docs/handling-events.html)
- [SyntheticEvent](https://reactjs.org/docs/events.html)
- [Handling React Events](https://www.knowledgehut.com/blog/web-development/handling-react-events-guide)

#### 1.4 `State`

`State`的管理是各大框架面临的一个 `Major Issue`。
当应用规模较小，需要管理的 `State` 较少且 `Data flow` 比较简单时，完全可以使用框架提供的功能实现([])。
比如在 `React` 中，通过 `State` 和 `Prop` 应该就能完成简单功能的开发，稍微复杂一点也可以由 `Context` 实现。

但是当应用规模和复杂度较大时（我也没碰过大型项目啊，淦！），上述方法会出现问题（啥问题？我不理解，这些话我都是听别人说的，没有实际体验都是瞎扯淡）。
因此一些状态管理工具就推出了，比如 `React` 中的 `Redux` `Mobx` `Recoil`, `Vue` 中的 `Vuex`。

虽然我不懂，但感觉好厉害的样子。不过学习这些状态管理工具背后的 `设计思想` 应该对于写出优雅的程序有帮助吧！（应该吧？）

**Resources List:**

- [Getting Started with Redux](https://redux.js.org/introduction/getting-started)

#### 1.5 生命周期

在组件化的今天，组件的生命周期的出现是一件很自然的事情。
组件的生命周期是几个不同的阶段，比如组件的创建，初始化，安装，状态更新，卸载等。
日常开发中我们所使用的生命周期其实是框架提供的生命周期钩子函数，这些钩子函数本身并不是生命周期阶段，而是阶段中间的一个点。比如：
beforeCreate -> `组件创建` -> created -> beforeInit -> `组件初始化` -> inited -> beforeUpdate `状态更新` -> updated
上述举例并不完全，并且不同的框架对于生命周期的定义也有所不同。但是大致的流程是相似的，一通百通。
不过好像听说在 `React` 中，`Hooks` 的出现把生命周期函数干翻了，也不知道是真是假，后续再研究一下。
