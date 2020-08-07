*********
Manifolds
*********

Manifolds
=========

:math:`\rn` is the set of all :math:`n`-tuples of real numbers. A set
:math:`M` is defined to be a manifold if each element of :math:`M` has
an open neighbourhood with a continuous bijection onto an open set of
:math:`\rn` for some :math:`n`. This mathematical object is rather
degenerate, and hasn’t got, for example, a notion of distance, and what
structure is defined is only at a local level.

The elements, :math:`P` of :math:`M` have a unique :math:`n`-tuple, the
co-ordinates of :math:`P`:

.. math::

   \label{eq:5}
     \qty( x_1(P), x_2(P), \dots, x_n(P) )

Let :math:`f:U(P) \to \rn` be a function from a neighbourhood :math:`U`
around :math:`P\in M` of :math:`M` onto an open set
:math:`f(U) \in \rn`, then the pair, :math:`(U,f)` are a chart. The open
neighbourhoods must overlap if all points of :math:`M` must be included
in at least one, and so these overlaps give an additional
characterisation of the manifold. Suppose :math:`V` is a neighbourhood
overlapping :math:`U`, such that :math:`V` has a map :math:`g` onto an
open region of :math:`\rn`, this region may be completely disjoint from
the equivalent region for :math:`U`. The open intersection of :math:`U`
and :math:`V` is described by two coordinate systems, so there should be
an expression connecting the two. Such an equation is a *coordinate
transformation*.

[Manifold] A manifold is a second-countable Hausdorff space which is
locally homeomorphic to Euclidean space.

[Chart] A chart :math:`(U, f_U)` of a manifold is an open set :math:`U`
together with a mapping :math:`f_U: U \to \rn`.

[Coordinates] The coordinates :math:`(x^1, \cdots, x^n)` of the image
:math:`f_U(x) \in \rn` are the coordinates of :math:`x` in the chart
:math:`(U, f_U)`; the local coordinate system.

If a whole system of charts, an atlas, can be constructed such that
every point in :math:`M` is in at least one neighbourhood, and every
chart is :math:`C^k`-related to every overlapping neighbour the manifold
is :math:`C^k`. Any such manifold for :math:`C^1` or greater is a
differentiable manifold.

Many mathematical spaces can be considered as manifolds, for example the
space of Lorentz boosts, mechanical phase space, solution spaces for
functions, and vector spaces. Groups also have representations as
manifolds; a Lie group, e.g. the group of rotations of a rigid object in
space is also a :math:`C^{\infty}` manifold.

[Orientability] Let :math:`M^n` be a differentiable
:math:`n`-dimensional manifold equipped with an atlas
:math:`\set{\phi_a}`, and suppose that for any two charts of the atlas,
:math:`\phi_{\alpha}`, and :math:`\phi_{\beta}` the Jacobian of the
transition function :math:`\phi_{\beta \alpha} = \phi_{\beta} \circ
  \phi_{\alpha}^{-1}` is positive at all points in the domain, then
:math:`M` is an orientable manifold.

A Jacobian which is negative will reverse the orientation of a
coordinate system.

Global Properties
=================

At a local level all manifolds look like :math:`\rn`, but on a global
level this is not the case. For example a sphere, :math:`S^2` and a
crayon are both two-dimensional manifolds, and neither has a single map
to :math:`\mathbb{R}^2`, but there is a continuous map from one to the
other. If there is a :math:`C^{\infty}` bijective map from one
:math:`C^{\infty}` manifold to another, then the two map is a
*diffeomorphism* from one manifold to the other.

[scale=0.45]

[yshift=120] (0,0) – (10,0); at (-1.2,0)
:math:`\lambda \in \mathbb{R}^1` ; in 0,1,...,10 (re) at (, 0);

[xshift=-50] (0,0) to[out=-10,in=150] (6,-2) – (12,1) to[out=150,in=-10]
(5.5,3.7) – cycle;

[scale=0.4, xshift=300] (A) at (0,0); node at (11.5, 0.8) :math:`U`;
(0,0) to[out=-10,in=150] (6,-2) – (12,1) to[out=150,in=-10] (5.5,3.7) –
cycle;

