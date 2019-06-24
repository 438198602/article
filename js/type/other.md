# js其他判断

## string 相关

### isNonBlankString

判断给定的值是否为` 非空字符串 `。如果是返回true，否则返回false。

```
function isNonBlankString(val) {
  return typeof val === 'string' && (/\S/).test(val);
}
```

### isBlankString

判断给定的值是否为` 空字符串 `。如果是返回true，否则返回false。

```
function isBlankString(val) {
  return typeof val === 'string' && val.trim().length === 0;
}
```

## element

### isEl

判断给定的值是否为` dom元素 `。如果是返回true，否则返回false。

```
function isEl(val) {
  return isObject(val) && val.nodeType === 1;
}
```

注：`isObject(val)`，请参考[`js type`](https://github.com/lvzhenbang/article/blob/master/learning/js.type.md#isobject)

### isTextNode

判断给定的值是否为` 文本节点 `。如果是返回true，否则返回false。

```
function isTextNode(val) {
  return isObject(val) && val.nodeType === 3;
}
```

注：`isObject(val)`，请参考[`js type`](https://github.com/lvzhenbang/article/blob/master/learning/js.type.md#isobject)


## iframe

### isInframe

```
function isInFrame() {
  try {
    return window.parent !== window.self;
  } catch (x) {
    return true;
  }
}
```

注：在Safari中，如果获取`parent` 或 `self`，将抛出异常，因此需要使用`try/catch`。