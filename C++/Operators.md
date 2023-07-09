* Assignment operators are right-associative
	```x=y=z=15 => x=(y=(z=15))```
	So you should have assignment operators return a reference to \*this (left hand argument)
* Assignment operator should handle if the object is the same
	``if(this == &copy) return *this;``
* Copying functions should be sure to copy all of an object's data members and all of its base class parts
