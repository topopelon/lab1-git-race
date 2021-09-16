# Integration Test

The file [IntegrationTest](./IntegrationTest.kt) contains the Test needed for easily verifying the different modules of the server always work correctly together.

JUnit and SpringBootTest are used for running the tests.

Currently it contains the following test:  
+ testHome: Tests the homepage of the server, checking if the word "Hello" shows up as a title

+ testCss: Tests the bootstrap, by checking if all its headers use a css type