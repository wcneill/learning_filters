# Multi-Target Tracking Self-Study Syllabus

## Goal

Develop the knowledge and intuition necessary to design, implement,
evaluate, and deploy a multi-target tracking system. The
emphasis is on understanding *why* algorithms work, not just
implementing them.

------------------------------------------------------------------------

# Phase 1 --- Single-Target Estimation (2--3 weeks)

**Goal:** Become completely fluent with Bayesian filtering.

### Topics

-   Bayesian filtering
-   Kalman filter
-   Process models
-   Measurement models
-   Covariance propagation
-   Innovation
-   Validation gating
-   Filter consistency (NIS / NEES)

### Deliverable

-   A Kalman filter library that you trust.
-   Ability to derive and tune process and measurement models.

------------------------------------------------------------------------

# Phase 2 --- Detection & Statistical Decision Theory (3--4 weeks)

**Fundamental Question**

> Is this measurement real?

### Topics

-   Probability density functions
-   Likelihood
-   Maximum likelihood estimation
-   Maximum a posteriori (MAP)
-   Hypothesis testing
-   Neyman--Pearson detection
-   Detection probability (Pd)
-   False alarm probability (Pfa)
-   ROC curves

### Deliverable

Understand how detections are produced and thresholded.

------------------------------------------------------------------------

# Phase 3 --- Clutter & Point Processes (2--3 weeks)

**Fundamental Question**

> What do false alarms look like statistically?

### Topics

-   Poisson processes
-   Spatial Poisson processes
-   Clutter density
-   Birth models
-   Death models
-   Missed detections

### Deliverable

A realistic sensor simulator capable of generating clutter and missed
detections.

------------------------------------------------------------------------

# Phase 4 --- Data Association (6--8 weeks)

**Fundamental Question**

> Which measurement belongs to which target?

### Topics

-   Validation gates
-   Mahalanobis distance
-   Nearest Neighbor (NN)
-   Global Nearest Neighbor (GNN)
-   Cost matrices
-   Assignment problems
-   Hungarian algorithm
-   Murty's algorithm (optional)

### Deliverable

A multi-target tracker using deterministic data association.

------------------------------------------------------------------------

# Phase 5 --- Track Management (4--6 weeks)

**Fundamental Question**

> When should a track begin or end?

### Topics

-   Track initiation
-   Tentative tracks
-   Confirmation logic
-   Track deletion
-   Coasting
-   Missed detections
-   Track quality metrics

### Deliverable

A tracker that can operate indefinitely without manual intervention.

------------------------------------------------------------------------

# Phase 6 --- Simulation & Evaluation (4--6 weeks)

**Fundamental Question**

> Does the tracker actually work?

### Topics

-   Ground-truth generation
-   Crossing targets
-   Closely spaced targets
-   Maneuvering targets
-   Clutter generation

### Performance Metrics

-   Track continuity
-   Track purity
-   False tracks
-   ID switches
-   Track latency

### Deliverable

A repeatable benchmarking framework for comparing tracking algorithms.

------------------------------------------------------------------------

# Phase 7 --- Joint Probabilistic Data Association (JPDA) (4--6 weeks)

Study this only after identifying limitations of nearest-neighbor
association.

**Fundamental Question**

> What if several associations are plausible?

### Topics

-   Association probabilities
-   Marginalization
-   Soft assignment
-   Expected innovations

### Deliverable

Compare JPDA against the baseline tracker.

------------------------------------------------------------------------

# Phase 8 --- Multiple Hypothesis Tracking (MHT) (6--10 weeks)

**Fundamental Question**

> What if multiple explanations should be preserved simultaneously?

### Topics

-   Hypothesis trees
-   Hypothesis scoring
-   N-scan pruning
-   Murty's algorithm
-   Computational complexity

### Deliverable

Compare MHT against JPDA using the same benchmark scenarios.

------------------------------------------------------------------------

# Phase 9 --- Random Finite Sets (Optional)

Study only if product requirements justify the additional complexity.

### Topics

-   Finite Set Statistics (FISST)
-   Random Finite Sets
-   PHD filter
-   CPHD filter
-   Multi-Bernoulli filters
-   Labeled Multi-Bernoulli (LMB)
-   Generalized Labeled Multi-Bernoulli (GLMB)

### Deliverable

Determine whether an RFS-based tracker provides meaningful performance
improvements for your application.

------------------------------------------------------------------------

# Continuous Study

Continue strengthening:

-   Linear algebra
-   Probability
-   Bayesian inference
-   Numerical optimization
-   Scientific computing
-   Monte Carlo simulation

These subjects support every stage of multi-target tracking.

------------------------------------------------------------------------

# Recommended Implementation Milestones

1.  Single-target Kalman filter ✓
2.  Multiple independent tracks
3.  Nearest-neighbor association
4.  Global nearest-neighbor association
5.  Robust track management
6.  Simulation and evaluation framework
7.  JPDA prototype
8.  MHT prototype
9.  Select the simplest algorithm that satisfies the product
    requirements

------------------------------------------------------------------------

# Guiding Philosophy

Do **not** aim to implement the most sophisticated tracker first.

Instead:

1.  Build the simplest tracker that works.
2.  Measure its performance objectively.
3.  Identify where it fails.
4.  Introduce more sophisticated algorithms only when they solve an
    observed problem.

This approach minimizes technical risk while producing useful software
throughout the project.
