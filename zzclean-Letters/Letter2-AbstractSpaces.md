# Letter no. 2: Abstract spaces

Hi!

What is a "space"? One can view this question (or maybe some more sophisticated version of it) as THE most fundamental problem of mathematics, and hence it is also a natural starting point for this correspondence course. What we would really like is to (1) understand the true geometry of our universe, unifying quantum field theory with gravity, and (2) find an ultimate "arithmetic" geometry which should explain the behaviour of zeta functions and many other things. Two examples: Here's a [paper of Louis Crane](https://arxiv.org/pdf/gr-qc/0602120.pdf) which suggests that topos theory and higher categories should play a role in quantum gravity, and a [paper of Shai Haran](https://arxiv.org/abs/1508.04636) where on page 5 he explains three of the fundamental problems related to a geometry underlying zeta functions. This paper of Shai Haran uses "generalized rings" (related to monoids) in order to build new geometrical foundations, but other authors use other tools.

My intention is that we will soon get to topos theory and much more, but today we'll cover more elementary ideas.

I imagine that in the Realm of Kan, there is a mountain known to the locals simply as "the Mountain Top" (bad pun intended) where elementary approaches to the theory of abstract spaces are located. This mountain has a squarish-shaped plateau on top and its four sides (east, north, west and south) represent the four most basic approaches to answering the question "What is a space".

## East side: Point-set topology

Def: A *topological space* is a set X together with a collection of subsets of X that contains X and the empty set, and is closed under finite intersections and arbitrary unions. The subsets in this collection are called *open* subsets. A function between two topological spaces is called *continuous* if it pulls back open sets to open sets.

There are equivalent definitions using either neighbourhoods or closed sets as a starting point.

Read more here:

https://en.wikipedia.org/wiki/Topological_space

We will write Top for the category of topological spaces and continuous functions (or "maps").

Taking the above as a definition of an "abstract space" has some advantages, notably that it is very general. By this I mean that most other definitions of "abstract space" admit a natural machine to Top. A disadvantage on the categorical level is that the category Top is not cartesian closed, i.e. there is no natural identification of Hom(X x Y, Z) with Hom(X, Z^Y). If we instead of working with Top choose the category CGHaus of compactly generated Hausdorff topological spaces, such an identification exists, and identifies not just the two Hom-sets, but the two Hom-spaces. For this to make sense, one has to be precise about how to define Hom(X, Y) and X x Y as topological spaces (this involves the so-called compact-open topology, and also a certain functor from Top to CGTop, where the latter category is the category of compactly generated spaces).

Read here for more details, and we can discuss this further if needed:

- https://en.wikipedia.org/wiki/Cartesian_closed_category
- https://en.wikipedia.org/wiki/Compactly_generated_space

We will come back to topological spaces later, in the Zophie paradigm, but let me start sketching it here.

### Zophie paradigm sketch

Type: Topological space

Given a topological space X, we can also talk about X-points and X-subsets (each of these is a dependent type with a topological space as parameter).

**Properties that a topological space may have:**

- Connected
- Totally disconnected
- Profinite
- Hausdorff
- Compact
- Sequentially compact
- Locally compact
- Compactly generated
- Metrizable
- Uniformizable
- Second-countable
- Paracompact

Remarks:
- If X is paracompact and Hausdorff, then X admits a partition of unity, a notion which is important in many settings: https://en.wikipedia.org/wiki/Partition_of_unity
- The field of p-adic numbers is an important example of a profinite (and hence also totally disconnected) topological space.
- The property "locally compact" is important for Pontryagin duality and the abstract Fourier transform: https://terrytao.wordpress.com/2009/04/06/the-fourier-transform/
- The property "second-countable" appears in the definition of a topological manifold.
- Many more properties are listed here (but note that the whole point of this letter is to indicate which notions you actually need to know about, and most of the properties in the link below are not super-important, in my opinion): https://en.wikipedia.org/wiki/Topological_property

**Relations between topological spaces**

- Homeomorphic (i.e. isomorphic)
- Homotopy equivalent

**Properties that a continuous map may have**

- Be a homotopy equivalence
- Be a weak homotopy equivalence
- Be a fibration
- Be a weak fibration (also called a Serre fibration)
- Be a cofibration

Remarks:
- More properties are inherited from general category theory. As an example, an epimorphism in Top is just a surjective morphism, but an epimorphism in the category of Hausdorff spaces is a morphism with dense image.

**Relations between X-subsets and X-points**

- To contain
- To be a neighbourhood of

I'll stop the Zophie sketch here and continue elsewhere with more details! Obviously, this is just a beginning; we haven't even started on operations, invariants, or more general machines. I just wanted to make the pattern clear in that we start with a type (topological space), from which we can build various dependent types (in this case X-points and X-subsets) and an associated "morphism type" which maybe can be viewed as a dependent type with TWO topological spaces as parameters. On these types, we have machines (properties, relations, invariants, operations, and more general machines), some of which are functorial...

## North side: Abstract opens

Back to the Mountain Top, another approach to "abstract spaces" is to take "opens" as a fundamental concept. There are two common ways of making this precise.

- The category Loc of *locales* is the dual of the category of frames, where a frame is a certain kind of lattice. Details here:

https://en.wikipedia.org/wiki/Pointless_topology

https://en.wikipedia.org/wiki/Complete_Heyting_algebra

