---
title: Inbox
---

## [[Babel]]
### babel-plugin-bulk-import 插件
用于批量 import，语法类似[[glob]]
```
import * as Features from './features/*.js'
/* Features would be
    {
        featureA: {feature: 'A'}, // featureA.js
        featureB: {feature: 'B'} // featureB.js
    }
*/
```
## [[React]]
### 从后台拉取数据，通过 Props 传给某个组件，需要一个和数据配套的 key 赋给组件，数据变化之后 key 跟着变。不能 key 先变再改变数据
```
const [data, setData] = useState(null);
// 用来控制 DataView 的销毁与构建
const [dataId, setDataId] = useState('');
const getData = () => {
  fetchData().then((res) => {
    setData(res.data);
    // 不能交换这两个的位置
    setDataId(res.data.id);
  });
};
return (
  <DataView key={dataId} />
)
```
上面的例子也可以直接改成 `const dataId = data.id`，上面的例子更适用 `dataId` 不能由 `data` 推导出的情况
### 由 create-react-app 创建的项目开发过程中有 [[eslint]] 检查，非常影响开发体验，可以用以下方式关掉
```shell
cross-env DISABLE_ESLINT_PLUGIN=true yarn start
```
## #bookmark Windows 10 自带输入法安装小鹤双拼
https://iwenson.com/%E5%B0%8F%E9%B9%A4%E5%8F%8C%E6%8B%BC.reg
## [[CSS]]
### 多行省略号
```CSS
.text {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
```
## [[Vim]]
### #bookmark [Vim宏录制与重复操作-Vim入门教程(28) | vim教程网](https://vimjc.com/vim-recording.html)
### 使用系统剪贴板
`set clipboard=unnamed`
### Neovim 配置文件地址
`vim ~/.config/nvim/init.vim`
