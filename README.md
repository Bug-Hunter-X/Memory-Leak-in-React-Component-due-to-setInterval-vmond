# React setInterval Memory Leak
This repository demonstrates a common mistake in React: using setInterval within useEffect without proper cleanup.  This can lead to memory leaks and unexpected behavior.

The `bug.js` file contains the problematic code. The `bugSolution.js` file shows the corrected version.

**Problem:** The setInterval function continuously updates the count state. Without clearing the interval when the component unmounts, the interval continues to run, causing a memory leak. 

**Solution:** Use the return value of useEffect to cleanup the interval when the component unmounts.