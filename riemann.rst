*********************************
Connections for Riemann Manifolds
*********************************

.. math::

   \providecommand{\of}[1]{\tilde{#1}}

Parallelism on curved surfaces
==============================

A differentiable manifold has no concept of parallelism between vectors
defined at two points. An affine connection provides a rule to provide
such a concept. Consider transporting a vector across the surface of a
sphere from a pole to the equator, keeping it tangent to the sphere at
all times, without rotating it as it is transported. Then transporting
the vector 90 degrees around the equator, and returning to the pole, we
find the vector rotated by 90 degrees; clearly there is no global
concept of parallelism. So we define a rule for conducting this
transport in a parallel fashion.

Covariant Derivative
====================

Suppose we have a curve, :math:`C`, and a connection. The tangent to
:math:`C` is :math:`U = \dv{\lambda}`, and we have a vector :math:`V`
from the tangent space :math:`T_P` at :math:`P`. By
parallel-transporting :math:`V` along the curve we generate a new vector
field, and as this does not change along the curve, the curve’s
derivative with respect to the field is zero, so

.. math::

   \label{eq:41}
     \nabla_U V = 0

If :math:`W` is a vector field defined everywhere along :math:`C` then
its covariant derivative can be defined in a similar way to Lie
derivatives,

.. math::

   \label{eq:42}
     ( \nabla_U W)_P = \lim_{\epsilon \to 0} \frac{W_{\lambda_0 + \epsilon}(\lambda_0) - W(\lambda_0)}{\epsilon}

where :math:`W_{\lambda_0+\epsilon}` is the parallel transported field
which equals :math:`W` at the point :math:`\lambda_0+\epsilon`. The
operation of transportation is not the same as the dragging-back of the
Lie derivative, which requires the whole congruence, and not just the
curve. The :math:`\nabla_U` object is a differential operator:

.. math::

   \label{eq:43}
     \nabla_U (fW) = f \nabla_U W + W \nabla_U f = f \nabla_U W + W \dv{f}{\lambda}

It can be extended to tensors of arbitrary type by the Leibniz rules,

.. math::

   \label{eq:44}
     \nabla_U (A \otimes B) = (\nabla_U A) \otimes B + A \otimes (\nabla_U B)

.. math::

   \label{eq:45}
     \nabla_U \langle \of{\omega}, A \rangle = \langle \nabla_U \of{\omega}, A \rangle + \langle \of{\omega}, \nabla_U A \rangle

Now suppose the parameter along the curve is changed from
:math:`\lambda` to :math:`\mu`, so the new tangent is :math:`gU`, for
:math:`g = \dv{\lambda}{\mu}`, then

.. math::

   \label{eq:46}
     \nabla_{gU} W = g \nabla_U W

We also require

.. math::

   \label{eq:47}
   (\nabla_U W)_P +(\nabla_V W)_P = (\nabla_{U+V} W)_P

The fact that :math:`\nabla W` is a tensor field—the gradient of
:math:`W` allows the curve can be removed from the definition of the
covariant derivative.

Covariant derivatives of a basis
================================

Any tensor may be described as a linear combination of basis tensors,
which can be derived from basis vectors, and the connection can be
retrieved from knowledge of the gradients of the basis vectors, so we
define

.. math::

   \label{eq:48}
     \nabla_{e_i} e_j = \tensor{\Gamma}{^k_{ji}} e_k

with the symbol :math:`\tensor{\Gamma}{^k_{ji}}` the Christoffel
symbols; for fixed :math:`(i,j)` this is the :math:`k`\ th component of
the vector field :math:`\nabla_i e_j`, defining
:math:`\nabla_i \equiv \nabla_{e_i}`. These completely determine the
connection, although are not the components of a tensor.

Knowing the derivatives of the basis vectors, for an arbitrary tensor,
with :math:`U=\dv{\lambda}`, then

.. math::

   \label{eq:49}
     \nabla_U V = U^i \nabla_{e_i}(V^j e_j) = U^i( \nabla_{e_i} V^j )e_j + U^i V^j \nabla_{e_i} e_j

given that :math:`V^j` is a function, :math:`U^i \nabla_i (V^j) =
\dv{V^j}{\lambda}`, so

.. math::

   \label{eq:50}
     \nabla_U V = \dv{V^j}{\lambda} e_j + U^i V^j \tensor{\Gamma}{^k_{ji}}e_k = \qty( \dv{V^j}{\lambda} + \tensor{\Gamma}{^j_{ki}} V^k U^i ) e_j

If :math:`e_i = \dv{\mu}` then :math:`\nabla_i (V^j) = \dv{V^j}{\mu}`,
with :math:`V^j` function along the curve with parameter :math:`\mu`, if
:math:`e_i = \pdv{x^i}` is a coordinate vector, then

.. math::

   \label{eq:51}
     \nabla_i V^j = \pdv{x^i} V^j = \tensor{V}{^j_{,i}}

which introduces the comma notation for forms. Likewise we can
introduce the semicolon notation for a covariant derivative,

.. math::

   \label{eq:52}
     \tensor{(\nabla V)}{^j_i} = \tensor{V}{^j_{,i}} + \tensor{\Gamma}{^j_{ki}} V^k = \tensor{V}{^j_{;i}}

Torsion
=======

A connection is symmetric if the quantities :math:`\comm{U}{V}` and
:math:`\nabla_UV - \nabla_V U` are equal.

.. math:: \comm{U}{V} = \nabla_U V- \nabla_V U

For a non-symmetric connection we can define the torsion,

.. math::

   \label{eq:53}
     \tensor{T}{^k_{ji}} e_k = \nabla_{e_j} e_j - \nabla_{e_j} e_i - \comm{e_i}{e_j}

The symmetric part of the connection can be defined for any connection:

.. math::

   \label{eq:54}
     \tensor{\Gamma}{^k_{\rm (S)}_{ij}} = \tensor{\Gamma}{^k_{ij}} - \half \tensor{T}{^k_{ij}}

Geodesics
=========

A geodesic is a curve which parallel transports its own tangent vector.
The geodesic equation is

.. math::

   \label{eq:55}
     \nabla_U U = 0

For :math:`\lambda` the parameter of the curve, and :math:`\set{x^i}` a
coordinate system this becomes

.. math::

   \label{eq:56}
     \dv{U^i}{\lambda} + \tensor{\Gamma}{^i_{jk}} U^j U^k = \dv[2]{x^i}{\lambda} + \tensor{\Gamma}{^i_{jk}} \dv{x^j}{\lambda} \dv{x^k}{\lambda} = 0

If the parameter of a curve is changed from :math:`\lambda` to
:math:`\mu = a
\lambda +b`, for :math:`a`, :math:`b` constants, we find the parameter
:math:`\mu` is also a solution of the geodesic equation, and so a
geodesic’s paramater is *affine*.

Only the symmetric part of the connection contributes to the geodesic
equation, and this allows the effect of torsion to be seen
geometrically; a vector parallel transported along a geodesic with
torsion will be rotated relative to nearby geodesics.

Normal coordinates
==================

The geodesics through a point :math:`P` provide a bijection of the
neighbourhood of :math:`P` onto the origin of its tangent space,
:math:`T_P`, because each element in :math:`T_P` defines a unique
geodesic through :math:`P`, so each vector in :math:`T_P` can be
associated with a point which is an affine parameter,
:math:`\Delta \lambda =1` along the curve from :math:`P`.

With this map and an arbitrary basis for :math:`T_P` we have the normal
coordinates of a point :math:`Q`. Such a map will normally only be
bijective in a neighbourhood of :math:`P`.

A useful property of normal coordinates is that
:math:`\tensor{\Gamma}{^i_{jk}} = 0` at :math:`P`, but not necessarily
anywhere else, so the derivative is non-vanishing.

The Riemann tensor
==================

The Riemann tensor is a multiplicative operator which is also a
:math:`(1,1)`-tensor, defined

[The Riemann tensor]

.. math::

   \label{eq:59}
       \comm{\nabla_U}{\nabla_V} - \nabla_{\comm{U}{V}} \equiv {\mathbf{\mathsf{R}}}(U,V)

 Its components are defined

.. math:: \tensor{{\mathbf{\mathsf{R}}}}{^l_{kij}} e_l = \comm{\nabla_i}{\nabla_j} e_k - \nabla_{\comm{e_i}{e_j}} e_k

We can see a geometrical interpretation of :math:`{\mathbf{\mathsf{R}}}`
by considering a vector field, :math:`A`, defined along a curve with
tangent :math:`U`. Parallel transporting :math:`A` to :math:`Q` produces
a vector in :math:`T_P`, :math:`A(Q \to P)` is the *image* of :math:`P`
at :math:`A(Q)`; if :math:`A` and :math:`U` are analytic

.. math:: A(Q \to P) = \exp( \lambda \nabla_U ) \eval{A}_P

With two commuting congruences, :math:`U = \dv*{\lambda}` and
:math:`V = \dv*{\mu}`, and a vetor is parallel transported from
:math:`R` to :math:`Q` along :math:`V` we get a vector at :math:`Q`,

.. math:: A(R \to Q) = \exp(\mu \nabla_V) \eval{A}_Q

For :math:`\mu` the parameter distance from :math:`Q` to :math:`R`.
Transporting this vector to :math:`P` we get

.. math::

   A(R \to Q \to P) = \exp(\lambda \nabla_U) \exp(\mu \nabla_V)
   \eval{A}_P

We can move the vetor around the other two edges of a square to get to
the same point, and find that the two methods produce different results,
the difference being

.. math::

   \label{eq:61}
     \delta A = \lambda \mu \comm{\nabla_U}{\nabla_V} A + \mathcal{O}(3)

which is the Riemann tensor. This is the change in :math:`A` produced
if it is parallel transported about a closed loop, which is the area,
:math:`\lambda \mu` of the loop times the Riemann tensor.

.. math:: \delta A^i = \lambda \mu \tensor{{\mathbf{\mathsf{R}}}}{^i}{_{jkl}}A^j U^k V^l

Geodesics which start parallel do not stay parallel—this is geodesic
deviation. Consider a congruence of geodesics, with tangent :math:`U`,
and a connecting vector, :math:`\xi` which is Lie dragged by the
congruence. The measure of the change in the geodesics come from the
seconds derivative of the vector :math:`\xi`,
:math:`\nabla_U \nabla_U \xi` which measures how the separation of
geodesics changes. Then

.. math::

   \begin{aligned}
     \nabla_U \nabla_U \xi &= \nabla_U \qty( \ld{U}{\xi} + \nabla_{\xi}U) \\
     &= \nabla_U \nabla_{\xi} U \\ &= \comm{\nabla_U}{\nabla_{\xi}} U +
     \nabla_{\xi} \nabla_U U\end{aligned}

The last term disappears since :math:`U` is a geodesic, and so

.. math::

   \label{eq:62}
     \nabla_U \nabla_U \xi = {\mathbf{\mathsf{R}}}(U, \xi) U

which has a component form

.. math::

   \qty( \tensor{\xi}{^i_{;j}} U^j )_{;k} U^k = \tensor{R}{^i_{jkl}}
   U^j U^k \xi^l

The left-hand side can be simplified, as
:math:`\tensor{U}{^j_{;k}} U^k = 0`, and so

.. math::

   \label{eq:63}
     \tensor{\xi}{^i_{;j;k}}U^j U^k = \tensor{R}{^i_{jkl}}U^j U^k \xi^l

We normally require a manifold with a metric and a connection to have
some compatibility demands. For example, the divergence of a vector
field; the covariant divergence is defined

.. math:: \div V \equiv \nabla_i V^i

and the volume-form divergence is

.. math::

   \ld{V}{\of{\omega}} = \qty(\operatorname{div}_{\of{\omega}} V)
   \of{\omega}

Then :math:`\nabla` and :math:`\of{\omega}` are compatible if
:math:`\operatorname{div}`.

If the manifold has a metric tensor, :math:`{\mathbf{\mathsf{g}}}`, then
an inner product is defined at any point, and the connection and metric
are compatible if parallel transport preserves the inner product of two
vectors. Thus a metric determines its compatible symmetric connection, a
*metric connection*.

We can express the compatibility of the metric and the connection by
asserting that they are compatible iff

.. math::

   \label{eq:64}
     \nabla {\mathbf{\mathsf{g}}}= 0

 and

.. math::

   \label{eq:65}
     \tensor{\Gamma}{^i_{jk}} = \half g^{il} (g_{lj,k} + g_{lk,j} - g_{jk,l})

Metric Connections
==================

Metric connections have additional properties which general connections
do not have, these can be derived in a normal coordinate system. The
earlier conditions in equations and there is the implication

.. math::

   \label{eq:66}
     \tensor{\Gamma}{^i_{jk}} = 0 \text{ at } P \iff g_{lm,n} = 0 \text{ at } P

We now have the implication, that in normal coordinates at a point
:math:`P`,

.. math::

   \label{eq:67}
     \tensor{R}{_{ijkl}} \equiv \tensor{g}{_{im}} \tensor{R}{^m_{jkl}} 
     = \half \qty( \tensor{g}{_{il,jk}} - \tensor{g}{_{ik, jl}}+ \tensor{g}{_{jk, il}} - \tensor{g}{_{jl, ik}})

which has the property

.. math::

   \label{eq:68}
     \tensor{R}{_{ijkl}} = \tensor{R}{_{klij}}

We can define two new quantities, the Ricci tensor,

.. math::

   \label{eq:69}
     \tensor{R}{_{kl}} = \tensor{R}{^i_{kil}}

which is symmetric, and the Ricci scalar,

.. math::

   \label{eq:70}
     R = \tensor{g}{^{kl}} \tensor{R}{_{kl}}

And, given the Bianchi identities,

.. math:: \tensor{R}{^i_{j[il;m]}} = 0 \qquad \tensor{g}{^{jl}}\tensor{R}{^i_{j[il;m]}} = 0

then

.. math::

   \label{eq:72}
     \qty( \tensor{R}{^{ij}} - \half R g^{ij} )_{;j} = 0
     
The Weyl tensor can then be defined

.. math::

   \label{eq:73}
     \tensor{C}{^{ij}_{kl}} = \tensor{R}{^{ij}_{kl}} - 2 \tensor{\delta}{^{[i}_{[k}} \tensor{R}{^{j]}_{l]}} + \frac{1}{3} \tensor{\delta}{^{[i}_{[k}} \tensor{\delta}{^{j]}_{l]}} R
