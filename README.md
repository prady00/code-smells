# Classic Code smells 


# Bloaters

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

## Long Methods

In their description of this smell, Fowler and Beck explain several good reasons why short methods are superior to long methods. A principal reason involves the sharing of logic. Two long methods may very well contain duplicated code. Yet if you break those methods into smaller methods, you can often find ways for the two to share logic. Fowler and Beck also describe how small methods help explain code. If you don’t understand what a chunk of code does and you extract that code to a small, well-named method, it will be easier to understand the original code. Systems that have a majority of small methods tend to be easier to extend and maintain because they’re easier to understand and contain less duplication

## Large Classes

Fowler and Beck note that the presence of too many instance variables usually indicates that a class is trying to do too much. In general, large classes typically contain too many responsibilities

## Data Clumps

You can rename the current file by clicking the file name in the navigation bar or by clicking the **Rename** button in the file explorer.

## Long Parameter List

Long lists of parameters in a method, though common in procedural code, are difficult to understand and likely to be volatile. Consider which objects this method really needs to do its job - it's okay to make the method to do some work to track down the data it needs

## Primitive Obsession

Primitives, which include integers, Strings, doubles, arrays and other low-level language elements, are generic because many people use them. Classes, on the other hand, may be as specific as you need them to be, since you create them for specific purposes. In many cases, classes provide a simpler and more natural way to model things than primitives. In addition, once you create a class, you’ll often discover how other code in a system belongs in that class. Fowler and Beck explain how primitive obsession manifests itself when code relies too much on primitives. This typically occurs when you haven’t yet seen how a higher-level abstraction can clarify or simplify your code.

# Tool Abusers

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

## Switch Statements

This smell exists when the same switch statement (or “if…else if…else if” statement) is duplicated across a system. Such duplicated code reveals a lack of object orientation and a missed opportunity to rely on the elegance of polymorphism

## Refused Bequest

This smell results from inheriting code you don't want. Instead of tolerating the inheritance, you write code to refuse the "bequest" -- which leads to ugly, confusing code, to say the least

## Alternative Classes w/ Different Interfaces

occurs when the interfaces of two classes are different and yet the classes are quite similar. If you can find the similarities between
the two classes, you can often refactor the classes to make them share a common interface

## Temporary Fields

Objects sometimes contain fields that don't seem to be needed all the time. The rest of the time, the field is empty or contains irrelevant data, which is difficult to understand. This is often an alternative to Long Parameter List

# Change Preventers

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

## Divergent Change

Occurs when one class is commonly changed in different ways for different reasons. Separating these divergent responsibilities decreases the chance that one change could affect another and lower maintenance costs

## Shotgun Surgery

This smell is evident when you must change lots of pieces of code in different places simply to add a new or extended piece of behavior.

## Parallel Inheritance Hierarchies

This is really a special case of Shotgun Surgery - every time you make a subclass of one class, you have to make a subclass of another


# Dispensibles

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

## Lazy Class

A class that isn’t doing enough to pay for itself should be eliminated

## Speculative Generality

All your files are listed in the file explorer. You can switch from one to another by clicking a file in the list.

## Data Class

You can rename the current file by clicking the file name in the navigation bar or by clicking the **Rename** button in the file explorer.

## Duplicated Code

Duplicated code is the most pervasive and pungent smell in software.It tends to be either explicit or subtle. Explicit duplication exists in identical code, while subtle duplication exists in structures or processing steps that are outwardly different, yet essentially the same

# Couplers

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

## Feature Envy

Data and behavior that acts on that data belong together. When a method makes too many calls to other classes to obtain data or functionality, Feature Envy is in the air

## Inappropriate Intimacy

Sometimes classes become far too intimate and spend too much time delving into each others’ private parts. We may not be prudes when it comes to people, but we think our classes should follow strict, puritan rules. Over-intimate classes need to be broken up as lovers were in ancient days

## Message Chains

Occur when you see a long sequence of method calls or temporary variables to get some data. This chain makes the code dependent on the relationships between many potentially unrelated objects.

## Middle Man

Delegation is good, and one of the key fundamental features of objects. But too much of a good thing can lead to objects that add no value, simply passing messages on to another object.

# References 

http://www.industriallogic.com/wp-content/uploads/2005/09/smellstorefactorings.pdf
