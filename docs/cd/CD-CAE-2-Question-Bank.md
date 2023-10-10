# Question Bank CAE-2

## Questions
1. No
2. [What is the Syntax Directed Definition (SDD) for the simple desk calculator, Write andexplain. What would be the parse tree for 1* 2 + 3n](#ans2)
3. [What do you mean by syntax tree? Explain the constructing syntax tee for expressiona-4+c.](#ans3)


2. No

## 2. What is the Syntax Directed Definition (SDD) for the simple desk calculator, Write andexplain. What would be the parse tree for 1* 2 + 3n
###### Ans2
Syntax Directed Definition (SDD) for a simple desk calculator grammar along with an explanation:

```markdown

1. E -> E1 + T { E.val = E1.val + T.val; }
2. E -> E1 - T { E.val = E1.val - T.val; }
3. E -> T { E.val = T.val; }
4. T -> num { T.val = num.value; }
5. T -> (E) { T.val = E.val; }
```

Explanation:

- Rule 1 handles addition in expressions. When an addition operation is encountered, it calculates the value of the expression on the left (E1.val) and the value of the term on the right (T.val), and then stores the result in the attribute E.val.

- Rule 2 handles subtraction in expressions. Similar to Rule 1, it calculates the value of the expression on the left and the term on the right and stores the result in E.val.

- Rule 3 represents the case when there is no addition or subtraction operation, only a single term. In this case, it assigns the value of the term to E.val.

- Rule 4 handles numeric constants (num). It assigns the value of the numeric constant to the attribute T.val.

- Rule 5 handles expressions enclosed in parentheses. It sets the value of the term inside the parentheses to the attribute T.val.

Now, let's construct the parse tree for the expression "1 * 2 + 3n" using the provided SDD:

Parse Tree:

```markdown
      +
     / \
    *   3n
   / \
  1   2
```

In this parse tree:

- The "*" represents multiplication.
- The "+" represents addition.
- "1" and "2" are numeric constants, so T.val for both is their respective values (1 and 2).
- "3n" is an expression in parentheses, so T.val for this term is the value of the expression inside the parentheses, which is 3.

## 3. What do you mean by syntax tree? Explain the constructing syntax tee for expressiona-4+c.

###### ans3

A syntax tree, also known as a parse tree or abstract syntax tree (AST), is a hierarchical representation of the syntactic structure of a sentence or expression in a formal language, typically derived from a context-free grammar. It visually represents how the various components of the language construct relate to each other and how they should be interpreted by a compiler or interpreter.

A syntax tree is composed of nodes and edges, where each node represents a syntactic construct (such as a terminal or non-terminal symbol in a grammar), and the edges represent the relationships between these constructs, indicating how they are combined to form valid expressions or statements. The root of the tree represents the highest-level construct, and its branches and sub-branches break down the expression into smaller components, following the grammar rules.

Here is the construction of a syntax tree for the expression "a - 4 + c":

```markdown
       -
      / \
     a   +
        / \
       4   c
```

In this tree:

- The root node represents the subtraction operation ("-").
- The left child of the root node represents the variable "a."
- The right child of the root node represents an addition operation ("+").
- The left child of the addition node represents the numeric constant "4."
- The right child of the addition node represents the variable "c."

## 4. What is the translation scheme with right recursive grammar? E->E+T|E-T |T <br> T ->(E) num <br> Show the annotated parse-tree with the value of the attribute E.val at root for 9-5+2.

###### Ans4

Translation scheme for the right-recursive grammar:

```markdown
E -> E1 + T { E.val = E1.val + T.val; }
E -> E1 - T { E.val = E1.val - T.val; }
E -> T { E.val = T.val; }
T -> (E) { T.val = E.val; }
T -> num { T.val = num.value; }
```

Now, let's show the annotated parse tree with the value of the attribute E.val at the root for the expression 9 - 5 + 2:

```plaintext
     +
    / \
   -   2
  / \
 9   5
```

In this annotated parse tree, the value of the attribute E.val at the root is 6, which is the result of the expression 9 - 5 + 2.

## 5. Consider the following grammar<br>D->TL<br>T ->int I real <br>L -> L,id | id<br>i. Construct a syntax- Directed translation scheme with inherited attribute L.in<br>ii.Show the parse treefor input string intX, Y, Z

###### Ans5

The syntax-directed translation scheme (SDT) with the inherited attribute L.in for the given grammar:

```plaintext
D -> TL { D.in = L.in; }
L -> L, id { L.in = L1.in; print(id.lexeme, L.in); }
L -> id { L.in = id.lexeme; }
T -> int I real { print(I.lexeme, T.in); }
```

Now, let's construct the parse tree for the input string "intX, Y, Z":

```markdown
       D
      / \
     T   L
    /   / \
 int   L,id
  |   / | \
  I  X  L,id
   |   / | \
 real  Y  L,id
        / | \
       Z  ε
```

In this parse tree, the inherited attribute L.in is passed from parent nodes to child nodes and printed for each id node. The output will be "X, X, Y, X, Y, Z" as each id is printed with L.in.

## 6. Let synthesize attribute 'Val' gives the value of binary number generated by 'S' inthe following Grammar (For example on input 100.101.s val=4.625)<br>s->L.L|L<br>L->LB|B<br>B->0|1<br>Give the synthesized attributes to determine S. Val

###### Ans6

The synthesized attributes to determine S.Val for the given grammar:

```plaintext
S -> L.L { S.Val = L1.Val + L2.Val / 2; }
S -> L { S.Val = L.Val; }
L -> L1 B { L.Val = L1.Val * 2 + B.Val; }
L -> B { L.Val = B.Val; }
B -> 0 { B.Val = 0; }
B -> 1 { B.Val = 1; }
```

In this attribute grammar, S.Val is synthesized based on the binary number generated by the grammar rules. The value of S.Val is calculated by combining the values of L1.Val and L2.Val for the L.L production. For L and B productions, the values are determined based on the binary digits encountered.

## 7. What are the requirements for a translation scheme when both synthesized and inherited attributes are present? Find whether the following scheme satisfies allthe requirements? Justify your answer.<br>S->A1A2{A1.in=1; A2.in=2}<br>A->a {print (A.in)}.

###### Ans7

A translation scheme with both synthesized and inherited attributes must satisfy certain requirements to ensure that the attributes are correctly computed and propagated. Here are the requirements for a translation scheme with both synthesized and inherited attributes:

- Attribute Initialization: All inherited attributes must be initialized before they are used in computations. This ensures that the inherited attributes have meaningful values when they are needed.
- Attribute Computation Order: The order in which attributes are computed and propagated must respect the dependencies between them. Inherited attributes should be computed before they are used to compute synthesized attributes.
- Attribute Usage: All attributes, both inherited and synthesized, should be used correctly in the translation scheme. They should be used in a way that accurately represents the desired semantics of the source language.

Now, let's analyze the provided translation scheme:

```plaintext
S -> A1 A2 { A1.in = 1; A2.in = 2; }
A -> a { print(A.in); }
```

In this scheme, we have two attributes, A1.in and A2.in, which are inherited attributes, and we have the synthesized attribute A.in. Let's check if the scheme satisfies the requirements:

- Attribute Initialization: The scheme initializes the inherited attributes A1.in and A2.in by assigning values 1 and 2, respectively. So, the requirement for attribute initialization is met.

- Attribute Computation Order: In this scheme, there are no dependencies between attributes that require a specific order of computation. The inherited attributes `A1.in` and `A2.in` are set at the beginning of the S production, and the synthesized attribute `A.in` is computed within the A production. There is no circular dependency or ambiguity in the computation order. So, the requirement for attribute computation order is met.

- Attribute Usage: The usage of attributes in the scheme appears to be correct. The inherited attributes are used to initialize values, and the synthesized attribute `A.in` is used in the `print` statement. However, it's worth noting that the attribute `A.in` is synthesized but not explicitly initialized or computed within the scheme. This could be a potential issue if `A.in` needs to be used further in the translation process. As it stands, it would print `A.in`, but it's not clear what value it holds. It would be more meaningful if `A.in` was computed or initialized before it is printed.

## 8. Consider the following grammar :
```markdown
L->E
E->E1+T | T
T->T1*F|F
F->(E)|digit
```

**Where digit is a terminal symbol.**  
(i) Obtain the Syntax Directed Definition (SDD) for the above grammar  
(ii) Implement the above grammar using LR parser  
(iii) Show the moves generated on by the translator in  
(ii) on input "5 + 3* 4'.

###### Ans8

(i) Syntax Directed Definition (SDD) for the given grammar:
To create an SDD for the given grammar, we can define attributes and associate semantic actions with each production. Here's an SDD for the given grammar:

```plaintext
L -> E { L.val = E.val; }
E -> E1 + T { E.val = E1.val + T.val; }
E -> T { E.val = T.val; }
T -> T1 * F { T.val = T1.val * F.val; }
T -> F { T.val = F.val; }
F -> (E) { F.val = E.val; }
F -> digit { F.val = digit.lexeme; }
```

In this SDD, we define a synthesized attribute 'val' for each non-terminal to compute and store the value of the corresponding expression. The attribute 'val' represents the value of the expression generated by each production.

(ii) Implementing the grammar using an LR parser:
To implement the given grammar using an LR parser, you would typically use a tool like Yacc/Bison or a parser generator. However, I can provide you with a high-level overview of how the grammar can be implemented.

Define the grammar in a format suitable for the parser generator tool. For example:

```css
%token digit
%%
L: E { /* Code to handle the value of L.val */ }
E: E '+' T { /* Code to handle the value of E.val */ }
 | T { /* Code to handle the value of E.val */ }
T: T '*' F { /* Code to handle the value of T.val */ }
 | F { /* Code to handle the value of T.val */ }
F: '(' E ')' { /* Code to handle the value of F.val */ }
 | digit { /* Code to handle the value of F.val */ }
```

- Use a parser generator tool to generate the parser code based on this grammar. The tool will generate code that constructs a parse tree and handles the semantic actions associated with each production.

(iii) Showing the moves generated by the translator on input "5 + 3 * 4":

Assuming an LR parser is used, here's a simplified step-by-step explanation of how the parser would process the input:

- Input: "5 + 3 * 4"
- The parser starts with an empty stack and an initial state.
- It reads "5" and shifts it onto the stack.
- The stack now contains: [5]
- It reads "+" and shifts it onto the stack.
- The stack now contains: [5, +]
- It reads "3" and shifts it onto the stack.
- The stack now contains: [5, +, 3]
- It reduces "3" to "F" using the production F -> digit.
- The stack now contains: [5, +, F]
- It reads "*" and shifts it onto the stack.
- The stack now contains: [5, +, F, *]
- It reads "4" and shifts it onto the stack.
- The stack now contains: [5, +, F, *, 4]
- It reduces "4" to "F" using the production F -> digit.
- The stack now contains: [5, +, F, *, F]
- It reduces "F * F" to "T" using the production T -> T1 * F.
- The stack now contains: [5, +, T]
- It reduces "T + T" to "E" using the production E -> E1 + T.
- The stack now contains: [E]
- The parser accepts the input, and the final value of the expression is in the attribute E.val.

## 9. What are Syntax Directed Translations (SDTS)? What are its types? Explain with a suitable example

###### Ans9

Syntax-Directed Translations (SDTs) are a formal method used in compiler design and programming language processing to associate semantic actions with the production rules of a grammar. SDTs combine the process of parsing (generating a parse tree or an abstract syntax tree) with the execution of actions that produce meaningful output or perform specific tasks based on the input source code. These actions are associated with specific grammar productions and are executed during parsing to create a translation or transformation of the source code.

Types of Syntax-Directed Translations (SDTs):

- Inherited Attribute Grammars (IAGs): In IAGs, attributes can flow from parent nodes to child nodes in the syntax tree. Inherited attributes are computed at higher-level nodes and can be passed down to lower-level nodes to provide context or information needed for translation. IAGs are commonly used in type checking and semantic analysis phases of a compiler.

- Synthesized Attribute Grammars (SAGs): In SAGs, attributes are computed at the child nodes and then propagated up to the parent nodes.
- Synthesized attributes represent information that is calculated or generated at the leaf nodes of the syntax tree and combined as the tree is constructed to produce the final result. SAGs are often used for code generation.

Here's an example to illustrate Syntax-Directed Translations (SDTs) using a simple expression grammar:

Consider the following expression grammar:

```r
E -> E + T | T
T -> T * F | F
F -> (E) | num
```

We want to associate attributes and actions with this grammar to evaluate arithmetic expressions and compute their values.

- Inherited Attribute Grammars (IAGs):
- Let's use IAGs to perform type checking and ensure that "+" and "*" operators are used with compatible operands. We'll introduce an inherited attribute IAG.type to represent the type of the subexpression:

```plaintext
E -> E1 + T { E1.type = T.type; E.type = compatible(E1.type, T.type); }
T -> T1 * F { T1.type = F.type; T.type = compatible(T1.type, F.type); }
F -> (E) { F.type = E.type; }
F -> num { F.type = int; }
```

In this example, compatible is a function that checks if two types can be used together in an expression. The type attribute is inherited from parent nodes to child nodes to ensure type consistency.

Synthesized Attribute Grammars (SAGs):
Let's use SAGs to compute the value of arithmetic expressions:

```plaintext
E -> E1 + T { E.val = E1.val + T.val; }
E -> T { E.val = T.val; }
T -> T1 * F { T.val = T1.val * F.val; }
T -> F { T.val = F.val; }
F -> (E) { F.val = E.val; }
F -> num { F.val = num.value; }
```

In this example, the val attribute is synthesized from child nodes to parent nodes to compute the final value of the expression. The value attribute represents the numeric value of a terminal symbol num.