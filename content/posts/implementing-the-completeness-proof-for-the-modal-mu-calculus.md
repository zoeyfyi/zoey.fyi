---
title: "Implementing the completeness proof for the modal $\\mu$-calculus"
date: 2020-04-12T22:26:50+01:00
draft: false
toc: false
images:
tags:
  - mu-calculus
  - computer science
---

## Abstract

When analysing a logic, one property of interest is its' completeness. A logic is complete iff every valid formula is provable, and by proof we mean every formula is derivable from a deductive system which comprises axioms and rules of inference. 
  
In 1983 Kozen presented $\mu$-calculus in the form we know it today and gave a complete deductive system for a restricted version. It wasn't until 1995 when Walukiewicz proved completeness for the full language with a stronger deductive system then with Kozen's original axiomatization in 2000. In this report, we present an implementation of Walukiewicz original proof procedure.

## Report

The full report can be found [here](/mu-calculus/report.pdf).

## Examples

Note, some of these images are extremely large and may not display properly within a web browser, use an image viewer such as [FEH](https://feh.finalrewind.org/).

| Formula | Tableau | Automaton | Unwinding | Assignment |
| ------- | :-----: | :-------: | :-------: | :--------: |
| $\mu X_0. (p_0 \land \neg p_0) \lor \langle a_0 \rangle X_0$ | [view](/mu-calculus/example-0-tableau.png) | [view](/mu-calculus/example-0-automaton.png) | [view](/mu-calculus/example-0-unwinding.png) | [view](/mu-calculus/example-0-assignment.png) | 
| $\mu X_0. (p_1) \land (\langle a_0 \rangle ((\langle a1 \rangle (((X_0) \lor (X_0)) \lor (p_0))) \land (\langle a_0 \rangle (X_0))))$ | [view](/mu-calculus/example-1-tableau.png) | [view](/mu-calculus/example-1-automaton.png) | [view](/mu-calculus/example-1-unwinding.png) | [view](/mu-calculus/example-1-assignment.png) |
| $\nu X_0. \mu X_1. \nu X_2. \nu X_3. (\langle a1 \rangle (\langle a_1 \rangle (X_1))) \land ((\langle a1 \rangle([a_1] (((p_1) \langle ((p_1) \lor ((X_1) \lor (X_2)))) \land (p_0)))) \lor ((\langle a0 \rangle (X_0)) \land ((p_1) \land (\langle a0 \rangle(X_3)))))$ | [view](/mu-calculus/example-2-tableau.png) | [view](/mu-calculus/example-2-automaton.png) | [view](/mu-calculus/example-2-unwinding.png) | [view](/mu-calculus/example-2-assignment.png) |
| $\mu X_0. \mu X_1. \nu X_2. \langle a_0 \rangle(([a_1] (((X_1) \land (X_0)) \land (X_1))) \land (([a_1] (X_2)) \land (\langle a_1 \rangle(X_0))))$ | [view](/mu-calculus/example-3-tableau.png) | [view](/mu-calculus/example-3-automaton.png) | [view](/mu-calculus/example-3-unwinding.png) | [view](/mu-calculus/example-3-assignment.png) |
