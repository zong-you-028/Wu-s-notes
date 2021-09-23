標籤: #CSS 

---

# color

```css
color: steelblue;
color: #ba8509;
color: rgb(186, 133, 9);
```

# background

## background

```css
background: rgb(204, 229, 255);
background: url("https://images.unsplash.com/photo-1485827404703-89b55fcc595e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2000&q=80");
background: url("../img/img-1.jpg");
background: rgba(204, 229, 255, 0.4);
```

## background color

```css
background-color: rgb(0,0,0);
```

only accept color

## background image

```css
background-image: url("../img/img-1.jpg");	//works the same
```

## background repeat

```css
background-repeat: no-repeat;
background-repeat: repeat;
```

Is set to repeat by default.

當使用圖片但是圖片不夠大無法塞進去時，就會用重複的方法填滿，可以用這個 [[Property (CSS) | property]] 改善

但是圖片並不會放大塞滿整個背景，其他背景的區塊會是空的

![[css background repeat off 範例.png]]

## background size

```css
//寬 高
background-size: 50px 100px;
background-size: cover;
background-size: contain;
```

1. 設定寬和高
2. 直接設定一張圖要蓋住整個背景
3. 設定圖為最大(但不一定可以蓋住整個畫面)

---

參考資料:

[CSS tutorial - youtube](https://youtu.be/1Rs2ND1ryYc)