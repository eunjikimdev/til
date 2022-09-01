<h1>객체(object)안에 함수(fuction)넣기</h1>

```javascript
const myElement = document.querySelector("h1");

fuction handledBlue() {
  myElement.style.color = "blue";
}

fuction handledGreen() {
  myElement.style.color = "green";
};
  
myElement.addEventListener("click", handledBlue);
myElement.addEventListener("click", handledGreen);
```

이것을 const hello = {} 안에 정리해 넣어야 할 경우,
```javascript
const myElement = document.querySelector("h1");

const hello = {
  handledBlue: function(){
    myElement.style.color = "blue";
  },
  handledGreen: function(){
    myElement.style.color = "green";
  }
};

myElement.addEventListener("click", hello.handledBlue);
myElement.addEventListener("click", hello.handledGreen);
```

