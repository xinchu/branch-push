## Install

```console
$ npm install branch-push
```


## Usage
### 说明.默认远端分支名称为`dist`, 默认 `git origin url`为当前`.git config`里的远端库地址
```js
import branch from 'branch-push';
```
## Example
```js

//指定目录，默认dist分支，默认使用已有的远端库
branch('./dist')
  .then(()=>{
  console.log('OK');
  })
  .catch(e=>{
    //print error
    console.log( e );
  });

//指定目录，指定分支，默认使用已有的远端库
branch('./dist', 'deploy')
  .then(()=>{
  console.log('OK');
  })
  .catch(e=>{
    //print error
    console.log( e );
  });

//指定目录，指定分支，指定远端
branch('./dist', 'deploy', 'git@github.com:xinchu/branch-push.git')
  .then(()=>{
    console.log('OK');
  })
  .catch(e=>{
    //print error
    console.log( e );
  });

```

## 常用项目的例子
```angularjs
    angular demo
```
```react
    react   demo
```
```vue
    vue    demo
```

## API

### chalk.`<style>[.<style>...](string, [string...])`

Example: `chalk.red.bold.underline('Hello', 'world');`

Chain [styles](#styles) and call the last one as a method with a string argument. Order doesn't matter, and later styles take precedent in case of a conflict. This simply means that `chalk.red.yellow.green` is equivalent to `chalk.green`.

Multiple arguments will be separated by space.

### chalk.enabled

Color support is automatically detected, as is the level (see `chalk.level`). However, if you'd like to simply enable/disable Chalk, you can do so via the `.enabled` property.

Chalk is enabled by default unless expicitly disabled via the constructor or `chalk.level` is `0`.

If you need to change this in a reusable module, create a new instance:

```js
const ctx = new chalk.constructor({enabled: false});
```

### chalk.level

Color support is automatically detected, but you can override it by setting the `level` property. You should however only do this in your own code as it applies globally to all Chalk consumers.

If you need to change this in a reusable module, create a new instance:

```js
const ctx = new chalk.constructor({level: 0});
```

Levels are as follows:

0. All colors disabled
1. Basic color support (16 colors)
2. 256 color support
3. Truecolor support (16 million colors)

### chalk.supportsColor

Detect whether the terminal [supports color](https://github.com/chalk/supports-color). Used internally and handled for you, but exposed for convenience.

Can be overridden by the user with the flags `--color` and `--no-color`. For situations where using `--color` is not possible, add the environment variable `FORCE_COLOR=1` to forcefully enable color or `FORCE_COLOR=0` to forcefully disable. The use of `FORCE_COLOR` overrides all other color support checks.

Explicit 256/Truecolor mode can be enabled using the `--color=256` and `--color=16m` flags, respectively.



## Maintainers

- [Sindre Sorhus](https://github.com/)
- [Josh Junon](https://github.com/)


## License

MIT
