---
id: a39963a4c10bc8b4d4f06d7e
title: 過濾數組元素
challengeType: 1
forumTopicId: 16046
dashedName: seek-and-destroy
---

# --description--

You will be provided with an initial array as the first argument to the `destroyer` function, followed by one or more arguments. 從初始數組中移除所有與後續參數相等的元素。

The function must accept an indeterminate number of arguments, also known as a variadic function. You can access the additional arguments by adding a rest parameter to the function definition or using the `arguments` object.

# --hints--

`destroyer([1, 2, 3, 1, 2, 3], 2, 3)` 應返回 `[1, 1]`。

```js
assert.deepEqual(destroyer([1, 2, 3, 1, 2, 3], 2, 3), [1, 1]);
```

`destroyer([1, 2, 3, 5, 1, 2, 3], 2, 3)` 應返回 `[1, 5, 1]`。

```js
assert.deepEqual(destroyer([1, 2, 3, 5, 1, 2, 3], 2, 3), [1, 5, 1]);
```

`destroyer([3, 5, 1, 2, 2], 2, 3, 5)` 應返回 `[1]`。

```js
assert.deepEqual(destroyer([3, 5, 1, 2, 2], 2, 3, 5), [1]);
```

`destroyer([2, 3, 2, 3], 2, 3)` 應返回 `[]`。

```js
assert.deepEqual(destroyer([2, 3, 2, 3], 2, 3), []);
```

`destroyer(["tree", "hamburger", 53], "tree", 53)` 應返回 `["hamburger"]`。

```js
assert.deepEqual(destroyer(['tree', 'hamburger', 53], 'tree', 53), [
  'hamburger'
]);
```

`destroyer(["possum", "trollo", 12, "safari", "hotdog", 92, 65, "grandma", "bugati", "trojan", "yacht"], "yacht", "possum", "trollo", "safari", "hotdog", "grandma", "bugati", "trojan")` 應返回 `[12,92,65]`。

```js
assert.deepEqual(
  destroyer(
    [
      'possum',
      'trollo',
      12,
      'safari',
      'hotdog',
      92,
      65,
      'grandma',
      'bugati',
      'trojan',
      'yacht'
    ],
    'yacht',
    'possum',
    'trollo',
    'safari',
    'hotdog',
    'grandma',
    'bugati',
    'trojan'
  ),
  [12, 92, 65]
);
```

# --seed--

## --seed-contents--

```js
function destroyer(arr) {
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

# --solutions--

```js
function destroyer(arr) {
  var hash = Object.create(null);
  [].slice.call(arguments, 1).forEach(function(e) {
    hash[e] = true;
  });
  return arr.filter(function(e) { return !(e in hash);});
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```
