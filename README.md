# modal

### middle

1, 添加容器

```html
<button id="modal-btn"> click me, I make a modal</button>

<div class="modal" id="myModal">
  <div class="modal-wrapper">
  	<div class="modal-header">
  		<span class="close-btn">&times;</span>
  	 	<span class="title"></span>
  	</div>	
  	<div class="modal-content">
		<p>this is content</p>  	  
  	</div>
  	<div class="modal-footer">
  		<input type="button" id="btn2">
  		<input type="button" id="btn1">
  	</div>
  </div>
</div>
```

2, 依次引入css、js

```
<link rel="stylesheet" href="modal.m.css">
```
```
<script src="modal.js"></script>
```

3, 编辑js: 实例化Modal

```js
window.onload = function() {
    document.querySelector("#modal-btn").onclick = function () {
      var myModal = document.querySelector("#myModal")
      myModal.style.display = "block"
      var modal = new Modal(myModal,{
        show_btn1:true, //btn1 是否可见
        show_btn2:true,	//btn2 是否可见
        title:"remove tag", //title
        btn1_value: "cancel", //btn1 name
        btn2_value: "confirm", //btn2 name
        func1: function () {
          //when clicked btn1, func1 will be execute
          console.log("func1")
        },
        func2:function() {
         //when clicked btn2, func2 will be execute
          console.log("func2")
        },
      })
    }
}
```

### right

1, 添加容器

```html
<button id="modal-btn"> click me, I make a modal</button>

<div class="modal" id="myModal">
  <div class="modal-wrapper">
  	<div class="modal-header">
  		<span class="close-btn">&times;</span>
  	 	<span class="title"></span>
  	</div>	
  	<div class="modal-content">
		<p>this is content</p>  	  
  	</div>
  	<div class="modal-footer">
  		<input type="button" id="btn2">
  		<input type="button" id="btn1">
  	</div>
  </div>
</div>
```

2, 依次引入css、js

```
<link rel="stylesheet" href="modal.r.css">
```
```
<script src="modal.js"></script>
```

3, 编辑js: 实例化Modal

```js
window.onload = function() {
    document.querySelector("#modal-btn").onclick = function () {
      var myModal = document.querySelector("#myModal")
      myModal.style.display = "block"
      var modal = new Modal(myModal,{
        show_btn1:true, //btn1 是否可见
        show_btn2:true,	//btn2 是否可见
        title:"remove tag", //title
        btn1_value: "cancel", //btn1 name
        btn2_value: "confirm", //btn2 name
        func1: function () {
          //when clicked btn1, func1 will be execute
          console.log("func1")
        },
        func2:function() {
         //when clicked btn2, func2 will be execute
          console.log("func2")
        },
      })
    }
}
```