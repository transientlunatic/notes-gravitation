*********************
Calculus on manifolds
*********************

.. include:: macros.rst

Lie Derivatives
===============
	     
It can be helpful to define a notion of a derivative over a manifold without needing to refer to a coordinate system.
This is problematic thanks to the lack of a consistent definition of distance over an entire manifold.
It is, however, possible to define curves on a manifold, which can have parameter values which map back to :math:`\mathbb{R}`, and it is these curves which the Lie derivative uses to define a notion of distance.

	     
Congruences
-----------
	     
It is important to be able to define the notion of a set of paths over a manifold.

A congruence is a set of curves which fill a manifold, or some part of it without intersecting.

Each point is on only one curve, and as each curve is a 1D collection of points we can assemble the curves into an (:math:`n-1`)-dimensional manifold. The congruence thus provides a mapping from the manifold back onto itself.

.. glossary::

   congruence
      A congruence is a set of integral curves on a manifold which is defined by a non-vanishing vector field.

With this notion of a congruence it is useful to think about how functions will behave across the manifold.
To do this we consider sliding, or "dragging" them along congruences, and seeing how they behave.
      
Lie dragging
------------
      
If the parameter on the curves is :math:`\lambda` then any small number :math:`\Delta \lambda` defines a mapping :math:`\lambda \to \Delta \lambda` in which each point is moved :math:`\Delta \lambda` further along the same curve.

If this map exists for all :math:`\Delta \lambda` then there is a 1D differentiable family of such mappings, which forms a Lie Group with the composition law
:math:`\Delta \lambda_1 + \Delta \lambda_2`.

Such a mapping is a Lie dragging.

Lie dragging a function
-----------------------

For a function :math:`f` defined on a manifold the Lie dragging defines a function :math:`f^{*}_{\Delta\lambda}` such that if a point :math:`P`
was mapped to a point :math:`Q`, after moving along the curve the new field :math:`f^{*}_{\Delta \lambda}` has the same value at :math:`Q` as :math:`f` had at :math:`P`, that is

.. math:: f(P) = f^{*}_{\Delta \lambda} (Q)

If :math:`f^{*}_{\Delta \lambda} (Q) = F(Q)` for all :math:`Q` the function is invariant under the mapping.
If it is invariant under all :math:`\Delta \lambda` then it is **Lie Dragged** by the field :math:`\frac{\dd}{\dd \lambda}`.
Because of this, a Lie dragged function will have :math:`\frac{\dd f}{\dd \lambda} = 0`.

Lie dragging a vector field
---------------------------

In the limit of infinitessimal :math:`\Delta \lambda` and infinitessimal separation between two curves, :math:`(1)` and :math:`(2)`, if :math:`\frac{\dd}{\dd \mu}` at the point :math:`P` stretches from :math:`P` to :math:`R` along :math:`(A)`, then :math:`\frac{\dd}{\dd \mu^{*}_{\Delta \lambda}}`
will stretch from :math:`Q` to :math:`S` on :math:`(A')`.
If  :math:`\frac{\dd}{\dd\mu}` is Lie dragged, then it will also stretch from :math:`Q` to :math:`S`, implying

.. math::`\left[\frac{\dd}{\dd \lambda}, \frac{\dd}{\dd \mu} \right] = 0.`
      
Thus a vector field is Lie dragged if its Lie Bracket with the dragging field vanishes.

The Lie Derivative
------------------

The concept of dragging permits the definition of a derivative along the congruence.
There is a problem of defining distance in vector and tensor fields; for a curve between points the distance is the difference in the
curves parameter for the two points.
Another consideration is whether two vectors at different points are parallel or not.

On a simple manifold there is no sense in this question, as there is no way to move vectors around in a parallel manner, and for this we need an affine connection.
However, the notion of congruence can provide a substitute; to compare vectors at points :math:`\lambda` and :math:`\lambda + \Delta \lambda`
on a given curve we can Lie drag the vector at :math:`\lambda + \Delta \lambda` back to :math:`\lambda`, defining a new vector at :math:`\lambda`, which can be subtracted from the old one, giving the difference between them which is unique given the congruence.

This allows the definition of a derivative of the form

.. math::
   :label: def-lie-derivative

        \lim_{\Delta \lambda \to 0} \frac{f^{*}(\lambda_0) - f(\lambda_0)}{\Delta \lambda} = \lim_{\Delta \lambda \to 0} \frac{f(\lambda_0 + \Delta \lambda) - f(\lambda_0)}{\Delta \lambda} = \left[ \frac{\dd f}{\dd \lambda}\right]_{\lambda_0}

We can define an operator for this derivative, :math:`\ld_V` with :math:`V` the vector field generating the mappings, so

