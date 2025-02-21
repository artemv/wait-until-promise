# API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## setPromiseImplementation

[waitUntilPromise.js:27-29](https://github.com/SimenB/wait-until-promise/blob/633e29fac0b5e27bfb7891291cf01485a79107a9/waitUntilPromise.js#L27-L29 "Source code on GitHub")

Set a custom [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) implementation.

**Parameters**

-   `implementation` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** A promise implementation to use instead of native [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise).

## waitUntilPromise

[waitUntilPromise.js:42-86](https://github.com/SimenB/wait-until-promise/blob/633e29fac0b5e27bfb7891291cf01485a79107a9/waitUntilPromise.js#L42-L86 "Source code on GitHub")

Create a [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) that resolves if the given escapeFunction returns a truthy value, and rejects if it throws
or does not return truthy within the given maxWait.

**Parameters**

-   `escapeFunction` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** The function called every checkDelay, and the result of which is the resolved
    value of the promise. If it returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) its result will be waited for and checked.
-   `maxWait` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** The time to wait before rejecting the promise. (optional, default `50`)
-   `checkDelay` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** The time to wait before each invocation of {escapeFunction}. (optional, default `1`)

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** A promise resolved with the value of escapeFunction, or rejected with the exception thrown by it
or it times out.
