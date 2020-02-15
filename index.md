<html lang="en">
    <head>
        <title>Cufyorg</title>
        <script>
            window.onload = function() {
              let link = top.document.createElement("link");
              link.type = "image/*";
              link.rel = "icon";
              link.href = "https://cufyorg.github.io/origin_ic.png";
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
[base-format]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/text/Format.java
[base-type]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/lang/Type.java
[base-value]:https://www.github.com/cufyorg/base/blob/master/src/main/java/cufy/lang/Value.java

[concurrent]:https://www.github.com/cufyorg/concurrent
[concurrent-loop]:https://www.github.com/cufyorg/concurrent/blob/master/src/main/java/cufy/lang/Loop.java
[concurrent-instructor]:https://www.github.com/cufyorg/concurrent/blob/master/src/main/java/cufy/lang/Instructor.java
[concurrent-lock]:https://www.github.com/cufyorg/concurrent/blob/master/src/main/java/cufy/lang/Lock.java

[json]:https://www.github.com/cufyorg/json
[json-json]:https://www.github.com/cufyorg/json/blob/master/src/main/java/org/cufy/text/JSON.java
[json-json_converter]:https://www.github.com/cufyorg/json/blob/master/src/main/java/org/cufy/lang/JSONConverter.java

[beans]:https://www.github.com/cufyorg/beans
[beans-bean]:https://www.github.com/cufyorg/beans/blob/master/src/main/java/cufy/beans/Bean.java

[io]:https://www.github.com/cufyorg/io
[io-buffer]:https://www.github.com/cufyorg/io/blob/master/src/main/java/cufy/nio/Buffer.java
[io-io*]:https://www.github.com/cufyorg/io/tree/master/src/main/java/cufy/io/
[io-loadable]:https://www.github.com/cufyorg/io/blob/master/src/main/java/cufy/lang/Loadable.java
[io-file_loadable]:https://www.github.com/cufyorg/io/blob/master/src/main/java/cufy/io/FileLoadable.java
[io-url_loadable]:https://www.github.com/cufyorg/io/blob/master/src/main/java/cufy/io/URLLoadable.java
[io-format_loadable]:https://www.github.com/cufyorg/io/blob/master/src/main/java/cufy/text/FormatLoadable.java

# **Util** [<font size="3">(cufyorg:util)</font>][util]
Raw static util for classes. All classes in this repository are in package 'cufy.util'. In this repo, No classes expected to be instanced. And
all methods are not designed other than to be static. Each class has a name representing what class it focuses on, Followed by '$' to reduce name
clashing. (ex. "cufy.util.Collection$" for a util class that focuses on the class "java.util.Collection")

- ### **Arrays** [<font size="3">(cufy.util.Array$)</font>][util-arrays]
Utilities for java raw arrays. This class provides various kinds of methods that help dealing with raw arrays. This class is designed to deal with 
both reflection and standard environments. Methods that designed for reflection environments have '0' at the last of their names. Those methods
will except any type provided to them.

- ### **Readers** [<font size="3">(cufy.util.Reader$)</font>][util-readers]
Utilities for java.io.Reader. This class designed to do/apply common operations on a specific position of a reader. No method in this class allowed
to use 'reset' or 'mark' or 'close' on the reader provided. Just to not mess-up the reader for the caller. Also, methods are not responsible where
the reader stopped after invoking them.

- ### **Reflects** [<font size="3">(cufy.util.Reflect$)</font>][util-reflects]
Utilities for reflection environments. Methods in this class focused for dealing with/around the class 'java.lang.Class'. And about getting
information from it. Also about converting it from a class to another.

- ### **Throwables** [<font size="3">(cufy.util.Throwable$)</font>][util-throwables]
Utilities for throwables and exceptions. It has some useful glitches too.

---

# **Base** [<font size="3">(cufyorg:base)</font>][base]
The base logic for most repositories. Like the standard solutions for dynamic classes. And additional types to be used on all repositories. This 
repository shouldn't have scoped solutions. It's only for standers and protocols. This repository should not implement any repository from cufy
other than 'cufyorg:util'. This repository most uses the package 'cufy.lang'. Most of the classes are designed to be superclasses.

- ### **Invoke** [<font size="3">(cufy.beans.Invoke)</font>][base-invoke]
Base class for those classes that are just a collection of methods. This class will manage method grouping. And query methods for the class
implementing it. Then save those queries for later use.

- ### **Converter** [<font size="3">(cufy.lang.Converter)</font>][base-converter]
Using the class 'Invoke', This is like a hock for those classes that are just a collection of methods that converts the types of values. This class
uses the annotations to query the best methods for the specific type of conversion. Since the class uses the class 'Invoke', So it will store the
method for each conversion to reduce the next conversion cost.

- ### **Format** [<font size="3">(cufy.lang.Format)</font>][base-format]
Using the class 'Invoke', This is like a hock for those classes that are just a collection of methods that format/parse objects to/from strings. 
This class uses the annotations to query the best methods for the specific type of formatting/classification/parsing. Since the class uses the class
'Invoke', So it will store the method for each formatting/parsing to reduce the next formatting/parsing cost. The Parsing methods of this class
designed to get the input from a reader then parse it to a buffer. And The Formatting methods are designed to get the input as an object then parse
it to a writer.

- ### **Type** [<font size="3">(cufy.lang.Type)</font>][base-type]
A value annotation holds data about a range of types. Like maybe it holds the types List and Map. It has also a static method to test types if it's
included in that annotation or not.

- ### **Value** [<font size="3">(cufy.lang.Value)</font>][base-value]
A value annotation holds data about how to construct a value. Useful for annotation environment. Since annotations don't allow any type of values. 
It uses a class of converter and a string for the value and the class of the targeted value.

---

# **Concurrent** [<font size="3">(cufyorg:concurrent)</font>][concurrent]
Simplifications and interfaces/protocols to deal with concurrent environment. Like loops, nested loops and threads or locks. This repository most uses
the packages 'cufy.lang' and 'cufy.util.concurrent'.

- ### **Loop** [<font size="3">(cufy.lang.Loop)</font>][concurrent-loop]
A class represents a loop. The class holds the position of that loop. The code of that loop. And how to iterate the code. It also contains methods to
interrupt or change or get data from/to that loop concurrently.

- ### **Instructor** [<font size="3">(cufy.lang.Instructor)</font>][concurrent-instructor]
A class that works like a remote to multiple loops. Like sending/interrupting or changing the position of those loops.

- ### **Lock** [<font size="3">(cufy.lang.Lock)</font>][concurrent-lock]
A thread that gain/release object lock access depending on the position of it. By gaining that lock then sleeping.

---

# **JSON** [<font size="3">(cufyorg:json)</font>][json]
JSON support. Like parse/format or convert utils. This repository most uses the package 'org.cufy.text'.

- ### **JSON** [<font size="3">(org.cufy.text.JSON)</font>][json-json]
Using 'Format' from the base repo. This class can format/parse or even classify any json text. This class supports the standard JSON text. Plus
recursion and comments.

- ### **JSONConverter** [<font size="3">(org.cufy.lang.JSONConverter)</font>][json-json_converter]
Using both 'JSON' and 'BaseConverter'. This class can preform all the basic conversions, Plus can preform string->object and object->string using
JSON Format.

---

# **Beans** [<font size="3">(cufyorg:beans)</font>][beans]
Abstract classes and interfaces that change the behavior of the implemented classes. Like changing the way accessing the class's fields or the way
invoking the class's methods. This repository most uses the package 'cufy.beans'.

- ### **Bean** [<font size="3">(cufy.beans.Bean)</font>][beans-bean]
An interface changes the act of the fields of the class implementing it. The classes that implement this class change to be used as a map
(JavaScript like). All of the fields of that class will be like a map-entry holder (like property on beans). Fields not annotated with property
annotation will be excluded. The annotation parameters will change the behavior of the class with that field annotated.

---
# **IO** [<font size="3">(cufyorg:io)</font>][io]
I/O interfaces and solutions for I/O interfaces. This repository is not for classes that designed to be just a part of an application.  This
repository most uses the packages 'cufy.io', 'cufy.nio'.

- ### **Buffer** [<font size="3">(cufy.nio.Buffer)</font>][io-buffer]
A class that holds data and provide it using a cursor. Its cursor can be set manually but it can't store data at a position other than the
position of its cursor. It’s cursor increments dynamically when any data stored at it.

- ### **Buffered- InputStream / Reader** [<font size="3">(cufy.io.*)</font>][io-io*]
Since not all readers and input-streams don't support 'mark()' and 'reset()'. These classes stores the read data after invoke 'mark()'. Then supply
the user with the buffered data after invoking 'reset()'.

- ### **Remote- InputStream / OutputStream / Reader / Writer** [<font size="3">(cufy.io.*)</font>][io-io*]
A boxing for streams, readers or writer to gain the ability to be controlled. The boxing uses Instructor to check what position it should be.

- ### **Loadable** [<font size="3">(cufy.lang.Loadable)</font>][io-loadable]
An interface to identify an object that can be loaded from a stream or a reader and can be saved to a stream or a writer. The implementing class
should able to provide an input-stream, an output-stream, a reader, and a writer. Also a controllable version of them. And should specify the way
to save-to/load-from the streams or reader and writer that it can provide.

- ### **FileLoadable** [<font size="3">(cufy.io.FileLoadable)</font>][io-file_loadable]
An implementation for the interface Loadable. The implementation provides the required stream, reader, and writer specified by the loadable
interface. It provides the required resources from the file that the implementing class provides to it.

- ### **URLLoadable** [<font size="3">(cufy.io.URLLoadable)</font>][io-url_loadable]
An implementation for the interface Loadable. The implementation provides the required stream, reader, and writer specified by the loadable
interface. It provides the required resources from the URL that the implement class provides to it.

- ### **FormatLoadable** [<font size="3">(cufy.text.FormatLoadable)</font>][io-format_loadable]
An implementation for the interface Loadable. The implementation provides the way to save-to/load-from the resources provided from the implement
class. The implementation uses a format (specified to be provide) to save and load data.