(0,0) .. controls (6,-0.2) and (5,1.5) .. coordinate[pos=0.0] (cux0)
coordinate[pos=0.1] (cux1) coordinate[pos=0.2] (cux2)
coordinate[pos=0.3] (cux3) coordinate[pos=0.4] (cux4)
coordinate[pos=0.5] (cux5) coordinate[pos=0.6] (cux6)
coordinate[pos=0.7] (cux7) coordinate[pos=0.8] (cux8)
coordinate[pos=0.9] (cux9) coordinate[pos=1.0] (cux10) (12,1);
(cux10)+(0.3,0) node [right] :math:`P \in M`;

in 0,1,...,10 (cux) edge [accent-blue, shorten >=0.1cm, shorten <=
0.1cm, line width=0.3mm, <-, out=90, in=270] (re); (re) circle (3pt);
(cux) circle (3pt); (13, 3) node :math:`f`; (3, -2) node :math:`g`;

[yshift=-210, xshift=-50] (C) at (0, 0.5); (0,0) – (12.1,0); (0,0) –
(0,5); (0,0) rectangle (12,5); (10,0.5) node
:math:`g(U) \in \mathbb{R}^n`; (E) at (12, 4);

(0, 0.5) edge coordinate[pos=1/10] (cdx4) coordinate[pos=3/10] (cdx5)
coordinate[pos=6/10] (cdx6) coordinate[pos=9/10] (cdx7) (8, 5);

in 4,5,...,7 (cdx) circle (3pt);

in 4,5,...,7 (cux) edge [accent-red, shorten >=0.1cm, shorten <= 0.1cm,
line width=0.3mm, ->, out=270, in=90] (cdx);

Curves and Functions on Manifolds
=================================

A curve is a differentiable mapping from an open set of
:math:`\mathbb{R}^1` into :math:`M`, so each point :math:`\lambda` on
the real line is associated with a point in :math:`M`.

A function on :math:`M` is a rule assigning a real number to each point
of :math:`M`. When a region of :math:`M` is mapped to :math:`\rn` the
function becomes a function of :math:`\rn`. If this is differentiable on
:math:`\rn` it is defined as being differentiable on :math:`M`. That is

.. math:: g(P \in M) = g(x_1(P), \dots, x_n(P)) = g(x_1, \dots x_n)

Now, consider a curve, :math:`c`, which passes through :math:`P \in M`,
which is described by :math:`x^i = x^i(\lambda)` for
:math:`i \in \set{1, \dots, n}`, and a differentiable function
:math:`g(x^i)` on :math:`M`. :math:`g` has a value at each point along
the curve, so there is a differentiable function, :math:`g(\lambda)`
along the curve which gives the value of :math:`c` at the point with a
parameter value :math:`\lambda`,

.. math::

   g(\lambda) = g(x^1(\lambda), \dots, x^n(\lambda) ) =
   g(x^i(\lambda))

 Differentiating, and applying the chain rule,

.. math::

   \label{eq:6}
     \dv{g}{\lambda} = \dv{x^i}{\lambda} \dv{g}{x^i}

 using Einstein notation.

In Euclidean space the set :math:`\set{ \dv*{x^i}{\lambda} }` would be
components of a vector tangent to the curve :math:`x_i(\lambda)`, and
would be the tangent to an infinite number of curves through :math:`P`.

Manifolds do not necessarily have a notion of distance between points,
so vectors must be defined in terms only of infinitessimal
neighbourhoods of the points of :math:`M`.

Vectors
=======

Suppose :math:`a` and :math:`b` are two numbers and
:math:`x^i = x^i(\mu)` is another curve through :math:`P`, then at
:math:`P`,

.. math:: \dv{\mu} = \dv{x^i}{\mu} \pdv{x^i}

 and

.. math:: a \dv{\lambda} + b\dv{\mu} = \qty( a \dv{x^i}{\lambda} + b \dv{x^i}{\mu} ) \pdv{x^i}

 The numbers inside the bracket are the components of a new vector,
tangent to a curve at :math:`P`, so a curve must exist, with parameter
:math:`\phi` such that at :math:`P`,

.. math:: \dv{\phi} = \qty( a \dv{x^i}{\lambda} + b \dv{x^i}{\mu} ) \pdv{x^i}

 collecting this, at :math:`P`,

.. math:: a \dv{\lambda} + b \dv{\mu} = \dv{\phi}

 forming a vector space.

