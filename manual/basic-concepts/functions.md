# Functions

Functions in uNode are used to define behavior. They are used to create some focused logic used to complete a specific task and can be invoked, or called, to execute the node created inside of them. 

Characteristics of Functions:
- A function is root that contains a series of node.
- Each function can have attributes, modifier, parameter, and generic parameter.

> [!TIP]
> To keep your graph organized, the use of function is very recommended instead of 'Event' inside `State Graph`.

## Return Types

All function have a return type. What does this mean? When you call a function, it can return a value or not. If it does not, it still has a return type and we call that a `void` return type. If a method is typed as `void`, it simply means that the function doesn’t return a value to it's caller.

## Parameters

Parameters is the data that can be passed to functions. You can add as many parameters as you want.

Characteristics of Parameters:
- Parameter has they own name, and a return type.
- Parameters act as variables inside the function the value of parameter can be retrieved or modified.