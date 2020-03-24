# JavaScript Exercises

## What is the output of the following logs?
```js
console.log(0.1 + 0.2);        // 0.30000000000000004
console.log(0.1 + 0.2 == 0.3); // false
```

## What is the output of y?
```js
var y = 1;
if (function f(){}) {
    y += typeof f;
}
console.log(y); // 1undefined
```

## Which order are the logs in?
```js
(function() {
    console.log(1);
    setTimeout(function () {
        console.log(2);
    }, 1000);
    setTimeout(function () {
        console.log(3);
    }, 0);
    console.log(4);
})(); // 1, 4, 3, 2
```

## What is the output of the logs?
```js
for (var i = 0; i < 3; i++) {
    setTimeout(function () {
        console.log(i);
    }, 1000 + i);
} // 3, 3, 3
```

To fix the output via ES6:
```js
for (let i = 0; i < 3; i++) {
    setTimeout(function () {
        console.log(i);
    }, 1000 + i);
}
```

To fix the output via IIFE:
```js
for (var i = 0; i < 3; i++) {
    setTimeout(function (local_i) {
        return function() {
            console.log(local_i);
        }
    }(i), 1000 + i);
}
```

## Implement the multiply function to get this output.
```js
console.log(multiply(2)(3)(4)); // 24
console.log(multiply(4)(3)(3)); // 36
```

The `multiply` function:
```js
function multiply(x) {
    return function(y) {
        return function(z) {
            return x * y * z;
        }
    }
}
```

## Implement the createBase function to get this output.
```js
var addSeven = createBase(7);
console.log(addSeven(10)); // 17
console.log(addSeven(20)); // 27
```

The `createBase` function:
```js
function createBase(base) {
    return function(addend) {
        return base + addend;
    }
}
```

## Implement the counter function to get this output.
```js
var c = counter();
c.add(5);
c.add(9);
console.log(c.retrieve()); // 14
```

The `counter` function:
```js
function counter() {
    var _counter = 0;
    return {
        add: function(addend) {
            _counter += addend;
        },
        retrieve: function () {
            return _counter;
        }
    };
}
```

## Convert the following into promises.
```js
const fs = require('fs');
fs.readFile('somefile.txt', function (e, data) {
    fs.readdir('somedir', function (e, files) {
        fs.mkdir('someotherdir', function (e) {
            // Assume some logic to put the files in this new directory
        });
    });
});
```

The functions that return promises:
```js
const fs = require('fs');
const readFilePromise = (file) => new Promise((resolve) => {
    fs.readFile(file, function(e, data) {
        if (e) {
            reject(e);
        }
        resolve(data);
    });
});

const readDirPromise = (dir) => new Promise((resolve) => {
    fs.readdir(dir, function(e, data) {
        if (e) {
            reject(e);
        }
        resolve(data);
    });
});

const makeDirPromise = (dir) => new Promise((resolve) => {
    fs.mkdir(dir, function(e, data) {
        if (e) {
            reject(e);
        }
        resolve(data);
    });
});
```

To run the promise chain:
```js
readFilePromise('somefile.txt')
    .then(data => readDirPromise('somedir'))
    .then(files => makeDirPromise('someotherdir'))
    .catch(error => throw new Error(error));
```
