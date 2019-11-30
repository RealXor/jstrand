# jstrand
C++ library (and soon to be Bytecode Editor) to decompile, manipulate and compile Java binary class files

# Structure 
The structure of jstrand aims to be as simple as possible, whilst still providing a solid amount of features and good performance when compiling. It's built on top of a single header file `jstrand.h` which will avoid the pain and hassle of multiple includes when trying to use jstrand. 

The structure as of writing this Readme is as follows:

```
{jstrand location}\jstrand.h // library main header file, simple logging and default includes 
                  \jvm.h // main header file for all JVM related utilities, contains ClassFile wrapper 
                  \class\class_info.h // stores all class related utilities
```

# Speed
Speed was the goal when writing this library, so I'm trying to optimize this as much as possible (ex. Memory isn't allocated and written to but rather copied into existing memory and smart pointers) Current benchmarks have revealed promising results, being able to parse the constants table of a class file that's a megabyte big within 3 thousands of a second. 

# ZIP Archiving
With the recent surge in ZIP exploits related to entry names, entry sizes and the likes jstrand will come bundled with its own simple ZIP parser to make sure it stays future proof along the way. 

# Credits 
Me - Everything at the moment

You can contribute as well! Once we've gotten a working library issues will be reopened and you can voice your concerns anytime you feel like it. Note: Edits are not guaranteed. 
