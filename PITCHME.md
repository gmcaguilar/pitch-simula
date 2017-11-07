---?image=assets/bg2.jpg&size=100% auto

### Simula  

*Gabrielle Aguilar & Jason Bacani*

---?image=assets/bg2.jpg&size=100% auto

### SIMULA I

+++

#### Kristen Nygaard

![nygaard](assets/nygaard.jpg)

+++

#### Kristen Nygaard

- Norwegian computer scientist |
- Born on August 27, 1926 Oslo, Norway |
- University of Oslo (MS in Mathematics) |
- Acknowledged as co-inventor of Object-Oriented Programming |

+++

#### Problem

- 1950s: Describing how a system works was usually done using flow diagrams and a list of rules. |
- 1957: Nygaard wanted a better way of doing this. |
- Nygaard saw the potential with computer-aided simulations |
- He wanted to standardize the procedures of simulating a system using a computer language. |
- However, he needed someone more skilled in programming.. |

+++

#### Ole-Johan Dahl

![dahl](assets/dahl.jpg)

+++

#### Ole-Johan Dahl

- Norwegian computer scientist |
- Born on October 12, 1931 Mandal, Norway |
- University of Oslo (MS in Numerical Mathematics) |
- Acknowledged as co-inventor of Object-Oriented Programming |

+++

#### Birth of SIMULA I

- Nygaard and Dahl met at the Norwegian Defense Research Establishment (NDRE) |
- January 1962: Dahl joined Nygaard in developing this computer language at the NCC (Norwegian Computing Center) in Oslo |
- May 1962: SIMULA I was born, a simulation language |

+++

#### SIMULA I

- Simulation language |
- Used to program simulations on a computer |
- Not a general-purpose programming language |

+++?image=assets/dahl-nygaard2.jpg&size=100% auto

---?image=assets/bg2.jpg&size=100% auto

### SIMULA 67

+++

#### Transition to Generality

- Dahl and Nygaard realized they could make a general-purpose language from Simula I

> We can not just produce new special purpose languages the whole time, because they will not be widely implemented.  - Kristen Nygaard

+++

- Also, Dahl and Nygaard were influenced by the movement toward general-purpose languages at that time.
(ALGOL, PL/I)

> we have spent so much time with all these people working on general purpose languages, that I must admit we have to some extent fallen in love with the concept.. - Kristen Nygaard

+++

#### Ideas for Generality

- 1963: Dahl and Nygaard started to come up with ways to implement generality

- 1966: Concept of an object and a class were introduced by the two

- 1967: Paper about these novel concepts was presented at the IFIP(Intl. Fed. for Information Processing) conference in Oslo. This was considered the first formal declaration of SIMULA 67.

+++

#### SIMULA 67

- First object-oriented language(classes, subcluasses, methods, instances)
- General-purpose
- Near complete superset of ALGOL-60

---?image=assets/bg2.jpg&size=100% auto

### Simula Tutorial

+++

#### Value Types
- Integer
- Real
- Boolean
- Character

+++

#### Reference Types
- Reference (pointer)
- Text (string)

+++

#### Value-Type and Text Declarations
- &lt;DataType&gt; &lt;VariableName&gt;;
  - `Integer i; Real r;`
  - `Boolean b; Character c;`
  - `Text t;`

+++

#### Object-Reference Declarations
- Ref(&lt;ClassName&gt;) &lt;VariableName&gt;;
  - parentheses are terminal symbols
  - `Ref(ProgrammingLanguage) Simula;`

+++

#### Value Assignment
- &lt;VariableName&gt; := &lt;Expression&gt;
  - `i := 1; r := 0.5`
  - `b := true; c := 'A';`

+++

#### Reference Assignment
- &lt;VariableName&gt; :- &lt;Expression&gt;
  - `Simula :- New ProgrammingLanguage;`

+++

#### Comments
- !{&lt;Character&gt;};
  - `! this is a comment;`

+++

#### Input/Output
Data Type | Input |	Output
----------|-------|-------
Integer	| I := inint; |	outint(I, 10);
Real | X := inreal; | outreal(X, 2.10);
Character	| C := inchar; | outchar(C);
Text | <ul><li>T := intext(20);</li><li>inimage;</li></ul> | <ul><li>outtext ("OK!");</li><li>outimage;</li></ul>

