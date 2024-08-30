# CompSci 2a Assessment - Conversion And LRU Cache

Welcome to the conversion and LRU cache assessment!

The coding portion of this assessment consists of two problems:

1. Hexadecimal to string, a conversion problem (6 specs)
2. User registration, an LRU cache problem (11 specs)

The code file for each problem is in the __problems__ directory. Your objective
is to complete the code in the __problems__ directory so that all specs pass.
Each spec is worth 1 point. Further instructions appear below.

You will have **2 hours and 55 minutes** to complete the assessment (including
the multiple choice portion).

## Points breakdown

* __Multiple Choice Section:__ 14 points total  
* __Coding Problem Section:__ 17 points total

__Total Possible Points:__ 31 points  
__Points Required to Pass:__ 25 points

## Resources

For this assessment, you are allowed to use the following resources:

* [a/A curriculum on Canvas][canvas]
* [MDN]
* A whiteboard or paper to work out problems/code, but it must be within camera
  range
* VS Code or a console for coding, testing, and experimentation during any part
  of the test, including multiple-choice questions
* Node
* Postman (when useful)
* Previously written code you wrote yourself
  * Except for code from previous assessment submissions
* Comments within code
  * If there are comments in your code about your specific code and about what
    your code is doing, that is appropriate. If your comments are about concepts
    and based on the readings, then that counts as notes. Those would not be
    appropriate.

You are **NOT** allowed to refer to any other resources, including--but not
limited to--other websites (e.g., StackOverflow), communication apps (e.g.,
Slack, Discord), search engines, notes, or code from previous assessment
submissions.

[canvas]: https://appacademy.instructure.com/
[MDN]: https://developer.mozilla.org/en-US/

## Setup

1. Clone this starter repo and open it in VS Code.
2. Run `npm install` in the root directory.
3. Run `npm test` to see all the specs you need to pass.
4. Read the instructions below to get started!

## Problem 1: Hexadecimal to string

Convert a Hexadecimal array of numbers into decimal values. The decimal values
should be treated as ASCII character codes and converted into characters. Return
a string of those characters.

See the [MDN docs for `String.fromCharCode()`][fromCharCode-mdn] method
for how to convert character codes into ASCII characters.

Fill out the code in the __problems/01-hexadecimal-to-string.js__ file. Test
your code using the following command:

```bash
npm test test/01-hexadecimal-to-string-spec.js
```

The code file also has local tests that you can run with `node`. To run them,
simply uncomment the tests you want to run and then run the following command in
the terminal:

```bash
node problems/01-hexadecimal-to-string.js
```

## Problem 2: User registration

You have joined a new team and are given the task of investigating the user
registration service. The service works fine but has grown increasingly sluggish
as the site has gained in popularity.

1. Only a fixed number of users can be registered at once. If a new user
   registers after the max has been reached, the user who has been registered
   the longest is unregistered.

2. Once a username is taken, that username can **never** be chosen again, even
   if that user is unregistered.

Your goal is to optimize this code so it can register 1 million new users with a
max of 500 thousand users in under 1000ms.

### User registration hints

1. Start by understanding the problem and identifying performance bottlenecks.
2. Use Big-O analysis: Which operations can be optimized?
3. Consider all the tools (data structures) you have learned this week and pick
   the right tool for the job.  An optimal solution for this problem will use 1
   set, 1 linked list, and 0 arrays.
   * **Important Note:** You **MUST** use the `LinkedList` class provided for
     you in the starter code.

Fill out the code in the __problems/02-user-registration.js__ file.

There are two sets of test specs for this problem, implementation and timing
specs.

You can test the implementation of your code with the implementation specs using
the following command:

```bash
npm test test/02a-user-registration-implementation-spec.js
```

You can test the optimization of your code with the timing specs using the
following command:

```bash
npm test test/02b-user-registration-timing-spec.js
```

An important note for the timing specs:

There is a time buffer built into the timing specs to account for processor
speeds. Your actual grade will be scored on a processor that is different from
yours, so the amount of test specs you actually fail/pass may be different from
what you see in your local machine when you run the timing specs. Make sure you
read the instructions carefully to check that you achieved what the problem is
asking you to do.

## Submission

When you are ready to submit:

1. Run `npm test` to re-run all of the unit tests.

2. Fix any syntax errors that cause the tests to crash. **If a unit test crashes
   or the tests fail to complete their run, you will receive a 0 for the coding
   portion of this assessment.** You can fail specs, but all the tests have to
   be able to finish running.

   **Tip:** If you run out of time to debug, just comment out any code that is
   causing your programs to crash.

3. Add, commit, and push your changed files:

   ```sh
   git add .
   git commit -m "Finish the assessment (or some such descriptive message)"
   git push
   ```

   **Note:** The first time you run `git push`, git will tell you to run a more
   complete version of the command:

   ```sh
   git push --set-upstream origin <your branch>
   ```

You can run tests, `add` files, and `commit` files as often as you wish, but
only your first **two pushes** will be graded. (If for some reason you need more
than two pushes, you must plead your case to an Instructor.)

Good luck!

**Copyright App Academy. Please do not share this repo or post any parts of it
online. App Academy will take violations very seriously.**

[fromcharcode-mdn]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode
