# vue-print-nb-update
对vue-print-nb的修改，更新

## 2020-09-16
添加了成功打开预览界面之前的回调（用来隐藏不需要打印的Dom），成功打开预览界面之后的回调（显示隐藏的Dom），点击打印或者取消后的回调（一般前面两个就够用了）


# 原作者是Power-kxLee。这个组件在github上的地址：https://github.com/Power-kxLee/vue-print-nb


# 原作者的教程：

# vue-print-nb

This is a directive wrapper for printed, Simple, fast, convenient, light.

## Install

#### NPM
```bash
npm install vue-print-nb --save
```

```javascript
import Print from 'vue-print-nb'

Vue.use(Print);
```
## Run demo
Download the project, install dependencies, run demo
```
npm run serve
-Local:   http://localhost:8080/
```

## Description

#### Print the entire page:

```
<button v-print>Print the entire page</button>
```


#### Print local range:

HTML:
```
    <div id="printMe" style="background:red;">
        <p>葫芦娃，葫芦娃</p>
        <p>一根藤上七朵花 </p>
        <p>小小树藤是我家 啦啦啦啦 </p>
        <p>叮当当咚咚当当　浇不大</p>
        <p> 叮当当咚咚当当 是我家</p>
        <p> 啦啦啦啦</p>
        <p>...</p>
    </div>

    <button v-print="'#printMe'">Print local range</button>
```
Pass in a string type directly
* `id`: ID of local print range

#### More
HTML:
```
 <button v-print="printObj">Print local range</button>
 
  <div id="printMe" style="background:red;">
        <p>葫芦娃，葫芦娃</p>
        <p>一根藤上七朵花 </p>
        <p>小小树藤是我家 啦啦啦啦 </p>
        <p>叮当当咚咚当当　浇不大</p>
        <p> 叮当当咚咚当当 是我家</p>
        <p> 啦啦啦啦</p>
        <p>...</p>
    </div>
```
JavaScript:
```
export default {
    data() {
        return {
            printObj: {
              id: "printMe",
              popTitle: 'good print',
              extraCss: 'https://www.google.com,https://www.google.com',
              extraHead: '<meta http-equiv="Content-Language"content="zh-cn"/>'
            }
        };
    }
}
```
You can also pass in an object type `Objcet`

### API
* `id`:  *requisite Partial printing of the incoming ID
* `standard`: Document type, default is html5, optional `html5`, `loose`, `strict`
* `extraHead`: Additional tags attached to the head tag, separated by commas
* `extraCss`:  Additional link connections, separated by commas
* `popTitle`: Title shows the title
* `endCallback()`: Callback events after printing
## License

[MIT](http://opensource.org/licenses/MIT)