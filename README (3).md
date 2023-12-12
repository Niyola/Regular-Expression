
# Project Title
EXPRESSION TRANSFORMATION PROJECT
# Author Name: Eniola Adesuyi (xadesu00)

A brief description of what this project does and who it's for
The code provided is like a translator for mathematical expressions. When you give it a mathematical expression written in a way that we humans understand, it breaks it down into smaller parts called tokens, like numbers, symbols (+, -, *, /, %, ^), and brackets.

After breaking it down, it rearranges these parts into a specific order that a computer can easily calculate. This rearranged order is called a postfix expression. For instance, instead of writing "3 + 4", the computer prefers "3 4 +". then i use  string  which is an ordered sequence of characters, where each character has a specific position or index within the string.


Once it has this rearranged expression, it converts it back into the more familiar form that we humans use. This is called an infix expression. For example, it turns "3 4 +" back into "3 + 4".

The code demonstrates how this translation process works for a particular mathematical expression. It's like a teaching example, showing how a computer might break down, rearrange, and then reconstruct a simple math problem.

This code could be useful for people learning about how computers handle and calculate math problems written in a way that resembles human language. It's a starting point to understand how computers process and evaluate mathematical expressions, but it's not designed for handling very complex math or advanced functions.

def add(x, y):
    return "(" + str(x) + " + " + str(y) + ")"

def sub(x, y):
    return "(" + str(x) + " - " + str(y) + ")"

def mul(x, y):
    return "(" + str(x) + " * " + str(y) + ")"

def div(x, y):
    return "(" + str(x) + " / " + str(y) + ")"

def mod(x, y):
    return "(" + str(x) + " % " + str(y) + ")"

def pow(x, y):
    return "(" + str(x) + " ^ " + str(y) + ")"

def transform_functions(expression):
    return expression.replace('add', 'add ').replace('sub', 'sub ').replace('mul', 'mul ').replace('div', 'div ').replace('mod', 'mod ').replace('pow', 'pow ')

def convert_expression(expression):
    eval_expression = transform_functions(expression)
    return eval(eval_expression)

# Example usage
composed_function = "add(5, mul(3, sub(10, pow(6, 4))))"
math_expression = convert_expression(composed_function)
print(math_expression)
