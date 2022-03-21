# css 记录

- ## css实现网格背景

    ![效果图](https://s2.ax1x.com/2019/10/09/u4gKGn.png)

    ```
    <div class="bg-grid"></div>

    .bg-grid {
        margin-top: 20px;
        width: 200px;
        height: 200px;
        background-image: linear-gradient(rgba(255, 255, 255, 1) 2px, transparent 0), linear-gradient(to right, rgba(255, 255, 255, 1) 2px, transparent 0), linear-gradient(rgba(255, 255, 255, 0.2) 1px, transparent 0), linear-gradient(to right, rgba(255, 255, 255, 0.2) 1px, transparent 0);
        background-position: -50px -50px;
        background-size: 100px 100px, 100px 100px, 100% 10px, 10px 100%;
    }
    ```

    **Tips**
    [linear-gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/linear-gradient)

- ## 多行文本超出隐藏

    ![效果图](https://s2.ax1x.com/2019/10/09/u4fIpj.png)

    ```
    .news-text {
        width: calc(100% - 63px);
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        /*! autoprefixer: off */
        -webkit-box-orient: vertical;
    }
    ```
    **Tips**
    [-webkit-line-clamp](https://developer.mozilla.org/en-US/docs/Web/CSS/-webkit-line-clamp)

- ## 滤镜灰度效果
    `filter: grayscale(100%);`

- ## 设置等宽数字（用于展示数字实时变动的情况）
  ```
  .yourcssclass {
    font-variant-numeric: tabular-nums;
  }
  ```