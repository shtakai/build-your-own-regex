# Build Your Own Regex

[![GuardRails badge](https://badges.production.guardrails.io/shtakai/build-your-own-regex.svg)](https://www.guardrails.io)

This is a test spec driven guide to help you build a simple regex engine.

This regex engine supports the following syntax:

| Syntax | Meaning | Example | matches |
|--------|---------|---------|---------|
| a | Matches the specified character literal | q | q |
| * | Matches 0 or more of the previous character | a* | "", a, aa, aaa  |
| ? | Matches 0 or 1 of the previous character | a? | "", a |
| . | Matches any character literal | . | a, b, c, d, e ... |
| ^ | Matches the start of a string | ^c | c, ca, caa, cbb ... |
| $ | Matches the end of a string | a$ | ba, baaa, qwerta ... |

The goal is to provide a syntax robust enough to match a large portion of regex use cases with minimal code. The included solution is under 40 LOC.

This repo has an accompanying blog post that explains the solution [here](https://nickdrane.com/build-your-own-regex/)

## Install

```js
npm install
npm test
```

Now simply make changes to the `regex.js` file until the tests pass. Note that the tests are all pending the begin with. Just change the `xdescribe`s to `describe`s to switch the tests on.

## Requirements

This project requires a strong understanding of __recursion__ and wonderfully showcases it's elegance with a non-trivial example.

## Thanks

 I was inspired by Rob Pike's [original implementation](https://www.cs.princeton.edu/courses/archive/spr09/cos333/beautiful.html) of this program in c and Peter Norvig's rendition of it in Udacity's ["Design of Computer Programs"](https://www.udacity.com/course/design-of-computer-programs--cs212) course.
