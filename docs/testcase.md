### What is a test case?
A test case traditionally is a combination of input arguments and 
intermediate and final results expected from function under microscope.

A test case could be marked as a pass if the intermediate and final 
results match with the expected values, but will be marked as a fail 
even if a single result does not match. These tests can be termed 
deterministic or of a polarized nature.

But not all test cases can be so polarized. Could we maybe mark a test
as half successful if only half of the final results match?

### NBI test cases
NBI fits within the pattern where a test case is an indication of how 
the behavior of the function should depict, but not necessary follow.
It is more of a guidance than a requirement.

For instance we could say that in summer, summer dominated appliances 
like AC should be recommended more than not. But not doing so, or 
reaching halfway into the goal does not make the test case as a failure. 
In this instance possibly this requirement could be classified as half
successful if the actual results match only half the time. 

But there could be other instances when things are more polarized. For instance, not showing recommendations for an appliance if the dollar 
spent was less than 2. A test case in this case is a failure if even one of the top 10 recommendations contains such an appliance.

So in general on a high level, there could be a couple of test class 
types: a polarized yes / no type and a linear type. There could be more
such as logistic but in the interest of keeping things simple, 
let's ignore other types.

### Actual example
Let's follow it up with an actual example in a notebook environment in
the notebook folder called first_run.ipynb. GL!