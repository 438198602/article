# javascript 常见判断

对象的字符串表示形式。

```
var toString = Object.prototype.toString;
```

## isArray

判断给定的值是否为为` 数组 `类型。如果是返回true，否则返回false。

```
function isArray(val) {
  return toString.call(val) === '[object Array]';
}

```

## isString

判断给定的值是否为` 字符串 `类型。如果是范围true，否则返回false。

```
function isString(val) {
  return typeof val === 'string';
}
```

## isNumber

判断给定的值是否为` 数字 `类型。如果是范围true，否则返回false。

```
function isNumber(val) {
  return typeof val === 'number';
}
```

## isUndefined

判断给定的值是否为` undefined `类型。如果是范围true，否则返回false。

```
function isUndefined(val) {
  return typeof val === 'undefined';
}
```

## isObject

判断给定的值是否为` object `类型。如果是范围true，否则返回false。

```
function isObject(val) {
  return val !== null && typeof val === 'object';
}
```

## isFunction

判断给定的值是否为` funciton `类型。如果是范围true，否则返回false。

```
function isFunction(val) {
  return toString.call(val) === '[object Function]';
}
```

## isDate

判断给定的值是否为` date `类型。如果是范围true，否则返回false。

```
function isDate(val) {
  return toString.call(val) === '[object Date]';
}
```

## isFile

判断给定的值是否为` file `类型。如果是范围true，否则返回false。

```
function isFile(val) {
  return toString.call(val) === '[object File]';
}
```

## isBlob

判断给定的值是否为` Blob `类型。如果是范围true，否则返回false。

```
function isBlob(val) {
  return toString.call(val) === '[object Blob]';
}
```

## isStream

判断给定的值是否为` stream `类型。如果是范围true，否则返回false。

```
function isStream(val) {
  return isObject(val) && isFunction(val.pipe);
}
```

## isArrayBuffer

判断给定的值是否为` ArrayBuffer `类型。如果是范围true，否则返回false。

```
function isArrayBuffer(val) {
  return toString.call(val) === '[object ArrayBuffer]';
}
```

## isArrayBufferView

判断给定的值是否为` ArrayBufferView `类型。如果是范围true，否则返回false。

```
function isArrayBufferView(val) {
  var result;
  if ((typeof ArrayBuffer !== 'undefined') && (ArrayBuffer.isView)) {
    result = ArrayBuffer.isView(val);
  } else {
    result = (val) && (val.buffer) && (val.buffer instanceof ArrayBuffer);
  }
  return result;
}
```

## isURLSearchParams

判断给定的值是否为` URLSearchParams `类型。如果是范围true，否则返回false。

```
function isURLSearchParams(val) {
  return typeof URLSearchParams !== 'undefined' && val instanceof URLSearchParams;
}
```

## isFormData

判断给定的值是否为` FormData `类型。如果是范围true，否则返回false。

```
function isFormData(val) {
  return (typeof FormData !== 'undefined') && (val instanceof FormData);
}
```
