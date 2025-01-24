# Lua Nested Table Iteration Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables.  The `pairs` function does not guarantee any particular iteration order, which can lead to unexpected behavior in code that relies on a specific order.

## The Problem

The `bug.lua` file contains a function `foo` that recursively iterates over a nested table using `pairs`.  However, the order of iteration might not be consistent across different Lua implementations or even different runs of the same program.

## The Solution

The `bugSolution.lua` file provides a solution that addresses this issue by using an alternative approach. In this case, the solution uses a sorted list of keys to guarantee a consistent order in nested table traversal. This ensures that the operations on the nested table occur in the desired order regardless of the implementation. However, keep in mind that other solutions might be preferred depending on the specific requirements of your application.