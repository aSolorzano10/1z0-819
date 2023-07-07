# Rules

## ACCESS MODIFIERS

- ***private*** The private modifier means the method can be called only from within the same class.
- ***Default (Package-Private)*** Access With default access, the method can be called only from classes in the same package. This one is tricky because there is no keyword for default access. You simply omit the access modifier.
- ***protected*** The protected modifier means the method can be called only from classes in the same package or subclasses. You’ll learn about subclasses in Chapter 8, “Class Design.”
- ***public*** The public modifier means the method can be called from any class.


## OPTIONAL SPECIFIERS
- ***static*** The static modifier is used for class methods and will be covered later in this chapter.
- ***abstract*** The abstract modifier is used when a method body is not provided. It will be covered in Chapter 9.
- ***final*** The final modifier is used when a method is not allowed to be overridden by a subclass. It will also be covered in Chapter 8.
- ***synchronized*** The synchronized modifier is used with multithreaded code. It is on the 1Z0-816 exam, but not the 1Z0-815 exam.
- ***native*** The native modifier is used when interacting with code written in another language such as C++. It is not on either OCP 11 exam.
- ***strictfp*** The strictfp modifier is used for making floating-point calculations portable. It is not on either OCP 11 exam.


## Applying Access Modifiers
- ***private:*** Only accessible within the same class
- ***Default (package-private) access:*** private plus other classes in the same package
- ***protected :*** Default access plus child classes
- ***public : protected*** plus classes in the other packages


## the protected rules apply under two scenarios:
- A member is used without referring to a variable. This is the case on lines 5 and 6. In this case, we are taking advantage of inheritance and protected access is allowed.
- A member is used through a variable. This is the case on lines 10, 11, 16, and 17. In this case, the rules for the reference type of the variable are what matter. If it is a subclass, protected access is allowed. This works for references to the same class or a subclass.
