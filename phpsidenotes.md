# PHP Side-notes

## What is a static method?
  Static methods are the inverse of instance methods.
  Instance methods are invoked on an *instance* of the class in which they are defined, in an instance method you'll have access to a class object via '''$this-> '''
### Example declaring a class object and accessing it via an instance method:

```
$object = new MyClass();
$result = $object->myInstanceMethod();
```

  Static methods are called upon the class itself as opposed to a class-object. static method can be accessed with the ```::``` syntax.

```
$result = MyClass::myStaticMethod();
```
  
