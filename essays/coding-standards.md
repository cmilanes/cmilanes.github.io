---
layout: essay
type: essay
title: "Professionals Have Standards"
# All dates must be YYYY-MM-DD format!
date: 2024-02-08
published: true
labels:
  - Software Engineering
  - Coding Standards 
  - ESLint
---

<img width="300px" class="img-fluid" src="../img/ESLint.png">

## No standards no problems

Throughout my undergraduate courses as a computer engineering student, I have had to write and work with a lot of different people with different opinions on how code should look for the same programming assignment. The lack of any baseline for a standard meant that this code ranged in readability and increased how difficult it was to debug. For example, someone could write C code with as minimal of indentation and spacing as possible, but it makes it extremely difficult to read. Due to everyone having a different style, it made collaboration a bit more tricky as the amount of time it would take to understand another person’s assignment would be based on how similar their styles were to mine.

## The Significance of Standards

The importance of coding standards varies based on the type of project that is being worked on. In large companies with large groups of software developers, having coding standards is vital. Without standards each developer could write and push code in their own style, causing the overall repository to become a mess, increasing the time it would take to analyze it, and increasing the overall time it takes to complete the project. On the other hand, for smaller projects like a school group project or experimental and toy programs, coding standards don’t have to be enforced as strictly. There should be a baseline standard for these projects, but it is not as imperative as in large scale development.

## ESLint - A strict rulebook

Before using ESLint, my programs were written in whatever way I felt was the most readable and made the most sense to me. Once trying ESLint, being conditioned to follow the linter’s strict rules was somewhat difficult for me because the general format is different to how I would normally write it. For example, one of the standards in ESLint that I had a hard time getting used to was the need to place spacing in between the parentheses of an argument in an if statement. I personally exclude this space, but ESLint will throw an error if it exists. Overall, I do believe that ESLint is a good tool to enforce good programming practices that lead to better, more readable code.
