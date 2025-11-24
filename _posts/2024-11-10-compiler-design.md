---
title: Mini-C Compiler Implementation
date: 2024-11-10 14:30:00 -0600
categories: [Portfolio, Education]
tags: [school project, c++, compilers, llvm]
---

## Project Description

For my Advanced Compilers course, I designed and implemented a fully functional compiler for a subset of the C language, dubbed "Mini-C". The compiler translates source code into LLVM Intermediate Representation (IR).

## Features

1.  **Lexical Analysis**: Implemented a scanner using Flex to tokenize the input source code.
2.  **Parsing**: Built a recursive descent parser to generate an Abstract Syntax Tree (AST) based on the language grammar.
3.  **Semantic Analysis**: Implemented type checking and scope resolution to ensure code validity.
4.  **Code Generation**: Utilized the LLVM C++ API to generate optimized IR code.

## Code Snippet

Here is a snippet of the AST node traversal for generating IR:

```cpp
Value* BinaryExprAST::codegen() {
    Value* L = LHS->codegen();
    Value* R = RHS->codegen();
    if (!L || !R) return nullptr;

    switch (Op) {
    case '+': return Builder->CreateFAdd(L, R, "addtmp");
    case '-': return Builder->CreateFSub(L, R, "subtmp");
    case '*': return Builder->CreateFMul(L, R, "multmp");
    case '<':
        L = Builder->CreateFCmpULT(L, R, "cmptmp");
        return Builder->CreateUIToFP(L, Type::getDoubleTy(TheContext), "booltmp");
    default:
        return LogErrorV("invalid binary operator");
    }
}
```

## Learnings

This project provided deep insights into how high-level constructs map to low-level machine instructions. Understanding the LLVM infrastructure was particularly valuable for grasping modern compiler optimization techniques.
