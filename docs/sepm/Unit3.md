# Unit 3 : Software Design
**Syllabus**

- [Design process](#design-process)

- [Design Concepts](#design-concepts)

- [Design Model](#design-model)

- [Design Heuristic](#design-heuristic)

- [Architectural Design](#architectural-design)

- [Architectural styles](#architectural-styles)

- [Architectural Mapping using Data Flow](#architectural-mapping-using-data-flow)

- [User Interface Design](#user-interface-design)

- [Component level Design (Class based components, traditional Components)](#component-level-design-class-based-components-traditional-components)

## Design Process

Software design process is a mechanism to transform user requirements into some suitable form, which helps the programmer in software coding and implementation. It deals with representing the client's requirement, as described in SRS (Software Requirement Specification) document, into a form, i.e., easily implementable using programming language.

## Objectives of Software Design

Following are the purposes of Software design:

1.  **Correctness:**Software design should be correct as per requirement.
2.  **Completeness:**The design should have all components like data structures, modules, and external interfaces, etc.
3.  **Efficiency:**Resources should be used efficiently by the program.
4.  **Flexibility:**Able to modify on changing needs.
5.  **Consistency:**There should not be any inconsistency in the design.
6.  **Maintainability:** The design should be so simple so that it can be easily maintainable by other designers.

## Design Concepts:

#### - Modularization

Modularization is a technique to divide a software system into multiple discrete and independent modules, which are expected to be capable of carrying out task(s) independently. These modules may work as basic constructs for the entire software. Designers tend to design modules such that they can be executed and/or compiled separately and independently.

Modular design unintentionally follows the rules of ‘divide and conquer’ problem-solving strategy this is because there are many other benefits attached with the modular design of a software.

Advantage of modularization:

- Smaller components are easier to maintain
- Program can be divided based on functional aspects
- Desired level of abstraction can be brought in the program
- Components with high cohesion can be re-used again
- Concurrent execution can be made possible
- Desired from security aspect

#### - Concurrency

In software design, concurrency is implemented by splitting the software into multiple independent units of execution, like modules and executing them in parallel. In other words, concurrency provides capability to the software to execute more than one part of code in parallel to each other.

It is necessary for the programmers and designers to recognize those modules, which can be made parallel execution.

#### - Coupling

Coupling is a measure that defines the level of inter-dependability among modules of a program. It tells at what level the modules interfere and interact with each other. The lower the coupling, the better the program.

There are five levels of coupling, namely -

- **Content coupling -** When a module can directly access or modify or refer to the content of another module, it is called content level coupling.
- **Common coupling-** When multiple modules have read and write access to some global data, it is called common or global coupling.
- **Control coupling-** Two modules are called control-coupled if one of them decides the function of the other module or changes its flow of execution.
- **Stamp coupling-** When multiple modules share common data structure and work on different part of it, it is called stamp coupling.
- **Data coupling-** Data coupling is when two modules interact with each other by means of passing data (as parameter). If a module passes data structure as parameter, then the receiving module should use all its components.

#### - Cohesion

Cohesion is a measure that defines the degree of intra-dependability within elements of a module. The greater the cohesion, the better is the program design.

There are seven types of cohesion, namely –

- **Co-incidental cohesion -** It is unplanned and random cohesion, which might be the result of breaking the program into smaller modules for the sake of modularization. Because it is unplanned, it may serve confusion to the programmers and is generally not-accepted.
- **Logical cohesion -** When logically categorized elements are put together into a module, it is called logical cohesion.
- **Temporal Cohesion -** When elements of module are organized such that they are processed at a similar point in time, it is called temporal cohesion.
- **Procedural cohesion -** When elements of module are grouped together, which are executed sequentially in order to perform a task, it is called procedural cohesion.
- **Communicational cohesion -** When elements of module are grouped together, which are executed sequentially and work on same data (information), it is called communicational cohesion.
- **Sequential cohesion -** When elements of module are grouped because the output of one element serves as input to another and so on, it is called sequential cohesion.
- **Functional cohesion -** It is considered to be the highest degree of cohesion, and it is highly expected. Elements of module in functional cohesion are grouped because they all contribute to a single well-defined function. It can also be reused.

## Design Model

Design modeling in software engineering represents the features of the software that helps engineer to develop it effectively, the architecture, the user interface, and the component level detail. Design modeling provides a variety of different views of the system like architecture plan for home or building. Different methods like data-driven, pattern-driven, or object-oriented methods are used for constructing the design model. All these methods use set of design principles for designing a model.
Designing a model is an important phase and is a multi-process that represent the data structure, program structure, interface characteristic, and procedural details. It is mainly classified into four categories – Data design, architectural design, interface design, and component-level design.

- **Data design:** It represents the data objects and their interrelationship in an entity-relationship diagram. Entity-relationship consists of information required for each entity or data objects as well as it shows the relationship between these objects. It shows the structure of the data in terms of the tables. It shows three type of relationship – One to one, one to many, and many to many. In one to one relation, one entity is connected to another entity. In one many relation, one Entity is connected to more than one entity. un many to many relations one entity is connected to more than one entity as well as other entity also connected with first entity using more than one entity.
- **Architectural design:** It defines the relationship between major structural elements of the software. It is about decomposing the system into interacting components. It is expressed as a block diagram defining an overview of the system structure – features of the components and how these components communicate with each other to share data. It defines the structure and properties of the component that are involved in the system and also the inter-relationship among these components.
- **User Interfaces design:** It represents how the Software communicates with the user i.e. the behavior of the system. It refers to the product where user interact with controls or displays of the product. For example, Military, vehicles, aircraft, audio equipment, computer peripherals are the areas where user interface design is implemented. UI design becomes efficient only after performing usability testing. This is done to test what works and what does not work as expected. Only after making the repair, the product is said to have an optimized interface.
- **Component level design:** It transforms the structural elements of the software architecture into a procedural description of software components. It is a perfect way to share a large amount of data. Components need not be concerned with how data is managed at a centralized level i.e. components need not worry about issues like backup and security of the data.

## **Design Heuristic**

The main goal of heuristic evaluations is to identify any problems associated with the design of user interfaces. A heuristic, or heuristic technique, is any approach to problem solving or self-discovery that employs a practical method that is not guaranteed to be optimal, perfect, or rational, but is nevertheless sufficient for reaching an immediate, short-term goal or approximation.

The simplicity of heuristic evaluation is beneficial at the early stages of design. This usability inspection method does not require user testing which can be burdensome due to the need for users, a place to test them and a payment for their time. Heuristic evaluation requires only one expert, reducing the complexity and expended time for evaluation.

## Principles of Design Heuristic

**Automate unwanted workload**:

- free cognitive resources for high-level tasks.

- eliminate mental calculations, estimations, comparisons, and unnecessary thinking.

· **Reduce uncertainty**:

- display data in a manner that is clear and obvious.

· **Fuse data**:

- reduce cognitive load by bringing together lower level data into a higher-level summation.

  **Present new information with meaningful aids to interpretation**:

- use a familiar framework, making it easier to absorb.

- use everyday terms, metaphors, etc.

  **Use names that are conceptually related to function**:

- Context-dependent.

- Attempt to improve recall and recognition.

- Group data in consistently meaningful ways to decrease search time.

  **Limit data-driven tasks**:

- Reduce the time spent assimilating raw data.

- Make appropriate use of color and graphics.

## **Architectural Design**

The architecture is not the operational software. Rather, it is a representation that enables a software engineer to:

(1) Analyze the effectiveness of the design in meeting its stated requirements,

(2) Consider architectural alternatives at a stage when making design changes is still relatively easy, and

(3) Reduce the risks associated with the construction of the software.

**Software architecture** is the high level structure of a software system, the discipline of creating such structures, and the documentation of these structures. It is the set of structures needed to reason about the software system, and comprises the software elements, the relations between them, and the properties of both elements and relations.

### Software architecture exhibits the following:

- **Multitude of stakeholders:** software systems have to cater to a variety of stakeholders such as business managers, owners, users and operators. These stakeholders all have their own concerns with respect to the system. Balancing these concerns and demonstrating how they are addressed is part of designing the system.This implies that architecture involves dealing with a broad variety of concerns and stakeholders, and has a multidisciplinary nature.

- **Separation of concerns:** the established way for architects to reduce complexity is by separating the concerns that drive the design. Architecture documentation shows that all stakeholder concerns are addressed by modeling and describing the architecture from separate points of view associated with the various stakeholder concerns. These separate descriptions are called architectural views (see for example the 4+1 Architectural View Model).

- **Quality-driven:** classic software design approaches (e.g. Jackson Structured Programming) were driven by required functionality and the flow of data through the system, but the current insight is that the architecture of a software system is more closely related to its quality attributes such as fault-tolerance, backward compatibility, extensibility, reliability, maintainability, availability, security, usability, and other such –ilities. Stakeholder concerns often translate into requirements on these quality attributes, which are variously called non-functional requirements, extra-functional requirements, behavioral requirements, or quality attribute requirements.

- **Recurring styles:** like building architecture, the software architecture discipline has developed standard ways to address recurring concerns. These “standard ways” are called by various names at various levels of abstraction. Common terms for recurring solutions are architectural style, strategy or tactic, reference architecture and architectural pattern.

- **Conceptual integrity:** a term introduced by Fred Brooks in The Mythical Man-Month to denote the idea that the architecture of a software system represents an overall vision of what it should do and how it should do it. This vision should be separated from its implementation. The architect assumes the role of “keeper of the vision”, making sure that additions to the system are in line with the architecture, hence preserving conceptual integrity.

## Architectural styles

The software needs the architectural design to represents the design of software. IEEE defines architectural design as “the process of defining a collection of hardware and software components and their interfaces to establish the framework for the development of a computer system.” The software that is built for computer-based systems can exhibit one of these many architectural styles.  
Each style will describe a system category that consists of :

- A set of components(eg: a database, computational modules) that will perform a function required by the system.
- The set of connectors will help in coordination, communication, and cooperation between the components.
- Conditions that how components can be integrated to form the system.
- Semantic models that help the designer to understand the overall properties of the system.

The use of architectural styles is to establish a structure for all the components of the system.

### **Taxonomy of Architectural styles:**

**1] Data centered architectures:**

- A data store will reside at the center of this architecture and is accessed frequently by the other components that update, add, delete or modify the data present within the store.
- The figure illustrates a typical data centered style. The client software access a central repository. Variation of this approach are used to transform the repository into a blackboard when data related to client or data of interest for the client change the notifications to client software.
- This data-centered architecture will promote integrability. This means that the existing components can be changed and new client components can be added to the architecture without the permission or concern of other clients.
- Data can be passed among clients using blackboard mechanism.

**Advantage of Data centered architecture**

- Repository of data is independent of clients
- Client work independent of each other
- It may be simple to add additional clients.
- Modification can be very easy

![](https://media.geeksforgeeks.org/wp-content/uploads/20221024125745/Screenshot20221024at12560-300x161.png)

**Data centered architecture**

**2] Data flow architectures:**

- This kind of architecture is used when input data is transformed into output data through a series of computational manipulative components.
- The figure represents pipe-and-filter architecture since it uses both pipe and filter and it has a set of components called filters connected by lines.
- Pipes are used to transmitting data from one component to the next.
- Each filter will work independently and is designed to take data input of a certain form and produces data output to the next filter of a specified form. The filters don’t require any knowledge of the working of neighboring filters.
- If the data flow degenerates into a single line of transforms, then it is termed as batch sequential. This structure accepts the batch of data and then applies a series of sequential components to transform it.

**Advantages of Data Flow architecture**

- It encourages upkeep, repurposing, and modification.
- With this design, concurrent execution is supported.

**The disadvantage of Data Flow architecture**

- It frequently degenerates to batch sequential system
- Data flow architecture does not allow applications that require greater user engagement.
- It is not easy to coordinate two different but related streams

![](https://img.brainkart.com/imagebk10/lKptndm.jpg)

**Data Flow architecture**

**3] Call and Return architectures:** It is used to create a program that is easy to scale and modify. Many sub-styles exist within this category. Two of them are explained below.

- **Remote procedure call architecture:** This components is used to present in a main program or sub program architecture distributed among multiple computers on a network.
- **Main program or Subprogram architectures:** The main program structure decomposes into number of subprograms or function into a control hierarchy. Main program contains number of subprograms that can invoke other components.

![program architecture](https://media.geeksforgeeks.org/wp-content/uploads/Program-architecture.png)

**4] Object Oriented architecture:** The components of a system encapsulate data and the operations that must be applied to manipulate the data. The coordination and communication between the components are established via the message passing.

**Characteristics of Object Oriented architecture**

- Object protect the system’s integrity.
- An object is unaware of the depiction of other items.

**Advantage of Object Oriented architecture**

- It enables the designer to separate a challenge into a collection of autonomous objects.
- Other objects are aware of the implementation details of the object, allowing changes to be made without having an impact on other objects.

**5]** **Layered architecture:**

- A number of different layers are defined with each layer performing a well-defined set of operations. Each layer will do some operations that becomes closer to machine instruction set progressively.
- At the outer layer, components will receive the user interface operations and at the inner layers, components will perform the operating system interfacing(communication and coordination with OS)
- Intermediate layers to utility services and application software functions.
- One common example of this architectural style is OSI-ISO (Open Systems Interconnection-International Organisation for Standardisation) communication system.

![](https://www.tutorialride.com/images/software-engineering/layered-architecture.jpg)

## Architectural Mapping using Data Flow

A mapping technique, called structured design, is often characterized as a data flow-oriented design method because it provides a convenient transition from a data flow diagram to software architecture.

- The transition from information flow to program structure is accomplished as part of a six step process:

- (1) The type of information flow is established,
- (2) Flow boundaries are indicated,
- (3) The DFD is mapped into the program structure,
- (4) Control hierarchy is defined,
- (5) The resultant structure is refined using design measures.
- (6) The architectural description is refined and elaborated.

- Example of data flow mapping, a step-by-step “transform” mapping for a small part of the SafeHome security function.
- In order to perform the mapping,
- The type of information flow must be determined. It is called **_transform flow and exhibits a linear quality._**
- Data flows into the system along an incoming flow path where it is transformed from an external world representation into internalized form. Once it has been internalized, **it is processed at a transform center.**
- Finally, it flows out of the system along an outgoing flow path that transforms the data into external world form.

## User Interface Design

User interface is the front-end application view to which user interacts in order to use the software. The software becomes more popular if its user interface is:

- Attractive
- Simple to use
- Responsive in short time
- Clear to understand
- Consistent on all interface screens

There are two types of User Interface:

1.  **Command Line Interface:** Command Line Interface provides a command prompt, where the user types the command and feeds to the system. The user needs to remember the syntax of the command and its use. eg Unix, MSDos.
2.  **Graphical User Interface:** Graphical User Interface provides the simple interactive interface to interact with the system. GUI can be a combination of both hardware and software. Using GUI, user interprets the software. eg Windows, Android.

### UI Design Principles

**Structure:** Design should organize the user interface purposefully, in the meaningful and usual based on precise, consistent models that are apparent and recognizable to users, putting related things together and separating unrelated things, differentiating dissimilar things and making similar things resemble one another. The structure principle is concerned with overall user interface architecture.

**Simplicity:** The design should make the simple, common task easy, communicating clearly and directly in the user's language, and providing good shortcuts that are meaningfully related to longer procedures.

**Visibility:** The design should make all required options and materials for a given function visible without distracting the user with extraneous or redundant data.

**Feedback:** The design should keep users informed of actions or interpretation, changes of state or condition, and bugs or exceptions that are relevant and of interest to the user through clear, concise, and unambiguous language familiar to users.

**Tolerance:** The design should be flexible and tolerant, decreasing the cost of errors and misuse by allowing undoing and redoing while also preventing bugs wherever possible by tolerating varied inputs and sequences and by interpreting all reasonable actions.

### User Interface Golden rules

The following rules are mentioned to be the golden rules for GUI design, described by Shneiderman and Plaisant in their book (Designing the User Interface).

- **Strive for consistency** - Consistent sequences of actions should be required in similar situations. Identical terminology should be used in prompts, menus, and help screens. Consistent commands should be employed throughout.
- **Enable frequent users to use short-cuts** - The user’s desire to reduce the number of interactions increases with the frequency of use. Abbreviations, function keys, hidden commands, and macro facilities are very helpful to an expert user.
- **Offer informative feedback** - For every operator action, there should be some system feedback. For frequent and minor actions, the response must be modest, while for infrequent and major actions, the response must be more substantial.
- **Design dialog to yield closure** - Sequences of actions should be organized into groups with a beginning, middle, and end. The informative feedback at the completion of a group of actions gives the operators the satisfaction of accomplishment, a sense of relief, the signal to drop contingency plans and options from their minds, and this indicates that the way ahead is clear to prepare for the next group of actions.
- **Offer simple error handling** - As much as possible, design the system so the user will not make a serious error. If an error is made, the system should be able to detect it and offer simple, comprehensible mechanisms for handling the error.
- **Permit easy reversal of actions** - This feature relieves anxiety, since the user knows that errors can be undone. Easy reversal of actions encourages exploration of unfamiliar options. The units of reversibility may be a single action, a data entry, or a complete group of actions.
- **Support internal locus of control** - Experienced operators strongly desire the sense that they are in charge of the system and that the system responds to their actions. Design the system to make users the initiators of actions rather than the responders.
- **Reduce short-term memory load** - The limitation of human information processing in short-term memory requires the displays to be kept simple, multiple page displays be consolidated, window-motion frequency be reduced, and sufficient training time be allotted for codes, mnemonics, and sequences of actions.

## **Component level Design**

**Component-based software engineering (CBSE)** (also known as **component-based development (CBD)**) is a branch of software engineering that emphasizes the separation of concerns in respect of the wide-ranging functionality available throughout a given software system. It is a reuse-based approach to defining, implementing and composing loosely coupled independent components into systems. This practice aims to bring about an equally wide-ranging degree of benefits in both the short-term and the long-term for the software itself and for organizations that sponsor such software.

Software engineering practitioners regard components as part of the starting platform for service-orientation. Components play this role, for example, in web services, and more recently, in service-oriented architectures (SOA), whereby a component is converted by the web service into a _service_ and subsequently inherits further characteristics beyond that of an ordinary component.

## What is Component Level Design?

- A complete set of software components is defined during architectural design
- But the internal data structures and processing details of each component are not represented at a level of abstraction that is close to code
- _Component-level design defines, the data structures algorithms, interface characteristics, and communication mechanisms allocated to each component_
- A component-level design can be represented using some intermediate representation (e.g. graphical, tabular, or text-based) that can be translated into source code
- The design of data structures, interfaces, and algorithms should conform to well-established guidelines to help us avoid the introduction of errors
- A component communicates and collaborates with other components

## References

- https://www.geeksforgeeks.org/software-engineering-software-design-process/
- https://www.javatpoint.com/software-engineering-software-design
- https://www.brainkart.com/article/Design-Heuristic_9077/
- https://www.geeksforgeeks.org/software-engineering-architectural-design/
- -https://ecomputernotes.com/software-engineering/architecturaldesign
- http://softwareengineeringmca.blogspot.com/2017/07/architectural-mapping-using-data-flow-transform-mapping.html
- https://www.scribd.com/document/464837735/Architectural-mapping-using-Data-flow
- https://www.brainkart.com/article/Architectural-styles,-Architectural-Design,-Architectural-Mapping-using-Data-Flow_9079/
- https://www.geeksforgeeks.org/software-engineering-user-interface-design/
- https://www.javatpoint.com/software-engineering-user-interface-design
- https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm
- https://www.tutorialspoint.com/software_engineering/software_user_interface_design.htm
- http://epgp.inflibnet.ac.in/epgpdata/uploads/epgp_content/S000007CS/P001067/M022567/ET/1504860540SE-MOD17-e-TEXT.pdf
- https://www.educative.io/answers/what-is-the-component-design
- https://cuitutorial.com/component-level-design/
