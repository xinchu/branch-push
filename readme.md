## Install

```console
$ npm install branch-push
```


## Usage
### 默认远端分支名称为`dist`, 默认 `git origin url`为当前`.git config`里的远端库地址
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
    react demo
```
```vue
    vue demo
```

## API

### aa



### bb

### cc


## License

MIT
