# GLV-Endomorphism
GLV Multiplication for BLS curves on G1 using Endomorphism

# Optimization of BLS Elliptic Curve Scalar multiplication on G1

This repository provides an implementation of BLS pairings-friendly elliptic curve computations on G1. We have encapsulated all related elliptic curve (EC) functions within a Python class, including:

- Generating random points on the curve.
- Generating random torsion points on the curve.
- Points addition and multiplication with a scalar.
- Hashing to G1, implemented securely using the Simplified Shallue-van de Woestijne-Ulas Method (Simplified SWU for AB == 0).

## Goal

The primary goal of this code is to demonstrate a proposed GLV points multiplication for torsion points on G1. Three different approaches are implemented:

1. **Standard Lookup Table Scheme:** Utilizing a standard lookup table computation scheme with a proposed recording scheme to handle both recording and sign alignment in a one secure implementation.

2. **Endomorphisms Acceleration:** Proposing an acceleration of the lookup table computation using endomorphisms on G1. Half of the points in the table are computed explicitly (using point addition) while the others are inferred using endomorphism.

3. **Space-optimized Version:** A space-optimized version of the second approach, where the lookup table is halved, and only 16 points are truly generated (as opposed to 32 points in the standard approach).

We also propose a fast and efficient scheme to handle scalar decomposition and address even sub-scalars situations.

## Usage

The code implements G1 manipulation for BLS12, BLS24, and BLS48 curves. Code and demonstration are implemented as ".ipyb" files ready for Jupyter. The curve parameters are extensively described in the set located in '\libs\Parameters.py'.

Feel free to provide any comments or feedback.
