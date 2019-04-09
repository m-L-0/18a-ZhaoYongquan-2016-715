## CH6流程控制总结

### 流程控制中的API

| tf.where(condition,x=None, y=None,name=None ) | 传入一个参数：返回判断条件为真的每个元素的索引。             |
| :-------------------------------------------- | ------------------------------------------------------------ |
| **tf.identity**                               | 是用于创建张量副本的虚节点，即生成一个与输入张量相同`shape`与内容（元素）的新张量 |
| **tf.group**                                  | 用于将一系列`op`、`Tensor`组合成为一个`op`，`tf.group`没有返回值 |
| **tf.cond**                                   | 用来构建（双分支）选择结构                                   |
| **tf.case**                                   | 接收一个由`case`项组成的`list`，每个`case`项都是由条件与执行函数组成的元组。 |
| **tf.while_loop( cond, body, loop_vars）**    | 在条件cond成立时重复body。 cond是可返回的布尔标量张量；body是一个可调用的函数，它返回一个（可能是嵌套的）元组、namedtuple或者与loop_vars具有相同arity（长度和结构）和类型的张量列表；loop_vars是一个（可能是嵌套的）元组，namedtuple或被传递给cond和body的张量的列表。 |
| **tf.tuple( tensors, name=None )**            | 可以将输入的多个张量组成一个元组                             |