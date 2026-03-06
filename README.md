# learning
learning about javascript
JavaScript 方法学习笔记
本仓库记录了学习 JavaScript 过程中常用的内置方法，按类别整理，方便查阅。

目录
字符串方法

数组方法

对象方法

数学方法

其他方法

字符串方法

方法	作用	示例

slice(start, end)	提取字符串的一部分，返回新字符串	"Hello".slice(1,4) → "ell"

repeat(count)	重复字符串指定次数	"ha".repeat(3) → "hahaha"

replace(search, replace)	替换匹配的子串（只替换第一个）	"cat".replace("c","b") → "bat"

indexOf(searchValue)	返回首次出现的位置，未找到返回 -1	"hello".indexOf("l") → 2

endsWith(searchString)	判断是否以指定字符串结尾	"hello".endsWith("lo") → true

toUpperCase()	转为大写	"hi".toUpperCase() → "HI"

toLowerCase()	转为小写	"HI".toLowerCase() → "hi"

split(separator)	按分隔符拆分成数组	"a,b".split(",") → ["a","b"]

charCodeAt(index)	返回指定位置字符的 Unicode 编码	"a".charCodeAt(0) → 97

String.fromCharCode(code)	将 Unicode 编码转为字符	String.fromCharCode(97) → "a"

trim()	移除首尾空白字符	" hi ".trim() → "hi"

concat(str2, ...)	连接多个字符串	"a".concat("b","c") → "abc"

数组方法

方法	作用	示例

push(element)	末尾添加元素，返回新长度	arr.push(4)

pop()	移除并返回最后一个元素	arr.pop()

unshift(element)	开头添加元素	arr.unshift(0)

shift()	移除并返回第一个元素	arr.shift()

slice(start, end)	返回数组片段（新数组）	[1,2,3].slice(1,2) → [2]

splice(start, deleteCount, ...items)	在指定位置插入/删除元素（修改原数组）	arr.splice(1,0,'x')

concat(array2, ...)	合并数组（返回新数组）	[1].concat([2,3]) → [1,2,3]

reverse()	反转数组（修改原数组）	[1,2,3].reverse() → [3,2,1]

join(separator)	将数组元素连接成字符串	['a','b'].join('-') → "a-b"

indexOf(element)	返回元素首次出现的位置	[1,2,3].indexOf(2) → 1

includes(element)	判断是否包含某元素	[1,2].includes(2) → true

filter(callback)	过滤出符合条件的元素（新数组）	[1,2,3].filter(x=>x>1) → [2,3]

map(callback)	对每个元素操作并返回新数组	[1,2].map(x=>x*2) → [2,4]

reduce(callback, initial)	累积计算	[1,2,3].reduce((a,b)=>a+b,0) → 6

flat(depth)	扁平化嵌套数组	[1,[2]].flat() → [1,2]

length 属性	获取数组长度	arr.length

对象方法

方法	作用	示例

hasOwnProperty(prop)	检查对象自身是否拥有某属性	obj.hasOwnProperty('name')

Object.keys(obj)	返回对象自身可枚举属性名的数组	Object.keys({a:1,b:2}) → ['a','b']

Object.values(obj)	返回对象自身可枚举属性值的数组	Object.values({a:1,b:2}) → [1,2]

Object.entries(obj)	返回键值对数组	Object.entries({a:1}) → [['a',1]]

delete obj.prop	删除对象属性	delete obj.age

数学方法

方法	作用	示例

Math.max(...nums)	返回最大值	Math.max(1,5,2) → 5

Math.min(...nums)	返回最小值	Math.min(1,5,2) → 1

Math.random()	返回 [0,1) 随机数	Math.random()

Math.floor(x)	向下取整	Math.floor(3.9) → 3

Math.pow(base, exp)	幂运算	Math.pow(2,3) → 8

其他方法

方法	作用	示例

Number(value)	将值转换为数字	Number('123') → 123

JSON.stringify(obj, null, 2)	将对象转为格式化的 JSON 字符串	JSON.stringify({a:1}, null, 2)

JSON.parse(str)	将 JSON 字符串解析为对象	JSON.parse('{"a":1}')

循环与迭代

语法	适用场景	说明

for...in	遍历对象属性名（或数组索引）	for(let key in obj)

for...of	遍历可迭代对象的值（数组、字符串等）	for(let val of arr)

forEach	数组遍历	arr.forEach((item,index)=>{})

注意事项

for...in 遍历数组时，索引是字符串类型，且可能遍历到原型属性，不建议用于数组。

splice() 会修改原数组，而 slice() 不会。

使用 Math.max(...arr) 时确保 arr 不为空，否则返回 -Infinity。

concat() 对于数组参数会展开一层，如需保持嵌套需额外包装。
