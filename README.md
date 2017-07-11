---
title: 前端规范
date: 2017-07-10 19:54:14
note: 2017-07-10 19:54:14 第一次制定
---



# 前言

既然制定了规范，就需要严格遵守。

如果觉得不合理或者想做贡献，请提出issue。

# 前端规范

## JS

- 用'===', '!=='代替'==', '!='；	


- 引号
  - 最外层统一使用单引号

- 变量
  - s：表示字符串。例如：sName，sHtml；

  - n：表示数字。例如：nPage，nTotal；

  - is：表示逻辑。例如：bChecked，bHasLogin；

  - a：表示数组。例如：aList，aGroup；

  - r：表示正则表达式。例如：rDomain，rEmail；

  - fn：表示函数。例如：fnGetHtml，fnInit；

    - **某事件响应函数命名方式为fn+触发事件对象名+事件名或者模块名**，例如：fnDivClick()，fnAddressSubmitButtonClick()

    - 如果有内部函数，使用_fn+动词+名词形式，内部函数必需在函数最后定义，例如：

      ```javascript
      function fnGetNumber(nTotal) {
          if (nTotal < 100) {
              nTotal = 100;
          }
          return _fnAdd(nTotal);
       
          function _fnAdd(nNumber) {
              nNumber = nNumber + 1;
              return nNumber;
          }
      }
      alert(fnGetNumber(10)); //alert 101
      ```

  - o：表示以上未涉及到的其他对象，例如：oButton，oDate；

  - g：表示全局变量，例如：gUserName，gLoginTime；

  - $：表示Jquery对象。例如：$Content，$Module；

  - dom：表示Dom对象，例如：domForm，domInput；

  - 对齐方式，使用sublime对齐插件Alignment用来方便对齐(https://www.granneman.com/webdev/editors/sublime-text/packages/how-to-install-and-use-sublime-alignment/)：

    ```javascript
     var client        = require('util-restify');
     var log4js        = require('log4js');
     var logger        = log4js.getLogger();                    
    ```

  - 变量申明放在顶部，使用逗号隔开换行而不是每一行重新new，例如：

    ```javascript
    var a = 1,
        b = 2
    ```


- 面向对象规范

  - 待添加

- 注释规范

  - 函数 

    ```javascript
    /**
     * @func
     * @desc 一个带参数的函数
     * @param {string} a - 参数a
     * @param {number} b=1 - 参数b默认值为1
     * @param {string} c=1 - 参数c有两种支持的取值</br>1—表示x</br>2—表示xx
     * @param {object} d - 参数d为一个对象
     * @param {string} d.e - 参数d的e属性
     * @param {string} d.f - 参数d的f属性
     * @param {object[]} g - 参数g为一个对象数组
     * @param {string} g.h - 参数g数组中一项的h属性
     * @param {string} g.i - 参数g数组中一项的i属性
     * @param {string} [j] - 参数j是一个可选参数
     * @return {[undefined]} - [副作用]
     */
    function foo(a, b, c, d, g, j) {
        ...
    }
    ```

- 异步
  - 禁止回调地狱出现，采用更加优雅的Promise方案或者Generator方案

- 其他
  - 需要尽力减少全局变量污染，所有模块请用()()立即执行函数包裹
  - 通用功能请用模块化的写法进行抽象，以便复用
  - 禁止使用分号，需要使用分号的具体情况只有这五个符号：+、 - 、(、 [、 /，也就是说，凡是新的一行代码以上述五个符号开头，那么之前一句的末尾是需要分号的，而在实际情况中，以+，- 开头的新一行代码几乎不可能出现
  - 开发过程中打印的日志请在调试完毕后删除或者注释
  - 代码空行不超过1行
  - 禁止使用++i、i++这种简化书写却增加理解难度的代码

## Css

- 遵守BEM命名规范



- 使用SASS进行Css模块化实践



- 建议的命名规范：.page-head {}.sub-content {}，拒绝：.pageHead {} .sub_content {}


## 命名规则

### 项目命名

全部采用小写方式， 以下划线分隔。例：my_project_name

### 目录命名

参照项目命名规则；有复数结构时，要采用复数命名法。例：scripts, styles, images, data_models

### JS文件命名

参照项目命名规则。例：account_model.js

### CSS, SCSS文件命名

参照项目命名规则。例：retina_sprites.scss

### HTML文件命名

参照项目命名规则。例：error_report.html

## 其他

- 每天进行code review
- 代码review完之后才能提交测试(对时间要求比较着急的需求才可以绕过此限制)
- 必须对自己负责的issue跟到底
- 测试有权拒绝测试烂代码
- 前端有权拒绝对接不通过测试的后台接口
- 前端有权要求增加工时以交付更加优质的代码



## 前端最基本要求：

- 适配手机端


- 前端要参与到产品设计中去


- 一次性的开发任务也必须严格遵守本规范



## 每周前端例会

-新需求完成情况

-代码优化情况

-新技术学习分享

-issue跟进情况，owner





