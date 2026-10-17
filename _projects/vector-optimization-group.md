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

The organization develops complementary tools for benchmark problems, line searches, solvers, and experimental evaluation.

### MultiObjectiveProblems.jl

[MultiObjectiveProblems.jl](https://github.com/VectorOptimizationGroup/MultiObjectiveProblems.jl), previously named MOProblems.jl, is a curated library of benchmark problems for multiobjective optimization. It provides a consistent evaluation API, analytical derivatives for supported problems, and metadata-based catalog queries. The package is now registered in Julia's General registry and can be installed by name:

```julia
import Pkg
Pkg.add("MultiObjectiveProblems")
```

The [documentation](https://vectoroptimizationgroup.github.io/MultiObjectiveProblems.jl/stable/) includes mathematical formulations, usage examples, an API reference, and bibliographic sources.

### MultiObjectiveLineSearches.jl

[MultiObjectiveLineSearches.jl](https://github.com/VectorOptimizationGroup/MultiObjectiveLineSearches.jl) provides reusable line searches for multiobjective optimization. Its current method, `BackTracking`, uses an Armijo-type sufficient decrease condition on all objectives, with safeguarded quadratic interpolation.

I developed this independent package by refactoring the line-search implementation previously included in MOSolvers.jl. I describe the refactoring and the use of AI coding tools in a [research update]({% link _posts/2026-10-17-julia-packages-for-multiobjective-optimization.md %}). Its [documentation](https://vectoroptimizationgroup.github.io/MultiObjectiveLineSearches.jl/dev/) covers usage, mathematical formulations, the API, and literature references.

The package is public but is not yet registered in General. It can be installed directly from GitHub:

```julia
import Pkg
Pkg.add(url = "https://github.com/VectorOptimizationGroup/MultiObjectiveLineSearches.jl")
```

### Solvers and evaluation

- [**MOSolvers.jl**](https://github.com/VectorOptimizationGroup/MOSolvers.jl): methods and solvers for multiobjective optimization. The separate line-search package makes this numerical component available for reuse beyond a single solver package.
- **MOMetrics.jl**: evaluation metrics for multiobjective optimization. It remains private while under development. Some relevant metrics and related information are already available in the JuMP ecosystem; MOMetrics.jl is intended to complement this existing work with metrics useful for the group's problems and methods.

## Current stage

This initiative is naturally connected to my research background, since my PhD focused on multiobjective optimization. It is also an opportunity to deepen my experience with Julia, package development, documentation, testing, and open source collaboration. Julia is a modern open source language with competitive performance and expressive syntax, but several scientific areas would still benefit from a broader contributor base.

The initiative is progressing from research code toward reusable scientific packages. The registration of MultiObjectiveProblems.jl and the extraction of MultiObjectiveLineSearches.jl are recent steps in this direction. Further work includes API maturation, solver integration, and broader experimental evaluation. The long-term goal is to strengthen the packages, encourage external contributions, and possibly create a dedicated website for the Vector Optimization Group.
