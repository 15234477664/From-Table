# From-Table
Vue中对From表单中的Table表格中的输入项进行验证

在实际使用中经常会遇到需要在From表单中使用table表格进行表单提交，同时又需要对From表单中的字段进行校验，效果如图所示：

![Image text](https://github.com/15234477664/From-Table/blob/master/img/1.png)

这个校验中，最关键的问题在于如何给el-form-item 动态绑定prop。

![Image text](https://github.com/15234477664/From-Table/blob/master/img/2.png)

js代码如下：

![Image text](https://github.com/15234477664/From-Table/blob/master/img/3.png)

上述代码中比较关键的部分有一下两点：
1、:prop="‘domains.’+scope.$index+’.name’" ，用于动态绑定prop到el-form-item；

2、this.$set(this.fromData,‘domains’,this.domains) ，用于为fromData设置domains这个节点。
