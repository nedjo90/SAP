Unit objectives:

- Develop a simple ABAP program
- Describe ABAP syntax
- Add comments to code
- Consult keyword documentation
- Implement a simple dialog using the PARAMETERS statement
- Customize the ABAP editor


# Developing a simple ABAP Program

```ABAP
REPORT ZBC100_FIRST_PROGRAM

write 'Hello World'.
```

>space required after WRITE =>  ` ` 
>period required at end of statement `.`


Characteristics of ABAP:
- individual statements
- the first word in a statement is called an ABAP keyword
- two words must be separated by a space
- statements can be indented
- the ABAP runtime system does not differentiate between upper and lowercase in keywords, additions and operands


``` ABAP
Key functions:
-> CTRL + F2 = check syntax
-> CTRL + F3 = activate :
	> save program = system stores are an inactive version of the program in the repository
	> activating generates the runtime object that is used for execution
	> a transport request can be released only if the programs inside it are active
	> a transaction code linked to an ABAP program will run the active version of that program
-> F8 = Direct Processing (test or execute program)
```
# Introducing ABAP syntax

Characteristics of ABAP:

- typed
- enables multi-lingual applications
- enables SQL access
- has been enhanced as an object-oriented language
- platform-independent
- upward-compatible

=> designed for dialog-based business applications.
=> using translatable text elements, you can develop multi-lingual applications.
=>the Open SQL standard embedded in ABAP allows direct database access.
=> ABAP Object OOP for ABAP
=> ABAP syntax has the same meaning or function, regardless of the relational DB system and operating system for the application and presentation server.
=> App. impl. in ABAP will run in future releases.

ABAP Statements:

- Start with a keyword
- End with a period (without exception)
- May contain additions and operands (depending on the keyword used)
- Can span multiple lines
- Words must be separated by at least one space

Same keyword used multiple times:

```ABAP
PARAMETERS pa_name TYPE string.
PARAMETERS pa_total TYPE i.
```

Chained statement:

```ABAP
PARAMETERS: pa_name TYPE string,
			pa_total TYPE i.
```

(chained statements do not improve performance => better syntax)

Comments:

- `*`  at the start of line => whole line is a comment
- `"` at any position the remaining content in the line is a comment

Good practice => comment whole line


Keyword documentation = cursor + F1


# Implementing a simple dialog

`PARAMETERS` defines an input field on what is known as a ==Selection Screen==.
Every parameter => a single corresponding input field on the selection screen.
Selection screen includes an Execute button.

``PARAMETERS`` = variable