.. math::
   :label: lie-derivative-function
	   
    \ld_{V} f = V(f) = \frac{\dd f}{\dd \lambda}

Carrying out the same procedure on a field :math:`U = \frac{\dd}{\dd \mu}`, and considering the definition of a vector in terms of its effect on functions, so we define an arbitrary function :math:`f`.
At
:math:`\lambda_0` the field :math:`U` gives the derivative
:math:`\left(\frac{\dd f}{\dd \mu}\right)_{\lambda_0}` and at
:math:`\left(\frac{\dd f}{\dd \mu}\right)_{\lambda_0 + \Delta \lambda}`; by dragging
:math:`U(\lambda_0 + \Delta \lambda)` we get a new field
:math:`U^{*}=\frac{\dd}{\dd \mu^{*}}`, then :math:`[U^{*}, V] = 0`, and
:math:`U^{*}(\lambda_0 + \Delta \lambda) = U(\lambda_0+\Delta \lambda)`.

The vanishing commutator implies

.. math::
   
   \frac{\dd}{\dd \lambda} \frac{\dd}{\dd \mu^{*}} f = \frac{\dd}{\dd \mu^{*}} \frac{\dd}{\dd \lambda} f

We then define the Lie derivative :math:`\ld_V U` as the vector field operating on :math:`f` to give

.. math::

   \left[ \ld_V {U} \right] (f) = \lim_{\Delta \lambda \to 0} \left( \frac{\dd}{\dd \lambda} \frac{\dd}{\dd \mu} f - \frac{\dd}{\dd \mu^{*}} \frac{\dd}{\dd \lambda} f \right)

This is true for all :math:`f`, so

.. math::

   \ld_{V} {U} = \frac{\dd}{\dd\lambda} U - \frac{\dd}{\dd \mu} V = [{V},{U}]

Lie Derivatives of a One-form
-----------------------------

Fields of one-forms and tensors are defined in terms of scalar functions
and vector fields, so a definition of a Lie derivative can also be found
for a one-form. A one-form field is said to be Lie dragged if its value
on any dragged vector field is constant, so the Lie derivative of
:math:`\covec{\omega}` along a vector field :math:`V` is defined

.. math::

   \label{eq:23}
     \ld{V}{\of{\omega}} = \qty(\ld{V}{\of{\omega}})(W) + \of{\omega} \qty(\ld{V}{W})

 extending this to tensors of higher order,

.. math::

   \label{eq:24}
     \ld{V}{(\ten{A} \otimes \ten{B})} = (\ld{V}{\ten{A}}) \otimes \ten{B} + \ten{A} \otimes (\ld{V}{\ten{B}})

Submanifolds
============

**A submanifold**, is a smooth subset of another manifold :math:`M`. In
Euclidean 3-space surfaces and curves are submanifolds. Thus, An
:math:`m`-dimensional submanifold, :math:`S`, of an
:math:`n`-dimensional manifold :math:`M` is a set of points with the
property that in some open neighbourhood in :math:`M` of any point
:math:`P` of :math:`S` there exists a coordinate system for :math:`M` in
which the points of :math:`S` are characterised by :math:`x^1 = x^2 =
\cdots = x^{n-m} = 0`.

Solutions of differential equations are usually relations, say,
:math:`\set{y_i = f_i(x^1, \dots, x^m), i=1, \dots, p}`, which can be
thought of as submanifolds with the coordinates :math:`\set{x^1, \dots,
  x^m}` of a larger manifold with coordinates
:math:`\set{y^1, \dots, y^p,
  x^1, \dots, x^m}`. Suppose :math:`P` is a point on a submanifold
:math:`S` (dimension :math:`m`) of :math:`M` (dimension :math:`n`). A
tangent space of a point in :math:`S` is a subspace of the tangent space
of the same point in :math:`M`.

Frobenius’ Theorem
==================

In any coordinate patch :math:`S` there are coordinates
:math:`\set{y^a}` and basis vectors :math:`\set{\pdv{y^a}}` for vector
fields on :math:`S`; these basis fields naturally commute. Any two
fields on :math:`S` will have a Lie Bracket which is tangent to
:math:`S`, and if a set of :math:`m` :math:`C^{\infty}` vector fields
defined in a region :math:`U` of :math:`M` have Lie Brackets with one
another all of which are linear combinations of :math:`m` vector fields,
then the integral curves of the fields mesh to form a family of
submanifolds. Each point of :math:`U` is on one and only one
submanifold, and so the submanifolds fill :math:`U` in the same way as a
congruence of curves, and forms a *foliation* of :math:`U`, with each
submanifold a *leaf*.

[The Generators of :math:`S^2`] Consider the :math:`\phi`-direction
basis vector in spherical polars,

