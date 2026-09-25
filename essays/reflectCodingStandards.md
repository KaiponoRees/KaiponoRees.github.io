---
layout: essay
type: essay
title: "Reflect on Coding Standards"
# All dates must be YYYY-MM-DD format!
date: 2026-09-24
published: true
labels:
  - Engineering
  - TypeScript
  - Software Engineering
---

<img width="500px" class="rounded float-start pe-4" src="../img/esLintPic2.png">

## Coding Standards ESLint and VSCode

When people hear the phrase “coding standards,” they may only think about small formatting rules, such as how many spaces to use for indentation, where to place curly braces, or whether to use single or double quotation marks. These details can sometimes feel unimportant because they do not change what a program does. However, after working with ESLint and TypeScript, I realized that coding standards involve much more than making code look clean. They can improve readability, identify mistakes, and teach programmers how to use a programming language more effectively.

## My First Thoughts/Experience with ESLint

<img width="500px" class="rounded float-start pe-4" src="../img/esLintPic.png">

My first week using ESLint with Visual Studio Code was both frustrating and useful. One of the first problems I experienced was that the terminal reported 32 errors, while the VS Code editor only displayed six. This made the assignment more confusing because I expected every error from the terminal to appear as a red underline in the editor.

I also ran into configuration problems involving the Airbnb style guide and the ESLint extension. Before I could work on fixing the actual code, I had to understand why the command-line tool and the editor were behaving differently. This showed me that development tools can be helpful, but they must be installed and configured correctly before they can provide their full benefits.

Once ESLint started working correctly, I was finally able to see all of the errors and begin fixing them. Having 32 errors in such a small file seemed overwhelming at first, but many of them were related to the same types of problems.

## Formatting is Just Apart of It

Some of the ESLint errors initially seemed overly strict. It identified missing spaces, unnecessary semicolons, inconsistent formatting, and a missing newline at the end of the file. Fixing these errors sometimes felt tedious because the program could still run without many of those changes.

It was tempting to think that if the code worked, then small formatting details should not matter. However, code is not written only for the computer. It is also written for other programmers and for the original programmer who may return to it several months later. Consistent formatting makes it easier to understand the structure of a program without wasting time trying to interpret another programmer’s personal coding style.

When everyone follows the same standards, code becomes much easier to read. A programmer can focus on understanding what the code does instead of being distracted by inconsistent spacing, indentation, or naming.

## Troubleshooting Before Running the Code

ESLint also found problems that were more serious than formatting. For example, it warned me about reassigning a function parameter, using an unsafe any value, failing to return a value on every possible path, and using == instead of ===.

These rules can prevent bugs rather than simply changing the appearance of the code. A missing space will probably not break a program, but an unexpected any value or inconsistent return behavior can create problems that are difficult to diagnose later.

Because ESLint reports both formatting and programming issues, it acts as a combination of a style checker and an early warning system. It helps programmers find problems before the program is executed or submitted. Even though fixing all the errors can be annoying, it is better to find those problems early than to discover them later when the program becomes larger and more complicated.

## Learning Through Coding Standards

I agree that coding standards can help someone learn a programming language. ESLint does not only say that something is wrong. It normally provides the name of the rule that was violated. Looking up that rule can explain why one approach is safer or more commonly used than another.

For example, being told to use const instead of let teaches the programmer to avoid unnecessary reassignment. Being told to use === instead of == introduces the issue of JavaScript’s automatic type conversion. TypeScript-related ESLint rules also encourage programmers to use proper types instead of depending on any.

Each error can become a small lesson about the language. Instead of allowing me to continue using bad habits, ESLint forces me to slow down, examine my code, and understand why a different approach might be better. This can be frustrating while completing an assignment, but it can also help build better programming habits over time.

## Finding A Balance

Coding standards should support developers instead of controlling every decision they make. A rule that makes sense for one project may not make sense for another. Teams should understand why their rules exist and adjust them when necessary.

Disabling a rule can be reasonable, but it should be an intentional decision rather than a way to avoid fixing code. If developers automatically turn off every rule that causes difficulty, they lose the benefits that ESLint provides. At the same time, having too many unnecessary rules can make developers focus more on satisfying the tool than improving the program.

The most useful coding standards are the ones that make code safer, clearer, and easier to maintain.

## My Thoughts

Overall, my first experience with ESLint has been both painful and useful. The configuration issues and large number of errors were frustrating, especially when the terminal and VS Code editor did not agree. However, correcting the errors helped me produce cleaner and safer TypeScript code.

More importantly, this experience changed how I view coding standards. They are not merely rules about spaces and curly braces. When used properly, coding standards improve communication, prevent common mistakes, and help programmers develop better habits while learning a language.

I may not enjoy seeing 32 ESLint errors appear in my terminal, but I now understand that those errors are trying to help me improve my code. Fixing them takes time, but each correction makes the program more consistent and teaches me something that I can use in future assignments.

## AI Use

Used Grammarly to check over my spelling, format, and grammar to ensure I write a cohesive and easy to read essay. 