In any given coordinate system there are special curves, the coordinate
lines. The derivations along them are :math:`\pdv*{x^i}`, and
:math:`\dv*{\lambda}` has components on the basis, showing that
:math:`\set{\dv*{x^i}{\lambda}}` are a basis for a vector space.

Basis Vectors and basis vector fields
=====================================

At any point :math:`P` the space :math:`T_P` is a vector space with the
same dimension :math:`n` as the manifold, and is the tangent space. Any
collection of linearly independent vectors can form a basis, and if
there is a coordinate system :math:`\set{x^i}` in a neighbourhood
:math:`U` of :math:`P` then these coordinate define a coordinate basis
at all points in :math:`U`.

[Tangent Vector] Let :math:`M^m` be a differential manifold, :math:`p` a
point on it, and :math:`U` be an open neighbourhood of :math:`M`. Let
:math:`\epsilon>0`, and :math:`\gamma :
  (-\epsilon, \epsilon) \to U` be a differentiable curve on :math:`M`
such that :math:`\gamma(0) = p`. For any differentiable function
:math:`f:U \subset M
  \to \mathbb{R}` the directional derivative of :math:`f` along
:math:`\gamma` to be the number

.. math:: D_{\gamma}(f) = \eval{\dv{t}( f (\gamma(t) ) )}_{t=0}

The operator :math:`D_{\gamma}` is called the tangent vectorto
:math:`\gamma` at :math:`p`.

[Tangent Space] The tangent space of :math:`M` at :math:`p`, :math:`T_p`
is a vector space with the same dimension as the manifold composed of
all of the tangent vectors to the manifold at :math:`p`. If :math:`x` is
a coordinate system which contains :math:`p`, then the set of
:math:`\pdv*{x}` are the basis of the tangent space; and this is a
coordinate basis.

At any point :math:`P` an arbitrary vector :math:`\vec{V}` is

.. math:: \vec{V} = V^i \pdv{x^i} = V^j \bar{e}_j = V^j \partial_j

for an arbitrary basis :math:`\set{\vec{e}_i}`. Thus :math:`\set{V^i}`
are the components of :math:`\vec{V}` in :math:`\set{ \pdv*{x^i}}`, and
:math:`\set{V^j}` the components in :math:`\vec{e}_j`, where a useful
notation, :math:`\partial_i \equiv \pdv*{x^i}` is introduced.

Differential of a map
=====================

[Differential] Let :math:`\phi: M^m \to N^n` be a differentiable map
between differentiable manifolds. We define the differential of
:math:`\phi` at :math:`p
  \in M` as the linear transformation between vector spaces

.. math::

   \begin{aligned}
       \dt{\phi_p} : T_pM & \to T_{\phi(p)N} \\
   D_{\gamma} &\mapsto D_{\phi \circ \gamma}
     \end{aligned}

Fibre bundles
=============

[Homeomorphism] A homeomorphism is an bijection from one space to the
other which is continuous, and its inverse is continuous.

[Fibre Bundle] A fibre bundle is a space, :math:`E`, which has a base
manifold :math:`B`, a projection :math:`\pi: E \to B`, a typical fibre
:math:`F` a structure group :math:`G` of homeomorphisms of :math:`F`
onto iteself, and a family :math:`\set{U_j}` of open sets which cover
:math:`B`, which satisfy

#. Locally the bundle is trivial: the bundle over any set :math:`U_j`
   which is just :math:`\pi^{-1}(U_j)` has a homeomorphism onto
   :math:`U_j \times
     F`. Part of this is a homeomorphism from each fibre, say
   :math:`\pi^{-1}(x)`, :math:`x\in B` onto :math:`F`. Call this map
   :math:`h_j(x)` labelled both by :math:`x` defining the fibre, but
   also by :math:`j` indexing the set :math:`U_j` which contains
   :math:`x`.

#. When two sets :math:`U_j` and :math:`U_k` overlap a point :math:`x`
   in their intersection has two homeomorphisms, :math:`h_j(x)` and
   :math:`h_k(x)` from the fibre onto :math:`F`. Thus
   :math:`h_j(x) \circ h_k^{-1}(x)` is a homeomorphism of :math:`F` onto
   :math:`F`. This must be an element of :math:`G`.

