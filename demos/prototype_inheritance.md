
# Prototype Inheritance Discussion

Parent object Sergio
Sebastian - child.

Inheritance model of JS, people generally assume things behave the same way in JS as other languages.

Java/C# - Inheritance between specification. Class is the specification, object is the instance.
JS - No specification, inheritance between live objects.

## C#/Java Inheritance
Parent and child -> DNA transference is a one-time transfer. 
After that they're independent.

## JS Inheritance
JS it is not that way. objects are all tied to the prototype. 
Live, ongoing relationship between the two objects at run-time.

Prototype chain for properties and example with Sebastian involving McD's.
Sebastian has his own amt property that hides his parent's.
This is called *shadowing*.

Javascript's *delete* operator can delete the amount property of Sebastian's object 
and restore the access to the parent object's property.

Sergio (parent object) has an address property. Sebastian decides to move away.

sebastian.address.state = 'NC';
sebastian.address.state = 'CA';

Getting goes up the chain to find the property. Setting does not.

Need to assign the entire address object 

sebastian.address is a GET and will refer to Sergio's address property.



