---
title: React
tags: 前端
---

- 从后台拉取数据，通过 Props 传给某个组件，需要一个和数据配套的 key 赋给组件，数据变化之后 key 跟着变。不能 key 先变再改变数据
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
- 由 create-react-app 创建的项目开发过程中有 [[eslint]] 检查，非常影响开发体验，可以用以下方式关掉
  ```shell
  cross-env DISABLE_ESLINT_PLUGIN=true yarn start
  ```