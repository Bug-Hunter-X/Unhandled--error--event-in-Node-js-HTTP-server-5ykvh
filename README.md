This repository demonstrates a common error in Node.js HTTP servers: unhandled errors.  The `bug.js` file contains a server that lacks proper error handling. When an error occurs (e.g., network issue), the server crashes without providing any useful information. The `bugSolution.js` file shows how to add error handling to prevent this.

**To Reproduce:**

1.  Run `node bug.js`
2.  Interrupt the server (e.g., by abruptly closing the connection)
3.  Observe the lack of informative error messages and the server crash.

**Solution:**

The `bugSolution.js` demonstrates the correct way to handle errors by listening for the 'error' event on the server object. This provides more detailed error information, preventing unexpected crashes and improving application stability.