- A *site* (or Grothendieck site) is a category equipped with a Grothendieck topology. Sites form a category Sites. Details here:

https://en.wikipedia.org/wiki/Grothendieck_topology

https://www.ams.org/notices/200409/what-is-illusie.pdf

https://stacks.math.columbia.edu/download/sites.pdf

The point here is that an "open" is not necessarily a set.

The theory of sites is fundamental for algebraic geometry, which is why I imagine this approach being on the North side of the mountain, facing the domains of algebraic geometry further north.

There is a lot to say about sites, and we will come back to them! A small comment though is that it is weird that we have a word (ringed site) for a site equipped with a sheaf of rings, but there is no word (AFAIK) for a site equipped with a sheaf of abelian groups. We really need a word for this, maybe "Abel site"???

## West side: Distance approaches

Yet another approach is the "distance approach". By far the most important definition is:

Def: A metric space is a set X together with a metric, i.e .a function d: X x X --> X that is positive, symmetric and sub-additive.

Some properties that a metric space may have (again as a first step towards a Zophie formalization):

- Complete
- Bounded
- Being ultrametric
- Any property that a topological space may have (note that there is a canonical functor from metric spaces to topological spaces, but different metrics may give the same topology on a set, and not all topologies are induced by a metric. )

Some properties that a function between metric spaces may have:

- Continuous
- Uniformly continuous
- Lipschitz-continuous
- Being a contraction
- Being an isometry

Some of the most elementary Zophie theorems would state that there are reverse implications from each of first four of these properties to the next.

There are various weaker versions of the concept "metric space", notably uniform space, approach space, and pseudo-metric space. Important examples of pseudo-metric spaces come from semi-norms on vector spaces.

More details here:
- https://en.wikipedia.org/wiki/Metric_space
- https://en.wikipedia.org/wiki/Approach_space
- https://en.wikipedia.org/wiki/Uniform_space
- https://en.wikipedia.org/wiki/Pseudometric_space

The famous Math 55 first-year course at Harvard ("the most difficult undergraduate course in America") covers metric spaces as one of the main topics. It might be interesting to look at some course notes and problem sets from this course, just to get a feel for the level.

http://www.math.harvard.edu/~elkies/M55b.16/index.html

https://www.quora.com/Where-can-I-find-problems-notes-and-lectures-of-Math-55-and-Statistics-class

http://web.evanchen.cc/notes/Harvard-55a.pdf

http://web.evanchen.cc/notes/Harvard-55b.pdf



## South side: Combinatorial approaches

Finally, (facing south, towards the fabled Island of Combinatorics) there are *combinatorial* approaches to the notion of an abstract space.

The most important combinatorial definitions are:

- CW complex (also called a cell complex)
- Simplicial set

Other important notions include:

- Simplicial complex
- Delta-complex (used in the book of Hatcher)
- Abstract simplicial complex
- Delta-set (also called a semi-simplicial set)
- Cubical sets, dendroidal sets, and various other cousins of simplicial sets

Links for more details:

- https://en.wikipedia.org/wiki/Simplicial_complex
- https://en.wikipedia.org/wiki/Abstract_simplicial_complex
- The book of Hatcher defines CW complexes (pp. 5 and the first appendix from p. 519) and Delta-complexes (pp. 102)
- https://en.wikipedia.org/wiki/Delta_set
- https://en.wikipedia.org/wiki/Simplicial_set
- https://arxiv.org/abs/1703.07098
- https://mathoverflow.net/questions/11045/are-non-empty-finite-sets-a-grothendieck-test-category

Note in particular that for any test category T (in the sense of Grothendieck) we have the category of T-sets, and a T-set is a dependent type with a test category as parameter.

# Wrapping up

As far as I know, these are all the basic key notions of "abstract space" that you need to know about. Of course there is a LOT more to say about each of the individual notions, and we haven't even started talking about manifolds, schemes, or non-commutative spaces, but we have started a kind of crash course on geometrical structures.

For now, before we finish, just a recap of the eight most important definitions:
- East side: Topological spaces (Top) and Compactly Generated Hausdorff spaces (CGHaus).
- North side: Locales and Sites.
- West side: Metric spaces and Pseudometric spaces.
- South side: CW complexes and Simplicial sets  

My hope now is that based on reading this letter, you will read and digest some of the formal definitions already today, but if you don't have the time or motivation to learn what a CW complex is right away, at least we can now talk freely about CW complexes, and when you have seen them pop up a few times in interesting contexts, you will be motivated to devour the formal definitions and more.

Next time I would like to write more about various machines between different types of "abstract spaces", such as various notions of "geometric realization", and the functor taking a topological space and producing a compactly generated space (it's the right adjoint to the inclusion functor).  

Finally, a little bit of physics to be taken in before bedtime. Note in particular that the underlying "spaces" here seem to be of combinatorial nature, and that the "dimension" of such a space apparently can depend on the "scale".
https://en.wikipedia.org/wiki/Causal_dynamical_triangulation

An unrelated but interesting question (for another day) is whether one can build a new arithmetic geometry from the idea that morphisms which are surjective and finite etale should be n-to-1 maps on the level of dark point counts...

Finally (again, this time for real), here is a pre-view of some of the stuff we will discuss in the (hopefully near) future:

https://homotopical.wordpress.com/2009/04/20/what-is-geometry/
