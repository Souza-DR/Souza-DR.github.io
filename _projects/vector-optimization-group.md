---
layout: page
title: Vector Optimization Group
description: An open source Julia initiative for vector and multiobjective optimization.
img: assets/img/KW2image.jpg
importance: 1
category: work
featured: true
search: true
---

<div class="row align-items-start">
   <div class="col-md-6 mb-3">
    {% include figure.liquid loading="eager" path="assets/img/KW2image.jpg" alt="Illustration of an objective space for a multiobjective optimization problem KW2" caption="Illustration of an objective space for a multiobjective optimization problem KW2." class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-md-6">
    <p>
      The <a href="https://github.com/VectorOptimizationGroup"><strong>Vector Optimization Group</strong></a> is an early-stage GitHub organization dedicated to open source Julia software for vector and multiobjective optimization. It provides a space for hosting packages, organizing code, and, over time, attracting contributions from colleagues interested in developing Julia tools for multiobjective optimization.
    </p>
  </div>
</div>

## Motivation

Several mature tools for multiobjective optimization are available in languages such as Python and MATLAB. The corresponding Julia ecosystem is still more limited. The Vector Optimization Group was created as an attempt to help fill this gap while supporting the gradual development of reusable and openly available software.

The first idea was to integrate vector optimization problems into established Julia ecosystems such as [JuliaSmoothOptimizers](https://github.com/JuliaSmoothOptimizers) or [JuMP](https://jump.dev/). In particular, general collections such as [OptimizationProblems.jl](https://github.com/JuliaSmoothOptimizers/OptimizationProblems.jl) seemed like natural candidates for hosting multiobjective test problems. However, their current infrastructure relies heavily on the [NLPModels.jl](https://github.com/JuliaSmoothOptimizers/NLPModels.jl) API, which is designed for scalar optimization problems and does not directly support multiple objectives. This limitation motivated a separate structure for organizing problems, solvers, and evaluation metrics for multiobjective optimization.

JuMP deserves separate consideration. Its ecosystem already provides a well-designed structure for multiobjective models and solvers. In particular, [MultiObjectiveAlgorithms.jl](https://github.com/jump-dev/MultiObjectiveAlgorithms.jl) implements several algorithms for multiobjective optimization, together with support for multiple solutions and related information such as ideal points. These methods are valuable, but they generally follow techniques that are different from the direct vector-optimization methods considered in this project. JuMP's support has also continued to evolve: although practical support for nonlinear multiobjective models has historically been more limited than support for linear models, the current MathOptInterface documentation includes a [`VectorNonlinearFunction`](https://jump.dev/JuMP.jl/stable/moi/reference/standard_form/#MathOptInterface.VectorNonlinearFunction) representation. The applicability of each solver still depends on the problem class and algorithm. Given this current support, one of the next objectives of the Vector Optimization Group is to express selected multiobjective problems using the JuMP/MathOptInterface structure and develop a compatibility interface for the group's packages. In the longer term, the goal is to support interfaces compatible with both the JuMP/MathOptInterface ecosystem and the JuliaSmoothOptimizers/NLPModels ecosystem.

## Packages

The organization currently hosts three main packages:

- [**MOProblems.jl**](https://github.com/VectorOptimizationGroup/MOProblems.jl): a collection of multiobjective optimization test problems.
- [**MOSolvers.jl**](https://github.com/VectorOptimizationGroup/MOSolvers.jl): methods and solvers for multiobjective optimization.
- [**MOMetrics.jl**](https://github.com/VectorOptimizationGroup/MOMetrics.jl): evaluation metrics for multiobjective optimization.

MOProblems.jl and MOSolvers.jl already have functional public versions. MOMetrics.jl is still private while under development. Some relevant metrics and related information are already available in the JuMP ecosystem; MOMetrics.jl is intended to complement this existing work with metrics useful for the problems and methods developed by the Vector Optimization Group.

## Current Stage

This initiative is naturally connected to my research background, since my PhD focused on multiobjective optimization. It is also an opportunity to deepen my experience with Julia, package development, documentation, testing, and open source collaboration. Julia is a modern open source language with competitive performance and expressive syntax, but several scientific areas would still benefit from a broader contributor base.

The project remains at an early stage. The code was initially developed in a concentrated way, leaving room for refactoring, improved documentation, internal reorganization, and API maturation. The long-term goal is to strengthen the packages, encourage external contributions, and possibly create a dedicated website for the Vector Optimization Group.
