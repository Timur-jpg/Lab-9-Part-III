------------------------------------------------------------------------
Super Calculator
Author: Hacker T. Largebrain
------------------------------------------------------------------------

This program implements a highly efficient calculating engine for
a pocket calculator. It includes a complete test rig to demonstrate
that the engine works as it should.


22. CalcEngineTester calcEngi1 = new CalcEngineTester();
    calcEngi1.testAll();
    Testing the addition operation.
    The result is: 7
    Testing the subtraction operation. 
    The result is: 5
    All tests passed. 
    
    No, I believe the test is misleading.
    
23. The first call gives 1 
    No, it is different
    The second call gives 7 
    Yes 
    It should always give 7
    
24. No, it gives two different answers, it returns 5 the first call (the correct return) and -13 the following times (the wrong return),
    
25. The testMinus() method returns 5 on the first call and -13 on subsequent calls. This raises questions about whether the clear() method properly resets all internal state variables like leftOperand and previousOperator, or if leftover state from previous calculations is causing incorrect results.

26. Method called displayValue leftOperand previousOperator 
    numberPressed(4)   4             3            '+' 
       equals()        7             0            '+' 
   getDisplayValue()   7             0            '+' 

27. No, the equals() method only checks if previousOperator is '+' or else assumes it's '-'. If previousOperator is still the default value ' ' (space), the else branch will incorrectly perform subtraction instead of handling it properly.

28. After calling clear(), the displayValue is 0 and leftOperand is 0, but previousOperator remains '+' instead of being reset to ' ' like it was initially. This means the engine is not in the same state as the previous call to clear, and this leftover operator will cause subsequent calculations to incorrectly apply addition logic, leading to wrong results.
    

