# Unit 2: Test Case Design Strategies

- [Unit 2: Test Case Design Strategies](#unit-2-test-case-design-strategies)
    - [Using Black Box Approach to Test Case Design](#using-black-box-approach-to-test-case-design)
    - [Random Testing](#random-testing)
    - [Requirements-based Testing](#requirements-based-testing)
    - [Boundary Value Analysis](#boundary-value-analysis)
    - [Equivalence Class Partitioning](#equivalence-class-partitioning)
    - [State-based Testing](#state-based-testing)
    - [Cause-Effect Graphing](#cause-effect-graphing)
    - [Compatibility Testing](#compatibility-testing)
    - [User Documentation Testing](#user-documentation-testing)
    - [Domain Testing](#domain-testing)
    - [Using White Box Approach to Test Design](#using-white-box-approach-to-test-design)
    - [Test Adequacy Criteria](#test-adequacy-criteria)
    - [Static Testing vs. Structural Testing](#static-testing-vs-structural-testing)
    - [Code Functional Testing](#code-functional-testing)
    - [Coverage and Control Flow Graphs](#coverage-and-control-flow-graphs)
    - [Covering Code Logic](#covering-code-logic)
    - [Paths](#paths)
    - [Code Complexity Testing](#code-complexity-testing)
    - [Evaluating Test Adequacy Criteria](#evaluating-test-adequacy-criteria)
    - [Defect Report Format and Test Cases Format](#defect-report-format-and-test-cases-format)

**Overview:** Test case design is a crucial aspect of the software testing process, determining the effectiveness of identifying defects and ensuring the software meets its requirements. Different strategies guide the creation of test cases to achieve comprehensive test coverage.

### Using Black Box Approach to Test Case Design

**Definition:** Black box testing involves evaluating the system's functionality without knowledge of its internal code. Test cases are designed based on the expected behavior of the software, treating it as a "black box."

**Advantages:**

- Encourages an external perspective, focusing on user experience.
- Testers do not need knowledge of the internal code, promoting independence.
- Effectively uncovers issues related to incorrect input processing or improper system responses.

**Considerations:**

- Test cases are created based on specifications, requirements, and user documentation.
- Scenarios cover normal, boundary, and erroneous inputs to ensure comprehensive coverage.

### Random Testing

**Definition:** Random testing involves generating test inputs without a specific pattern or predefined sequence. This strategy aims to simulate real-world scenarios by introducing unexpected inputs.

**Advantages:**

- Mimics unpredictable user behavior.
- Identifies unexpected system responses and errors.
- Useful for discovering issues in system robustness and stability.

**Considerations:**

- Testers randomly select inputs without a specific order or logic.
- Essential for uncovering hidden defects that may not be evident through structured testing.

### Requirements-based Testing

**Definition:** Requirements-based testing aligns test case design with the specified software requirements. Each test case is created to validate that the software meets the documented functional and non-functional requirements.

**Advantages:**

- Ensures that the software functions as intended according to documented specifications.
- Facilitates traceability, linking each test case to specific requirements.
- Helps in comprehensive coverage of all specified functionalities.

**Considerations:**

- Test cases are directly derived from requirements documents.
- Requires a clear understanding of the requirements to ensure accurate test case creation.

### Boundary Value Analysis

**Definition:** Boundary value analysis involves testing the software at the boundaries of acceptable input values. This strategy aims to identify errors that may occur near the edges of permissible data ranges.

**Advantages:**

- Targets potential weaknesses at the limits of input domains.
- Often exposes off-by-one errors and boundary-related issues.
- Useful for enhancing the robustness and reliability of the software.

**Considerations:**

- Test cases focus on values at the lower and upper limits, as well as just beyond those limits.
- Particularly effective for input fields, array indices, and other scenarios where data boundaries are critical.

### Equivalence Class Partitioning

**Overview:** Equivalence Class Partitioning is a testing technique that divides the input data into groups or classes, treating each group as equivalent. The objective is to reduce the number of test cases while ensuring that each class is tested at least once.

**Advantages:**

- Efficiently handles a large number of potential input combinations.
- Ensures thorough testing by covering each equivalence class.
- Identifies defects associated with specific groups of input data.

**Considerations:**

- Input conditions are grouped into classes that are expected to exhibit similar behavior.
- Test cases are designed to represent each class, validating the software's response within the same equivalence class.

* * * * *

### State-based Testing

**Definition:** State-based testing involves assessing the behavior of a system based on its different states. Systems transition between various states in response to inputs or events, and testing is performed to verify correct state transitions.

**Advantages:**

- Focuses on the dynamic behavior of the system over time.
- Identifies issues related to state transitions, persistence, and consistency.
- Suitable for systems with complex logic involving different states.

**Considerations:**

- Test cases are designed to cover transitions between different states.
- State diagrams and specifications are essential for effective state-based testing.

* * * * *

### Cause-Effect Graphing

**Overview:** Cause-Effect Graphing is a systematic technique for designing test cases based on cause-and-effect relationships between input conditions and the corresponding system behavior. It helps in identifying combinations of input conditions that trigger specific effects.

**Advantages:**

- Provides a structured approach for identifying test cases.
- Reduces redundancy by focusing on the essential combinations of input conditions.
- Ensures comprehensive coverage of input scenarios.

### Compatibility Testing

**Definition:** Compatibility Testing verifies that the software functions correctly across different environments, devices, and configurations. It ensures that the application is compatible with various operating systems, browsers, and hardware.

**Advantages:**

- Identifies issues related to platform-specific functionalities.
- Ensures a consistent user experience across diverse environments.
- Mitigates risks associated with software deployment on different devices.

**Considerations:**

- Test cases are designed to validate the software on various platforms and configurations.
- Compatibility testing may include checks for different browsers, operating systems, and network environments.

* * * * *

### User Documentation Testing

**Overview:** User Documentation Testing focuses on validating the accuracy, completeness, and usability of user documentation, including manuals, guides, and help systems. This ensures that end-users have access to clear and reliable information.

**Advantages:**

- Enhances user experience by providing accurate and helpful documentation.
- Reduces user confusion and support requests.
- Verifies that documentation aligns with the software's actual functionality.

**Considerations:**

- Test cases involve reviewing and testing each section of the user documentation.
- Assessments include the clarity of instructions, correctness of information, and accessibility of help resources.

### Domain Testing

**Definition:** Domain testing is a software testing technique where input data is selected from a specific domain or a set of valid and invalid inputs. The primary goal is to ensure that the software functions correctly for various input values and conditions within a specific domain.

**Purpose:** The purpose of domain testing is to identify and address potential issues related to input values, ensuring that the software behaves as expected across different ranges and scenarios within the defined domain.

### Using White Box Approach to Test Design

**White Box Testing:** White box testing involves examining the internal logic and structure of the code. Testers have knowledge of the codebase, allowing them to design test cases based on the code's structure, paths, and conditions.

**Test Design:** In the context of a white box approach, test design refers to creating test cases that specifically target and exercise the internal paths and conditions of the code. This approach aims to achieve thorough coverage of the codebase.

### Test Adequacy Criteria

**Definition:** Test adequacy criteria are standards used to determine when testing is complete. These criteria help measure the effectiveness of the testing process and ensure that a sufficient number of test cases have been executed.

**Examples:** Test adequacy criteria include various coverage metrics such as statement coverage, branch coverage, and path coverage. These metrics help assess the comprehensiveness of the testing effort.

### Static Testing vs. Structural Testing

| Feature                  | Static Testing                             | Structural Testing                         |
|--------------------------|--------------------------------------------|--------------------------------------------|
| **Nature of Testing**    | Examines the software without execution.   | Involves the execution of the software.     |
| **Timing**               | Performed early in the development process.| Typically performed after coding is done.  |
| **Focus**                | Reviews, inspections, and walkthroughs.    | Examines the internal structure of the code.|
| **Objective**            | Identifies defects and issues in the early stages. | Verifies the correctness of the internal structure.|
| **Examples**             | Code reviews, inspections, static analysis. | White box testing, unit testing, integration testing.|

### Code Functional Testing

**Definition:** Code functional testing is a type of testing that evaluates the functionality of the software by directly examining its source code. It may involve unit testing, integration testing, or system testing to ensure that the code performs the intended functions.

### Coverage and Control Flow Graphs

**Coverage:** Coverage in the context of testing refers to the extent to which the source code has been tested. Coverage metrics include statement coverage, branch coverage, and path coverage, providing insights into the thoroughness of the testing process.

**Control Flow Graphs:** Control flow graphs are graphical representations of the paths that a program can take during its execution. They help in understanding the control flow and are valuable in designing test cases to cover different paths and scenarios within the code.

### Covering Code Logic

Code logic coverage refers to the extent to which the logical constructs within the code have been exercised by test cases. This includes ensuring that various decision points, conditions, and loops in the code have been tested. Coverage metrics such as statement coverage, branch coverage, and path coverage are commonly used to measure the effectiveness of code logic coverage.

### Paths

Paths in the context of software testing refer to the unique routes or sequences of statements that can be taken during the execution of a program. Testing various paths helps ensure comprehensive coverage of the code. Path testing involves designing test cases that traverse different paths to identify potential issues related to the flow of control within the program.

### Code Complexity Testing

Code complexity testing focuses on assessing the complexity of the source code. Code complexity is often associated with the readability and maintainability of the code. Techniques like cyclomatic complexity are used to measure code complexity. Higher complexity may indicate a higher risk of defects, making it important to address such areas during testing.

### Evaluating Test Adequacy Criteria

Test adequacy criteria are standards used to determine when testing is sufficient. Evaluating these criteria ensures that the testing process is comprehensive and that different aspects of the software have been adequately covered. Common test adequacy criteria include statement coverage, branch coverage, and path coverage, which help measure the effectiveness of the testing effort.

### Defect Report Format and Test Cases Format

Defect report format is a standardized way of documenting and communicating issues or bugs identified during testing. It typically includes details such as the defect description, steps to reproduce, severity, and status. Test cases format refers to the structured documentation of test cases, including input values, expected results, and the steps to execute the test. Consistent formats enhance communication and collaboration within the testing team.
