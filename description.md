# Documentation

# How to test the code

Testing is handled using JUnit, a powerful framework that allows you to check different aspects of your code.

Unit tests can be run with the following commands.

```bash
cd lab1-git-race
gradle test
```

All verification tasks, including unit tests, can be run with the following commands. Gradle offers a flag, -i, that can be used to show more information while running the checks.

```bash
cd lab1-git-race
gradle check
```

## Integration Tests

There's 3 tests, stored at `src/test/kotlin`, that have been made for this Kotlin Webpage

---

### HTML/CSS Tests

The file `src/test/kotlin/IntegrationTest.kt` contains two tests that checks the main behaivour of the HTML page itself:

- `testHome()` checks if making a request at `http://localhost:$port` (With `$port` in this case being 0 for the shake of the test), yields both:

  - A `OK` HTTP Status Code.
  - A HTML body with `<title>hello`.

    If this happens, we can assume the webpage's HTML is the one intended.
- `testCss()` checks if the CSS of the webpage has basic functionality. For this, it request `http://localhost:$port/webjars/bootstrap/5.1.0/css/bootstrap.min.css` from the Web Server, and checks if it has a response with:

  - A `OK` HTML Status.
  - A body with `"body"`.
  - A file with a header equal to that of `"text/css"`.

This ensures the webpage has a valid CSS file.
