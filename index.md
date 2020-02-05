<html lang="en">
    <head>
        <title>Cufyorg</title>
        <script>
            window.onload = function() {
              let link = top.document.createElement("link");
              link.type = "image/x-icon";
              link.rel = "shortcut icon";
              link.href = "/favicon.ico";
              top.document.getElementsByTagName("head")[0].appendChild(link);
            };
        </script>
    </head>
</html>

[util]:https://www.github.com/cufyorg/util
[util-arrays]:https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Array$.java
[util-readers]:https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Reader$.java
[util-reflects]:https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Reflect$.java
[util-throwables]:https://github.com/cufyorg/util/blob/master/src/main/java/cufy/util/Throwable$.java

[base]:https://www.github.com/cufyorg/base
[base-invoke]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/beans/Invoke.java
[base-converter]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/lang/Converter.java
[base-format]:https://www.github.com/cufyorg/base/blobl/master/src/main/java/cufy/text/Format.java
[base-type]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/lang/Type.java
[base-value]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/lang/Value.java

[beans]:https://www.github.com/cufyorg/beans
[beans-bean]:https://www.github.com/cufyorg/beans/blob/master/src/main/java/cufy/beans/Bean.java

[concurrent]:https://www.github.com/cufyorg/concerrent
[concurrent-loop]:https://www.github.com/cufyorg/concerrent/blob/master/src/main/java/cufy/lang/Loop.java
[concurrent-instructor]:https://www.github.com/cufyorg/concerrent/blob/master/src/main/java/cufy/lang/Instructor.java
[concurrent-lock]:https://www.github.com/cufyorg/concerrent/blob/master/src/main/java/cufy/lang/Lock.java

[json]:https://www.github.com/cufyorg/json
[json-json]:https://www.github.com/cufyorg/json/blob/master/src/main/java/org/cufy/text/JSON.java
[json-json_converter]:https://www.github.com/cufyorg/json/blob/master/src/main/java/org/cufy/lang/JSONConverter.java

# **Util** [<font size="3">(cufyorg:util)</font>][util]
A raw static utils for classes. All classes in this repository are in package 'cufy.util'. In this repo, No classes expected to be instanced. And
all methods are not designed other than to be static. Each class has a name representing what class it focuses on, Followed by '$' to reduce name
clashing. (ex. "cufy.util.Collection$" for a util class that focuses on the class "java.util.Collection")

- ### **Arrays** [<font size="3">(cufy.util.Array$)</font>][util-arrays]
Utilities for java raw arrays. This class provide various kinds of methods that helps dealing with raw arrays. This class is designed to deal with 
both reflection and standard environments. Methods that designed for reflection environments have '0' at the last of their names. Those methods
will except any type provided to them.

- ### **Readers** [<font size="3">(cufy.util.Reader$)</font>][util-readers]
Utilities for java.io.Reader. This class designed to do/apply common operation on a specific positions on a reader. No method in this class allowed
to use 'reset' or 'mark' or 'close' on the reader provided. Just to not mess-up the reader for the caller. Also methods are not responsible where
the reader stopped after invoking them.

- ### **Reflects** [<font size="3">(cufy.util.Reflect$)</font>][util-reflects]
Utilities for reflection environments. Methods in this class focused for dealing with/around the class 'java.lang.Class'. And about getting
information from it. Also about converting it from a class to another.

- ### **Throwables** [<font size="3">(cufy.util.Throwable$)</font>][util-throwables]
Utilities for throwables and exceptions. It has some useful glitches too.

---

# **Base** [<font size="3">(cufyorg:base)</font>][base]
The base logic for most repositories. Like the standard solutions for dynamic classes. And additional types to be used on all repos. This repo
shouldn't have scoped solutions. It's only for standers and protocols. This repo shouldn't have any repo from cufy other than 'cufyorg:util'. This
repo most uses the package 'cufy.lang'. Most of the classes are designed to be super classes.

- ### **Invoke** [<font size="3">(cufy.beans.Invoke)</font>][base-invoke]
Base class for those classes that are just a collection of methods. This class will manage method grouping. And query methods for the class
implementing it. Then save those queries for later use.

- ### **Converter** [<font size="3">(cufy.lang.Converter)</font>][base-converter]
Using the class 'Invoke', This is like a hock for those classes that are just a collection of methods that converts the types of values. This class
uses the annotations to query the best methods for specific type of conversions. Since the class uses the class 'Invoke', So it will store the
method foreach conversion to reduce the next conversion cost.

- ### **Format** [<font size="3">(cufy.lang.Format)</font>][base-format]
Using the class 'Invoke', This is like a hock for those classes that are just a collection of methods that format/parse objects to/from strings. 
This class uses the annotations to query the best methods for specific type of formatting/classification/parsing. Since the class uses the class
'Invoke', So it will store the method foreach formatting/parsing to reduce the next formatting/parsing cost. The Parsing methods of this class
designed to get the input from a reader then parse it to a buffer. And The Formatting methods are designed to get the input as an object then parse
it to a writer.

- ### **Type** [<font size="3">(cufy.lang.Type)</font>][base-type]
A value annotation holds data about a range of types. Like maybe it holds the types List and Map. It has also a static method to test types if it's
included in that annotation or not.

- ### **Value** [<font size="3">(cufy.lang.Value)</font>][base-value]
A value annotation holds data about how to construct a value. Useful for annotation environment. Since annotations don't allow any type of values. 
It uses a class of converter and a string for the value and the class of the targeted value.

---

# **Beans** [<font size="3">(cufyorg:beans)</font>][beans]
Abstract classes and interfaces that change the behavior of the implemented classes. Like changing the way accessing the class's fields or the way
invoking the class's methods. This repo most uses the package 'cufy.beans'.

- ### **Bean** [<font size="3">(cufy.beans.Bean)</font>][beans-bean]
An interface changes the act of the fields of the class implementing it. The classes that implement this class change to be used as a map
(JavaScript like). All of the fields of that class will be like a map-entry holder (like property on beans). Fields not annotated with property
annotation will be excluded. The annotation parameters will change the behavior of the class with that field annotated.

---

# **Concurrent** [<font size="3">(cufyorg:concurrent)</font>][concurrent]
Simplifications and interfaces/protocols to deal with concurrent environment. Like loops, nested loops and threads or locks. This repo most uses
the packages 'cufy.lang' and 'cufy.util.concurrent'.

- ### **Loop** [<font size="3">(cufy.lang.Loop)</font>][concurrent-loop]
A class represents a loop. The class holds the position of that loop. The code of that loop. And how to iterate the code. Also contains methods to
interrupt or change or get data from/to that loop concurrently.

- ### **Instructor** [<font size="3">(cufy.lang.Instructor)</font>][concurrent-instructor]
A class that works like a remote to multiple loops. Like sending/interrupting or changing the position of those loops.

- ### **Lock** [<font size="3">(cufy.lang.Lock)</font>][concurrent-lock]
A thread that gain/release object lock access depending on the position of it. By gaining that lock then sleeping.

---

# **JSON** [<font size="3">(cufyorg:json)</font>][json]
JSON support. Like parse/format or convert utils. This repo most uses the package 'org.cufy.text'.

- ### **JSON** [<font size="3">(org.cufy.text.JSON)</font>][json-json]
Using 'Format' from the base repo. This class can format/parse or even classify any json text. This class supports the standard JSON text. Plus
recursion and comments.

- ### **JSONConverter** [<font size="3">(org.cufy.lang.JSONConverter)</font>][json-json_converter]
Using both 'JSON' and 'BaseConverter'. This class can preform all the basic conversions, Plus can preform string->object and object->string using
JSON Format.