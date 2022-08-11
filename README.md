# Parallel Test Runner - Exercise: Synchronization

This program is a test suite with individual unit tests running in parallel using multiple threads.

When running these tests normally (sequentially), the test runner can take 10+ seconds to complete. 
On the other hand, when the test runner execute the tests in parallel, it takes only a few seconds total to complete, 
since all the test methods run concurrently with one another.

*Note:* If you peek in `CalculatorTest.java`, you'll notice the tests aren't really doing a whole lot; 
they use `Thread#sleep()` to make them artificially long-running for the purposes of this exercise.


## Compiling and Running

Try out the parallel test runner!

    javac -cp . *.java tests/*.java
    java -ea -cp . TestRunner tests/ tests.CalculatorTest

## Output

The output should look something like this

    Passed tests: [tests.CalculatorTest#testAddition, tests.CalculatorTest#testMultiplication, tests.CalculatorTest#testDivision]
    FAILED tests: [tests.CalculatorTest#testSubtraction]
    Test execution took 3 second(s).