In two overlapping neighbourhoods there are homeomorphisms
:math:`h_j(x)` and :math:`h_k(x)` which map :math:`\vec{v}` to
:math:`\alpha_{(j)}` and to :math:`\alpha_{(k)}`, and so the
homeomorphism :math:`h_j(x) \circ h_k^{-1}(x): F
\to F` maps :math:`\alpha_{(k)} \to \alpha_{(j)}`, which is equivalent
to multiplication by a real number
:math:`r_{jk} = \alpha_{(j)}/a_{(k)}`, which must be a non-zero real
number. Thus the structure group is :math:`\mathbb{R}^1 - \set{0}`,
which is a Lie group under multiplication.

The difference between two bundles over a base space is the bundles’
*structure group*.

If the coordinates :math:`\lambda_j` can be arranged in such a way that
:math:`\lambda_j` and :math:`\lambda_k` increase in the same direction
in :math:`S^1` in the overlap region, then :math:`S^1` is orientable. In
such an overlap all :math:`r_{jk}` are positive, so the structure group
becomes :math:`\mathbb{R}^+`, and by scaling the coordinates so that
:math:`\dv*{\lambda_j}{\lambda_k} =
1` in every overlap the group reduces to the identity element, thus the
structure group is trivial and we have a bundle structure.

Consider the combination of a manifold :math:`M` with all of its tangent
spaces :math:`T_P`. This is equivalent to the set of all vectors at all
points in the manifold, and can be defined as a new manifold :math:`TM`;
a *fibre bundle*, with the fibres the spaces :math:`T_P`, and has
dimension :math:`m+n`, with :math:`m` the dimension of each fibre, and
:math:`n` of the base manifold. An example of a fibre bundle is the
structure of space and time in the Newtonian world view, where the base
space is :math:`\mathbb{R}^1`, with :math:`\mathbb{R}^3` fibres, that is
a base of time with fibres of space. This follows, as there is no
absolute concept of space in Newtonian physics, and so there is no
connection between points on each fibre.

[Cartesian Product Space] A Cartesian product space of two spaces
:math:`M` and :math:`N`, denoted :math:`M \times
N` is the set of all ordered pairs :math:`(a,b)` for :math:`a \in M` and
:math:`b \in
N`, and if :math:`M` and :math:`N` are manifolds then :math:`M \times N`
is also a manifold; the set of coordinates :math:`\set{x^i}` of an open
set :math:`U` of :math:`M` taken with :math:`\set{y^i}` of an open set
:math:`V` of :math:`N` form a set of :math:`m+n` coordiates for the open
set :math:`(U,V)` of :math:`M \times N`.

Fiber bundles are locally product spaces; they are locally trivial, as
they look like product spaces, but not usually globally trivial. For
example, :math:`TS^2` is the tangent bundle of a 2-sphere; were it
globally tivial there would be a diffeomorphism of :math:`TS^2` onto
:math:`S^2 \times
\mathbb{R}^2`. Consider the set :math:`(P, \bar{V})` in the product
space; the invserse map gives a nowhere-zero cross-section of
:math:`TS^2`, but a vector field must always have a zero, and so
:math:`TS^2` has no global product structure. A tangent bundle
:math:`TS^1` *is* identical to :math:`S^1
\times \mathbb{R}`, but if the circle is cut at a point :math:`P`, and a
twist is introduced, making a Möbius strip, the resulting bundle is not
a product space, as no bijection exists from one bundle onto all of the
other.

[Tangent Bundle] Let :math:`M^n` be a differentiable manifold. The
disjoint union of all tangent planes to :math:`M`,

.. math:: \coprod_{p \in M} T_p M

is a vector bundle with the fibre :math:`\rn` over :math:`M`, called the
tangent bundle to :math:`M`, denoted :math:`TM`.

Integral Curves
===============

For a :math:`C^1` vector field there is always a curve which has the
field as a tangent at each of its points; these are its integral curves.

Let the components of the field be :math:`V^i(P) = v^i(x^j)` in a
coordinate system :math:`\set{x^i}` The statement that this is a tangent
vector to a curve parameterised by :math:`\lambda` is

.. math::

   \label{eq:7}
     \dv{x^i}{\lambda} = v^i(x^j)

 which is a set of first-order ODEs for :math:`x^i(\lambda)`, which
always has a unique solution in a neighbourood of :math:`P`.

Lie Brackets
============

Any linearly independent set of vector fields can serve as a basis, but
not all come from coordinate systems; all coordinate systems commute,
but in general not all vector fields commute, and the commutator,

