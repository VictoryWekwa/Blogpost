## The Conditional statement

In writing codes in any programming language, controlling the flow of the program is very important that is why the conditional statements are used.  

In Python, there is the **if**, **else** and the **elif** statements and they are used to control the flow of a program and set conditions to meet a particular rule or requirements.

## IF STATEMENT

The **if** statement is used to check if one of the conditions set is either true or false.

## Syntax

In writing the **if** statement, the **if** keyword is used, followed by the condition and the colon.


```
if condition:
 do this
``` 



The body of the ***if*** statement is indented and follows the python indentation rule of being consistent in either using four spaces or a tab.

The if statement cannot be written empty without any codes in it, instead the **pass** statement is written to avoid errors .

```
if condition:
    pass
``` 


## Example

```
condition = 'name'
if condition=='name':
    print('Hello')
``` 
**Result:**
```
Hello
``` 



If statement can also be nested.
This means that you can write an if statement inside another if statement.


```
if condition:
    do this:
    if condition2:
        do this
``` 


## ELSE STATEMENT

The else statement is used when the code  does not meet the set condition or requirements.

## Syntax 

Just like the if statement, the else statement is followed by colon and indented.


```
else:
    do this
``` 

## Example

In writing a program to check the weather condition.

```
weather = 'is_hot'
if weather== 'is_cold':
    print("The weather is cold")
else:
    print("The weather is so hot!")
    
``` 
**Result:**

```
The weather is so hot!
``` 


## ELIF STATEMENT

The elif statement is used  to try another condition if the code does not meet a set condition or requirement. Multiple elif statement can be used in a statement to check for several other conditions. It is usually written before the else statement in a block of code.
If the requirement for the elif is not met, the the else statement runs.

## Syntax

In writing the elif statement, the condition is written followed by the colon.


```
elif condition:
    do this
``` 

## Example

Modifying the above program:

```
weather='is_hot'
if weather == 'is_cold':
    print("The weather is cold")
elif weather == 'is_hot':
    print("The weather is so hot!")
else:
    print ("Looks like a great weather today")
``` 
**Result:**

```
The weather is so hot!
``` 

Multiple elif can also be written in a program.


```weather='is_mild'
if weather =='is_cold':
    print ("The weather is cold")
elif weather == 'is_hot':
    print("The weather is so hot!")
elif weather == 'is_mild':
    print("The weather is neither cold nor hot.")
else:
    print("Great weather today!")
``` 
Result:

```
The weather is neither cold nor hot.
``` 


![Python_if_elif_else_statement.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1597868106939/p3OJ45EJq.jpeg)

 [image source]( https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.cnblogs.com%2Fls-2018%2Fp%2F8780812.html&psig=AOvVaw0-sCyS5MxSuAr-0YOlZIRt&ust=1597953941730000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCKjnkt6JqOsCFQAAAAAdAAAAABAd) 

The flowchart above gives more explanation on running the **if**, **elif** and **else**.

Thank you for reading, kindly like this article or leave a comment.