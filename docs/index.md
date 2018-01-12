# 风格

## 通用排版

1. 使用空格而不是 tab 缩进。
理由：tab 宽度不可控。
[ESLint](https://eslint.org/docs/rules/indent)

2. 缩进大小为四个空格。
理由：可读性更强，代码嵌套层级一目了然。
缺点：缩进占用了更多的空间。
[ESLint](https://eslint.org/docs/rules/indent)：`indent: ["error", 4]`

3. 强制分号
理由：不要依赖于 ASI，部分情况必须使用分行。
缺点：美观度，看个人喜好。
[ESLint](https://eslint.org/docs/rules/semi)：`semi: ["error", "always"]`

4. 不能连续空格
理由：浪费空间。
缺点：没有缺点。
[ESLint](https://eslint.org/docs/rules/no-multi-spaces)：`no-multi-spaces: "error"`

5. 禁止使用 tab
理由：使用 tab 容易造成代码排版不可控。
缺点：应该没有什么地方一定要使用 tab 吧。
[ESLint](https://eslint.org/docs/rules/no-tabs)：`no-tabs: "error"`
[ESLint](https://eslint.org/docs/rules/no-mixed-spaces-and-tabs)：`no-mixed-spaces-and-tabs: "error"`
