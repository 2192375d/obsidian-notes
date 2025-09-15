---
title: piecewise polynomial interpolation
created: Saturday 30th August 2025 17:26
last_modified: Saturday 30th August 2025 17:25
aliases: []
tags:
  - math/application/interpolation
course: CSCC37
---
# piecewise polynomial interpolation
Compared to other interpolation technique, piecewise polynomial interpolation has the advantage of fitting lots of points using a bunch of low degree polynomials, and con of losing smoothness of the points.

__Piecewise polynomial interpolation__ is done through using a polynomial for each subinterval $[t_{i},t_{i+1}]$. For this reason, every $t_{i}$ are called __knots__, __breakpoints__, or __control points__

The simplest example is piecewise linear interpolation, using a bunch of straight lines.

