# Research Log – [Project name]

## Meta
- Field: Differential Geometry, Geometric Analysis
- Start date: 23/12/2025
- Current status: Wiri
- Target output: (preprint / note / dead-end / discard)

---

## Entry 2025-12-23

### Question / Goal
I'm trying to prove some diffeomorphic problem. 

### Context
- Related papers: John M. Lee's exercise

### Attempt
So i tried to show that the level set x^4 + y^2 + z^2 = 1 (viewed as the level set Phi^-1(0,1) )is diffeomorphic with S^2. And i wish that the sphere projection will be effective for bijection and smooth's proof (i will call this function is F).
However, this approach seems stuck at the step proving its inverse is smooth beacause it is quite brute forcing to prove some ugly double square root functions is smooth. So Lee suggested me to prove that it has constant rank after proving it is bijective by pointing out its inverse function (Mr Ly Kim Ha proved bijective <=> exists inverse). 

To prove it has constant rank, i compute its jacobian and realize it has rank 3 ''almost everywhere'' (its just some speaking phrases, not from measure theory), but the dimension of domain and codomain require me just 2. And it's really voluminous to point out that the following Jacobian has rank >= 2 or find its kernel by solve useless system of equations (because i really hate matrices in Linear Algebra). There is a more geometric way to do this. First, i realize the kernel of the Jacobian is actually the tangent vectors on the level set that disappear after differentiating, moreover, these vectors seems does not belong to the tangent space of "T_p level set" but from T_p ambient space" containing "T_p level set". Then the constant rank claim is transfered to prove that  "T_p level set" and kernel of F does not intersect. Moreover, i remember that i can compute dFp through a curve that i just need to take derivative of one variable (which is easy) rather than through Jacobian, which is quite stupid that i have just got stuck. 

After some calculation, i obtain a result that is quite nice: the kernel tangent vector must be parallel to its point (viewed as a vector). The task now is just showing something not real. This step is simple, i define the following level set as the level set of the other function G: R^4 -> R, G(x,y,z) = x^4 + y^2 + z^2 - 1 (of couse the level set now is G^-1(0) instead of Phi^-1(0,1)). Its Jacobian is nice, and the regular level set theorem (or something similarly) show that dGp(v) must be zero. But i calculated something like k(4x^4 + 2s^2 + 2t^2) = 0, which only occurs when k = 0 or the kernel vector is just zero. So now we are done.


### Insight
- Reason stuck: brute-force Jacobian hides geometry
- Kernel of dF must be radial; radial vectors cannot lie in T_p M.
- Direct Jacobian rank computation is inefficient.

## Entry 2025-12-24

### Question / Goal
Not embedded submanifolds problem

### Context
- Related papers: Problem 5.7.

### Attempt
So this is a really tiring problem. The hardest part lies in the case F^{-1}(0). My first approach is trying to prove the level set R: x^3 + xy + y^3 = 0 is a connected topological manifold to use Classification theorem. However, i realize R is not actually a manifold while its only singularity messed everything up, moreover, just from a pure equation, how to prove it is connected by the way? Polar coordinate save us all. 

Changing the coordinate, then this abtract set become a not very simple curve. The target is to prove that i can seperate the set into 3 connected parts after removing the origin. It's quite disturbing because the radius jumps from positive to negative sometimes, and trigonometry formula does not allow me to control it easily. But it's okay. I could finally handle it (spend one night for it). Just split the graph of R^2 into 6 parts, removing 3 parts that make the radius negative (it is just a symmetry with angle pi anyway). Then with those three remaining parts, it gave me what i needed, each one contain only one single curve. Then by using the k-slice conditon (from embedding) i can point out the contradiction easily. The case for c = 1/27 is simple.

### Insight
- Classification is quite unreliable useless for some non-manifold or almost manifold structure. It is better used for global problem.
- Polar coordinate is still good for parametrization. But the price is a quite huge cognitive load for trigonometry (but still worth it).
- Don't trust any topology-only-one-line solution until solving it by yourself (by analysis or something you good at).
