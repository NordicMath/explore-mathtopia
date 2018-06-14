# Physics in the Zophie paradigm?

Question: Can we learn physics faster by using the Zophie paradigm along the way?

Let's take an example, essentially copied from the middle of this page:
http://math.ucr.edu/home/baez/week27.html
I will include a few definitions in condensed form, but the point is that we could formalize the language (syntax, not semantics, I guess) in Zophie even without knowing a single one of these definitons. Note also that I am skipping a few machines (for example when talking of "unit vectors") but all these undefined terms could be formalized in exactly the same fashion as the others.

Ok, so here is the example:

Type: FD quantum system.

Semantic remark: FD stands for finite-dimensional.

Machines:
- Underlying Hilbert space.
  Input: A FD quantum system. Output: A FD Hilbert space.
- Operators.
  Input: A FD Hilbert space. Output: A set.
  Elements in the set are called operators.
- Self-adjoint.
  Input: An operator. Output: A Boolean.
- Observables.
  Input: A FD quantum system. Output: A set.
  Elements of the set are called observables.

Semantic remarks:
- Def: An observable is a self-adjoint operator on H.
- Def: A state is a positive normalized linear functional on the observables.

More machines:
- Being a density operator.
  Input: An operator on H. Output: A Boolean.
- State associated to a unit vector.
  Input: A unit vector in H. Output: A state.
- State associated to a density operator.
  Input: A density operator. Output: A state.
- Superposition of states. Def: Normalized linear combinations of unit vectors.
  Input: Two states and real number in (0,1). Output: A state.
- Mixture of states (weighted average of linear functionals)
  Input: Two states: Output: One state.
- Entropy of a state:
  Input: One state. Output: A real number.
- Being a pure state.
  Input: A state. Output: A Boolean.

Theorems:
- A state is pure iff it is associated to a unit vector.
- Every state appears as the state associated to a density operator.
- Every state appears as a mixture of pure states.
- A state in pure iff its entropy is zero.
