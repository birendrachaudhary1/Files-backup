---
title: "Day 2: Understanding Conditionals in Shell Scripting (if, else, elif)."
datePublished: Mon Jan 06 2025 14:45:31 GMT+0000 (Coordinated Universal Time)
cuid: cm5l5lwwe000e08lehfk70eml
slug: day-2-understanding-conditionals-in-shell-scripting-if-else-elif
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1736091542168/153ac06a-bfd5-49fc-9e97-dde831295e23.png
tags: ubuntu, linux, scripting

---

Conditionals allow us to make decisions in your shell scripts. They let you run different blocks of code depending on whether a condition is true or false.

1\. **if Statement**

#!/bin/bash  
x=5  
if \[ $x -gt 3 \]; then  
echo "x is greater than 3"  
fi

— `[ $x -gt 3 ]`: This is the condition.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736089440822/2a2888e7-e1aa-4bd0-a21b-5caa6c45b6b7.png align="center")

2\. **else Statement**  
The `else` statement is used to specify what should happen if the `if` condition is **false**.

#!/bin/bash

x=2  
if \[ $x -gt 3 \]; then  
echo "x is greater than 3"  
else  
echo "x is not greater than 3"  
fi

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736089680870/77e7a7fd-f3d0-4393-8db3-c6f4e4154e4b.png align="center")

3\. **elif Statement**

`elif` (else if) is used to check multiple conditions. It runs if the first `if` condition is false but the `elif` condition is true.

#!/bin/bash  
x=3  
if \[ $x -gt 3 \]; then  
echo "x is greater than 3"  
elif  
\[ $x -eq 3 \]; then echo "x is equal to 3"  
else  
echo "x is less than 3"  
fi

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736090846234/87bc8f85-6345-4150-9a59-90fc9de87454.png align="center")

4\. **Combining Multiple Conditions**

You can combine conditions using `&&` (AND) or `||` (OR).

# **AND** (`&&`): All conditions must be true.  

#!/bin/bash

#Initialize x with a value or get it from user input

x=1 # Example of initializing x with a default value

#Alternatively, you can prompt the user for input

#read -p "Enter the value of x: " x

#Ensure x is not empty and is a valid number

if \[\[ -n "$x" && "$x" =~ ^\[0-9\]+$ \]\]; then  
if \[ "$x" -gt 2 \] && \[ "$x" -lt 5 \]; then  
echo "x is between 2 and 5"  
else  
echo "x is not between 2 and 5"  
fi  
else  
echo "Error: x is not defined or is not a valid number"  
fi  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736174036772/45ca8c08-4eac-40f8-8128-61c08c131b82.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736174060912/40356db6-8b78-49a2-8a4f-75a9a7224636.png align="center")

  

#   
**OR** (`||`): At least one condition must be true.

  
#!/bin/bash

#Initialize x with a value or get it from user input

x=15 # Example of initializing x with a default value

#Alternatively, you can prompt the user for input

#read -p "Enter the value of x: " x

#Ensure x is not empty and is a valid number

if \[\[ -n "$x" && "$x" =~ ^\[0-9\]+$ \]\]; then  
if \[ "$x" -lt 2 \] || \[ "$x" -gt 10 \]; then  
echo "x is either less than 2 or greater than 10"  
else  
echo "x is between 2 and 10"  
fi  
else  
echo "Error: x is not defined or is not a valid number"  
fi

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736174262717/555554c1-e0a4-46f3-8d0a-374443745138.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736174303818/3ceb6972-4d6e-40ad-92e6-39d6e92617fe.png align="center")

5. ### Conclusion
    

Today, we learned how to use **if**, **else**, and **elif** statements to make decisions in your scripts. we explored logical operators like **AND (**`&&`) and **OR (**`||`) and practiced handling different conditions. Input validation and quoting variables were emphasized to avoid errors.

*If you have any questions or face issues, feel free to drop a comment below or mail me at* [***birendra2783@gmail.com***](mailto:birendra2783@gmail.com)*!*