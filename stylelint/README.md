# stylelint

## Usage

Create a .stylelintrc at the root folder of the project, add the content below:

```js
const { stylelint } = require('@darwinia/lints/stylelint');

module.exports = stylelint;
```

## 规则

1. 禁止使用未知的 at 规则。ignore： tailwind include mixin

1. 禁止在右括号之前有空行

1. 在左括号之后必须有一个空格或空白行

1. 十六进制颜色必须使用小写

1. 十六进制颜色必须使用完整写法

1. 禁止在声明语句之前有空行

1. 数字 0 不需要带单位

1. 最大空行数 1

1. 禁止空源

1. 禁止行尾空白

1. 禁止缺少文件末尾的换行符

1. 限制小数位数：3

1. 禁止数字中的拖尾 0

1. 禁止使用未知的伪元素

1. 禁用未知的类型选择器

1. 类选择器匹配模式： /^([a-z][a-z0-9]*)(-[a-z0-9]+)*$/ 类名称必须使用kebab-case风格
