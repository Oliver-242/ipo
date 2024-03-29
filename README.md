<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
  <h1>How To Use This Tool</h1>

  <p>This project has already been published on PYPI so just follow the tutorial below. <b>In terminal</b></p>

    pip install nwisepy

  <p>and then in your <b>python file</b></p>

    from nwisepy import Pairwise

  <p>An example <b>python code</b></p>

    from nwisepy import Pairwise
    
    parameters = [['a', 'b', 'c'], [1, 2, 3], [4, 5, 6]]
  
    result = Pairwise(parameters, 2).result()
    for idx, value in enumerate(result):
      print(f'{idx}: {value}')

  <p>and <b>output</b></p>

    0: ['a', 1, 4]
    1: ['a', 2, 5]
    2: ['a', 3, 6]
    3: ['b', 1, 6]
    4: ['b', 2, 4]
    5: ['b', 3, 5]
    6: ['c', 1, 5]
    7: ['c', 2, 6]
    8: ['c', 3, 4]

  <h1>Pairwise Testing Algorithm</h1>

  <p>Welcome to the Pairwise Testing Algorithm README! This document provides an introduction to the concept of Pairwise testing and its significance in software testing.</p>

  <h2>Introduction</h2>

  <p>Pairwise testing, also known as all-pairs testing or combinatorial testing, is a software testing technique that aims to systematically reduce the number of test cases that need to be executed while still providing thorough coverage. The primary goal is to detect defects that may arise due to interactions between different input parameters.</p>

  <h2>How It Works</h2>

  <p>The Pairwise algorithm generates a set of test cases that covers all possible pairs of input values at least once. By testing combinations of parameters in pairs, the algorithm helps identify potential issues related to the interaction of these parameters without the need to test every possible combination.</p>

  <h2>Benefits</h2>

  <ul>
    <li><strong>Efficiency:</strong> Pairwise testing significantly reduces the number of test cases, making the testing process more efficient while maintaining a high level of coverage.</li>
    <li><strong>Effective Coverage:</strong> The algorithm ensures that all possible pairs of input values are tested, helping uncover defects that may be missed with other testing methods.</li>
    <li><strong>Time and Resource Savings:</strong> By minimizing the number of test cases, Pairwise testing saves time and resources, making it a cost-effective approach.</li>
  </ul>

  <h2>Implementation Example</h2>

  <p>Here's a simple example of how Pairwise testing can be implemented in a hypothetical software system using Python:</p>

  <pre>
    def generate_pairwise(*parameters):
        test_cases = []
        for i, param1 in enumerate(parameters[0]):
            for j, param2 in enumerate(parameters[1]):
                for k, param3 in enumerate(parameters[2]):
                    test_cases.append([param1, param2, param3])
        return test_cases
  
    # Define input parameters and their possible values
    parameter1_values = ["A", "B", "C"]
    parameter2_values = ["X", "Y"]
    parameter3_values = ["1", "2", "3"]
  
    # Generate Pairwise test cases
    test_cases = generate_pairwise(parameter1_values, parameter2_values, parameter3_values)
  
    # Execute test cases
    for test_case in test_cases:
        # Perform testing with the combination of input values
        print(test_case)
  </pre>

  <h2>More Information</h2>

  <p><href>http://pairwise.org</href> has details on this testing methododology.</p>
</body>
</html>
