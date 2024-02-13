# ST CAE 1 Question Bank Solution

<div style="position: relative; width: 100%; height: auto; max-width: 100%; padding-top: 56.25%;">
  <iframe src="https://drive.google.com/file/d/13kdke2JD1bJrmUyjTgz4A7qnlhslyPOV/preview" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" frameborder="0" scrolling="no"></iframe>
</div>

- [ST CAE 1 Question Bank Solution](#st-cae-1-question-bank-solution)
  - [1. Define software testing and define](#1-define-software-testing-and-define)
  - [2. Find out the myth related to software testing \& write down its explanation whether it is true or false?](#2-find-out-the-myth-related-to-software-testing--write-down-its-explanation-whether-it-is-true-or-false)
  - [3. Explore some software failure test cases \& Explain any two of them](#3-explore-some-software-failure-test-cases--explain-any-two-of-them)
  - [4. How does testing help in producing quality software?](#4-how-does-testing-help-in-producing-quality-software)
  - [5.Explain the different stages of STLC in detail](#5explain-the-different-stages-of-stlc-in-detail)
  - [6. Difference between](#6-difference-between)
  - [7. Explain defect repository with all labels in detail?](#7-explain-defect-repository-with-all-labels-in-detail)
  - [8. What is the role of tester for developing a defect repository](#8-what-is-the-role-of-tester-for-developing-a-defect-repository)
  - [9. Elaborate defect analysis \& prevention with the help of diagram](#9-elaborate-defect-analysis--prevention-with-the-help-of-diagram)
  - [10. What are the benefits of defect prevention of software?](#10-what-are-the-benefits-of-defect-prevention-of-software)
  - [11. What are the different consequences of an effective test case. Write down the approaches for test case design](#11-what-are-the-different-consequences-of-an-effective-test-case-write-down-the-approaches-for-test-case-design)
  - [12. Distinguish  between whitebox testing and blackbox testing](#12-distinguish--between-whitebox-testing-and-blackbox-testing)
  - [13. List out the different methods for blackbox Testing and explain any two of it](#13-list-out-the-different-methods-for-blackbox-testing-and-explain-any-two-of-it)
  - [14. Elaborate equivalence class partitioning method used in blackbox testing](#14-elaborate-equivalence-class-partitioning-method-used-in-blackbox-testing)
  - [15. Elaborate boundary value analysis method used in blackbox testing](#15-elaborate-boundary-value-analysis-method-used-in-blackbox-testing)
  - [16. Write down example of application which uses equivalence class partitioning and boundary value analysis](#16-write-down-example-of-application-which-uses-equivalence-class-partitioning-and-boundary-value-analysis)
  - [17. Write a short note on compatibility and configuration testing](#17-write-a-short-note-on-compatibility-and-configuration-testing)
  - [18. Elaborate static testing and structural testing used in whitebox approach](#18-elaborate-static-testing-and-structural-testing-used-in-whitebox-approach)
  - [19. Short note on code functional testing and control flow graphs](#19-short-note-on-code-functional-testing-and-control-flow-graphs)
  - [20. Short note on test adequacy criteria](#20-short-note-on-test-adequacy-criteria)


## 1\. Define software testing and define

a) failure
b) error
c) bugs
d)Fault
e)test cases
f)test bed

**a) Definition of Software Testing:**

Software testing is a process of evaluating a software application or system to find defects or errors, and to verify that it meets the specified requirements. The goal of testing is to ensure that the software functions correctly, performs reliably under various conditions, and satisfies the end-user expectations.

**b) Failure:**

A failure occurs when the software does not perform as expected or intended. It is a deviation from the expected behavior or functionality of the software. Failures can happen due to defects or errors present in the software.

**c) Error:**

An error, also known as a mistake or a defect, is a human action that results in incorrect or unexpected behavior of the software. Errors can occur during any phase of the software development process and can lead to defects in the software.

**d) Bug:**

A bug is a specific instance of an error or defect in the software that causes it to behave unexpectedly or not as intended. Bugs are identified during the testing process and need to be fixed by the development team.

**e) Fault:**

A fault, also known as a defect or a bug, is a flaw or imperfection in the software's code or design that can cause the software to fail or behave unexpectedly. Faults are the root cause of failures in software systems.

**f) Test Cases:**

Test cases are detailed instructions or procedures that are designed to validate whether the software functions correctly under specific conditions. Each test case typically consists of inputs, expected outputs, and execution steps. Test cases are used to systematically verify the behavior of the software and to identify defects.

**g) Test Bed:**

A test bed is an environment configured for testing software applications or systems. It includes hardware, software, network configurations, and other necessary resources required to execute test cases and evaluate the software's performance.

## 2\. Find out the myth related to software testing & write down its explanation whether it is true or false?

One common myth related to software testing is:

**Myth:** "Testing can guarantee that there are no bugs in the software."

**Explanation:** This myth is false. While testing is essential for identifying and minimizing defects in software, it cannot guarantee that there are no bugs present. Testing can only provide information about the quality and reliability of the software based on the tests conducted. However, it is practically impossible to test all possible scenarios and combinations, so there may still be undiscovered bugs or defects in the software.

## 3\. Explore some software failure test cases & Explain any two of them

Here are two examples of software failure test cases:

1. **Memory Leak in a Web Application:** Test Case: Continuously perform a specific action on a web application (e.g., navigating between pages or submitting forms) for an extended period. Explanation: If the web application has a memory leak issue, the memory consumption of the application will continuously increase over time. Eventually, the application may become unresponsive or crash due to excessive memory usage, leading to a failure.

2. **Database Connection Failure in an E-commerce System:** Test Case: Simulate a scenario where the database server becomes unavailable while the e-commerce system is processing orders. Explanation: If the e-commerce system relies on a database for storing and retrieving order information, a failure in the database connection can cause the system to be unable to process orders properly. This can lead to errors, timeouts, or incomplete transactions, resulting in a negative impact on the user experience and business operations.

## 4\. How does testing help in producing quality software?

Testing plays a crucial role in producing quality software by:

- **Identifying Defects:** Testing helps in identifying defects, errors, and bugs in the software early in the development process, allowing them to be fixed before the software is deployed to production.

- **Validating Requirements:** Testing ensures that the software meets the specified requirements and performs as expected under various conditions.

- **Enhancing Reliability:** Thorough testing increases the reliability and robustness of the software by uncovering potential issues and weaknesses.

- **Improving User Satisfaction:** By detecting and fixing defects, testing contributes to improving the overall user experience and satisfaction with the software.

- **Reducing Risks:** Testing helps in mitigating risks associated with software failures, security vulnerabilities, and performance issues, thereby increasing the overall stability and resilience of the software.

## 5\.Explain the different stages of STLC in detail

The Software Testing Life Cycle (STLC) consists of several stages, each with its specific objectives, activities, and deliverables. The stages of STLC typically include:

1. **Requirement Analysis:**

    - Objective: Understand the software requirements and identify testable components.
    - Activities: Reviewing requirements documents, identifying testable scenarios, and creating a requirements traceability matrix.

2. **Test Planning:**

    - Objective: Define the test strategy, test objectives, scope, resources, and timelines.
    - Activities: Developing the test plan, identifying test cases, defining entry and exit criteria, and allocating resources.

3. **Test Case Development:**

    - Objective: Design test cases to validate the functionality of the software.
    - Activities: Creating test cases based on requirements, specifying test data, and documenting test procedures.

4. **Test Environment Setup:**

    - Objective: Establish the test environment required for executing test cases.
    - Activities: Setting up hardware, software, databases, networks, and other necessary components for testing.

5. **Test Execution:**

    - Objective: Execute test cases and validate the behavior of the software.
    - Activities: Running test cases, recording test results, capturing defects, and retesting fixes.

6. **Defect Tracking and Management:**

    - Objective: Identify, report, and track defects found during testing.
    - Activities: Logging defects in a defect tracking system, prioritizing defects based on severity and impact, and collaborating with development teams to resolve defects.

7. **Test Closure:**

    - Objective: Assess the testing process, summarize test results, and prepare test closure reports.
    - Activities: Analyzing test metrics, documenting lessons learned, obtaining stakeholders' sign-off, and archiving test artifacts.

## 6\. Difference between

**a) Verification and Validation:**

- **Verification:** Verification is the process of evaluating software artifacts to ensure that they meet specified requirements and standards. It focuses on checking whether the software is being built correctly according to the defined specifications. Verification activities include reviews, inspections, walkthroughs, and static analysis techniques.

- **Validation:** Validation is the process of evaluating the software to ensure that it meets the customer's requirements and expectations. It involves testing the software against the user's needs and real-world scenarios to determine whether it behaves as intended. Validation activities include dynamic testing, system testing, and acceptance testing.

**Key Difference:** Verification ensures that the software is built correctly, while validation ensures that the right software is built.

**b) Static and Dynamic Testing:**

- **Static Testing:** Static testing is a type of testing that is performed without executing the software code. It involves reviewing and analyzing software artifacts, such as requirements documents, design specifications, and source code, to identify defects, errors, and inconsistencies. Static testing techniques include reviews, inspections, walkthroughs, and static code analysis.

- **Dynamic Testing:** Dynamic testing is a type of testing that involves executing the software code to observe its behavior and verify its functionality. It includes running test cases, providing inputs, and evaluating the outputs to validate the software against specified requirements. Dynamic testing techniques include unit testing, integration testing, system testing, and acceptance testing.

**Key Difference:** Static testing is performed without executing the software, focusing on early defect detection, while dynamic testing involves executing the software to validate its behavior and functionality.

**c) White Box and Black Box Testing:**

- **White Box Testing:** White box testing, also known as clear box testing or structural testing, is a testing technique that involves examining the internal structure and implementation of the software code. Testers have access to the source code and design details and use this knowledge to design test cases based on code paths, branches, and logic. White box testing techniques include statement coverage, branch coverage, path coverage, and code walkthroughs.

- **Black Box Testing:** Black box testing is a testing technique that focuses on testing the functionality of the software without considering its internal implementation. Testers do not have access to the source code and test the software based on its external behavior and specifications. Black box testing techniques include equivalence partitioning, boundary value analysis, decision tables, and use case testing.

**Key Difference:** In white box testing, testers have access to the internal structure of the software and design test cases based on code logic, while in black box testing, testers focus on testing the functionality of the software without knowledge of its internal implementation.

## 7\. Explain defect repository with all labels in detail?

A defect repository, also known as a bug tracking system or issue tracking system, is a centralized database or tool used to manage and track defects or issues identified during the software development and testing process. It serves as a repository for recording, prioritizing, assigning, and tracking the status of defects from their identification to resolution.

Labels commonly associated with defects in a defect repository include:

- **ID:** A unique identifier assigned to each defect for tracking purposes.
- **Summary/Title:** A brief description of the defect to provide an overview.
- **Description:** Detailed information about the defect, including steps to reproduce, observed behavior, and any relevant screenshots or logs.
- **Priority:** The importance or urgency of fixing the defect, often categorized as high, medium, or low.
- **Severity:** The impact of the defect on the software's functionality or performance, ranging from critical to minor.
- **Status:** The current state of the defect in the defect resolution process, such as New, In Progress, Fixed, Verified, Closed, etc.
- **Assigned To:** The individual or team responsible for investigating, fixing, or verifying the defect.
- **Created By:** The person who reported or identified the defect.
- **Creation Date:** The date and time when the defect was reported.
- **Last Updated:** The date and time when the defect was last modified or updated.
- **Comments/Notes:** Additional information, updates, or discussions related to the defect.

The defect repository facilitates effective defect management by providing a centralized platform for communication, collaboration, and tracking of defects among project stakeholders, including developers, testers, project managers, and stakeholders.

## 8\. What is the role of tester for developing a defect repository

The tester plays a crucial role in developing a defect repository by:

- **Reporting Defects:** The tester is responsible for identifying, documenting, and reporting defects or issues encountered during the testing process.
- **Providing Detailed Information:** The tester should provide detailed information about each defect, including steps to reproduce, expected behavior, observed behavior, and any relevant logs or screenshots.
- **Assigning Priority and Severity:** Based on the impact and urgency of fixing the defect, the tester should assign appropriate priority and severity levels to ensure that critical defects are addressed promptly.
- **Tracking Defect Status:** The tester should monitor the status of reported defects, communicate with the development team to ensure timely resolution, and update the defect repository with any changes or updates.
- **Verifying Fixes:** After the development team fixes the defects, the tester is responsible for verifying the fixes to ensure that the issues have been resolved satisfactorily before closing the defects.

By actively participating in the defect management process, the tester contributes to improving the quality and reliability of the software by ensuring that defects are identified, addressed, and resolved effectively.

## 9\. Elaborate defect analysis & prevention with the help of diagram

Defect analysis and prevention involve identifying the root causes of defects in software development and implementing measures to prevent similar issues from occurring in the future. The following diagram illustrates the process of defect analysis and prevention:

```mathematica
                  ┌───────────┐
        ┌────────►│ Defect    │
        │         │ Analysis  │
        │         └───────────┘
        │                │
        │       Identify Root Causes
        │                │
        │         ┌───────────┐
        └─────────│ Defect    │
                  │ Prevention│
                  └───────────┘
                         │
               Implement Preventive Measures
                         │
             Monitor and Evaluate Effectiveness
```

**Defect Analysis:** In this phase, defects identified during testing or production are analyzed to determine their root causes. This involves investigating factors such as design flaws, coding errors, inadequate requirements, communication issues, and process deficiencies that contributed to the defects.

**Defect Prevention:** Based on the findings of defect analysis, preventive measures are implemented to address the root causes and prevent similar defects from occurring in the future. This may involve improving development processes, enhancing communication and collaboration among team members, implementing coding standards and guidelines, providing training and education, and leveraging automated tools and techniques for defect prevention.

**Monitoring and Evaluation:** The effectiveness of the preventive measures is monitored and evaluated over time to ensure that they are achieving the desired outcomes. This involves tracking key metrics related to defect reduction, quality improvement, and process efficiency and making adjustments or refinements to the preventive measures as needed.

By systematically analyzing defects, identifying root causes, and implementing preventive measures, organizations can improve the quality and reliability of their software products, reduce rework and maintenance costs, and enhance customer satisfaction.

## 10\. What are the benefits of defect prevention of software?

Defect prevention in software development offers several benefits, including:

- **Cost Savings:** By preventing defects early in the development process, organizations can avoid the costs associated with rework, bug fixes, and post-release support.
- **Improved Quality:** Defect prevention leads to higher-quality software products with fewer defects, resulting in enhanced reliability, performance, and user satisfaction.
- **Increased Productivity:** By addressing root causes and improving development processes, defect prevention reduces the time and effort spent on fixing defects, allowing teams to focus on delivering value-added features and enhancements.
- **Faster Time to Market:** With fewer defects and reduced rework, organizations can accelerate the software development lifecycle and bring products to market more quickly, gaining a competitive edge.
- **Enhanced Customer Satisfaction:** High-quality software products with fewer defects result in improved customer satisfaction and loyalty, leading to positive reviews, referrals, and repeat business.

## 11\. What are the different consequences of an effective test case. Write down the approaches for test case design

**Consequences of an Effective Test Case:**

1. **Defect Detection:** Effective test cases help in detecting defects or errors in the software, ensuring that potential issues are identified and addressed before the software is deployed.
2. **Requirements Validation:** Test cases validate that the software meets the specified requirements and performs as expected, ensuring that it meets the needs of the end-users.
3. **Quality Assurance:** Well-designed test cases contribute to the overall quality assurance process by verifying the functionality, reliability, and performance of the software.
4. **Risk Mitigation:** Test cases help in identifying and mitigating risks associated with software failures, security vulnerabilities, and performance issues, reducing the likelihood of critical failures in production.
5. **Cost Savings:** Detecting and fixing defects early in the development process through effective test cases helps in reducing the cost of rework, maintenance, and post-release support.

**Approaches for Test Case Design:**

1. **Equivalence Partitioning:** Divide the input data into partitions or equivalence classes to design test cases that represent each class, ensuring thorough coverage with minimal test cases.
2. **Boundary Value Analysis:** Focus on testing boundary conditions or edges of equivalence classes to uncover defects related to boundary behavior, often revealing issues that may not be apparent with normal input values.
3. **State Transition Testing:** Identify different states of the software and design test cases to verify transitions between states, ensuring that the software behaves correctly as it moves through different states.
4. **Decision Table Testing:** Create decision tables to model different combinations of inputs and conditions, allowing for systematic testing of all possible scenarios and combinations.
5. **Use Case Testing:** Based on the functional requirements, design test cases that represent end-to-end scenarios or use cases, ensuring that the software functions correctly in real-world scenarios.

## 12\. Distinguish  between whitebox testing and blackbox testing

**White Box Testing:**

- Also known as clear box testing or structural testing.
- Testing technique that examines the internal structure and implementation of the software.
- Testers have access to the source code and design details.
- Test cases are designed based on code paths, branches, and logic.
- Focuses on code coverage criteria such as statement coverage, branch coverage, and path coverage.
- Examples include unit testing, integration testing, and code reviews.

**Black Box Testing:**

- Testing technique that focuses on testing the functionality of the software without considering its internal implementation.
- Testers do not have access to the source code and test the software based on its external behavior and specifications.
- Test cases are designed based on requirements, specifications, and user expectations.
- Focuses on testing inputs, outputs, interfaces, and system behavior.
- Examples include functional testing, system testing, acceptance testing, and usability testing.

## 13\. List out the different methods for blackbox Testing and explain any two of it

**Methods for Black Box Testing:**

1. Equivalence Partitioning
2. Boundary Value Analysis
3. Decision Table Testing
4. State Transition Testing
5. Use Case Testing

**Explanation of Equivalence Partitioning:** Equivalence Partitioning is a black box testing technique that divides the input data into partitions or equivalence classes, where each class represents a set of input values that should produce similar results. The goal is to design test cases that cover each equivalence class, ensuring thorough testing while minimizing the number of test cases needed.

**Explanation of Boundary Value Analysis:** Boundary Value Analysis is a black box testing technique that focuses on testing the boundary conditions or edges of equivalence classes. Test cases are designed to include input values at the lower and upper boundaries of each equivalence class, as well as just above and below those boundaries. This approach helps in uncovering defects related to boundary behavior, such as off-by-one errors or boundary-related inconsistencies.

## 14\. Elaborate equivalence class partitioning method used in blackbox testing

**Equivalence Class Partitioning:** Equivalence class partitioning is a black box testing technique that divides the input data into partitions or equivalence classes, where each class represents a set of input values that should produce similar results when processed by the software. The objective is to design test cases that cover each equivalence class, ensuring thorough testing while minimizing the number of test cases needed.

**Steps in Equivalence Class Partitioning:**

1. **Identify Input Conditions:** Analyze the requirements and identify input conditions or variables that influence the behavior of the software.
2. **Divide Inputs into Classes:** Divide the input data into partitions or equivalence classes based on the identified input conditions. Each equivalence class should have similar characteristics and produce similar results when processed by the software.
3. **Select Test Cases:** Design test cases to represent each equivalence class, ensuring that they cover both valid and invalid input values. Test cases should include inputs from each equivalence class to provide comprehensive coverage.
4. **Execute Test Cases:** Execute the selected test cases and observe the behavior of the software. Verify that it behaves as expected for inputs from each equivalence class, detecting any deviations or discrepancies that may indicate defects or errors.
5. **Refine Test Cases:** Refine the test cases based on feedback and additional insights gained during testing. Adjust the input values and conditions as needed to improve test coverage and effectiveness.

**Example:** Consider a software application that requires a user to enter their age, with valid age values ranging from 18 to 65. Equivalence class partitioning for this scenario would involve dividing the input values into three equivalence classes:

- Class 1: Age < 18 (Invalid)
- Class 2: 18 <= Age <= 65 (Valid)
- Class 3: Age > 65 (Invalid)

Test cases would be designed to cover each equivalence class, including inputs from both valid and invalid ranges, to ensure thorough testing of the software's behavior with different age values.

## 15\. Elaborate boundary value analysis method used in blackbox testing

**Boundary Value Analysis:** Boundary Value Analysis is a black box testing technique that focuses on testing the boundary conditions or edges of equivalence classes. Test cases are designed to include input values at the lower and upper boundaries of each equivalence class, as well as just above and below those boundaries. This approach helps in uncovering defects related to boundary behavior, such as off-by-one errors or boundary-related inconsistencies.

**Steps in Boundary Value Analysis:**

1. **Identify Equivalence Classes:** Identify the equivalence classes for each input condition or variable based on the requirements and specifications.
2. **Determine Boundary Values:** Determine the boundary values for each equivalence class, including the lower and upper boundaries.
3. **Design Test Cases:** Design test cases to include input values at the lower and upper boundaries of each equivalence class, as well as just above and below those boundaries. Test cases should cover both valid and invalid boundary values.
4. **Execute Test Cases:** Execute the designed test cases and observe the behavior of the software. Verify that it behaves as expected for boundary values, detecting any issues or inconsistencies that may indicate defects or errors.
5. **Analyze Results:** Analyze the results of the test cases and identify any defects or deviations from expected behavior. Report and prioritize the identified issues for resolution by the development team.

**Example:** Consider a software application that requires a user to enter a number between 1 and 100. Boundary value analysis for this scenario would involve designing test cases to include input values at the lower boundary (1), upper boundary (100), and just above and below these boundaries (0, 2, 99, 101). Test cases would verify the software's behavior for these boundary values, ensuring that it handles edge cases correctly and consistently.

## 16\. Write down example of application which uses equivalence class partitioning and boundary value analysis

**Example Application:** Online Banking System

**Equivalence Class Partitioning:**

- **Equivalence Classes:**
    1. Valid username/password combinations
    2. Invalid username/password combinations
    3. Empty username/password fields

- **Test Cases:**
    1. Test valid username and password combination (Equivalence Class 1)
    2. Test invalid username with valid password combination (Equivalence Class 2)
    3. Test valid username with invalid password combination (Equivalence Class 2)
    4. Test empty username field with valid password (Equivalence Class 3)
    5. Test valid username with empty password field (Equivalence Class 3)

**Boundary Value Analysis:**

- **Boundary Values:**
    1. Lower boundary: Minimum password length (e.g., 6 characters)
    2. Upper boundary: Maximum password length (e.g., 20 characters)

- **Test Cases:**
    1. Test password with minimum length - 6 characters
    2. Test password with maximum length - 20 characters
    3. Test password just above the lower boundary - 7 characters
    4. Test password just below the upper boundary - 19 characters

## 17\. Write a short note on compatibility and configuration testing

**Compatibility Testing:** Compatibility testing is the process of evaluating a software application's compatibility with different environments, platforms, browsers, devices, and operating systems. It ensures that the software functions correctly and performs optimally across various configurations, ensuring a consistent user experience. Compatibility testing helps in identifying compatibility issues, such as layout distortions, rendering errors, performance issues, or functionality inconsistencies, and ensures that the software meets the compatibility requirements specified by stakeholders.

**Configuration Testing:** Configuration testing is the process of testing a software application's behavior under different configurations or settings, such as different hardware configurations, software versions, network configurations, or system configurations. It verifies that the software functions correctly and behaves as expected under various configurations, ensuring that it can adapt to different environments and user preferences. Configuration testing helps in identifying configuration-related issues, such as compatibility conflicts, performance bottlenecks, or functionality limitations, and ensures that the software remains reliable and consistent across different configurations.

## 18\. Elaborate static testing and structural testing used in whitebox approach

**Static Testing:** Static testing is a white box testing technique that involves reviewing and analyzing software artifacts, such as requirements documents, design specifications, and source code, to identify defects, errors, and inconsistencies without executing the software. Static testing techniques include reviews, inspections, walkthroughs, and static code analysis. It helps in identifying issues early in the development process, ensuring that defects are detected and addressed before they propagate to later stages, reducing the cost and effort of fixing defects.

**Structural Testing:** Structural testing, also known as white box testing or clear box testing, is a testing technique that examines the internal structure and implementation of the software. Testers have access to the source code and design details and use this knowledge to design test cases based on code paths, branches, and logic. Structural testing techniques include statement coverage, branch coverage, path coverage, and code walkthroughs. It helps in validating the correctness and completeness of the software's internal logic and ensuring that all code paths are tested, minimizing the risk of undetected defects.

## 19\. Short note on code functional testing and control flow graphs

**Code Functional Testing:** Code functional testing is a white box testing technique that focuses on testing the functionality of individual code units, such as functions, methods, or procedures, by executing them with specific inputs and verifying the outputs against expected results. It involves designing test cases based on the functional specifications and requirements of the code units and validating that they perform as intended. Code functional testing helps in identifying defects or errors in the implementation of code units and ensuring that they meet the specified functional requirements.

**Control Flow Graphs:** Control flow graphs are graphical representations of the control flow or flow of execution within a software program. They depict the sequence of statements, decision points, and control structures, such as loops and conditionals, in a program, showing how control flows from one statement to another during program execution. Control flow graphs are used in structural testing techniques, such as branch coverage and path coverage, to analyze and visualize the possible code paths and control flow structures within a program, helping testers to design effective test cases and ensure thorough code coverage.

## 20\. Short note on test adequacy criteria

Test adequacy criteria, also known as coverage criteria or coverage metrics, are quantitative measures used to evaluate the adequacy or completeness of testing efforts and assess the extent to which the software has been tested. They define specific coverage goals or criteria that need to be satisfied to ensure thorough testing of the software. Test adequacy criteria help in determining whether sufficient test cases have been designed and executed to verify the functionality, reliability, and performance of the software.

**Common Test Adequacy Criteria:**

1. **Statement Coverage:** Ensures that each executable statement in the code has been executed at least once during testing.
2. **Branch Coverage:** Ensures that each decision point or branch in the code has been evaluated to both true and false outcomes during testing.
3. **Path Coverage:** Ensures that every possible path or sequence of statements in the code has been traversed at least once during testing.
4. **Condition Coverage:** Ensures that each Boolean condition in the code has been evaluated to both true and false outcomes during testing.
5. **Decision/Condition Coverage:** Ensures that each decision point or condition in the code has been evaluated to both true and false outcomes during testing.
