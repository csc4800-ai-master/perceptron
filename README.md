# Perceptron Training
The purpose of this assignment is to code the Perceptron training algorithm.

## Algorithm Pseudocode
```
Step 0:	Initialize weights and bias
		w = 0		b = 0
		Set learning rate alpha (0 < alpha <= 1)

Step 1:	While stopping condition is false

Step 2:		For each training set pair s:t

Step 3:			Set activation of input units
				x = s

Step 4:			Compute response of output unit
				yin = b + sum(xi * wi) = b + x⋅w
				y  = 1  if yin > theta
				y  = 0  if –theta <= yin <= theta
				y  = -1 if yin < -theta

Step 5:			Update weight and bias if an error occurred
				if (y <> t)
					wi = wi + alpha* t * xi
					b = b + alpha * t
Step 6:		Test stopping condition: if no weights changed in Step 2, stop, else continue
```

## Training
Train your algorithm with:
* **AND** Training set, binary input, bipolar targets
x1 | x2 | target
-- | -- | -----
1 | 1 | 1
1 | 0 | -1
0 | 1 | -1
0 | 0 | -1
* **AND** Training set, bipolar input and targets (`and-bipolar.json`)

## Program Requirements
* The code should generalize on the number of features (dimensions), and the
  number of examples
* The code should validate that it receives the command line argument and that
  it is able to open the file
* After training add code to test you trained neuron, you may use the `training`
  vector for this purpose and output the inputs of the trained neuron with its
  output for each example.
* Remember to use good programming practices
