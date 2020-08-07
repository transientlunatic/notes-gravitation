The topology of :math:`\mathbb{R}^n`
====================================

.. include:: macros.rst

The space :math:`\rn` is the usual :math:`n`-dimensional space of vector algebra, where a position can be described by a real :math:`n`-tuple,
:math:`(x_1, x_2,  \dots, x_n)`.

The local topology of :math:`\rn` is centred around the concept of a neighbourhood of a point in :math:`\rn`, and this allows the definition of a distance function between points, :math:`\vec{x}` and :math:`\vec{y}` in :math:`\rn`,

.. math::

   \label{eq:1}
   d(\vec{x},\vec{y}) = \left[ (x_1 - y_1)^2 + (x_2 - y_2)^2 + \cdots + (x_n - y_n)^2 \right]$^{\frac{1}{2}}$

.. glossary::

   neighbourhood
      A neighbourhood of a point :math:`x` in :math:`X` is a set :math:`N(x)` containing an open set which contains :math:`x`.

      
A family of neighbourhoods induces a notion of proximity to :math:`x`.

A :term:`neighbourhood` of radius :math:`r` of the point :math:`\vec{x}` in :math:`\rn` is thus the set of points :math:`N_r(\vec{x})` with a distance less than :math:`r` from :math:`\vec{x}`.
Such a neighbourhood is *discrete* if each point has a neighbourhood containing no other points; which is clearly untrue for :math:`\rn`, which is thus continuous.

A set of points :math:`S` in :math:`\rn` is *open* if every point :math:`x \in S` has a neighbourhood contained within :math:`S`.
The interval :math:`a<x<b` is an open neighbourhood, but :math:`a \leq x < b` is closed, as the points :math:`a=x` have neighbourhoods partially outside the set.

.. glossary::

   Hausdorff space
      A space is Hausdorff if any two distinct points in the space posess disjoint neighbourhoods.

We can draw a line between two points in :math:`\rn`, as we can have neighbourhoods about each point which do not intersect, which is the Hausdorff property of the space.

Using the distance function :math:`d(\vec{x}, \vec{y})` to define these properties induces a topology on a space, enabling the definition of open sets in the space, which have the properties

#. if :math:`O_1` and :math:`O_2` are open sets, then so is their intersection, :math:`O_1 \cap O_2`
#. the union of any collection of open sets is open.
   
To make (1) apply to all sets the empty set must be defined as open, and for (2) to work :math:`\rn` as a whole must be open.


Mappings
========

A map from a space :math:`M` to a space :math:`N` is a rule which associates elements :math:`x \in M` to elements :math:`y \in N`.
The simplest map is a function :math:`f:\mathbb{R} \to \mathbb{R}` taking :math:`x \mapsto f(x)`.

Some terminology for mappings of the form :math:`f:M \to N`:

.. glossary::

   image
      The set, :math:`T` of elements from the set :math:`N` which are mapped to from elements of :math:`S \subset M`.
      Denoted :math:`f(S)`.

   inverse-image
      The set :math:`S`.

There are a number of types of mapping.

.. glossary::

   many-to-one
      A map where multiple elements of :math:`S` map to the same element of :math:`T`.

   one-to-one
      A map where only one element of :math:`S` maps to each element of :math:`T`.

   inverse
      A map which takes :math:`T \to S`, and is only well-defined for one-to-one maps.

Let :math:`f:M \to N` and :math:`g: N \to P`, then the operation of function composition is defined as

.. math:: g \circ f : M \to P

A map :math:`f:M \to N` is continuous at :math:`x \in M` if any open set of :math:`N` containing :math:`f(x)` contains the image of an open set of :math:`M`, provided :math:`M`,\ :math:`N` are topological spaces.
:math:`f` is continuous on :math:`M` if it is continuous at all the points in :math:`M`.

If :math:`f(x_1, \dots, x_n)` is a function which is defined on an open region :math:`S` of :math:`\rn` the it is *differentiable of class* :math:`C^k` if all its partial derivatives of the order less or equal to :math:`k` exist and are themselves continuous on :math:`S`; :math:`f` is a :math:`C^k` function.


Real Analysis
=============

A real function is analytic if, at :math:`x=x_0` it has a Taylor
expansion about :math:`x_0` which converges to :math:`f(x)` in a
neighbourhood of :math:`x_0`,

.. math::
   :label: function-analytic-convergence
	   
     f(x) = f(x_0) + (x-x_0)  \left. \dvvp{f}{x}  \right|_{x_0}
            + \half (x-x_0)^2 \left. \dvvpn{f}{x}{2} \right|_{x_0}
            + \cdots

This clearly requires that :math:`f` be infinitely differentiable, but this is not a guarantee that :math:`f` is analytic, e.g. :math:`\exp(-1/x^2)` which is non-analytic as a real function, but becomes analytic with a singularity at :math:`z=0` as a complex function.

A real-valued function :math:`g(\cdots)` defined on an open region :math:`S` of :math:`\rn` is square-integrable if

.. math::

   \label{eq:3}
      \int_S \left[ g(x_1, \dots, x_n) \right]^2 \dd{x_1} \cdots \dd{x_n}

exists.
A square-integrable function can be approximated by an analytic function :math:`g'` such that the integral of :math:`(g - g')^2` over :math:`S` can be made arbitrarily small.

A :math:`C^{\infty}` function need not be analytic, so an analytic function is denoted :math:`C^{\omega}`.

An operator :math:`A` acts on functions defined on :math:`\rn`, and takes one function, :math:`f`, into another one, :math:`A(f)`.
Examples are multiplication, differentiation, and fixed-kernel integration.
The commutator of two operators is defined

.. math::

   \label{eq:4}
     [A,B](f) = (AB-BA)(f)


