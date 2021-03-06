# f2react

简单封装 [F2](https://antv.alipay.com/zh-cn/f2/3.x/index.html) 以便在React中使用.

[![NPM version][npm-image]][npm-url]
[![npm download][download-image]][download-url]

[npm-image]: http://img.shields.io/npm/v/f2react.svg?style=flat-square
[npm-url]: http://npmjs.org/package/f2react
[download-image]: https://img.shields.io/npm/dm/f2react.svg?style=flat-square
[download-url]: https://npmjs.org/package/f2react

## 示例Demo

- [简单使用及自适应宽度的例子](https://github.com/beautycss/f2react/tree/master/examples)
- [结合Antd Mobile和Dva的例子](https://github.com/beautycss/antd-mobile-dva-f2)

## 组件安装
```bash
$ npm i @antv/f2 --save
$ npm i f2react --save
```

## 组件使用

```js
import React, { Component } from 'react';
import createF2 from 'f2react';

const data = [
  { x: '1951 年', y: 38 },
  { x: '1952 年', y: 52 },
  { x: '1956 年', y: 61 },
  { x: '1957 年', y: 145 },
  { x: '1958 年', y: 48 },
  { x: '1959 年', y: 38 },
  { x: '1960 年', y: 38 },
  { x: '1962 年', y: 38 },
];

const Bar = createF2((chart) => {
  chart.interval().position('x*y');
  chart.render();
});

React.render(
  <Bar
    width={this.state.width}
    height={this.state.height}
    data={data}
  />
);
```
若在React工程中使用，建议看`examples`里的例子。

## 属性说明

<table class="table table-bordered table-striped">
  <thead>
    <tr>
        <th style="width: 100px;">名称</th>
        <th style="width: 50px;">类型</th>
        <th style="width: 100px;">默认值</th>
        <th>描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>width</td>
      <td>number(必须，若不使用autoWidth组件)</td>
      <td></td>
      <td>图表宽度</td>
    </tr>
    <tr>
      <td>height</td>
      <td>number(必须)</td>
      <td></td>
      <td>图表高度</td>
    </tr>
    <tr>
      <td>data</td>
      <td>arrayOf(object) (必须)</td>
      <td></td>
      <td>数据源</td>
    </tr>
    <tr>
      <td>configs</td>
      <td>any</td>
      <td></td>
      <td>createF2((chart, configs))中的参数</td>
    </tr>
  </tbody>
</table>

* 图表详细使用请查看 [F2官方API](https://antv.alipay.com/zh-cn/f2/3.x/api/index.html)
