1.git的使用
    git --version

    express app
    cd app
    git init
    git add *   //将所有文件都交给git管理
    git commit -m ''


    git log 
    git reset --hard 版本号
    git reflog --hard 版本号

    git branch //查看当前分支
    git branch dev
    git checkout dev   //切换分支


    git checkout master
    git merge dev   //将dev分支合并到master

    github.com  公共的git仓库

2.远程仓库
    1）与远程仓库绑定
        git remote add origin 远程地址
    2）提交
        git push origin master
    3)下载
        git clone 远程地址

3.es6
    也被称为ECMAScript2015
    转换工具babel
        es6 -> es5
    1)全局安装babel-cli  命令行中直接使用
        npm install babel-cli -g
        babel --version
    2)本地安装babel预设 转换规则
        babel-preset-latest
        babel-preset-es2015
        babel-preset-env
        babel-preset-react

        npm install babel-preset-latest
    3)编写配置信息
        .babelrc 放在项目的根目录中
        {
            "presets":["latest"]
        }
    4)使用babel进行转码
        1.编写es6的代码
        2.使用babel进行转码
            只能转码新语法，无法转码新功能

            babel hello.js --out-file hello.out.js
            或
            babel src --out-dir dist
        3.运行转码后文件
4.babel 的本地使用
    1) 本地安装
         npm install --save-dev babel-cli (相机)
         npm install --save-dev babel-preset-latest (镜头)
    2) 添加配置信息 (指定镜头)
        .babelrc
        {
            "presets":["latest"]
        }
    3)在package.json中添加脚本 (自动聚焦)
        {
            "scripts":{
                //"dev":"",
                "build":"babel src --out-dir dist"
            }
        }
    4)执行转换 (拍照)
        npm run build

5.变量
   1）let 申明变量 （var）
        1）let 声明的变量只在let命令所在的代码块中有效  存在局部作用域
        2）不存在变量提升
        3）不予许重复声明   let声明的变量只能声明一次
        4）暂时性死区  
    2）const
        具有所有let的特性
        1)声明变量必须显示初始化
        2）不允许重复赋值 只读
6.解构
    把一个完整的值解开，分给不同的变量
    var a = 3;
    var b = {name:'terry',age:123};
    一个表达式可以完成多个变量的赋值操作
    1）数组解构
        var arr = ['merry','larry','tom'];
        var a = arr[0];
        var b = arr[1];
        var c = arr[2];

        =>
        es6
        let[abc] = arr;
        