# Foreach

![](../../images/node_reference_foreach.png)

The Foreach node repeats Body port for each element in an array or an object collection.

## Examples

Graph:
![](../../images/node_reference_foreach_example1.png)

Generated script:
```cs
#pragma warning disable
using UnityEngine;
using System.Collections.Generic;

public class test : MonoBehaviour {
	public int[] array = new int[] { 1, 2, 4, 8, 16 };

	void Start() {
		foreach(var loopObject in array) {
			Debug.Log(loopObject);
		}
	}
}
```

Output:
```
1
2
4
8
16
```