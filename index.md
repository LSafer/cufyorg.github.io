Cufy is organization made by lsafer. An organization all about coding.

## [Util](https://www.github.com/cufyorg/util)
A raw static utils for classes. All classes in this repository are in package 'cufy.util'. In this repo, No classes expected to be instanted. And all methods are not designed other than to be static. Each class has a name representing what class it focusses on, Followed by '$' to reduce name clashings. (ex. "cufy.util.Collection$" for a util class that focusses on the class "java.util.Collection")

### [Array$](https://github.com/cufyorg/util/tree/master/src/main/java/cufy/util/Array$.java)
Utilities for java raw arrays. This class provide various kinds of methods that helps dealing with raw arrays. This class is designed to deal with both reflection and standerd environments. Methods that designed for reflection environments have '0' at the last of their names. Those methods will except any type provided to them.

### [Iterator$](https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Iterator$.java)
Utilities for java.util.Iterator. Nothing so special.

### [Object$](https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Object$.java)
Common methods accros all types. Nothing so special.

### [Reader$](https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Reader$.java)
Utilities for java.io.Reader. This class desinged to do/apply common operation on a specific positions on a reader. No method in this class allowed to use 'reset' or 'mark' or 'close' on the reader provided. Just to not messup the reader for the caller. Also methods are not responsible where the reader stopped after invoking them.

### [Reflect$](https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Reflect$.java)
Utilities for reflection environments. Methods in this class focused for dealing with/around the class 'java.lang.Class'. And about getting information from it. Also about converting it from a class to another.

### [String$](https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/String$.java)
Utilities for strings. The not that useful class. Nothing special.

### [Throwable$](https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Throwable$.java)
Utilities for throwables and exceptions. It has some glitches too.

# [cufyorg:core](https://www.github.com/cufyorg/core)
The main dependency for all Cufy Java/Groovy Repositories.

### [Beans](https://www.github.com/cufyorg/beans)
Abstract classes and interfaces that change the behavior of the implemented classes. Like changing the way accessing the class's fields or the way invoking the class's methods.

### [Concurrent](https://www.github.com/cufyorg/concurrent)
Utils to deal with concurrent actions and infinite loops.

### [IO](https://www.github.com/cufyorg/io)
Utils to deal with Input/Output ports. Like dealing with files or dealing with internet.

### [Misc](https://www.github.com/cufyorg/misc)
Other utils that may be helpful but not enough to be added to a categorized repository.
