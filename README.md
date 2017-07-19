# web-templates
整理一些web模板,在需要的时候直接用.




## vuejs

- [vue-admin](https://github.com/zzmhot/vue-admin)
- [CoPilot](https://github.com/misterGF/CoPilot)
- [vue-bulma-vue-admin](https://github.com/vue-bulma/vue-admin)
- [taylorchen709-vue-admin](https://github.com/taylorchen709/vue-admin)


## bootstrap

> http://www.bootcss.com/里有很多好用的库

#### 模板
- [AdminLTE](https://github.com/almasaeed2010/AdminLTE)

#### 工具

- [Bootstrap 可视化布局系统](http://www.bo。otcss.com/p/layoutit/)
- [Bootstrap 表单构造器](http://www.bootcss.com/p/bootstrap-form-builder/)

## 注意

- 安装`nodejs`: https://nodejs.org/en/download/package-manager/
- 安装cnpm: 国内的话可以使用淘宝定制的cnpm (gzip 压缩支持) 命令行工具代替默认的 npm,这样不仅速度快避免由于下载一些依赖导致失败.

## 问题

如果vuejs的VueRouter使用的是`history`模式,例如:
```
var router = new VueRouter({
  routes: routes,
  mode: 'history',
  scrollBehavior: function (to, from, savedPosition) {
    return savedPosition || { x: 0, y: 0 }
  }
})
```
当`npm build`后,使用`nginx`的话在其他页面刷新的话会导致**404**错误. 解决:
```
location / {

    root /root/dist;

    try_files $uri $uri/ /index.html =404;

}
```