.. math::

   \vec{e}_{\phi} = - y \vec{e}_z + x \vec{e}_y = \pdv{\phi} = -y
     \pdv{x} + x \pdv{y}

In quantum mechanics we can define an operator,
:math:`\Op{l}_z \propto \pdv{\phi}`, defining :math:`\Op{l}_x`, and
:math:`\Op{l}_y` in similar ways, then there are commutation relations,

.. math::

   \begin{aligned}
       \comm{\Op{l}_x}{\Op{l}_y} &= - \Op{l}_z \\
       \comm{\Op{l}_y}{\Op{l}_z} &= - \Op{l}_x \\
       \comm{\Op{l}_z}{\Op{l}_x} &= - \Op{l}_y
     \end{aligned}

 these generate a submanifold, apparently with three dimensions, but
noting that each of the operators is tangent to a sphere of constant
radius, and recalling that the contraction of this sphere with an
operator is the number of spherical surfaces which the operator pierces,
it’s clear that all of the operators are tangent to the sphere, and so
they generate a dimension 2 submanifold, the sphere, since they are
linearly dependent.

Invariance
==========

A principle use of Lie derivatives is to express the notion of a vector
field’s invariance under a transformation. A tensor field
:math:`\ten{T}` is invariant under a vector field :math:`\vec{V}` if

.. math:: \ld{\vec{V}}{\ten{T}} = 0

For example, if a system is invariant under rotations in a given plane
it is axisymmetric about that plane’s axis, and angular momentum is
conserved.

Suppose we have a set, :math:`F = \set{\ten{T_1}, \ten{T_2}, \dots}` of
tensor fields whose invariance properties have been studied, then the
set of all vector fields :math:`\vec{V}` under which the fields of
:math:`F` are invariant form a Lie algebra. In the example of the
angular momentum operators, which are linearly dependent as fields on
:math:`R^3`, to represent one field as a combination of the other two
the linear combination needs variable coefficients, so the fields are
linearly independent elements in the Lie Algebra, where the coefficients
must be constant.

Killing Vector Fields
=====================

A Killing vector field is a vector field :math:`\vec{V}` such that

.. math::

   \label{eq:26}
     \ld{\vec{V}}{\ten{g}} = 0

 for :math:`\ten{g}` the metric tensor, which, in component notation

.. math::

   \label{eq:27}
     \ten{\qty( \ld{\vec{V}}{g} )}_{ij} = V^k \pdv{x^k} \ten{g}_{ij}
                                        +\ten{g}_{ik} \pdv{x^j} V^k
                                        +\ten{g}_{kj} \pdv{x^i} V^k = 0

 The Killing vector field is then the metric which is invariant given a
specific vector field. Using a coordinate system where the integral
curves of :math:`\vec{V}` are one family of coordinate lines, e.g.~ for
the :math:`x^1` coordinate, then

.. math::

   \label{eq:28}
     \ten{ \qty( \ld{\vec{V}}{g} )}_{ij} =\pdv{x^1} \ten{g}_{ij} =0

 So the metric components are independent of the coordinate :math:`x^1`,
and conversely if there is a coordiante system where the representation
of the metric is independent of a certain coordinate the corresponding
basis vector to the coordinate is a Killing vector.

The metric tensor in Cartesian coordinates is :math:`\ten{g}_{ij} =
\ten{\delta}_{ij}` which is independent of :math:`x`, :math:`y`, and
:math:`z`, so the Killing vectors are :math:`\pdv{x}`, :math:`\pdv{y}`,
and :math:`\pdv{z}`. In spherical polar coordinates the same metric has
the components :math:`\ten{g}_{rr}=1`,
:math:`\ten{g}_{\theta \theta}=r^2`, and
:math:`\ten{g}_{\phi \phi} = r^2
\sin[2](\theta)`.

Consider a system which is axisymmetric, with angle :math:`\phi`, or is
close to axisymmetric (i.e.with a small perturbation from axisymmetric),
then, for an operator :math:`\Op{L}` and unknown :math:`\psi`,

.. math::

   \label{eq:29}
     \Op{L}(\psi) = 0

 where :math:`\Op{L}` is independent of a coordinate transformation
:math:`\phi \to
\phi + \textrm{const}`. The solutions of are not necessarily
axisymmetric, but scalar solutions can be Fourier-analysed in
:math:`\phi` as

.. math::

   \label{eq:30}
     \psi(\phi, x^i) = \sum_{m=-\infty}^{\infty} \psi_m(x^j) e^{i m \phi}

 the functions :math:`\psi_m(x^j)` satisfy the related differential
equation

