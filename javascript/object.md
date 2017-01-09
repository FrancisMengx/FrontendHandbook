## Object
Object is the most important data type in javascript, having a good
understanding of how it works and how to change and use an object is
largely beneficial for our development work.

There are several simple data types in javascript:
```
number
string
boolean
null
undefined
```

Other than these simple types everything else are objects.

> An object is a container of properties.

Each property has a name and value. The property name can be any string
including empty string, and value can any javascript value.

### Object Literals
object literals are the name/value pairs between curly braces.
E.G.
```javascript
{
  foo: "bar"
}

{
  "foo": "bar"
}
```

* note: the quotes arround the key name is optional

#### Retrieval
There are two ways to retrieve value in an object.
```javascript
foo.bar
foo["bar"]
```

#### Update
Like Retrieval there are two ways to update an object.
```javascript
foo.bar = "123"
foo.["bar"] = "123"
```

#### Prototype
Each javascript is linked to a prototyp object. All the object literals
is linked to Object.prototype object. You can also link prototype
manually by using ```Object.create``` function.

```javascript
let example = {
  foo: "this is foo",
  bar: "this is bar"
}

let another_example = Object.create(example)

console.log(another_example.foo)
> 'this is foo'
console.log(another_example.bar)
> 'this is bar'
```

Modifying the created object won't effect the prototype object:

```javascript
another_example.foo = "another foo"

console.log(another_example.foo)
> 'another example'
console.log(another_example.__proto__.foo)
> 'this is foo'
```

Prototype object are dynamically binded to the objects that uses it as
prototype object. Continue with the previous example.
```javascript
example.foobar = "this is foobar"
console.log(another_example.foobar)
> 'this is foobar'
```

#### Inspection
The key word ```typeof``` can check the type of an object.
```javascript
var example = {}
example.num1 = 1
typeof example.num1
> 'number'
```

Function ```hasOwnProperty``` can check if a object as certain property.
This function does not look at the prototype chain.
```javascript
var example = {}
example.num1 = 1
exmaple.string1 = "this is string"

var anotherObject = Object.create(example)
anotherObject.num1 = 2

console.log(example.hasOwnProperty("num1"))
> true
console.log(anotherObject.hasOwnProperty("num1"))
> true
console.log(example.hasOwnProperty("string1"))
> true
console.log(anotherObject.hasOwnProperty("string1"))
> false
```

#### Delete
The ```delete``` operator can be used to remove a property from an
object.
```javascript
console.log(anotherObject.num1)
> 2
delete anotherObject.num1
console.log(anotherObject.num1)
> 1
```
* Note: delete operator won't remove anything in the prototype chain.


