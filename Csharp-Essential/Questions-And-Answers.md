# Questions and Answers List 💪

1. ❓ **Explain the difference between a class and an object.**

   💁‍ *In short, a class is the definition of an object, and an object is instance of a class.
      We can look at the class as a template of the object: it describes all the properties, methods, states and behaviors that the implementing object will have. As mentioned, an object is an instance of a class, and a class does not become an object until it is instantiated. There can be more instances of objects based on the one class, each with different properties.*

2. ❓ **Explain the difference between managed and unmanaged code.**

   💁‍ *MANAGED CODE is a code created by the .NET compiler. It does not depend on the architecture of the target machine because it is executed by the CLR (Common Language Runtime), and not by the operating system itself. CLR and managed code offers developers few benefits, like garbage collection, type checking and exceptions handling.*
   
   *On the other hand, UMANAGED CODE is directly compiled to native machine code and depends on the architecture of the target machine. It is executed directly by the operating system. In the unmanaged code, the developer has to make sure he is dealing with memory usage and allocation (especially because of memory leaks), type safety and exceptions manually. In .NET, Visual Basic and C# compiler creates managed code. To get unmanaged code, the application has to be written in C or C++.*

3. ❓ **Explain the difference between boxing and unboxing. Provide an example.**

   💁‍ *Boxing is the process of converting a value type to the type object, and unboxing is extracting the value type from the object. While the boxing is implicit, unboxing is explicit.*

   🤜 *C# Example*
   ```
    int i = 13;
    object myObject = i; 	// boxing 
    i = (int)myObject;	// unboxing 
   ```

4. ❓ **Discuss the difference between constants and read-only variables.**

   💁‍ *While constants and read-only variable share many similarities, there are some important differences:*

      * *Constants are evaluated at the compile-time, while the read-only variables are evaluated at the runtime.*

      * *Constants support only value-type variables, while read-only variables can hold reference type variables.*
      * *Constants should be used when the value is not changing during the runtime, and read-only variables are used mostly when their actual value is unknown before the runtime.*

# References

1. [13 Essential .NET Interview Questions*](https://www.toptal.com/dot-net/interview-questions)
2. [Hire the Best Developer with These 15 .NET Interview Questions](https://www.roberthalf.com/technology/blog/9-net-interview-questions-with-sample-answers)
3. [50 C# Interview Questions And Answers] (http://www.c-sharpcorner.com/uploadfile/8ef97c/c-sharp-net-interview-questions-and-answers/)

