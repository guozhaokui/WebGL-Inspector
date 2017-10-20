
1. html的head中加
```html
        <script type="text/javascript" src="core/lib/gli.all.js"></script>
        <link rel="stylesheet" href="core/lib/gli.all.css"></head>
```
2. 创建webglctx之前
```javascript
if(window['gli']) gli.setupContext();
```

