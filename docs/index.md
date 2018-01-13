# 风格

## 通用排版

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

9. 使用单引号

    理由：排版更清爽，更多是习惯问题。

    [ESLint](https://eslint.org/docs/rules/quotes)：`"quotes": ["error", "single"]`

10. 在任何情况下，不能在行首使用逗号，而是行尾

    理由：习惯问题，大多数开发者采用的行尾逗号。

    缺点：如果不注意，尾部逗号在老版本的 IE 中可能导致报错，变量声明中可能造成内存泄露问题。

    [ESLint](https://eslint.org/docs/rules/comma-style)：`"comma-style": ["error", "last"]`
