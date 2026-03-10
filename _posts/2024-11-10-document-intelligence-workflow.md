---
title: Docuemnt Intelligence Workflow
date: 2024-11-10 14:30:00 -0600
categories: [Portfolio, Education]
tags: [school project, c++, compilers, llvm]
---

## Project Description

Build and design an AI enabled workflow capable of ingesting verbose read outs of Key Performance Idicator (KPI), distiling into key take aways and action items, injecting into PowerPoint, and finally socializing to interested parties acorss the organization. 

## Key Responsibilities

*   **API Design & Implemetation**:
*   **Agent Design & Implementation**:
*   **Data Curation & Ingestion**:
*   **CI/CD Pipeline**: Implemented a robust CI/CD pipeline using GitHub Actions and AWS CodePipeline to automate testing and deployment.

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
