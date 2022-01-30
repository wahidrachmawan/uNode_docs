# SetValue

![](../../images/node_reference_set.png)

The SetValue node is a node to Set value of a variable, and property.

## Examples

Graph:

![](../../images/node_reference_set_example1.PNG)

Generated script:
```cs
#pragma warning disable
using UnityEngine;
using System.Collections.Generic;

public class test : MonoBehaviour {
	public int variable1 = 0;

	void Start() {
		Debug.Log(variable1);
		variable1 = 100;
		Debug.Log(variable1);
	}
}
```

Output:
```
0
100
```