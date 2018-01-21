## 语法

### 多余的

### 避免错误（以下规则本身有可能引起错误，所以大部分都是必要的，理由不再赘述）

- 不给 const 声明的变量赋值

    [ESLint](https://eslint.org/docs/rules/no-const-assign)：`"no-const-assign": "error"`

- 不允许重复的类成员

    [ESLint](https://eslint.org/docs/rules/no-dupe-class-members)：`"no-dupe-class-members": "error"`

- 不允许重复导入 import

    [ESLint](https://eslint.org/docs/rules/no-var)：`"no-var": "error"`

- getter 必须有 return 值

    [ESLint](https://eslint.org/docs/rules/getter-return)：`"getter-return": "error"`

- 不允许在循环语句中使用 await，而是使用 promise.all 代替

    [ESLint](https://eslint.org/docs/rules/no-await-in-loop)：`"no-await-in-loop": "error"`

- 不用和 -0 比较，使用 Object.is(x, -0)

    [ESLint](https://eslint.org/docs/rules/no-compare-neg-zero)：`"no-compare-neg-zero": "error"`

- 不要在条件语句中赋值，因为大部分情况下是写错了

    [ESLint](https://eslint.org/docs/rules/no-cond-assign)：`"no-cond-assign": "error"`

- for 循环计数器方向必须正确，以免进入死循环

    [ESLint](https://eslint.org/docs/rules/for-direction)：`"for-direction": "error"`

### ES6+

- 不允许使用 var

    理由： var 声明的变量，作用域为当前块或者全局，容易造成变量污染；二来，var 声明的变量会提升作用域，容易给开发者带来困惑。

    缺点：一个变量如果需要在不同的作用域内使用时，比如一个块和它的父级，则需要先再父级作用域声明后再在块中赋值。

    [ESLint](https://eslint.org/docs/rules/no-duplicate-imports)：`"no-duplicate-imports": "error"`

- 如果变量不会再被改变，则必须使用 const 声明

    理由：增强代码的可读性。

    缺点：暂时没找到缺点。

    [ESLint](https://eslint.org/docs/rules/prefer-const)：`"prefer-const": "error"`

- 回调尽量使用箭头函数，但允许在使用命名函数以及函数内用到自引用 this 的时候使用 function 回调函数

    理由：箭头函数更加简洁，可读性更强。

    缺点：自引用绑定至词法作用域。

    [ESLint](https://eslint.org/docs/rules/prefer-arrow-callback)：`"prefer-arrow-callback": ["error", { "allowNamedFunctions": true }]`

- 对象字面量方法使用简写形式

    理由：跟上一条规则相同，简写简写，显得更简洁。

    [ESLint](https://eslint.org/docs/rules/object-shorthand)：`"object-shorthand": "error"`
