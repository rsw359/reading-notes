# *Javascript/Jquery*

## Error Handling & Debugging

### Order of Operations

- The JavaScript interpreter process code one line at a time
  - There are 2 phases of activity during the execution of a script:
    - Preparation:
      - Scope is created
      - Variables, functions and arguments are created
      - The value of `this` is determined
    - Execution:
      - Variables are assigned values
      - Functions are referenced and run
      - Statements are executed
    - If an exception is thrown, the interpreter stops and looks for exception handling code within the function
      - If no exception handler is present, the interpreter checks globally, then stops if none is present
      - At this point, an error pbject is created
    - There are seven types of error objects
      - Error: generic error
      - SyntaxError: syntax has not been followed
      - ReferenceError: tried to reference a variable that is not declared or within scope
      - TypeError: an unexpected data type cannot be coerced
      - RangeError: numbers not in accptable range
      - URIError: URI methods used incorrectly
      - EvalError: eval() function used incorrectly

  - Debug the script
    - The source of the error must be tracked down and corrected
      - Useful debugging workflow: pg 463
      - The console.log method is a key tool in this process(among other console methods: console.table, console.group, console.assert)
      - Breakpoints can be used to stop a script so it can be checked in a certain point in its execution, using them at each step is a useful method to see where a problem occurs
      - Conditions can be applied to a breakpoint so that it is only triggered under certain conditions.
  - Handle errors gracefully
  - If an error occurs that is out of your control, try, catch and throw, or finally statements can be used(p.481)
  