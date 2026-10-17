---
layout: post
published: true
title: Reusable Julia packages for multiobjective problems and line searches
date: 2026-10-17
description: Registering MultiObjectiveProblems.jl and extracting MultiObjectiveLineSearches.jl from research code.
tags: julia multiobjective-optimization scientific-software
categories: research
related_posts: false
---

Two recent developments in my work with the [Vector Optimization Group]({% link _projects/vector-optimization-group.md %}) make our Julia tools for multiobjective optimization easier to access and reuse: the registration of MultiObjectiveProblems.jl and the release of MultiObjectiveLineSearches.jl as an independent package.

## Benchmark problems available through General

[MultiObjectiveProblems.jl](https://github.com/VectorOptimizationGroup/MultiObjectiveProblems.jl), previously named MOProblems.jl, is now registered in Julia's General registry. Users can install it directly by name:

```julia
import Pkg
Pkg.add("MultiObjectiveProblems")
```

The package collects benchmark problems for multiobjective optimization behind a consistent evaluation API. It includes analytical derivatives for supported problems and catalog queries based on problem metadata. Its [documentation](https://vectoroptimizationgroup.github.io/MultiObjectiveProblems.jl/stable/) brings together usage examples, mathematical formulations, API details, and references.

For my research, this provides a common foundation for organizing numerical experiments and comparing methods on documented test problems.

## From solver code to a line-search package

The starting point for [MultiObjectiveLineSearches.jl](https://github.com/VectorOptimizationGroup/MultiObjectiveLineSearches.jl) was an existing line-search implementation in [MOSolvers.jl](https://github.com/VectorOptimizationGroup/MOSolvers.jl). I refactored that implementation into a separate package and developed dedicated documentation, with assistance from Claude Code and coding agents.

The motivation was to make this numerical component reusable across solver implementations. A line search takes a point and a search direction and seeks an acceptable step size. The currently available method, `BackTracking`, applies an Armijo-type sufficient decrease condition to all objectives and uses safeguarded quadratic interpolation.

The package is public but is not yet registered in General. Installation currently uses its GitHub URL:

```julia
import Pkg
Pkg.add(url = "https://github.com/VectorOptimizationGroup/MultiObjectiveLineSearches.jl")
```

The [documentation](https://vectoroptimizationgroup.github.io/MultiObjectiveLineSearches.jl/dev/) covers installation, usage, mathematical formulations with literature references, and the API.

## Building reusable research software

These packages address complementary parts of a numerical experiment: MultiObjectiveProblems.jl supplies benchmark problems, MultiObjectiveLineSearches.jl supplies step-size searches, and MOSolvers.jl provides optimization methods. Separating these responsibilities makes it possible to reuse and develop each component independently.

The use of AI coding tools was part of the refactoring and documentation process. The mathematical methods and the existing implementation supplied the starting point; the work focused on organizing that implementation as a package and documenting its interface and mathematical context.
