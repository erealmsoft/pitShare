## wrong way
```
var strA;
strA.indexOf('xx')

ArrayA.indexof('xx')
```

`strA` and `ArrayA` maybe null or undefined, will crash the process.

## right way

```
var strA;
starA && strA.indexOf('xx')

var ArrayA
if (ArrayA) {
   console.log(ArrayA.indexof('xx'));
}
```
