# vscode 入门

Created: September 12, 2022 9:45 PM
Status: Solved
Tags: vscode

返回上一个光标control+-

从上一个光标返回 control+shift+-

---

# ****Continue, Step Over, Step Into and Step Out actions in Visual Studio Code debugger explained****

[Continue, Step Over, Step Into and Step Out actions in Visual Studio Code debugger explained | pawelgrzybek.com](https://pawelgrzybek.com/continue-step-over-step-into-and-step-out-actions-in-visual-studio-code-debugger-explained/)

![Untitled](vscode%20%E5%85%A5%E9%97%A8%209a99ed15cdcd4c138d93adfe530959d0/Untitled.png)

## continue

Debugger executes the program and “breaks” only on user-defined breakpoints (red circles).

## Step over

Debugger executes the program statement by statement within the current execution context (scope).

## Step into

The debugger will execute the function body if the statement is a function call (a new execution context appears in the “call stack” tab).other features are same as Step over

## Step out

If the debugger is within a nested scope, this action proceeds until the function returns (exits the current execution context). In case the debugger is within the global scope, this action executes the program to the end.

---