.. math:: \comm{V}{W} = V W - W V

is a vector field with, in general, non-vanishing components. If
:math:`W` and :math:`V` are elements of a basis they cannot be expressed
as derivatives with respect to any coordinates. The commutator is the
Lie Bracket of the two vector fields, and shows that the
parameterisation of the integral curves of these vector fields is not
that of a coordinate system.

[Lie Bracket] Let :math:`X` and :math:`Y` be vector fields of class
:math:`C^1`, then the Lie Bracket is a vector field, defined by the
operation :math:`f \mapsto (XY -
  YX) f`, and is denoted :math:`\comm{X}{Y}`.

The vector :math:`\comm{V}{W}` can be viusualised as the difference in
moving a distance :math:`\Delta \lambda = \epsilon` along the :math:`V`
curve, then :math:`\Delta \mu = \epsilon` along a :math:`W` curve,
ending at a point :math:`A`. Going in the opposite order we end at a
point :math:`B`. The vector between these two points is
:math:`\epsilon^2 \comm{V}{W}`.

A Lie Algebra of vector fields on a region :math:`U` of :math:`M` is a
set :math:`A` of vector fields on :math:`U` which is a vector space
under addition, which is closed under the Lie Bracket operation.

For a basis to be a coordinate basis the fields of the basis must
commute,

.. math:: \comm{A}{B} = 0

[scale=0.7]

[] (-.2, 0) – (5.2,0); (0, -.2) – (0,5.2);

(0,0) rectangle (5,5); (0,0) grid (5,5);

(1,1) – (4,1) node [left, midway, below, black] :math:`\partial_\mu`;
(1,4) – (4,4) node [left, midway, above, black] :math:`\partial_\mu`;

(1,1) – (1,4) node [left, midway, black] :math:`\partial_\nu`; (4,1) –
(4,4) node [right, midway, black] :math:`\partial_\nu`;

[xshift=170]

(-.2, 0) – (5,0); (0, -.2) – (0,5);

(1,1) – (4,2) node [left, midway, below, black] :math:`W`; (1,4) – (4,5)
node [left, midway, above, black] :math:`W`;

(1,1) – (1,4) node [left, midway, black] :math:`V`; (4,2) – (5,5) node
[right, midway, black] :math:`V`;

(0,0) rectangle (5,5); (-.2,-.2) rectangle (5.5,5.2); in 0,0.55,...,4
(-.06, 0) – (+-1.2,6); in 0.3,...,6 (0,-0.6) – (6, +1.3);

One-forms
=========

Consider :math:`T_P`, the tangent space of vectors at a point :math:`P`.
A one-form, :math:`\of{\omega}` at :math:`P` associates a vector
:math:`\vec{V}` at P to a real number, :math:`\of{\omega}(\vec{V})`.

This function is linear; for vectors :math:`\vec{V}` and
:math:`\vec{W}`, and real numbers :math:`a` and :math:`b`,

.. math::

   \label{eq:8}
    \of{\omega}( a \vec{V} + b \vec{W} ) = a \of{\omega}(\vec{V}) + b
   \of{\omega}(\vec{W})

 can be multiplied by scalars,

.. math::

   \label{eq:9}
     (a \of{\omega})(\vec{V}) = a [ \of{\omega}(\vec{V})]

 and have the property

.. math::

   \label{eq:10}
     (\of{\omega} + \of{\sigma}) (\vec{V}) + \of{\omega}(\vec{V}) + \of{\sigma}(\vec{V})

They satisfy the axioms of a vector space, and are indeed the duals of
vectors, and have a tangent vector space :math:`T^{*}_P`.

A field of one-forms can represent the gradient of a function :math:`f`;
such a field is denoted :math:`\dd{f}`,

.. math:: \of{\dd{}}f (\dv*{\lambda}) = \dv{f}{\lambda}

In the vector space :math:`T^{*}_P` any :math:`n` linearly independent
one-forms can constitute a basis, however selecting a set of basis
vectors, :math:`\set{\vec{e}_i}` in :math:`T_P` induces a preferred
basis on :math:`T^{*}_P`, the dual basis :math:`\set{\of{\omega}^i}`.

These have the property

.. math:: \of{\omega}^i(\vec{e}_j) = \delta^i_j

Tensors
=======

