# Graphs

One of uNode key components is the graph. Graphs are visual representations of the logic in an application.

## Runtime Graphs

The Runtime Graphs can be referenced by other graphs directly without needed you to compile it into c# scripts. Runtime Graph can be run in both reflection and native c#. When the graph is not compiled, the graph is run with reflection which is slow compared to native but allow you to live edit it in playmode. And if the graph has been compiled the graph will be run with native c# which give you a performance boost but in return this doesn’t support live edit graph.

Here is the graph that is categorized as Runtime Graphs:

- Class Component
- Class Asset
- Class Singleton
- uNode Runtime

## C# Graphs

The C# Graphs are designed to create a pure c# scripts, this allow you to create from game logic to editor extensions but like its name the c# graphs can only be used by compiling it into c# scripts. With this types of graphs you can create from game logic to editor extension and this is the only graph that can be compiled to c# script without dependent on uNode Visual Scripting.

Here is the graph that is categorized as C# Graphs:

- C# Class
- C# Struct

## Types of Graphs

uNode has many different types of graphs, each of them can serve for different purpose.
Here is the list of avalaible graphs types:


| Graph           | Description                                                                                                                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Class Component | A runtime graph that's inherit from MonoBehaviour                                                                                                                                                            |
| Class Asset     | A runtime graph that's inherit from ScriptableAsset                                                                                                                                                          |
| Class Singleton | A runtime graph that's inherit from MonoBehaviour but act like Static Classes<br> This graph can be accessed from anywhere but it is guarantee that this graph only one instance can exist at the same time. |
| uNode Runtime   | A runtime graph like a Class Component graph but this graph that can be attached dirrectly to GameObject and can reference any object in the current scene that this graph is live                           |
| C# Class        | A c# graph that's intended for visually creating c# class. It can be inherited from any of C# Scripts and implementing any of C# Interfaces                                                                  |
| C# Struct       | A c# graph that's intended for visually creating c# struct. It can implementing any of C# Interfaces                                                                                                         |

### Graphs Features 

Legend:<br>
✅	= Supported<br>
❌	= Not Supported<br>
⚬	= Partially Supported<br>


| Features        | Class Component | Class Asset      | Class Singleton | C# Class          | C# Struct    | uNode Runtime |
| :---------------- | ----------------- | ------------------ | ----------------- | ------------------- | -------------- | --------------- |
| Variable        | ✅              | ✅               | ✅              | ✅                | ✅           | ✅            |
| Property        | ✅              | ✅               | ✅              | ✅                | ✅           | ✅            |
| Function        | ✅              | ✅               | ✅              | ✅                | ✅           | ✅            |
| Constructor     | ❌              | ❌               | ❌              | ✅                | ✅           | ❌            |
| State Graph     | ✅              | ❌               | ✅              | ✅                | ❌           | ✅            |
| Live Edit       | ✅              | ✅               | ✅              | ❌                | ❌           | ✅            |
| Reflection Mode | ✅              | ✅               | ✅              | ❌                | ❌           | ✅            |
| Attributes      | ⚬              | ⚬               | ⚬              | ✅                | ✅           | ❌            |
| Modifiers       | ⚬              | ⚬               | ⚬              | ✅                | ✅           | ❌            |
| Inheritance     | MonoBehaviour   | ScriptableObject | MonoBehaviour   | ✅ Any C# Classes | ❌           | MonoBehaviour |
| Interfaces      | Graph Interface | Graph Interface  | Graph Interface | C# Interface      | C# Interface | ❌            |

Features Description

- Reflection Mode	: For run a graph with reflection mode.
- Live Edit	: For live editing a graph during playmode.
- Attributes	: Attributes for classes, variables, properties, and functions. A partial mean that the attributes is only work on running with Native C# mode.
- Modifiers	: Modifiers for classes, variables, properties, and functions. A partial mean that it only have public and private modifier.
- Inheritance	: Default graph inheritance.
- Interfaces	: The supported interface implementations, it is C# Interface of Graph Interface.

## Types of Graph Canvas

uNode has two different types of graph canvas: Flow Graphs and State Graphs.

### Flow Graphs

Flow Graphs control and connect specific actions and values. The actions in a Flow Graph happen in a specific order. Actions could happen every frame, or when a specific event occurs.

uNode represents the actions in a Flow Graph through nodes.

In a Flow Graph, you can connect nodes together and use them to tell your application what it should do, and in what order.

Flow Graphs can access a large collection of nodes, which correspond to different features and functionality in the Unity Editor. You can access these nodes through uNode Item Selector.

### State Graphs

Unlike others State based Visual Scripting like Playmaker or Unity Visual Scripting State Graph. In uNode, State Graph is a combination of Flow Graph and State Graph so you can mix the Flow nodes and State nodes in easier way. The State Graph is just like a Flow Graph but with additional functionality like:

- In State Graph there's a special node that's only available in State Graphs like the Behavior Tree nodes and the State Nodes that act like Playmaker or Unity Visual Scripting's State Graph.
- In State Graph each of flow node will have state that's is success, running or failure, a Actions nodes that's not have a condition is always have success state.

The State Graphs is supported only on graph that's inherited from MonoBehavior or it's sub classes like:

- Class Component
- Class Singleton
- uNode Runtime
- C# Class that's inherited from MonoBehaviour or it's sub classes.
