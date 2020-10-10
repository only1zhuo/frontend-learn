参考：https://blog.daraw.cn/2016/08/17/how-to-monitor-changes-of-js-variable/

# 数据监听以及实现数据绑定
## 脏值检测（angular 的数据绑定原理）
缺点：每次更新值都需要遍历所有带有相关的数据 dom，然后一个一个将值设置进去，数据太多的时候，可能会出现性能问题
## ES5 的 Object.defineProperty()（vue2 的数据绑定原理）
缺点：无法监听对象的属性或数组的值更改
## ES6 的 Proxy（vue3 的数据绑定原理）
缺点：兼容性比较差，不过有 polyfill
## ES7 草案中的 Object.observe（已废弃）
已废弃，性能有瓶颈，不需要探究