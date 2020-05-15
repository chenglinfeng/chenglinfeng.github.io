---

layout: post
title:  "Algorithms Fourth Edition-Princeton University"
date:   2019-05-16 20:16:40 +0800
categories: jekyll update
---

## Fundamentals

**Creating and initializing an array.** Making an array in a Java program involves three distinct steps: 
* Declare the array name and type.
* Create the array. 
* Initialize the array values.

![](https://raw.githubusercontent.com/chenglinfeng/chenglinfeng.github.io/master/my_pics/2019-05-16-Algorithms%20Fourth%20Edition-Princeton%20University-pic1.png)

**Aliasing.** Note carefully that an array name refers to the whole array—if we assign one array name to another, then both refer to the same array, as illustrated in the following code fragment.

![](https://raw.githubusercontent.com/chenglinfeng/chenglinfeng.github.io/master/my_pics/2019-05-16-Algorithms%20Fourth%20Edition-Princeton%20University-pic2.png)This situation is known as aliasing and can lead to subtle bugs. If your intent is to make a copy of an array, then you need to declare, create, and initialize a new array and then copy all of the entries in the original array to the new array.

![](https://raw.githubusercontent.com/chenglinfeng/chenglinfeng.github.io/master/my_pics/2019-05-16-Algorithms%20Fourth%20Edition-Princeton%20University-pic3.png)

**Invoking a static method.** A method call followed by a semicolon is a statement that generally causes side effects. For example, the call Arrays.sort() in main() in BinarySearch is a call on the system method Arrays.sort() that has the side effect of putting the entries in the array in sorted order. When a method is called, its argument variables are initialized with the values of the corresponding expressions in the call. A return statement terminates a static method, returning control to the caller. If the static method is to compute a value, that value must be specified in a return statement (if such a static method can reach the end of its sequence of statements without a return, the compiler will report the error).

![](https://raw.githubusercontent.com/chenglinfeng/chenglinfeng.github.io/master/my_pics/2019-05-16-Algorithms%20Fourth%20Edition-Princeton%20University-pic4.png)