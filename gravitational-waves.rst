***********************
Gravitational radiation
***********************

Non-stationarity
================

A non-stationary metric has a metric with some dependence on the time
coordinate, :math:`t`, and an important consequence of these metrics is
that they permit gravitational radiation.

Weak fields
===========

In the absence of energy and matter spacetime is flat and Mikowskian. We
can introduce a perturbation, however, to make the metric “nearly-flat”,
with the form

.. math::

   \label{eq:229}
     g_{\alpha \beta} = \eta_{\alpha \beta} + h_{\alpha \beta}

 Where :math:`\eta_{\alpha \beta} = \diag(-1,1,1,1)` is the Minkowski
metric, and :math:`\abs{h_{\alpha \beta}} \ll 1`. This spacetime still
obeys Lorentz transformations, :math:`\Lambda`, so

.. math::

   \label{eq:1}
     g'_{\alpha \beta} = \Lambda_{\alpha'}^{\mu} \Lambda_{\beta'}^{\nu} g_{\mu \nu} =  \Lambda_{\alpha'}^{\mu} \Lambda_{\beta'}^{\nu} \eta_{\mu \nu} +  \Lambda_{\alpha'}^{\mu} \Lambda_{\beta'}^{\nu} h_{\mu \nu} = \eta_{\alpha \beta}' + h_{\alpha \beta}'

 Gauge transformations can also be applied, with the form

.. math::

   \label{eq:2}
     x'^{\alpha} = x^{\alpha} + \xi^{\alpha}(x^{\beta})

 for :math:`\xi^{\alpha}` functions of the coordinates
:math:`\set{x^{\alpha}}`, and so

.. math::

   \label{eq:3}
     \Lambda_{\alpha}^{\beta} = \delta^{\alpha}_{\beta} + \xi_{,\beta}^{\alpha}

 We can demand that the :math:`\xi^{\alpha}` are small, so

.. math:: \abs{\xi^{\alpha}_{,\beta}} \ll 1 \quad \forall \alpha,\beta

 Thus by the chain rule

.. math::

   \label{eq:5}
     \Lambda_{\alpha}^{\gamma} = \delta^{\alpha}_{\gamma} - \Lambda^{\gamma}_{\beta} \Lambda^{\beta}_{\alpha} \approx \delta^{\alpha}_{\gamma} - \xi_{,\gamma}^{\alpha}

If the unprimed coordinate system is nearly Lorentz, then

.. math::

   \begin{aligned}
     g'_{\alpha \beta} &= \Lambda_{\alpha}^{\nu} \Lambda_{\beta}^{\nu} g_{\mu \nu} \\
   &= \qty( \delta_{\alpha}^{\mu} \delta_{\beta}^{\nu} - \xi_{,\alpha}^{\mu} \delta_{\beta}^{\nu} - \xi^{\nu}_{,\beta} \delta_{\alpha}^{\mu} ) \eta_{\mu \nu} + \delta_{\alpha}^{\mu} \delta_{\beta}^{\nu} h_{\mu \nu} \\
   &= \nu_{\alpha \beta} + h_{\alpha \beta} -\xi_{\alpha, \beta} - \xi_{\beta , \alpha}\end{aligned}

 This has the same form as equation ([eq:229]) provided that

.. math:: h'_{\alpha \beta} = h_{\alpha \beta} - \xi_{\alpha, \beta} - \xi_{\beta, \alpha}

Clearly the new primed system is also nearly Lorentz.

Einstein’s equations in weak fields
===================================

In the nearly Lorentz system we have a restricted number of coordinate
transforms which can be used so that the resulting system is still
nearly Lorentz.

To the first order for small perturbations the Riemann-Christoffel
tensor for a nearly-flat space is

.. math::

   \label{eq:7}
     \tensor{R}{_{\alpha \beta \gamma \delta}} = \half \qty( h_{\alpha \delta, \beta \gamma}+ h_{\beta \gamma, \alpha \delta} - h_{\alpha \gamma, \beta \delta} - h_{\beta \delta,\alpha \gamma} )

 The Ricci tensor can then be obtained,

.. math::

   \label{eq:8}
     R_{\mu \nu} = \half \qty( h^{\alpha}_{\mu, \nu \alpha} + h^{\alpha}_{\nu, \mu \alpha} - h_{\mu \nu,\alpha}^{,\alpha} - h_{, \mu \nu} )

 for
:math:`h \equiv h^{\alpha}_{\alpha} = \eta^{\alpha \beta} h_{\alpha \beta}`.
Also the Ricci scalar,

.. math::

   \label{eq:9}
     R = \eta^{\alpha \beta} R_{\alpha \beta}

 allowing the Einstein tensor to be found,

.. math::

   \begin{aligned}
     G_{\mu \nu} &= R_{\mu \nu} - \half \eta_{\mu \nu} R \nonumber\\
   &= \half \qty[h_{\mu \alpha,\nu}^{,\alpha} + h_{\nu \alpha,\mu}^{, \alpha} - h_{\mu \nu,\alpha}^{,\alpha} - h_{, \mu \nu} - \eta_{\mu \nu} \qty( h_{\alpha \beta}^{,\alpha \beta} - h_{,\beta}^{,\beta})]\end{aligned}

 By rescaling the metric perturbations,

.. math::

   \label{eq:10}
     \bar{h}_{\mu \nu} \equiv h_{\mu \nu} - \half \eta_{\mu \nu} h

 then

.. math::

   \label{eq:11}
     G_{\mu \nu} = - \half \qty[ \bar{h}_{\mu \nu, \alpha}^{,\alpha} + \eta_{\mu \nu}\bar{h}_{\alpha \beta}^{, \alpha \beta} - \bar{h}_{\mu \alpha, \nu}^{,\alpha} - \bar{h}_{\nu \alpha, \mu}^{, \alpha}]

 Since

.. math:: G_{\mu \nu} = 8 \pi T_{\mu \nu}

 it follows

.. math::

   \label{eq:12}
     - \bar{h}_{\mu \nu,\alpha}^{,\alpha} - \eta_{\mu \nu}^{,\alpha \beta} + \bar{h}_{\mu \alpha, \nu}^{, \alpha} + \bar{h}_{\nu \alpha, \mu}^{,\alpha} = 16 \pi T_{\mu \nu}

 We can always find a gauge in which the last three terms are zero—the
Lorentz gauge, which is equivalent to adopting the coordinate system in
which

.. math:: \bar{h}^{\mu \alpha}_{, \alpha} = 0

 (i.e. the metric with the divergence of perturbations equal to zero),
thus

.. math::

   \label{eq:13}
     - \bar{h}_{\mu \nu, \alpha}^{,\alpha} = 16 \pi T_{\mu \nu}

Solutions in free space
-----------------------

Solutions in free space will be solutions of

.. math::

   \label{eq:14}
      \eta^{\alpha \alpha } \bar{h}_{\mu \nu, \alpha \alpha} = \bar{h}_{\mu \nu, \alpha}^{,\alpha} = 0

 which written in slightly more familiar notation is

.. math::

   \label{eq:15}
     \qty( - \pdv[2]{t} + \nabla^2 ) \bar{h}_{\mu \nu} = 0

 moving out of geometrised units, setting :math:`\eta^{00} = -c^{-2}`,
then

.. math::

   \label{eq:16}
      \qty( - \pdv[2]{t} + c^2\nabla^2 ) \bar{h}_{\mu \nu} = 0

 This has the form of a wave equation.

Plane wave solutions
====================

The simplest solutions to a wave equation are plane waves, which in this
case will take the form

.. math::

   \label{eq:17}
     \bar{h}_{\mu \nu} = \Re\qty(A_{\mu \nu} \exp( i k_\alpha x^{\alpha}) )

 for :math:`A_{\mu \nu}` the amplitude of the waves, and
:math:`k_{\alpha}` the wavevector. :math:`A_{\mu \nu}` is a symmetric
tensor, by fortune of :math:`\bar{h}_{\mu \nu}` being symmetric, and
this reduces the 16 distinct components to 10. Next we have

.. math::

   \label{eq:18}
     \tensor{\bar{h}}{_{\mu \nu, \alpha}^{,\alpha}} = \eta^{\alpha \sigma} \bar{h}_{\mu \nu, \alpha \sigma} = 0

 and so

.. math:: k^{\alpha} k_{\alpha} = 0

 Thus the wavevector is null. The frequency is

.. math:: \omega = k^t = \qty( k_x^2 + k_y^2 + k_z^2)^{\half}

 We also have a Lorentz gauge condition,

.. math:: \tensor{\bar{h}}(^{\mu \alpha}_{, \alpha} = \qty(\bar{h}_{\mu}^{\alpha})_{, \alpha} = 0

 thus

.. math::

   \label{eq:19}
     A_{\mu \alpha} k^{\alpha} = 0

 So the wave amplitudes are orthogonal to the wavevector. These are four
equations, so we reduce from ten to six amplitude components. We can
then introduce a gauge fix to remove further terms,

.. math:: h_{\mu \nu}^{\text{new}} = h_{\mu \nu}^{\text{old}} - \xi_{\mu,\nu} - \xi_{\nu,\mu}

 Such that

.. math::

   \label{eq:20}
     G_{\mu \nu} = h^{\text{new}, \alpha}_{\mu \nu,\alpha}

 This transformation requires vector components which satisfy

.. math::

   \label{eq:21}
     \qty( - \pdv[2]{t} + \nabla^2 ) \xi^{\mu} = \tensor{\bar{h}}{^{\text{old} \mu \nu}_{, \nu}}

 This doesn’t define :math:`\xi^{\mu}` uniquely, and we can still add
new vector quantities to this, provided the same relations hold. This
has given another four equations, and so the number of free parameters
in the amplitude is now just two.

If we restrict the form of :math:`A_{\mu \nu}` to satisfy

.. math::

   \label{eq:22}
     A^{\mu}^{\mu} = \eta^{\mu \nu} A_{\mu \nu} = 0, \quad A_{\alpha \beta}u^{\beta} = 0

 then the gauge choice is that of the Transverse-Traceless gauge. In a
background Lorentz frame with :math:`u^{\beta} = \delta_t^{\beta}` this
implies :math:`A_{\alpha t} = 0 \ \forall \alpha`.

If the spatial axes are oriented so that the wave travels in the
positive :math:`z`-direction then

.. math:: A_{\alpha z} = 0 \ \forall \alpha

 and so

.. math::

   \label{eq:23}
     \trt{\bar{h}}_{\mu \nu} = \trt{A}_{\mu \nu} \cos[ \omega(t-z) ]

 Thus

.. math::

   \label{eq:24}
     \trt{h}_{\mu \nu} = \trt{B}_{\mu \nu} \cos[ \omega(t-z) ]

 where :math:`\ten{B}` has constant components.

The implications of all of the reductions are that in the TT gauge the
amplitude takes the form

.. math::

   \label{eq:25}
     \trt{A}_{\mu \nu} =
     \begin{bmatrix}
        0 & 0      & 0       & 0 \\
   0      & A_{xx} & A_{xy}  & 0 \\
   0      & A_{xy} & -A_{xx} & 0 \\
   0      & 0      & 0       & 0
     \end{bmatrix}

Free particles
==============

Consider a background Lorentz frame where a particle is initially at
rest, and the TT gauge is chosen. The particle has a geodesic trajectory
given by

.. math:: \dv{u^{\beta}}{\tau} + \Gamma^{\beta}_{\mu \nu} u^{\mu} u^{\nu} = 0

 The initial acceleration of the particle is then

.. math:: \qty( \dv{u^{\beta}}{\tau})_0 = - \Gamma^{\beta}_{tt} = -\half \eta^{\alpha \beta} (h_{\alpha t,t + h_{t \alpha, t} - h_{t t, \alpha}} )

 But in the TT gauge :math:`A_{\alpha t}=0`, so
:math:`\bar{h}_{\alpha t} = 0`, and :math:`A_{\mu}^{\mu} = 0`, so
:math:`\bar{h} = \bar{h}_{\mu}^{\mu} = 0`, so
:math:`h_{\alpha t} = 0 \ \forall \alpha`. Thus

.. math:: \qty( \dv{u^{\beta}}{\tau})_0 = 0

 Thus a particle initially at rest stays at rest. Instead consider the
proper distance, between particles at :math:`x=0` and
:math:`x=\epsilon`.

.. math::

   \label{eq:26}
     \Delta \ell = \int \abs{ g_{\alpha \beta} \dd{x^{\alpha}} \dd{x^{\beta}}}^{\half} = \int_0^{\epsilon} \abs{g_{xx}}^{\half} \approx \epsilon \sqrt{g_{xx}(x=0)}

Thus

.. math::

   \label{eq:27}
     \Delta \ell \approx \qty[ 1 + \half \trt{h}_{xx} (x=0)] \epsilon

 Thus a passing gravitational wave produces a change in the proper
distance between test particles.

Now consider the geodesic deviation. Let :math:`\xi^{\alpha}` be the
vector connecting the test particles, then for a weak field

.. math::

   \label{eq:28}
     \pdv[2]{\xi^{\alpha}}{t} = R^{\alpha}_{\mu \nu \beta} u^{\mu} u^{\nu} \xi^{\beta}

 The particles are initially at rest, so :math:`u^{\mu} = (1,0,0,0)` and
:math:`\xi^{\beta} = (0, \epsilon, 0, 0)`. Thus

.. math::

   \label{eq:29}
     \pdv[2]{\xi^{\alpha}}{t} = \epsilon R^{\alpha}_{ttx} = - \epsilon R^{\alpha}_{txt}

 The RC tensor is then

.. math::

   \begin{aligned}
       R^x_{txt} &= \eta^{xx} R_{xtxt} = - \half \trt{h}_{xx,tt} \\
   R^y_{txt} &= \eta^{yy} R_{ytxt} = - \half \trt{h}_{xy,tt}
     \end{aligned}

Thus

.. math::

   \begin{aligned}
     \label{eq:30}
     \pdv[2]{t} \xi^x &= \half \epsilon \pdv[2]{t} {\trt{h}_{xx}} \\
   \pdv[2]{t} \xi^y &= \half \epsilon \pdv[2]{t} \trt{h}_{xy}\end{aligned}

If we assemble a ring of test particles we can measure the polarisation
of a gravitational wave. Say we now assemble the test particles at
:math:`x = \epsilon \cos(\theta)` and at :math:`y = \epsilon
\sin(\theta)`, then

.. math::

   \begin{aligned}
       \pdv[2]{t} \xi^x &= \half \epsilon \cos(\theta) \pdv[2]{t} \trt{h}_{xx} + \half \epsilon \sin(\theta) \pdv[2]{t} \trt{h}_{xy} \\
   \pdv[2]{t} \xi^y &=  \half \epsilon \cos(\theta) \pdv[2]{t} \trt{h}_{xy} - \half \epsilon \sin(\theta) \pdv[2]{t} \trt{h}_{xx}
     \end{aligned}

The solutions to these equations take the form

.. math::

   \begin{aligned}
       \xi^x &= \epsilon \cos(\theta) \qty( 1 + \half \trt{B}_{xx} \cos(\omega t)) + \half \epsilon \sin(\theta) \trt{B}_{xy} \cos(\omega t) \\
   \xi^y &= \epsilon \sin(\theta) \qty( 1 - \half \trt{B}_{xx} \cos(\omega t) ) + \half \epsilon \cos(\theta) \trt{B}_{xy} \cos(\omega t)
     \end{aligned}

These describe the equations of ellipses. As a wave passes by the
circular ring of test particles it deforms it into an ellipse, and then
back.

Gravitational radiation has two distinct polarisation states which are
illustrated in figure [fig:polarisation], and from this it is clear that
gravitational radiation is invariant under a 180 degree rotation around
its direction of propagation, compared to the 360 degree rotation for
electromagnetic radiation, or the 720 degree rotation. This can be
understood in terms of the gauge bosons of the fields.

In general, the classical radiation field of a particle with spin
:math:`S` is invariant under a rotation of :math:`360^{\circ}/S`. A
photon has spin :math:`S=1`, so clearly a graviton must be spin
:math:`S=2`.

Gravitational wave amplitude
============================

We always expect the received gravitational radiation at the earth to
have a very small amplitude, thanks to the inverse square relationship,
even if the metric where it was produced was a strong field metric. In
such a situation :math:`\abs{h_{\alpha \beta}}\sim 1`, close to the
source, when :math:`r \sim M`, but at any distance :math:`r`,

.. math::

   \label{eq:32}
     \abs{H_{\alpha \beta}} \sim \frac{M}{R}

 Even the formation of a blackhole in the Andromeda Galaxy would only
produce perturbations around

.. math:: h_{\alpha \beta} \sim 6\e{-19}

 (and even this is a severe over-estimate). Hence, detecting
gravitational radiation is a severe technological challenge.

Quadrupolarity
==============

In electromagnetic theory the dominant form of radiation is produced by
electric dipole radiation, where the luminosity output has the form

.. math::

   \label{eq:33}
     L~{ed} \propto e^2 \vec{a}^2 \propto e^2

 for an acceleration of :math:`\vec{\alpha}` and distance
:math:`\vec{d}` between two particles of charge :math:`e`. This is
proportional to the second time derivative of the magnetic dipole
moment,

.. math:: L~{ed} \propto \ddot{\mu}

In gravitation the equivalent of the electric dipole is the mass dipole,
and the mass dipole moment is

.. math::

   \label{eq:34}
     \vec{d} = \sum_{A_i} m_i \vec{x}_i

 for :math:`m_i` the rest mass, and :math:`\vec{x}_i` the position of
the :math:`i`\ th particle. The total linear momentum, :math:`\vec{p}`,
is then

.. math::

   \label{eq:35}
     \vec{p} = \vec{d} - \sum_i m_i \vec{x}_i

 Total linear momentum is conserved, so there cannot be mass dipole
radiation from any source. The magnetic dipole corresponds to the total
angular momentum, and this too is conserved, so the mass dipole has zero
luminosity. Quadrupole radiation is the lowest order form possible.
