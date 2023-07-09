* **Use constants instead of macros:** Constants get saved on the symbol table easy to debug and trace, macros doesn't even reach the compiler (they get transformed)-
* Member function is const only if it doesn't modify any of the object's data members (excluding static members)
* Const parameters in functions act like local const objects
* Always use const to help compiler detect usage errors
* When const and non-const member functions have identical implementations, we can have non-const version call the const version
* **Mutable:** If we need to modify any class member inside a const function, we can use mutable
* Function returning a const value is generally inappropiate, but sometimes it can help on client safety usage (like assigning the return value to an operation)
* **Iterators:** declaring an iterator const avoids the iterator to point to something different. Declaring a const_iterator type avoids modifying the content which the iterator points to.
