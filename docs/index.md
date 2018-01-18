# 风格

## 通用排版（与代码内容无关）

1. 使用空格而不是 tab 缩进。

    理由：tab 宽度不可控。

    [ESLint](https://eslint.org/docs/rules/indent)

2. 缩进大小为四个空格。

    理由：可读性更强，代码嵌套层级一目了然。

    缺点：缩进占用了更多的空间。

    [ESLint](https://eslint.org/docs/rules/indent)：`"indent": ["error", 4]`

3. 禁止使用 tab

    理由：使用 tab 容易造成代码排版不可控。

    缺点：应该没有什么地方一定要使用 tab 吧。

    [ESLint](https://eslint.org/docs/rules/no-tabs)：`"no-tabs": "error"`

    [ESLint](https://eslint.org/docs/rules/no-mixed-spaces-and-tabs)：`"no-mixed-spaces-and-tabs": "error"`

4. 强制分号

    理由：不要依赖于 ASI，部分情况必须使用分行。

    缺点：美观度，看个人喜好。

    [ESLint](https://eslint.org/docs/rules/semi)：`"semi": ["error", "always"]`

5. 不能连续空格

    理由：浪费空间。

    缺点：没有缺点。

    [ESLint](https://eslint.org/docs/rules/no-multi-spaces)：`"no-multi-spaces": "error"`

6. 行尾或空行不能有多余的空格

    理由：Diff 时容易使开发者误解。

    [ESLint](https://eslint.org/docs/rules/no-trailing-spaces)：`"no-trailing-spaces": "error"`

7. 不能连续空行，并且文件开头不能空行。

    理由：浪费空间。

    缺点：部分开发者可能会习惯在代码块之间空两行，习惯问题。

    [ESLint](https://eslint.org/docs/rules/no-multiple-empty-lines)：`"no-multiple-empty-lines": ["error", { "max": 1, "maxEOF": 1, "maxBOF": 0 }]`

8. 文件末尾空一行

    理由：让自己心里舒坦点，当然这也是常见的 UNIX 风格。

    缺点：浪费空间。

    [ESLint](https://eslint.org/docs/rules/eol-last)：`"eol-last": ["error", "always"]`

9. 尽量使用单引号

    理由：排版更清爽，更多是习惯问题。

    [ESLint](https://eslint.org/docs/rules/quotes)：`"quotes": ["error", "single"]`

10. 在任何情况下，不能在行首使用逗号，而是行尾

    理由：习惯问题，大多数开发者采用的行尾逗号。

    缺点：如果不注意，尾部逗号在老版本的 IE 中可能导致报错，变量声明中可能造成内存泄露问题。

    [ESLint](https://eslint.org/docs/rules/comma-style)：`"comma-style": ["error", "last"]`

11. 逗号后空一格

    理由：空一格使得可读性更强。

    缺点：浪费空间。

    [ESLint](https://eslint.org/docs/rules/comma-spacing)：`"comma-spacing": “error”`

12. 单行最多 120 个字符

    理由：单行过多不好，但是太少，像习惯性地设置成80也会太少，因为现在一个缩进就四个空格了，还有一个理由是 github 单行最多放下 <130 个字符。

    缺点：有时候真的还是单行更好排版，写代码时候回非常纠结。

    [ESLint](https://eslint.org/docs/rules/max-len)：`"max-len": ["error", { "code": 120 }]`


---


## 通用语句格式（与代码内容有关）

1. 每行只能有一条进行变量初始化的声明语句

    理由：可读性更强。

    缺点：增加了行数？

    [ESLint](https://eslint.org/docs/rules/one-var-declaration-per-line)：`"one-var-declaration-per-line": ["error", "initializations"]`

2. 每行只能有一条语句，不包括声明简写形式

    理由：可读性更强，排版更美观。

    缺点：增加了行数？

    [ESLint](https://eslint.org/docs/rules/max-statements-per-line)：`"max-statements-per-line": ["error", { "max": 1 }]`

3. 一元操作符后必须有一个空格，如果是关键字则不需要

    理由：习惯写法，阅读者更好懂。

    [ESLint](https://eslint.org/docs/rules/space-unary-ops)：`"space-unary-ops": "error"`

4. 两元操作符后前后必须有一个空格

    理由：可读性更强，排版更美观。

    缺点：习惯性问题。

    [ESLint](https://eslint.org/docs/rules/space-infix-ops)：`"space-infix-ops": "error"`

5. 关键字前后必须留一个空格

    理由：可读性更强，排版更美观。

    缺点：习惯性问题。

    [ESLint](https://eslint.org/docs/rules/keyword-spacing)：`"keyword-spacing": "error"`

6. 强制驼峰命名

    理由：习惯性写法。

    缺点：实际开发中难以统一，需要与后端协调。

    [ESLint](https://eslint.org/docs/rules/camelcase)：`"camelcase": "error"`

7. 大括号（代码块）前总是需要一个空格

    理由：个人习惯，多一个空格不会显得那么挤。

    缺点：习惯问题。

    [ESLint](https://eslint.org/docs/rules/space-before-blocks)：`"space-before-blocks": "error"`

8. 大于两级的链式调用必须换行

    理由：调用层级更加清晰，可读性更强。

    缺点：浪费空间？

    [ESLint](https://eslint.org/docs/rules/newline-per-chained-call)：`"newline-per-chained-call": ["error", { "ignoreChainWithDepth": 2 }]`

9. 冒号后必须加空格，而前面不能加

    理由：习惯问题，也是大多数人的习惯，可读性更强。

    缺点：习惯问题。

    [ESLint](https://eslint.org/docs/rules/semi-spacing)：`"semi-spacing": "error"`

10. 采用 1tbs(one true brace style) 大括号风格（大括号与关键字同行）

    理由：排版足够清晰且节省空间，也是大多数人的习惯。

    [ESLint](https://eslint.org/docs/rules/brace-style)：`"brace-style": "error"`

11. 所有语句块都需要大括号（警告）

    理由：便于维护。

    缺点：排版不够简单。

    [ESLint](https://eslint.org/docs/rules/curly-style)：`"curly-style": "warn"`


---


## 特定格式 -- 函数

1. 函数声明函数名与参数左括号间不空格

    理由：虽然纠结了很久，空格与不空格都使用过，最后还是选择了不空格，个人选择而已。

    [ESLint](https://eslint.org/docs/rules/space-before-function-paren)：`"space-before-function-paren": ["error", "never"]`

2. 函数调用函数名与括号间不允许空格

    理由：习惯 + 排版，并且容易给代码阅读者造成困惑。

    [ESLint](https://eslint.org/docs/rules/func-call-spacing)：`"func-call-spacing": "error"`

3. 大括号与声明同行

    理由：习惯。

    [ESLint](https://eslint.org/docs/rules/function-paren-newline)：`"function-paren-newline": ["error", "never"]`

4. 使用函数声明而不是函数表达式（警告）

    理由：保持风格的统一，并且可以利用函数作用域提升的特性。

    缺点：函数作用域提升容易造成读者的困惑。

    [ESLint](https://eslint.org/docs/rules/func-style)：`"func-style": ["warn", "declaration"]`


---

## 特定格式 -- 对象

1. 对象字面量属性键名冒号后需加一空格，冒号前不允许有空格

    理由：个人觉得这样排版更整洁，也是大多数人的习惯吧。

    [ESLint](https://eslint.org/docs/rules/key-spacing)：`"key-spacing": “error”`

2. 对象字面量，若属性有换行，则括号也都换号；若没有则都不换行。

    理由：排版更加统一以及整洁。

    [ESLint](https://eslint.org/docs/rules/object-curly-newline)：`"object-curly-newline": “error”`

3. 对象字面量，属性键值对与两个括号间永远都留一空格，除了空对象

    理由：边界分割更加清楚。

    缺点：有时候觉得有点多余，排版不紧凑。

    [ESLint](https://eslint.org/docs/rules/object-curly-spacing)：`"object-curly-spacing": [“error”, "always"]`

4. 对象不能在同一行定义多个属性

    理由：可读性更好，并且 diff 更好定位。

    [ESLint](https://eslint.org/docs/rules/object-property-newline)：`"object-property-newline": "error"`

5. 只有在需要时才允许对象属性使用引号

    理由：精简代码。

    缺点：开发者容易造成困惑，也会比较烦吧。

    [ESLint](https://eslint.org/docs/rules/quote-props)：`"quote-props": ["error", "as-needed"]`

---

## 空行规则（https://eslint.org/docs/rules/padding-line-between-statements）

1. return 前必须空行
2. 类前后必须空行
3. export 前必须空行

以上在 ESLint 中规则配置为：

```json
{
    "padding-line-between-statements": [
        "error",
        { "blankLine": "always" , "prev": "*", "next": "return" },
        { "blankLine": "always" , "prev": "*", "next": "class" },
        { "blankLine": "always" , "prev": "class", "next": "any" },
        { "blankLine": "always" , "prev": "*", "next": "export" },
    ]
}
```

## 其他规则

1. 类声明块中收尾空一行

    理由：边界清晰，增强可读性。

    缺点：浪费空间。

    [ESLint](https://eslint.org/docs/rules/padded-blocks)：`"padded-blocks": ["error", { “classes”: "error" }]`
