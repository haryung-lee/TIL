## 변수 (Variables)

### 동일한 type의 변수에 대해 같은 단어 사용

```jsx
// Bad
getUserInfo();
getClientData();
getCustomerRecord();

// Good
getUser();
```

### unnamed 상수에 이름 붙여주기

```jsx
// Bad
setTimeout(blastOff, 86400000);

// Good
const MILLISECONDS_PER_DAY = 60 * 60 * 24 * 1000; // 86400000
setTimeout(blastOff, MILLISECONDS_PER_DAY);
```

### 설명가능한 변수 사용하기

```jsx
// Bad
const address = "One Infinite Loop, Cupertino 95014";
const cityZipCodeRegex = /^[^,\\]+[,\\\s]+(.+?)\s*(\d{5})?$/;
saveCityZipCode(
  address.match(cityZipCodeRegex)[1],
  address.match(cityZipCodeRegex)[2]
);

// Good
const address = "One Infinite Loop, Cupertino 95014";
const cityZipCodeRegex = /^[^,\\]+[,\\\s]+(.+?)\s*(\d{5})?$/;
const [_, city, zipCode] = address.match(cityZipCodeRegex) || [];
saveCityZipCode(city, zipCode); // city와 zipCode
```

### 사소해 보이는 변수도 명시적으로 작성하기

```jsx
// Bad
const locations = ["Austin", "New York", "San Francisco"];
locations.forEach((l) => {
  doStuff();
  doSomeOtherStuff();
  // ...
  // ...
  // ...
  //
  dispatch(l); // l이 뭔데?
});

// Good
const locations = ["Austin", "New York", "San Francisco"];
locations.forEach((location) => {
  doStuff();
  doSomeOtherStuff();
  // ...
  // ...
  // ...
  dispatch(location);
});
```

### 같은 context 중복 작성하지 않기

```jsx
// Bad
const Car = {
  carMake: "Honda",
  carModel: "Accord",
  carColor: "Blue",
};

function paintCar(car, color) {
  car.carColor = color;
}

// Good
const Car = {
  make: "Honda",
  model: "Accord",
  color: "Blue",
};

function paintCar(car, color) {
  car.color = color;
}
```

### default 파라미터 잘 사용하기

```jsx
// Bad
function createMicrobrewery(name) {
  const breweryName = name || "Hipster Brew Co.";
  // ...
}

// Good
function createMicrobrewery(name = "Hipster Brew Co.") {
  // ...
}
```
