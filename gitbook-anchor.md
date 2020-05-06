#### gitbook如何添加锚点，在同一页面内跳转？  


* [目录结构·gitbook使用教程](http://gitbook.zhangjikai.com/structure.html)

   * 在GitBook官网新建space
   * 概要文件主要存放 GitBook 的文件目录信息，左侧的目录就是根据这个文件来生成的，默认对应的文件是 SUMMARY.md，可以在 book.json 重新定义该文件的对应值。
        ```
        {
            "structure": {
                "readme": "SUMMARY.md"
            }
        }
        ```
   * SUMMARY.md通过 Markdown 中的列表语法来表示文件的父子关系
        ```
        #SUMMARY.md 
        * [首页](README.md)  
           * [子页面1](chp01/x1.md)
           * [子页面2](chp02/x2.md) 
      ```  
    
    

* Markdown中如何让# * >等符号原样显示，不被解析成对应的Markdown语法  
markdown 中如果遇到有字符与原有语法冲突
   * 可以使用反斜杠（'\'）转义
   * 可以使用反引号"`"包裹需要转移的内容
   * ```


* 安装gitbook
    ```
    $ npm install gitbook-cli -g
    ```

* 默认插件  
    默认带有 5 个插件：
    1. highlight
    2. search
    3. sharing
    4. font-settings
    5. livereload


* 安装插件
   * 根目录 node_modules 文件下能看到安装那些插件。
        ```
        $ gitbook install ./
        ```
   * 单独安装插件，然后写入配置
        ```
        $ npm install gitbook-plugin-anchor-navigation-ex --save
        ```

* 本地预览
   * 进入你的 GitBook 书籍目录，右击 - 服务 - 新建位于文件夹位置的终端窗口，输入命令行：
       ```
       $ gitbook serve
       ```

* 添加锚点
   * 使用html添加锚点  
      * 本地gitbook可以  
      * 线上新版本GitBook无效（https://little-cloudz.gitbook.io/sparks-frontend/20200429#anchor1)
      * 旧版GitBook gitbooks.io域名下可以（https://hltj.gitbooks.io/sandbox/content/index.html）
        ```
        触发锚点：[1](#anchor1) 
        
        锚点位置：<div id="anchor1"></div>
        ```
 
 * 使用Anchors插件 - 添加 Github 风格的锚点
 * [gitbook-plugin-anchor-navigation-expand](https://www.npmjs.com/package/gitbook-plugin-anchor-navigation-expand)
 * [gitbook-plugin-anchor-navigation-ex-custom](https://www.npmjs.com/package/gitbook-plugin-anchor-navigation-ex-custom)  
    停更
 * [vuepress](https://www.vuepress.cn/)构建笔记


