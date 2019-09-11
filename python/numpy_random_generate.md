# Random generate in Numpy

## Integer
```
import numpy as np

# Generate integer from 0 to 99
i = np.random.randint(10)
# Generate integer from 10 to 99
I = np.random.randint(10,100)
# Generate 5 integer values from 10 to 99
j = np.random.randint(10,100,5)
# Generate 10 integer values from 10 to 99, and make 2*5 matrix
J = np.random.randint(10,100,(2,5))
```

## from distribution
Usnig numpy, there are a lot of generate method by many distribution.
```
import numpy as np

# Generate 3 values from the standard normal distribution
r = np.random.randn(3)
# Generate 6 values and make 2*3 matrix
R = np.random.randn(2,3)

# Generate from normal distribution(average=50, standard_deviation=10)
n = np.random.normal(50, 10)

# Generate from binomial distribution
# Number of coins that appear with a probability of 0.4
b = np.random.binomial(n=100, p=0.4)
```

