# Questions and Answers List 💪

1. ❓ **Explain the difference between a class and an object.**

   💁‍  *In short, a class is the definition of an object, and an object is instance of a class.
      We can look at the class as a template of the object: it describes all the properties, methods, states and behaviors that the implementing object will have. As mentioned, an object is an instance of a class, and a class does not become an object until it is instantiated. There can be more instances of objects based on the one class, each with different properties.*

2. ❓ **Explain the difference between managed and unmanaged code.**

   💁‍  *MANAGED CODE is a code created by the .NET compiler. It does not depend on the architecture of the target machine because it is executed by the CLR (Common Language Runtime), and not by the operating system itself. CLR and managed code offers developers few benefits, like garbage collection, type checking and exceptions handling.*
   
   *On the other hand, UMANAGED CODE is directly compiled to native machine code and depends on the architecture of the target machine. It is executed directly by the operating system. In the unmanaged code, the developer has to make sure he is dealing with memory usage and allocation (especially because of memory leaks), type safety and exceptions manually. In .NET, Visual Basic and C# compiler creates managed code. To get unmanaged code, the application has to be written in C or C++.*

3. ❓ **Explain the difference between boxing and unboxing. Provide an example.**

   💁‍  *Boxing is the process of converting a value type to the type object, and unboxing is extracting the value type from the object. While the boxing is implicit, unboxing is explicit.*

   🤜 *C# Example*
   ```
    int i = 13;
    object myObject = i; 	// boxing 
    i = (int)myObject;	// unboxing 
   ```

4. ❓ **Discuss the difference between constants and read-only variables.**

   💁‍  *While constants and read-only variable share many similarities, there are some important differences:*

      * *Constants are evaluated at the compile-time, while the read-only variables are evaluated at the runtime.*
      * *Constants support only value-type variables, while read-only variables can hold reference type variables.*
      * *Constants should be used when the value is not changing during the runtime, and read-only variables are used mostly when their actual value is unknown before the runtime.*

5. ❓ **Explain what LINQ is.**

   💁‍  *LINQ is an acronym for Language Integrated Query, and was introduced with Visual Studio 2008. LINQ is a set of       features that extends query capabilities to the .NET language syntax by adding sets of new standard query             operators that allow data manipulation, regardless of the data source. Supported data sources are: .NET               Framework collections, SQL Server databases, ADO.NET Datasets, XML documents, and any collection of objectsthat support `IEnumerable` or the generic `IEnumerable<T>` interface, in both C# and Visual Basic. In short, LINQ bridges the gap between the world of objects and the world of data.*

6. ❓ **Discuss what garbage collection is and how it works. Provide a code example of how you can enforce garbage                collection in .NET.**

   💁‍  *Garbage collection is a low-priority process that serves as an automatic memory manager which manages the allocation and release of memory for the applications. Each time a new object is created, the common language runtime allocates memory for that object from the managed Heap. As long as free memory space is available in the managed Heap,the runtime continues to allocate space for new objects. However, memory is not infinite, and once an application fills the Heap memory space, garbage collection comes into play to free some memory. When the garbage collector performs a collection, it checks for objects in the managed Heap that are no longer being used by the application and performs the necessary operations to reclaim the memory. Garbage collection will stop all running threads, it will find all objects in the Heap that are not being accessed by the main program and delete them. It will then reorganize all the objects left in the Heap to make space and adjust all the Pointers to these objects in both the Stack and the Heap.*

    🤜 *To enforce garbage collection in your code manually, you can run the following command (C#)*
   ```
   System.GC.Collect();
   ```

7. ❓ **What do the following acronyms in .NET stand for: IL, CIL, MSIL, CLI and JIT?**

   💁‍ ***IL**, or Intermediate Language, is a CPU independent partially compiled code. IL code will be compiled to native machine code using current environmental properties by **Just-In-Time** compiler (JIT). JIT compiler translates the IL code to an assembly code and uses the CPU architecture of the target machine to execute a .NET application. In .NET, IL is called **Common Intermediate Language** (CIL), and in the early .NET days it was called **Microsoft Intermediate Language** (MSIL).*

   ***CLI**, or Common Language Infrastructure, is an open specification developed by Microsoft. It is a compiled code library used for deployment, versioning, and security. In .NET there are two CLI types: process assemblies (EXE) and library assemblies (DLL). CLI assemblies contain code in CIL, and as mentioned, during compilation of CLI programming languages, the source code is translated into CIL code rather than into platform or processor specific object code.*
      
      *To summary:*

      1. *When compiled, source code is first translated to IL (in .NET, that is CIL, and previously called MSIL).*
      2. *CIL is then assembled into a bytecode and a CLI assembly is created.*
      3. *Before code execution, CLI code is passed through the runtime’s JIT compiler to generate native machine code.*
      4. *The computer’s processor executes the native machine code.*

8. ❓ **Explain the difference between the Stack and the Heap.**

   💁‍  *The short answer would be: in the Stack are stored value types (types inherited from `System.ValueType`), and in the Heap are stored reference types (types inherited from `System.Object`).*
   
   *We can say the Stack is responsible for keeping track of what is actually executing and where each executing thread is (each thread has its own Stack). The Heap, on the other hand, is responsible for keeping track of the data, or more precise objects.*

9. ❓ **Explain what inheritance is, and why it’s important.**

   💁‍  *Inheritance is one of the most important concepts in object-oriented programming, together with encapsulation and polymorphism. Inheritance allows developers to create new classes that reuse, extend, and modify the behavior defined in other classes. This enables code reuse and speeds up development. With inheritance, developers can write and debug one class only once, and then reuse that same code as the basis for the new classes. The class whose members are inherited is called the base class, and the class that inherits those members is called the derived class. By default, all classes in .NET are inheritable.*

# References

1. [13 Essential .NET Interview Questions*](https://www.toptal.com/dot-net/interview-questions)
2. [Hire the Best Developer with These 15 .NET Interview Questions](https://www.roberthalf.com/technology/blog/9-net-interview-questions-with-sample-answers)
3. [50 C# Interview Questions And Answers](http://www.c-sharpcorner.com/uploadfile/8ef97c/c-sharp-net-interview-questions-and-answers)

