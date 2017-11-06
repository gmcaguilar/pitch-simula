---?image=assets/bg2.jpg&size=100% auto

### Simula  

*Gabrielle Aguilar & Jason Bacani*

---?image=assets/bg2.jpg&size=100% auto

## SIMULA I

+++

### Kristen Nygaard

![nygaard](assets/nygaard.jpg)

+++

### Kristen Nygaard

- Norwegian computer scientist |
- Born on August 27, 1926 Oslo, Norway |
- University of Oslo (MS in Mathematics) |
- Acknowledged as the co-inventor of Object-Oriented Programming |

+++

### Problem

- 1950s: Describing how a system works was usually done using flow diagrams and a list of rules. |
- 1957: Nygaard wanted a better way of doing this. |
- Nygaard saw the potential with computer-aided simulations |
- He wanted to standardize the procedures of simulating a system using a computer language. |
- However, he needed someone more skilled in programming.. |

+++

### Ole-Johan Dahl

![dahl](assets/dahl.jpg)

+++

### Ole-Johan Dahl

- Norwegian computer scientist |
- Born on October 12, 1931 Mandal, Norway |
- University of Oslo (MS in Numerical Mathematics) |
- Acknowledged as the co-inverntor of Object-Oriented Programming |

+++

### Birth of SIMULA I

- Nygaard and Dahl met at the Norwegian Defense Research Establishment (NDRE) |
- January 1962: Dahl joined Nygaard in developing this computer language |
- May 1962: SIMULA I was born, a simulation language |

+++

### SIMULA I

- Simulation language |
- Used to program simulations on a computer |
- Not a general-purpose programming language |

+++?image=assets/dahl-nygaard2.jpg&size=100% auto

---?image=assets/bg2.jpg&size=100% auto

## SIMULA 67

+++

### Transition to Generality

- Dahl and Nygaard eventually realized that they had a powerful simulation language that would be an excellent platform for a general-purpose language.

> We can not just produce new special purpose languages the whole time, because they will not be widely implemented.  - Kristen Nygaard

+++

---?image=assets/bg2.jpg&size=100% auto

## Simula Tutorial

+++

### Value Types
- Integer
- Short Integer
- Real
- Long Real
- Boolean
- Character

+++

### Reference Types
- Object Reference
  - `ref(ClassName) x;`
   - Equivalent to `ClassName x;` object declaration in Java
   - The first part of `ClassName x = new ClassName();`
- Text
 - "Simula"

+++

### Simple Statements
- Assignment
  - `x := 1;`
- Reference Assignment
  - `x :- New ClassName;`
    - only after declaring an Object Reference `ref(ClassName) x;`
- Comments
  - `! this is a comment`
    - available in more recent implementations of SIMULA
  - `comment this might also be a comment;`
    - in older implementations

+++

## Structured/Compound Statements

+++

### Blocks
```
Begin
  ...
End;
```

+++

### Conditional Statements
```
If <condition> {and|or <condition>}
  Then <statement>
  [Else <statement>];
```
#### Boolean Operators
- For numeric and text values: =, <>, <=, >=, <, >
- For references (objects and text): ==, =/=

+++

### Hello World
```
Begin
  OutText("Hello World!");
  Outimage;
End;
```

+++

### Procedures
```
Begin
  ! Example procedure with two input parameters and one output parameter:
  ! Displays a right indented text
  Procedure RightText(T, N, FitsIn); Text T; Integer N;
               Name FitsIn; Boolean FitsIn;
  Begin
    Integer I;
    FitsIn := N >= T.Length;
    For i:=1 step 1 until N-T.Length do OutText(" ");
    OutText(T)
  End;

  RightText("Short", 30); OutImage;
  RightText("And the long one", 30);
End;
```

+++

### Functions
```
Begin
  Integer Procedure GCD(M, N); Integer M, N;
  Begin
     While M<>N do
        If M<N then N := N - M else M := M - N;
     GCD := M
  End;

  Integer A, B;
  OutText("Enter an integer number: "); OutImage;
  A := InInt;
  OutText("Enter an integer number: "); OutImage;
  B := InInt;
  OutText("Greatest Common Divisor of your numbers is ");
  OutInt(GCD(A,B), 4);
  OutImage;
End;
```

+++

### Classes
```
! Class with two parameters;
Class Rectangle (Width, Height); Real Width, Height;
Begin
  Real Area, Perimeter;  ! Attributes;

  Procedure Update;      ! Methods (Can be Virtual);
    Begin
      Area := Width * Height;
      Perimeter := 2*(Width + Height)
    End of Update;

  Boolean Procedure IsSquare;
    IsSquare := Width=Height;

    Update;                ! Life of rectangle started at creation;
    OutText("Rectangle created: "); OutFix(Width,2,6);
    OutFix(Height,2,6); OutImage
 End of Rectangle;
 ```
