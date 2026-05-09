---
layout: page
permalink: /talks/
title: talks
description: Talks, seminars, posters, and conference presentations.
nav: true
nav_order: 6
---

<!-- _pages/talks.md -->

<div class="publications">
  <h2 class="bibliography">2025</h2>

  <ol class="bibliography">
    <li>
      <div class="row">
        <div class="col-sm-3 col-md-2 mb-3 mb-sm-0">
          <a href="{{ '/assets/img/talks/JmatUFPI2025.jpg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/img/talks/JmatUFPI2025.jpg' | relative_url }}" alt="Group photo taken after the thematic session on optimization" class="img-fluid rounded z-depth-1" width="120">
          </a>
        </div>

        <div class="col-sm-9 col-md-10">
          <div class="title">Multiobjective Optimization Strategies: A Comparative Analysis Focused on Direct Vector Methods</div>

          <div class="author">
            13th UFPI Mathematics Conference
          </div>

          <div class="periodical">
            Piauí, Brazil, September 24, 2025.
          </div>

          <div class="links">
            <a href="https://www.overleaf.com/read/spptgvmvstgb#566438" class="btn btn-sm z-depth-0" role="button">Slides</a>
            <a class="abstract btn btn-sm z-depth-0" role="button">ABS</a>
          </div>

          <div class="abstract hidden">
            <p>Multiobjective optimization addresses complex problems in which multiple, often conflicting objectives must be considered simultaneously, and the main challenge is to find solutions that represent the best trade-off among them. This talk presents an overview of the main strategies for tackling such problems, organized into three distinct approaches.</p>
            <p>We discuss Scalarization Methods, which transform multiobjective problems into single-objective problems using techniques such as weighted sums, highlighting both their simplicity and the limitation of typically producing only one solution per run.</p>
            <p>In contrast, we explore Full-Front Approximation Methods, which aim to generate a set of trade-off solutions, or a Pareto front, often using evolutionary and genetic algorithms to provide a global view of possible optimal solutions in a single run.</p>
            <p>Finally, the main focus is on Direct Vector Optimization Methods, where the problem is handled directly in vector form, without the need for scalarization or population-based strategies. We present concepts such as the generalization of the gradient to a vector of objectives and the determination of descent directions that optimize simultaneously or identify the best local compromise, with examples including the Multiobjective Gradient Method and the Multiobjective Newton Method.</p>
          </div>
        </div>
      </div>
    </li>

    <li>
      <div class="row">
        <div class="col-sm-3 col-md-2 mb-3 mb-sm-0">
          <a href="https://www.ruder.io/optimizing-gradient-descent/#visualizationofalgorithms" target="_blank" rel="noopener">
            <img src="{{ '/assets/img/talks/contours_evaluation_optimizers.gif' | relative_url }}" alt="Contour plot comparing stochastic optimization methods" class="img-fluid rounded z-depth-1" width="120">
          </a>
        </div>

        <div class="col-sm-9 col-md-10">
          <div class="title">Stochastic Optimization Methods</div>

          <div class="author">
            Continuous Optimization Seminar - IMECC/UNICAMP
          </div>

          <div class="periodical">
            Campinas, Brazil, April 14, 2025.
          </div>

          <div class="links">
            <a href="https://www.overleaf.com/read/srrnsynybcmj#7dbfb3" class="btn btn-sm z-depth-0" role="button">Slides</a>
            <a class="abstract btn btn-sm z-depth-0" role="button">ABS</a>
          </div>

          <div class="abstract hidden">
            <p>We will address the fundamentals and recent advances in stochastic optimization methods, essential techniques for large-scale problems. Starting from basic Stochastic Gradient Descent (SGD), we will explore its advanced variants such as Momentum, Nesterov Accelerated Gradient, and adaptive methods (Adagrad, RMSProp, and Adam). We will discuss efficient strategies for mini-batch selection and provide practical guidelines for implementation and choosing the appropriate method for different applications.</p>
          </div>
        </div>
      </div>
    </li>
  </ol>

  <h2 class="bibliography">2023</h2>

  <ol class="bibliography">
    <li>
      <div class="row">
        <div class="col-sm-3 col-md-2 mb-3 mb-sm-0">
          <a href="{{ '/assets/img/talks/voronoi-1.jpg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/img/talks/voronoi-1.jpg' | relative_url }}" alt="Voronoi diagram used in an electrical impedance tomography reconstruction" class="img-fluid rounded z-depth-1" width="120">
          </a>
        </div>

        <div class="col-sm-9 col-md-10">
          <div class="title">Reconstruction of Voronoi Diagrams in Electrical Impedance Tomography</div>

          <div class="author">
            1st USP Postdoctoral Congress
          </div>

          <div class="periodical">
            São Paulo, Brazil, October 17, 2023.
          </div>

          <div class="links">
            <a href="https://drive.google.com/file/d/1ROyoOJb6kYS6QKzCMx0Ohb1JutW2yEM_/view?usp=sharing" class="btn btn-sm z-depth-0" role="button">Poster</a>
            <a class="abstract btn btn-sm z-depth-0" role="button">ABS</a>
            <a href="http://www.congressoposdocsusp.kinghost.net/sites/default/files/anexos-pagina/Congresso%20P%C3%B3s-Docs%20USP%202023_v2-Da%20Matriz%20Energ%C3%A9tica%20%C3%A0%20Ind%C3%BAstria%20Sustent%C3%A1vel.pdf" class="btn btn-sm z-depth-0" role="button">Book of Abstracts</a>
          </div>

          <div class="abstract hidden">
            <p>The inverse problem of electrical impedance tomography (EIT), also known as the inverse conductivity or Calderón’s problem, is an active field of research with an extensive literature; see for a thorough review of the topic. The goal of electrical impedance tomography is to reconstruct the electrical conductivity inside a medium, using measurements of the electrical potential on the boundary obtained by applying boundary currents. EIT is a low cost, noninvasive, radiation free and portable imaging modality with various applications in medical imaging, geophysics, civil engineering and nondestructive testing. In the EIT literature, the conductivity is often supposed to be a relatively smooth, continuous function. However, the case where the conductivity presents discontinuities is important for applications, in particular in geophysics and civil engineering, but also in medicine. In this project we consider the particular case where the conductivity is a piecewise constant function. The domain of definition of the conductivity can then be partitioned into cells such that the conductivity is constant in each cell. In this work we also suppose that the set of cells is given by a Voronoi diagram.</p>
          </div>
        </div>
      </div>
    </li>

    <li>
      <div class="row">
        <div class="col-sm-3 col-md-2 mb-3 mb-sm-0">
          <a href="{{ '/assets/img/talks/34CBM2023.jpg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/img/talks/34CBM2023.jpg' | relative_url }}" alt="Talk presentation at the 34th Brazilian Mathematics Colloquium" class="img-fluid rounded z-depth-1" width="120">
          </a>
        </div>

        <div class="col-sm-9 col-md-10">
          <div class="title">A Quasi-Newton Method with Wolfe Line Searches for Multiobjective Optimization</div>

          <div class="author">
            34th Brazilian Mathematics Colloquium (IMPA)
          </div>

          <div class="periodical">
            Rio de Janeiro, Brazil, July 24, 2023.
          </div>

          <div class="links">
            <a href="https://drive.google.com/file/d/1oLFNIlHDM9YcmAnSRpZbey1uEXCH28U5/view?usp=sharing" class="btn btn-sm z-depth-0" role="button">Slides</a>
            <a class="abstract btn btn-sm z-depth-0" role="button">ABS</a>
          </div>

          <div class="abstract hidden">
            <p>We propose a BFGS method with Wolfe line searches for unconstrained multiobjective optimization problems. The algorithm is well defined even for general nonconvex problems. Global convergence and R-linear convergence to a Pareto optimal point are established for strongly convex problems. In the local convergence analysis, if the objective functions are locally strongly convex with Lipschitz continuous Hessians, the rate of convergence is Q-superlinear. In this respect, our method exactly mimics the classical BFGS method for single-criterion optimization.</p>
          </div>
        </div>
      </div>
    </li>
  </ol>

  <h2 class="bibliography">2022</h2>

  <ol class="bibliography">
    <li>
      <div class="row">
        <div class="col-sm-3 col-md-2 mb-3 mb-sm-0">
          <a href="{{ '/assets/img/talks/IVCBJME2022.jpg' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/img/talks/IVCBJME2022.jpg' | relative_url }}" alt="Talk presentation at the 4th Brazilian Congress of Young Researchers in Mathematics" class="img-fluid rounded z-depth-1" width="120">
          </a>
        </div>

        <div class="col-sm-9 col-md-10">
          <div class="title">A Quasi-Newton Method with Wolfe Line Searches for Multiobjective Optimization</div>

          <div class="author">
            4th Brazilian Congress of Young Researchers in Mathematics (IV CBJME, UFPB)
          </div>

          <div class="periodical">
            João Pessoa, Brazil, October 6, 2022.
          </div>

          <div class="links">
            <a href="https://drive.google.com/file/d/1IdWPYeTfiUWiE1TQnfsMoqHeEd830-UG/view?usp=sharing" class="btn btn-sm z-depth-0" role="button">Slides</a>
            <a class="abstract btn btn-sm z-depth-0" role="button">ABS</a>
          </div>

          <div class="abstract hidden">
            <p>We propose a BFGS method with Wolfe line searches for unconstrained multiobjective optimization problems. The algorithm is well defined even for general nonconvex problems. Global and R-linear convergence to a Pareto optimal point are established for strongly convex problems. In the local convergence analysis, if the objective functions are locally strongly convex with Lipschitz continuous Hessians, the rate of convergence is Q-superlinear. In this respect, our method exactly mimics the classical BFGS method for single-criterion optimization.</p>
          </div>
        </div>
      </div>
    </li>
  </ol>

  <h2 class="bibliography">2021</h2>

  <ol class="bibliography">
    <li>
      <div class="row">
        <div class="col-sm-3 col-md-2 mb-3 mb-sm-0">
          <a href="{{ '/assets/img/talks/3-BFGS.png' | relative_url }}" target="_blank" rel="noopener">
            <img src="{{ '/assets/img/talks/3-BFGS.png' | relative_url }}" alt="Illustration of Wolfe line search conditions for multiobjective optimization" class="img-fluid rounded z-depth-1" width="120">
          </a>
        </div>

        <div class="col-sm-9 col-md-10">
          <div class="title">A Quasi-Newton Method with Wolfe Line Search for Multiobjective Optimization</div>

          <div class="author">
            29th IME/UFG Week and 6th IME/UFG Research and Graduate Seminar
          </div>

          <div class="periodical">
            Goiânia, Brazil, October 8, 2021.
          </div>

          <div class="links">
            <a href="https://drive.google.com/file/d/1owzBlIHVX5jVOOtaDkTGK7LCfckjvtsb/view?usp=sharing" class="btn btn-sm z-depth-0" role="button">Slides</a>
            <a class="abstract btn btn-sm z-depth-0" role="button">ABS</a>
            <a href="https://drive.google.com/file/d/1tZLgyPJkL9QiYkJ0SFctSpl0ZGh6YrQ2/view?usp=sharing" class="btn btn-sm z-depth-0" role="button">Proceedings</a>
          </div>

          <div class="abstract hidden">
            <p>We propose a BFGS method with Wolfe line search for unconstrained multiobjective optimization problems. The algorithm is well-defined even for general nonconvex problems. Global and R-linear convergence to a Pareto optimal point are established for strongly convex problems. In the local convergence analysis, if the objective functions are locally strongly convex with Lipschitz-continuous Hessians, then the convergence rate is Q-superlinear. In this sense, our method exactly reproduces the behavior of the classical BFGS method for scalar optimization.</p>
          </div>
        </div>
      </div>
    </li>
  </ol>
</div>
