---
draft: true
title: LLVM Intermediate Representation
summary: A low-level, platform-independent code representation used by the LLVM compiler framework for compilation across multiple architectures.
date: 2024-11-22
featureimage: careers-feature.jpg
caption: "Image caption :tada:"
authors:
  - ComputeDraft: author.jpeg
---


```ir
; This is a sample program in LLVM IR

@global_var = global i32 0


define i32 @main(i1 %cond) {

  br i1 %cond, label %then_block, label %else_block

  then_block:
      %x1 = add i32 0, 10
      br label %merge_block
  
  else_block:
      %x2 = add i32 0, 20
      br label %merge_block
  
  merge_block:
      %x = phi i32 [ %x1, %then_block ], [ %x2, %else_block ]
      %y = add i32 %x, 5
      ret i32 0
}
```