+++

#### Notable Operators
Operation | Symbol
----------|-------
Real Division | /
Whole Division | //
Modulus | rem(dividend, divisor)
Exponentiation | **
Concatination | &amp;

+++

#### Notable Operators (cont'd)
Operation | Symbol
----------|-------
equality | <ul><li>=</li><li>==</li><li>eqv</li></ul>
inequality | <ul><li>&lt;&gt;</li><li>=/=</li></ul>

+++

#### Block Statement
```
begin {<declaration>}
   {<statement>}
end;
```

+++

#### If Statement
```
if <condition> {and|or <condition>}
  then <statement>
  [else <statement>];
```

+++

#### GoTo Statement
```
LABEL: {<statement>}
...
goto LABEL;
```

+++

#### While Statement
```
while <condition> do <statement>;
```

+++

#### For Statement
```
for I := 1 step 1 until 100 do ...;
for I := 100 step -1 until 1 do ...;
for C := 'A', 'E', 'I', 'O', 'U', 'Y' do ...;
```
+++

#### Procedures
```
...
PROCEDURE ADD (A, B, C);
  NAME C; INTEGER A, B, C;
  BEGIN
    C := A + B;
  END;
...
ADD (x, y, z);
OUTINT (z);
```
@[2](*declare procedure name*)
@[3](*initialize variables*)
@[5](*perform addition and assign results to `C`*)
@[8](*call method and pass x,y,z*)
@[9](*output result*)
@[1]()
+++

#### Functions
```
...
INTEGER PROCEDURE SUM (A, B); INTEGER A, B;
  SUM := A + B;
...
OUTINT (SUM (I, J));
```
+++

#### Classes
```
CLASS POINT (X, Y); REAL X, Y;
	BEGIN
	  REAL PROCEDURE DIST;  
	    BEGIN DIST: = SQRT (X ** 2 + Y ** 2) END;
	END;

REF (POINT) P;
P :- NEW POINT (1.0, 3.0);
OUTREAL (PX); OUTIMAGE;
OUTREAL (PY); OUTIMAGE;
OUTREAL (P.DIST); OUTIMAGE;
```

+++

#### Class Inheritence
```
POINT CLASS SEGMENT (R, THETA); REAL R, THETA;
	BEGIN
	  PROCEDURE SHIFT (DX, DY); REAL DX, DY;
	  BEGIN
	    X: = X + DX; Y: = Y + DY;
	  END;
	END;

REF (SEGMENT) S;
S :- NEW SEGMENT (1, 3, 10, PI);
S.SHIFT (-10, + 4);
```

---?image=assets/bg2.jpg&size=100% auto

### Legacy

+++

#### Influences

![kay](assets/kay.jpg)

Simula 67 was one of the inspirations for Alan Kay in developing **Smalltalk**

+++

![gos](assets/gos.jpg)

James Gosling cites Simula as a major influence in the development of **Java**

+++

![bjarne](assets/bjarne.jpg)

Bjarne Stroustrup also acknowledges Simula 67 as an inspiration for **C++**

+++

#### Recognition

IEEE John Von Neumann Medal

![medal](assets/medal.jpg)

> For the introduction of the concepts underlying object-oriented programming through the design and implementation of SIMULA 67

+++

ACM A.M. Turing Award

![turing](assets/turing.jpg)

> For ideas fundamental to the emergence of object oriented programming, through their design of the programming languages Simula I and Simula 67.

+++

#### Landmarks

Simula Research Laboratory  
(Fornebu, Norway)

![lab](assets/lab.jpg)


+++

Ole-Johan Dahl's Hus  
(University of Oslo, Norway)

![house](assets/house.jpg)

+++

#### Knighthood

Commander of the Royal Norwegian Order of St. Olav  
(Circa 2000)

![knight](assets/knight.jpg)



---?image=assets/bg2.jpg&size=100% auto

### *End*

+++

### Sources

[http://campus.hesge.ch/daehne/2004-2005/langages/simula.htm]

[http://progopedia.com/language/simula-67/]

[http://www.simula67.info/]