Consider a point :math:`P` in a manifold :math:`M`, a *tensor* of type
:math:`{N \choose N'}` at :math:`P` is a linear function with :math:`N`
one-form arguments, and :math:`N'` vector arguments, which has a real
scalar value. Tensors are linear on every argument.

A :math:`{N \choose N'}` tensor field is a rule which assigns a
:math:`{N \choose N'}` tensor to each point in a space, and are
functions on :math:`M`.

It is possible to construct higher-order tensors out of lower order ones
with the tensor (outer) product operation; for two vectors :math:`V` and
:math:`W` the tensor product is defined such that

.. math::

   \label{eq:11}
     V \otimes W (\of{p}, \of{q}) := V(\of{p}) W(\of{q})

If the basis vectors and one-forms are given as arguments to the tensor
the components of the tensor are returned.

It is also possible to reduce the dimensionality of a tensor by a
process called *contraction* whereby an entire argument is removed from
the tensor by constructing an inner product of those parts of the tensor
with either a one form or a vector.

Basis Transformations
=====================

Consider a point :math:`P` in a manifold :math:`M`, where a vector basis
:math:`\set{e_i}` is defined, but we want to switch to a description in
another basis, :math:`\set{e_{j'}}`, then in :math:`T_P` there is a
linear transformation, :math:`\Lambda` between the old and the new
basis,

.. math::

   \label{eq:12}
     e_{j'} = \Lambda^i_{j'} e_i

 where :math:`\Lambda` is non-singular, but arbitrary. It is not a
tensor, since its indices refer to different bases. The transformation
matrix has an inverse, :math:`\Lambda^{k'}_j` such that

.. math:: \Lambda^{k'}_j \Lambda^j_i = \delta^{k'}_{i'}

 We require the inverse transformation for basis one-forms, as is
evident from the relation

.. math::

   \of{\omega}^i e_{j'} = \delta^{i}_{k} \Lambda^k_{j'} =
   \Lambda^i_{j'}

The general expression for the change of coordinates of a tensor takes
the form

.. math::

   \label{eq:71}
     \tensor{A'}{^{u_1\dots u_l}_{r_1 \dots r_m}} = \Lambda_{t_1}^{u_1} \cdots \Lambda_{t_l}^{u_l} \Lambda_{r_1}^{q_1} \cdots \Lambda_{r_m}^{q_m} \tensor{A}{^{t_1 \dots t_l}_{q_1 \dots q_m}}

The Metric Tensor
=================

The metric tensor is a linear function defining the inner product of two
vectors, such that

.. math::

   \label{eq:13}
     g(V,U) = g(U,V) := U \vdot V

 where :math:`g` is the symmetric non-singular metric tensor, with
components in the basis :math:`\set{e_i}` being

.. math::

   \label{eq:14}
     g_{ij} = e_i \vdot e_j

 The Euclidean metric is defined such that

.. math:: g_{ij} = \delta_{ij}

 We can always form a metric, given transformations of the Cartesian
basis,

.. math:: g_{i' j'} = \Lambda^k_{i'} g_{kl} \Lambda^l_{j'}

 This can be reduced to an equation of the form

.. math:: g' = D O^{-1} g OD

 thanks to the existance of a theorem allowing us to express any matrix
as a product of an orthogonal matrix, :math:`O` and a diagonal one,
:math:`D`.

From this we can see that orthogonal matrices compose the set of
transformations between arbitrary Cartesian bases; they form a
continuous group, :math:`O(n)`, which is the Euclidean symmetry group.

The Minkowski metric, with :math:`g = \diag(-1, 1, 1, 1)`, also has
transformation matrices which form the Lorentz group, :math:`L(n)`.

Some additional properties of the metric tensor are:

.. math::

   \label{eq:15}
     \tensor{g}{^{ij}} \tensor{g}{_{jk}} = \delta^i_k

 and since
:math:`g^{ki} V_i = g^{ki} g_{ij} V^j = \delta^k_j V^j = V^k`,

.. math::

   \label{eq:16}
       V_i = g_{ij} V^j

.. math::

   \label{eq:17}
       v^j = g^{jk} V_k

allowing the metric tensor to act as an index raising and lowering
operator.

Defining a :math:`{0 \choose 2}` tensor on a manifold :math:`M` provides
a rich structure, and allow definitions of quantities such as distance
and curvature.