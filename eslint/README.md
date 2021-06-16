# eslint

## Usage

In the eslint.json that you want to extends the rules of '@darwinia/lints/eslint', add the content below:

```json
{
  "extends": ["@darwinia/lints/eslint"],
  // ... other rules to be override.
}
```

## 规则

### 可读、可维护

1. 圈复杂度：函数的复杂度默认设置在5级，超出后则应该考虑重构函数，如果确实需要突破此复杂度，请在代码中使用注释

1. 禁用key名：error, any, Number, number, String, string, Boolean, boolean, Undefined, undefined

1. import顺序：有序排列

1. jsdoc风格的注释需要：对齐、统一缩进、描述语句后使用空行分隔、**不要**注释类型（TS对于类型本身就有自释性），'/'或'*' 后有空格

1. 行最大长度：120字符，但对于特殊内容忽略检查，如 url， 注释， 正则表达式等

1. this关键字：在对象和class外禁止使用

1. 魔鬼数字：除 0，1，-1，10 之外的数字，都就使用变量表达其意图

1. 禁止出现未使用的表达式及变量：忽略 “_” 开头的变量

1. 始终使用对象键值对的简写语法

1. 变量遮蔽：在关联作用域上避免出现同名变量

1. 变量声明：每个变量使用单独的关键字声明

1. 变量声明优先const：如果变量没有被重新赋值，必须使用const声明

1. 大括号位置：左：当前语句末尾，右：独占一行

1. 属性的引号：只在必要的时候使用带引号的属性名

### 健壮性

1. 相等：始终使用全等判断

1. for in 循环守卫：始终判断 hasOwnProperty

1. import 弃用检查：警告提示

1. for of：TS中优先使用for of循环

1. react hooks：必须符合hooks的使用规则，deps检查报 warning

### JS / TS特性

1. 位操作：js对位操作效率较低，如必须使用从头再来操作使用注释

1. arguments对象：禁止使用，实际上在es6里也没有必要使用

1. var关键字：禁止使用

1. parseInt：必须显示指明基数

1. 尾部分号：语句末尾始终使用分号

1. TS类的属性的可访问性：省略 public

1. TS 导出函数或类的公有方法的返回类型：只在必要的时候指定（推断类型与预期不符合时）

1. 使用函数类型而不是带有调用签名的接口

### 利于Review - 最小化代码更改

1. 箭头函数的参数：始终使用括号包围

1. 尾部逗号：函数不允许出现尾部括号；数据、对象、import、export 如果是多行时必须保留尾部逗号，否则不能出现尾部括号

### 安全性及其它

1. console：只保留必要的console，其它用于开发时调试目的的console在上线前都应该被删除

1. eval：禁止使用，严重的安全隐患

1. 禁止抛出字符错误

1. TS 的 /// 引用应该位于import 之前
