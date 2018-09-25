---
order: 0
title:
  zh-CN: 基本
  en-US: Basic
---

通过设置 `x`，`y` 属性，可以快速的构建出一个漂亮的柱状图，各种纬度的关系则是通过自定义的数据展现。

```ts
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-demo',
  template: `<g2-bar height="200" [title]="'销售额趋势'" [data]="salesData"></g2-bar>`
})
export class DemoComponent implements OnInit {
  salesData: any[] = [];
  ngOnInit(): void {
    for (let i = 0; i < 12; i += 1) {
      this.salesData.push({
        x: `${i + 1}月`,
        y: Math.floor(Math.random() * 1000) + 200
      });
    }
  }
}
```