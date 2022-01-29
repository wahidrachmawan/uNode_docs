# Nodes

Nodes are the most basic part of creating scripts in uNode. They can do a variety of things; for example, they can listen for events, get the value of a variable, or modify a component on a GameObject.

Nodes appear as "blocks" in the Graph Editor: 

You can arrange and connect these blocks to create logic for your application.

## Connections and ports

You can connect a port from one node to a compatible port on another node, to create a logical flow in your uNode graphs. uNode highlights ports on any other nodes in your graph where you can make a valid connection, and dims any ports where there isn't a valid connection.

Connections are also color-coded: connections that control the logic flow in your graph are green ( based on theme ), and connections for values are colored based on the value's type. For more information about types, see Object types.

Ports on the left side of a node are **Input Ports**. Ports on the right side of a node are **Output Ports**.

Input and output ports can also have different types: 
![](../../images/node_interface.png)

|Port  |Descripton  |
|---------|---------|
|Flow Port     |  Flow ports control the logical flow of your graphs. They tell uNode what order it should execute the nodes in a graph, from up to down.      |
|Value Port     |      Value ports send and receive data, such as number values or GameObjects, between nodes. They also have colors that correspond to the specific type they expect to receive as inputs, or send as outputs.   |

You can make multiple connections from a single Value Output port to different Value Input ports, or have multiple Flow Output ports that connect to a single Flow Input: 
![](../../images/node_ports.png)

You can't connect multiple Value Output ports to a single Value Input port, because it wouldn't be clear which value should use in your application. You also can't connect a single Flow Output port to multiple Flow Input ports, because uNode wouldn't know which node to run first. 