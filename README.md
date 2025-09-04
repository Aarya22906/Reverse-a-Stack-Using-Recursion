# Reverse-a-Stack-Using-Recursion
You are given a stack of integers, and your task is to write a function that reverses the stack using recursion. You are not allowed to use any additional data structure (like arrays, lists, or another stack). The only operations you are allowed to perform are push, pop, and peek on the stack. The reversal must be done using recursion only
def insert_at_bottom(stack, element):
    if not stack:
        stack.append(element)
        return
    temp = stack.pop()
    insert_at_bottom(stack, element)
    stack.append(temp)
def reverse_stack(stack):
    if not stack:
        return
    temp = stack.pop()
    reverse_stack(stack)
    insert_at_bottom(stack, temp)
stack = [1, 2, 3, 4]
reverse_stack(stack)
print("Reversed Stack:", stack)
