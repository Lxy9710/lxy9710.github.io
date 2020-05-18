---
title: "CSS知识总结"
date: 2020-04-08T22:24:47+08:00
draft: false
---

## 浏览器渲染原理
- 根据html构建html树
- 根据css构建css树
- 将两棵树合并成一棵渲染树
- layout布局（文档流，盒模型，计算大小和位置）
- paint绘制（边框颜色，文字颜色，阴影等画出来）
- compose合成（根据层叠关系展示画面）
  
三种更新方式：layout paint composite

## transition和animation
过渡的根本原则：可以实现数值变化就好。

- transiton
  
  可以为一个或者多个用数值表示的CSS属性发生变化时添加动画效果。
  
语法：

  ```
  transform: none;
  /* Function values */
transform: matrix(1.0, 2.0, 3.0, 4.0, 5.0, 6.0);
transform: translate(12px, 50%);
transform: translateX(2em);
transform: translateY(3in);
transform: scale(2, 0.5);
transform: scaleX(2);
transform: scaleY(0.5);
transform: rotate(0.5turn);
transform: skew(30deg, 20deg);
transform: skewX(30deg);
transform: skewY(1.07rad);
transform: matrix3d(1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0, 9.0, 10.0, 11.0, 12.0, 13.0, 14.0, 15.0, 16.0);
transform: translate3d(12px, 50%, 3em);
transform: translateZ(2px);
transform: scale3d(2.5, 1.2, 0.3);
transform: scaleZ(0.3);
transform: rotate3d(1, 2.0, 3.0, 10deg);
transform: rotateX(10deg);
transform: rotateY(10deg);
transform: rotateZ(10deg);
transform: perspective(17px);

/* Multiple function values */
transform: translateX(10px) rotate(10deg) translateY(5px);

/* Global values */
transform: inherit;
transform: initial;
transform: unset;

  ```

- animation
  
  时长：1s或1000ms

  过渡方式：跟transition取值一样。

  次数：3或2.4或infinite

  方向：reverse|alternate|alternate-reverse

  填充模式：none|forwards|backwards|both

  是否暂停：paused|running