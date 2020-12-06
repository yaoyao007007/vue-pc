20201202
    1.新建main.js
    2.新建App.js
    3.目录划分
        api:请求相关的
        components:公共组件
        assets:公共资源
        styles:公共样式
        utils:公共js
        store:vuex
        router:路由
        views：路由组件
    4.npm run bulid 打包项目
        map文件，提供与源代码映射的一个文件，
        打包后代码需要运行一下，查看是否出错
            npm i serve -g 可快速开启一个服务器运行资源
            serve -s dist 会快速启动一个服务器，服务器会运行dist目录下面的资源
            serve dist -p 5000 指定端口号
        测试完没有问题,即可删除map文件，剩下的文件就可发给运营人员
20201203
    5.eslint 检查代码规范工具
        1) packjson.json rules可以启动关闭某些规则
            'rules': {
                'no-new': 'off'
            }
        2) main.js中修改局部规则
            /* eslint-disable no-new */
            new Vue({
                el: '#app',
                render => h(App)
            })
        3) 新建vue.config.js文件，关闭全部规则检查
            module.exports={
                lintOnSave: false, // 关闭ESLint的规则检查
                lintOnSave: 'warning',// 输出提示错误, 但项目继续运行
            }
    


