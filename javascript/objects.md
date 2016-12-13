## Objects
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
```
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
```
foo.bar
foo["bar"]
```

#### Update
Like Retrieval there are two ways to update an object.
```
foo.bar = "123"
foo.["bar"] = "123"
```

#### Prototype

