# 子串查找-js

在 JavaScript 中，可以使用多种方式来匹配字符串中的特定子串，常用的方式包括：

1. 字符串的 `indexOf()` 方法：该方法返回字符串中第一个匹配子串的索引位置，如果没有找到匹配的子串，则返回 `-1`。例如：

   ```
   const str = 'hello world';
   const index = str.indexOf('world'); // 返回 6
   ```

2. 字符串的 `search()` 方法：该方法与 `indexOf()` 类似，也是返回字符串中第一个匹配子串的索引位置，如果没有找到匹配的子串，则返回 `-1`。不同的是，`search()` 方法可以接受正则表达式作为参数，可以更加灵活地进行匹配。例如：

   ```
   const str = 'hello world';
   const index = str.search(/world/); // 返回 6
   ```

3. 字符串的 `match()` 方法：该方法返回一个数组，包含所有匹配子串的内容。如果没有找到匹配的子串，则返回 `null`。`match()` 方法也可以接受正则表达式作为参数，可以更加灵活地进行匹配。例如：

   ```
   const str = 'hello world';
   const matches = str.match(/l/g); // 返回 ["l", "l", "l"]
   ```

4. 正则表达式的 `exec()` 方法：该方法与 `match()` 类似，也是返回一个数组，包含所有匹配子串的内容。不同的是，`exec()` 方法是正则表达式对象的方法，需要先创建一个正则表达式对象。另外，`exec()` 方法可以多次调用，每次返回一个匹配的子串，直到没有匹配项为止。例如：

   ```
   const str = 'hello world';
   const pattern = /l/g;
   let match;
   while ((match = pattern.exec(str))) {
     console.log(match[0]); // 打印匹配的子串
   }
   ```

除了上述方法之外，JavaScript 还提供了一些其他的字符串操作方法，如 `replace()`、`split()`、`substr()`、`slice()` 等等，可以根据不同的需求选择合适的方法来操作字符串。

在一些常见的浏览器中，如 Chrome、Firefox 和 Safari 等，通常情况下 `indexOf()` 方法的执行速度是最快的。这是因为 `indexOf()` 方法是由 JavaScript 引擎原生实现的，而其他方法则可能需要更多的额外操作，如正则表达式的解析、数组的创建等等。

不过，需要注意的是，每个方法的实际执行速度可能因浏览器、字符串长度、匹配子串的长度、正则表达式的复杂度等因素而有所不同。因此，在实际开发中，应该根据具体情况选择合适的方法，并进行性能测试和优化。
