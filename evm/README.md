## 运行项目
```
npm i
```

## zksync
```bash
yarn add zksync
yarn add ethers # ethers is a peer dependency of zksync

yarn add init 
```

## ES6
```bash
npm install eslint --save-dev
# 初始化eslint
./node_modules/.bin/eslint --init
# 
./node_modules/.bin/eslint --fix-dry-run --ext  js ./
./node_modules/.bin/eslint --fix --ext  js ./

# npm运行node项目, 需要babel编译, 才能支持import等高级语法;
npm install --save babel-core
npm install --save babel-preset-env 
npm install babel-cli -g
```

- vi .babelrc
```json
{                
    "presets": [ 
         "env"   
     ],          
    "plugins": []
}
```

- vi package.json
```json
{
    "type":"module", // 设置使用es6模块模式，默认commonJS
    "dependencies": {
        "ethers": "^5.7.2",
        "zksync": "^0.13.1"
    },
    "scripts": {
        "start":"babel-node main.js"
    },
}

```

## 参考文档
- https://docs.zksync.io/api/sdk/