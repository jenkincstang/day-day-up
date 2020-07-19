## TDD Test Driven Development

TDD is a development of tests before a feature implementation.

#### So how is it possible? It can be described by following steps:

1. You read and understand requirements for a particular feature.
2. You develop a set of tests which check the feature. All of the tests are red, due to absence of the feature implementation.
3. You develop the feature until all tests become green.
4. Refactor the code.

#### Developing with TDD has valuable advantages:

1. You have a better understanding of a feature you implement.
2. You have robust indicators of feature completeness.
3. Code is covered with tests and has less chance to be corrupted by fixes or new features.

Don’t think about this as one test for one method. That is possible, but as a rule one unit test implies invocation of several methods. This is called testing of behavior.

#### Design principle of Unit test

1. **Small and fast unit tests** : Create **small and fast unit tests**, because they should be executed before each commit to a Git repository and new build to a server. Consider an example with real numbers in order to understand importance of unit tests speed. Do not perform database connection in unit tests (by definition unit tests are isolated) or perform initialisations of expensive objects in the @Before block.
2. **Choose good names for unit tests** : A name of a test can be as long as you want, but it should represent what the test verifies. For example if I need to test a default constructor of the Account class, I’ll name it *defaultConstructorTest*. One more useful piece of advice for choosing a test’s name is to write the test logic *before* you name the test. While you are developing a test you learn what happens inside of it, making it easier to name.
3. **Unit tests should be predictable** : This is the most obvious requirement. I’ll explain it by example. In order to check the operation of a money transfer (with 5% fee) you have to know which amount you sent and how much you get as output. This test scenario can be implemented as sending of $100 and receiving of $95.
4. **Well-grained** : And finally unit tests should be **well-grained**. When you put one logical scenario per test you can achieve informative feedback. And in cases of a single failure, you will not lose information about the rest of the functionality.
5. **Test behaviour but not method**  : Don’t think about this as one test for one method. That is possible, but as a rule one unit test implies invocation of several methods. This is called testing of behavior.

#### Basics of test design techniques

1. **Classes of equivalence technique**  : Randomly select multiple values within the legal value range for unit testing.

2. **Boundary testing technique** : Get the boundary value of the legal value range and the boundary value of the illegal value range.

3. https://dzone.com/articles/introduction-to-java-tdd

4. https://javacodehouse.com/blog/test-driven-development-tutorial/

   