.. math::

   \label{eq:31}
     0 = \Op{L}_m(\phi_m) = e^{-i m \phi} L(\psi_m e^{im\phi})

 A solution :math:`\psi`, is an axial eigenvalue, :math:`m`, if

.. math::

   \label{eq:32}
     \ld{\vec{e}_{\phi}} \psi = i m \psi

 for :math:`\vec{e}_{\phi}` tangent to the circles of symmetry. Any
vector field satisfying

.. math:: \ld{\vec{e}_{\phi}}{\vec{V}} = i m \vec{V}

 can be expressed in terms of a linear combination of vector axial
harmonics with eigenvalue :math:`m`, of the form
:math:`\vec{e}_j e^{i m \phi}`, with coefficients independent of
:math:`\phi`.

Abstract Lie Groups
===================

A Lie group is a differential manifold which has a differentiable
structure compatible with the group structure, that is, the operation
:math:`G \times G \to G` by :math:`(x,y) \to x y^{-1}` is a
differentiable mapping.

| Consider a finite-dimensional Lie group, :math:`G`. Any neighbourhood
  of :math:`e` is mapped to a neighbourhood of :math:`g` by a mapping,
  which also carries all of the tangent vectors, so the mapping is
  denoted :math:`L_g : T_e \to
  T_g`.
| A vector :math:`V` is left-invariant if :math:`L_g` maps :math:`V` at
  :math:`e` to :math:`V` at :math:`g`, i.e. :math:`L_g: V(e) \to V(g)`,
  for all :math:`g`. It follows that :math:`L_g` maps
  :math:`V(h) \to V(gh)` for any :math:`h` in :math:`G`, giving a
  definition of a constant vector field on :math:`G`. If any two vector
  fields :math:`V` and :math:`W` are left-invariant then
  :math:`\comm{V}{W}` is also a left-invariant field, so the fields form
  a Lie algebra, :math:`\mathfrak{L}(G)`, or :math:`\mathfrak{g}`.

Let :math:`\set{V_{(i)}}` be a set of basis fields for a Lie algebra,
then

.. math::

   \label{eq:25}
     \comm{V_{(k)}}{V_{(l)}} = \ten{c}_{kl}^j V_{(j)}

 these :math:`c` are the structure constants which characterise the
algebra; if these disappear then the algebra is said to be Abelian.
These components transform as the components of a (1,2)-tensor, and each
Lie group and algebra has a unique structure tensor :math:`\ten{C}`.

For an integral curve of a field :math:`V` which passes through
:math:`e`; it has a tangent vector :math:`V_e`, and a unique parameter
:math:`t` for which :math:`e` corresponds to :math:`t=0`. The points on
the curve can be found by eponentiation of :math:`V`, :math:`\exp(tV)`,
defining a one-parameter subgroup of :math:`G`, and since each of these
passes through :math:`e` there must be an injective relationship between
the one-parameter subgroups of :math:`G` and its Lie algebra.

A theorem exists that states that every Lie algebra is the algebra of
one, and only one simply-connected Lie group.

Group Representations
=====================

A group representation is a means of describing an abstract group in
terms of linear transformations of vector spaces.

[Group Representation] A representation, :math:`\rho`, of a group
:math:`\mathrm{G}` on a vector space :math:`V` over a field :math:`K` is
a group homomorphism from :math:`\mathrm{G}` to the general linear
group, :math:`\mathrm{GL}(V)`,

.. math::

   \rho : \mathrm{G} \to
     \mathrm{GL}(V)

with the property

.. math::

   \rho(g_1 g_2) = \rho(g_1)
     \rho(g_2)

 for :math:`g_1, g_2` elements of :math:`\mathrm{G}`.

[Faithful representation] A faithful representation occurs if the group
homomorphism is an injective mapping, i.e. every element in the group is
represented in the general linear group.

Consider the cyclic group, :math:`{\mathrm{C_3}}=\set{1, u, u^2}`. This
has a representation on :math:`\mathbb{C}^2` as

.. math::

   \rho(1) = \begin{bmatrix}1&0\\0&1\end{bmatrix}, \quad \rho(u) =
   \begin{bmatrix}
     1 & 0 \\ 0 & u
   \end{bmatrix} \quad
   \rho(u^2) =
   \begin{bmatrix}
     1 & 0 \\ 0 & u^2
   \end{bmatrix}

 with :math:`u = e^{2 \pi i / 3}`, or, an isomorphic representation is

.. math::

   \rho(1) = \begin{bmatrix}1&0\\0&1\end{bmatrix}, \quad \rho(u) =
   \begin{bmatrix}
     u & 0 \\ 0 & 1
   \end{bmatrix} \quad
   \rho(u^2) =
   \begin{bmatrix}
     u^2 & 0 \\ 0 & 1
   \end{bmatrix}


