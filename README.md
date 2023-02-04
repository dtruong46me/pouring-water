# Pouring Water Problem

## Problem Description
We have three tanks with volumes of **10-liter**, **7-liter**, and **4-liter**. Initially, the **7-liter** and **4-liter** jars are filled with water, and the **10-liter** jars are empty. We are only allowed to use the 2 operation: 
* Pour the remaining amount of water from one tank to another
* Only stopping when the tank is empty or the other tank is full

**Problem:**
With this sequence of operations, can we leave exactly **2-liter** of water in a **4-liter** jar or **2-liter** of water in a **7-liter** jar?

**Solution:**
To solve this problem, we build a directed graph **G<V,E>**, where:
* The vertex set **V** is the triples of non-negative integer **(x,y,z)** where **x**, **y**, **z** represent the amount of water in the three flasks **10-liter**, **7-liter**, **4-liter** respectively. *For example, the top of **(0, 7, 4)** represents: the **10-liter** jar is empty, the **7-liter** and **4-liter** jars are filled with water.*
* There is an arc connecting from the vertex **(x, y, z)** to the vertex **(x', y', z')** if from **(x, y, z)** the pouring operation can be used as above to get **(x', y', z')**. *For example, **(0, 7, 4)** → **(4, 7, 0)** → **(10, 1, 0)** means that we poured all the water from the **4-liter** jar into the **10-liter** jar, and filled the **10-liter** jar from the **7-liter** jar.*

Let's run the DFS Algorithms on the graph **G** starting from the vertex **(0, 7, 4)** to find the solution to the pouring water problem.

**Requirements:**
Draw a DFS tree *(without dashed arcs)* using **Graphiz** starting from the vertex **(4, 7, 0)**. If you need to decide the order of the visited vertices, use an order that you think is natural

## Algoritms
- Depth First Search (DFS)
- Breath First Search (BFS)
- A* Algorithm

## Reference

