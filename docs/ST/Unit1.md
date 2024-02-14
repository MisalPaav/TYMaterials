# Unit 1

<div style="position: relative; width: 100%; height: auto; max-width: 100%; padding-top: 56.25%;">
  <iframe src="https://drive.google.com/file/d/13u_Vf-YldALM0Z-A-HGl4m565878kijr/preview" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" frameborder="0" scrolling="no"></iframe>
</div>

## Table of Contents

- [Unit 1](#unit-1)
  - [Table of Contents](#table-of-contents)
  - [Testing as a Process](#testing-as-a-process)
  - [Testing Axioms](#testing-axioms)
  - [Basic Definitions](#basic-definitions)
  - [Software Testing Principles](#software-testing-principles)
  - [The Tester's Role in a Software Development Org](#the-testers-role-in-a-software-development-org)
  - [Origins of Defects](#origins-of-defects)
  - [Cost of Defects](#cost-of-defects)
  - [Defect Classes](#defect-classes)
  - [Defect Repository and Test Design](#defect-repository-and-test-design)
  - [Defect Examples](#defect-examples)
  - [Developer/Tester Support of Developing a Defect Repo](#developertester-support-of-developing-a-defect-repo)
  - [Defect Prevention Strategies](#defect-prevention-strategies)
  - [Software Testing Life Cycle](#software-testing-life-cycle)

## Testing as a Process

Testing is a systematic investigation to identify, analyze, evaluate, and record any discrepancies between the expected and actual outcome of a software product. It is an essential part of the software development life cycle (SDLC) that helps ensure the quality and reliability of the software.

**Testing process:**

- **Requirement analysis:** Understanding the software requirements and specifications.\
- **Test planning:** Defining the scope of testing, test strategies, and test cases.\
- **Test design:** Creating test cases to cover various functionalities and scenarios.\
- **Test execution:** Executing the test cases and recording the results.\
- **Defect logging:** Identifying and reporting bugs or defects.\
- **Defect fixing:** Developers fix the identified defects.\
- **Regression testing:** Ensuring that fixes do not introduce new bugs.\
- **Test reporting:** Analyzing and reporting the testing results.

## Testing Axioms

Testing axioms are fundamental principles that guide software testing practices. They provide a framework for understanding the limitations and effectiveness of testing.

**Five key testing axioms:**

- **Testing shows the presence of defects, not their absence:** Testing can only reveal existing defects, it cannot guarantee the absence of future defects.\
- **Exhaustive testing is impossible:** Testing every possible input and scenario is impractical and often unnecessary.\
- **Early testing is more effective and less costly:** Identifying and fixing defects early in the development process is easier and less expensive than fixing them later.\
- **Defects cluster together:** Defects tend to occur in related areas of the software.\
- **Testing is context-dependent:** The effectiveness of testing depends on the specific context of the project, such as the software's purpose, target audience, and development environment.

## Basic Definitions

Here are some basic definitions of commonly used terms in software testing:

- **Defect:** A flaw or imperfection in the software that causes it to behave incorrectly.\
- **Error:** A mistake made by a developer during the coding process.\
- **Failure:** A violation of a software requirement.\
- **Test case:** A set of inputs, pre-conditions, and expected outputs that are used to test a specific functionality of a software application.\
- **Test suite:** A collection of test cases that are used to test a software application.\
- **Test automation:** Using tools and scripts to automate the execution of test cases.\
- **Static code analysis:** Analyzing the source code of a software application to identify potential problems.\
- **Dynamic testing:** Testing the software by running it and observing its behavior.\
- **Black-box testing:** Testing the software without any knowledge of its internal workings.\
- **White-box testing:** Testing the software with knowledge of its internal workings.

## Software Testing Principles

Software testing principles are guidelines that help testers to design and execute effective tests.

**Seven key software testing principles:**

- **Test early and often:** Start testing early in the development process and continue testing throughout the development lifecycle.\
- **Test for bad data and unexpected events:** Consider how the software will handle invalid or unexpected input.\
- **Test for both positive and negative scenarios:** Test both the expected functionality and the behavior under unexpected conditions.\
- **Use a variety of test techniques:** Use different types of testing methods to achieve comprehensive coverage.\
- **Automate repetitive tests:** Use automation tools to execute repetitive tasks and free up time for more exploratory testing.\
- **Document your test results:** Keep detailed records of your testing activities and findings.\
- **Be objective and unbiased:** Approach testing with a critical eye and avoid making assumptions about the software's quality.

## The Tester's Role in a Software Development Org

The tester plays a vital role in the software development organization, acting as a gatekeeper of quality and ensuring that software products meet desired standards. Their responsibilities encompass:

**1\. Design and execute tests:**

- Develop test cases to cover various functionalities and scenarios.
- Execute test cases manually or using automation tools.
- Analyze test results and identify defects.

**2\. Collaborate with stakeholders:**

- Work closely with developers, product managers, and other stakeholders to understand requirements and provide feedback.
- Participate in code reviews and design discussions.
- Communicate testing progress and results effectively.

**3\. Advocate for quality:**

- Champion quality throughout the development process.
- Propose improvements to testing practices and methodologies.
- Stay updated with the latest testing trends and technologies.

**4\. Analyze and report defects:**

- Investigate the root cause of defects.
- Report defects using a bug tracking system.
- Prioritize defects based on severity and impact.

**5\. Promote a culture of quality:**

- Encourage team members to think about quality throughout the development process.
- Facilitate knowledge sharing and learning opportunities.
- Foster a collaborative and open environment for discussing quality concerns.

tester working with a developer to debug a defect

## Origins of Defects

Defects can originate from various sources throughout the software development process. Here are some common causes:

**1\. Requirements errors:**

- Misunderstandings or ambiguities in the requirements document.
- Incomplete or inaccurate specifications.

**2\. Design errors:**

- Flaws in the software's architecture or design.
- Poor code quality or coding errors.

**3\. Integration errors:**

- Issues arising from integrating different parts of the software.
- Incompatibilities between components or technologies.

**4\. Test errors:**

- Inadequate test coverage or ineffective test cases.
- Mistakes made during the test execution process.

**5\. Environmental factors:**

- Hardware or software dependencies not met.
- Configuration issues or resource limitations.

**6\. Human errors:**

- Mistakes made by developers, testers, or other stakeholders.
- Lack of communication or collaboration.

## Cost of Defects

Defects have a significant cost impact on software development organizations. These costs include:

**1\. Development costs:**

- Time and resources spent fixing defects.
- Delays in release schedules.
- Increased maintenance costs.

**2\. Customer support costs:**

- Handling customer complaints and inquiries.
- Providing bug fixes and updates.
- Loss of customer satisfaction and loyalty.

**3\. Brand reputation damage:**

- Negative publicity resulting from software defects.
- Loss of market share and revenue.

**4\. Legal and regulatory costs:**

- Compliance with regulations and standards.
- Liability lawsuits for damages caused by software defects.

## Defect Classes

Defects can be categorized into different classes based on their nature and impact. Some common defect classes include:

**1\. Functional defects:**

- Cause the software to behave incorrectly or fail to meet functional requirements.
- Examples: missing functionality, incorrect calculations, user interface glitches.

**2\. Non-functional defects:**

- Affect the software's performance, usability, security, or reliability.
- Examples: slow performance, memory leaks, security vulnerabilities, compatibility issues.

**3\. Usability defects:**

- Make the software difficult or frustrating to use.
- Examples: unclear interface, confusing navigation, poor accessibility features.

**4\. Compatibility defects:**

- Prevent the software from working properly with other software or hardware.
- Examples: operating system compatibility issues, browser compatibility issues.

**5\. Documentation defects:**

- Errors or inconsistencies in the user manual, online help, or other documentation.
- Examples: missing information, unclear instructions, outdated content.

## Defect Repository and Test Design

A defect repository is a central database used to track and manage defects throughout the software development process. It allows teams to:

- Store information about each defect, including its description, severity, priority, and status.
- Assign defects to developers for fixing.
- Track the progress of defect fixing.
- Analyze trends and identify patterns in defects.

The information stored in the defect repository can be used to inform test design. For example, testers can use defect data to:

- Identify areas of the software that are prone to defects.
- Prioritize test cases based on the severity and impact of potential defects.
- Design

Defect Examples
---------------

Here are some examples of common defects in software:

**Functional Defects:**

- **Missing functionality:** A feature that is documented as being available but is not implemented.

- **Incorrect calculations:** The software performs calculations incorrectly, leading to inaccurate results.

- **User interface glitches:** Buttons that don't work, menus that don't display correctly, or unexpected behavior when interacting with the interface.

- **Data corruption:** Data is lost or corrupted, leading to inconsistent or unexpected behavior.

- **Security vulnerabilities:** The software has vulnerabilities that could allow attackers to gain unauthorized access or control.

**Non-functional Defects:**

- **Performance issues:** The software runs slowly or responds sluggishly to user input.

- **Resource leaks:** The software leaks memory or other resources, leading to performance degradation over time.

- **Compatibility issues:** The software does not work properly with specific hardware or software configurations.

- **Usability problems:** The software is difficult to learn or use, causing frustration for users.

- **Accessibility issues:** The software is not accessible to users with disabilities.

**Documentation Defects:**

- **Missing information:** The documentation is missing key information that users need to use the software effectively.

- **Inaccurate information:** The documentation contains incorrect information that can mislead users.

- **Outdated information:** The documentation is not updated to reflect changes in the software.

- **Unclear instructions:** The documentation is written in a way that is difficult to understand or follow.

- **Poor organization:** The documentation is not organized in a logical way, making it difficult for users to find the information they need.

Developer/Tester Support of Developing a Defect Repo
----------------------------------------------------

Developers and testers can play a key role in developing and maintaining a defect repository. Here are some ways they can support this process:

**Developers:**

- **Provide accurate and detailed descriptions of defects when reporting them.**

- **Assign the correct severity and priority to defects.**

- **Provide steps to reproduce the defect.**

- **Attach screenshots or videos to illustrate the defect.**

- **Fix the defects and update the defect repository with the resolution.**

**Testers:**

- **Thoroughly test the software and report any defects they find.**

- **Use the defect repository to track the progress of defect fixing.**

- **Provide feedback on the usability and clarity of the defect repository.**

- **Identify opportunities to improve the defect reporting process.**

Defect Prevention Strategies
----------------------------

Here are some strategies that can be used to prevent defects:

- **Requirements Management:** Clearly define and document requirements early in the development process.

- **Design Reviews:** Conduct design reviews to identify potential problems before coding begins.

- **Code Reviews:** Conduct code reviews to identify coding errors and potential problems.

- **Testing:** Perform thorough testing throughout the development process.

- **Static Code Analysis:** Use static code analysis tools to identify potential problems in the code.

- **Pair Programming:** Have two developers work together to write code, which can help to identify and fix errors as they are made.

- **Test-Driven Development:** Write test cases before writing code, which can help to ensure that the code meets requirements.

Software Testing Life Cycle
---------------------------

The Software Testing Life Cycle (STLC) is a framework that defines the different phases of testing that a software application should go through. The STLC typically includes the following phases:

- **Requirement Analysis:** Analyze the requirements for the software to ensure they are clear, complete, and consistent.
- **Test Planning:** Develop a test plan that outlines the testing activities that will be performed.
- **Test Design:** Design test cases to test the software's functionality, performance, usability, and other quality attributes.
- **Test Execution:** Execute the test cases and record the results.
- **Defect Logging:** Log any defects that are found and track their progress until they are fixed.
- **Test Reporting:** Report the results of the testing to stakeholders.
- **Regression Testing:** Perform regression testing to ensure that fixes do not introduce new defects.
