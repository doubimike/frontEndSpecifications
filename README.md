# 前端规范

## JS

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
              nNumber++;
              return nNumber;
          }
      }
      alert(fGetNumber(10)); //alert 101
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
    var a =1,
        b =2
    ```


- 面向对象规范

  - 待添加

- 注释规范

  - 函数 

    ```javascript
    /**
     * [fnGetWithdrawResult 轮询后台查看提现结果]
     * @param  {[str]} sOrderNo   [订单号]
     * @param  {[str]} sTimeoutId [定时器ID]
     * @return {[null]}            [副作用]
     */
    function fnGetWithdrawResult(sOrderNo, sTimeoutId) {}
    ```

- 异步
  - 禁止回调地狱出现，采用更加优雅的Promise方案或者Generator方案

- 其他
  - 需要尽力减少全局变量污染，所有模块请用()()立即执行函数包裹
  - 通用功能请用模块化的写法进行抽象，以便复用
  - 禁止使用分号？
  - 开发过程中打印的日志请在调试完毕后删除或者注释
  - 代码空行不超过1行
  - 禁止使用++i、i++这种简化书写却增加理解难度的代码

## Css

- 遵守BEM命名规范



- 使用SASS进行Css模块化实践



- 建议的命名规范：.page-head {}.sub-content {}，拒绝：.pageHead {} .sub_content {}



## 其他

- 每天进行code review
- 优化流程：建立issue，命名标准 22-mike-optimised-detail，优化完毕尽早，代码审核完之后才能提交测试
- 必须对自己负责的issue跟到底
- 测试有权拒绝测试烂代码
- 前端有权拒绝对接不通过测试的后台接口
- 前端有权要求增加工时以交付更加优质的代码



## 前端最基本要求：

- 适配手机端


- 前端要参与到产品设计中去


- 一次性的开发任务也必须严格要求自己



## 每周前端例会

-新需求完成情况

-代码优化情况

-新技术学习分享

-issue跟进情况，owner





