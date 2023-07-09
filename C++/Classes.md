<h2> Fields </h2>
* Always initialize your objects before using them
* Data members of an object are initialized before the body of a constructor is entered, so use initialization list on constructor instead of assignments
	``Class::Class(int param) : field(param) { ... body calls later ...	}
* A call to a copy constructor is more efficient than a call to the default constructor followed by copy assignment (that's why we use initialization list, to avoid assignment later)
* Also use initialization list when default-initializing data members (name())
* If we have multiple constructors, we can use a private method as initialization to share in all of them
* Data members are initialized in the order they are declared, so try to initialize them in the same order in the constructor to avoid misunderstandings
* Replace global static objects with local static objects (singleton pattern) to avoid initialization order problems across different translation units (scripts)
<h2> Generated Functions </h2>
* Constructor, copy constructor, copy assignment operator and destructor default methods will be created even if you don't declare them
* If you declared one of the methods already, they will not be overloaded by a default method.
* If some of the methods are not trivial, compiler will fail to generate default versions
* To avoid some functions to be used (copy constructor, copy assignment operator...), we can declare them (to avoid compiler generate them) and make them private (so no-one can use them), and not implement them (so even if other functions inside the class call them, they will do nothing)
<h2> Destructors </h2>
+ Polymorphic base classes should declare virtual destructors to avoid partially-destroyed objects.
+ If a class has any virtual functions, it should have a virtual destructor
+ Non-polymorphic or non-base classes shouldn't declare virtual destructors
+ Destructors should never emit exceptions, instead, move all code that can produce exceptions into another function that handles that (i.e. closeDatabase())
<h2>Others</h2>
* Never call virtual functions during construction or destruction because those calls will never go to derived classes as they are still not initialized
