***************************
Multimessenger observations
***************************

The advent of the first binary neutron star observation,
GW170817 :cite:`2017PhRvL.119p1101A`, to be observed by
detectors served as the advent of a new era in observational
astrophysics, with now able to sit alongside conventional
electromagnetic observations to probe the astrophysical nature of some
of the most extreme events in the universe.

When the same astrophysical object or event is observed through multiple
different observational approaches, or *messengers* the event is deemed
to be a event. There are four messengers of which observations are
currently made: electromagnetic radiation, gravitational waves, high-energy particles, and cosmic rays  [1]_.

Multimessenger astronomy: A very brief history
==============================================

While the discovery of GW170817 marked the beginning of with , it did
not mark the beginning of as a field. The earliest observations can be
traced to astroparticle observations of the solar flares in the
1940s :cite:`2015paas.book.....S`. The observation of
SN1987A, a type-II supernova in the Large Magellanic Cloud, was made
first in visible light at Las Campanas, but also later in ultraviolet.
Around three hours prior to the event’s detection in , a number of
observatories detected a burst of antineutrinos (with around 25
particles observed across three observatories). The first detection of
gravitational waves was made in 2015, with the observation of a
coalescence, and just under two years later the first observation of
from a coalescence was made, which coincided with a observed by the
Fermi satellite. An extensive observing campaign was launched as a
result of these observations, with observatories covering the entire
spectrum making observations of the event. These will be discussed in
detail in the section discussing GW170817.

Multimessenger astrophysical sources
====================================

The anticipated sources of gravitational wave signals fall into two
broad categories: transient sources, which produce a burst of over a
short period of time; and sources, which produce continuously. A number
of transient sources are considered as promising targets for astronomy,
and these are often referred to as *bright*.

Black hole coalescences
-----------------------

+------+-------+-------+------+
| EM   | GW    | HEN   | CR   |
+------+-------+-------+------+
| No   | Yes   | No    | No   |
+------+-------+-------+------+

events are not generally anticipated to be promising sources for
emission, despite being the most frequently observed source of , and the
result of the most energetic events in the observed universe. There has,
however, been speculation that under certain circumstances emission
could be produced as a result of a
coalescence :cite:`2016ApJ...819L..21L,2017ApJ...839L...7D`,
partly driven by the apparent observation of gamma rays around following
the signal from GW150914 :cite:`2016ApJ...826L...6C}`  [2]_.

Neutron star coalescences
-------------------------

+-------+-------+-------+------+
| EM    | GW    | HEN   | CR   |
+-------+-------+-------+------+
| Yes   | Yes   | ?     | No   |
+-------+-------+-------+------+

In contrast to coalescences, mergers are expected to produce large
quantities of radiation. These have long been assumed to be the source
of , and the observation of GW170817 provided strong confirmation that
they are the engine for at least a subset of observed .

    The initial emission is expected to be from high-energy, collimated
    gamma rays from the initial fireball.

kilonova
    UV through IR emission from nuclear processes in the
    ejecta :cite:`2010MNRAS.406.2650M`.

radio emission
    Resulting from the interaction of the jet with the interstellar
    medium.

Supernovae
----------

+-------+------+-------+------+
| EM    | GW   | HEN   | CR   |
+-------+------+-------+------+
| Yes   | ?    | Yes   | No   |
+-------+------+-------+------+

emission from supernova has been observed since 1064CE, when the which
created the Crab Nebula occurred and was observed by astronomers in
China (although an event in 0185 which was also observed in China may
also have been a supernova). The first observation of a occurred in
1987, SN 1987A, which was close enough (in the Large Magellanic Cloud)
that it could be observed in detail as it evolved. are known to emit
thermal neutrinos (neutrinos were detected from SN
1987A :cite:`1988PhRvD..38..448H`) and there are potential
mechanisms for the production of high energy neutrinos in as
well :cite:`2019arXiv190712506M`. We expect to be produced
during a core-collapse thanks to the asymmetrical nature of the
explosion, but the physics of are poorly understood, and as a result the
strength of signals from is unknown.

Blazars
-------

+-------+------+-------+------+
| EM    | GW   | HEN   | CR   |
+-------+------+-------+------+
| Yes   | No   | Yes   | ?    |
+-------+------+-------+------+

A blazar is an with a relativistic jet which is directed towards the
observer. A muon neutrino was detected from the blazar ``TXS 0506+056``
on 22 September 2017: the blazar had previously been observed in radio,
but this was the first detection of a source. ``TXS 0506+056`` is also a
gamma ray source, and the 2017 neutrino event coincided with it flaring
in gamma rays. This some evidence that ``TXS 0506+056`` should be a
source of pions, since the production of is likely a result of pion
decay. No cosmic rays from this source have been observed, however.

Pulsars
-------

+-------+------+-------+------+
| EM    | GW   | HEN   | CR   |
+-------+------+-------+------+
| Yes   | ?    | No    | No   |
+-------+------+-------+------+

Pulsars are neutron stars which produce a relativistic jet which can be
observed in radio. Neutron stars are known to be extremely spherical,
however any ellipticity or irregularities in the shape (like mountains)
will result in the star having a quadrupole moment, and therefore
producing as it rotates. To date no from pulsars have been observed, and
this allows an upper limit to be placed on the size of any mountains on
the surface of nearby pulsars (as of O2 the largest mountain would be
around :math:`\SI{5}{\centi\meter}`
:cite:`2019PhRvD..99l2002A`  [3]_).

Preparing GW alerts
===================

While detections can be interesting in their own right, the development
of relies on rapid communication between the detectors and
observatories. This is challenging, as not all events are likely to
produce emission, and the location of the event in the sky must be
determined. Once these quantities are determined events are reported
using the and on ``GraceDB`` (see
https://gracedb.ligo.org/superevents/public/O3/).

Localising GW signals on the sky
--------------------------------

If a network of at least two geographically separated detectors observes
a signal it is possible to ascertain the location in the sky,
:math:`\hat{\vec{\Omega}}`, from the difference in arrival times between
the two sites. For a detector at a position, :math:`\vec{r}_{D}`, and an
arbitrary reference location, :math:`\vec{r}_{0}`, this time delay,
:math:`\delta t`, will be

.. math::

   \label{eq:intro:detectors:timedelay}
   \delta t (\hat{\vec{\Omega}}) = \frac{1}{c} (\vec{r}_{0} - \vec{r}_{D}) \cdot \hat{\vec{\Omega}}.


This allows the location of the signal to be confined to a ring on the
sky corresponding to constant :math:`\Delta t`. Examples of these rings
for a source are plotted in figure [fig:det:advanced-timing]. Timing
uncertainty in the signal, which arises both from clock uncertainties
and uncertainties in defining a reference point in the received signal
increase the area of this region. As more detectors are added to the
network it is possible to reduce this area, as increasing the number of
detector pairs works to reduce the sky area compatible with the observed
delay times.

.. figure:: figures/timing-circles.*
   :alt: The isochrones for the 2nd generation detectors.


   Isochrones for the three detector pairs in the advanced
   network. For a single detector pair the localisation is a ring; with
   three detectors there are three pairs of detectors, and so three
   rings, and we can reduce the plausible locations the signal could
   have come from to the two places where all of the rings overlap.
   Isochrones for the three detector pairs in the advanced network. For
   a single detector pair the localisation is a ring; with three
   detectors there are three pairs of detectors, and so three rings, and
   we can reduce the plausible locations the signal could have come from
   to the two places where all of the rings overlap. 

Additional localisation information can be attained from the observed
amplitude of the signal in each detector. The signal will be convolved
with the antenna pattern (see figure [fig:det:aligo-antenna]); as each
detector is insensitive to some regions of the sky, the total plausible
localisation of the signal is reduced.

For a approaching the detector from an azimuth (relative to one of the
arms) and altitude (relative to the plane of the detector),
:math:`(\alpha, \delta)` on the sky these patterns for the :math:`+`-
and :math:`\times`-polarisations, :math:`F_{+}` and :math:`F_{\times}`,
will be

.. math::

   \begin{aligned}
   \label{eq:detectors:antennapattern:plus}
   F_{+} &= \frac{1}{2} (1 + \sin^{2}\delta) \cos 2\alpha \cos 2\psi - \sin\delta\sin 2 \alpha \sin 2 \psi \\
   F_{\times} &=  \frac{1}{2} (1 + \sin^{2}\delta) \cos 2\alpha \sin 2\psi - \sin\delta\sin 2 \alpha \cos 2 \psi.\end{aligned}

where :math:`\phi` is the polarisation angle of the .

.. figure:: figures/aligo-antenna-pattern
   :alt:
   Antenna pattern of an aLIGO detector, normalised so that the
   locations which the detection is most sensitive to are labelled
   :math:`1`, and those it is insensitive to are labelled :math:`0`.

   Antenna pattern of an aLIGO detector, normalised so that the
   locations which the detection is most sensitive to are labelled
   :math:`1`, and those it is insensitive to are labelled :math:`0`. 

Determining EM bright
---------------------

It’s important to be able to determine if the source of a is likely to
produce radiation which can be observed by conventional observatories.
An important part of this is determining if the source of a signal was a
or a . To do this we need to consider two quantities: the of the system,
which can be measured directly from the waveform, and the compactness of
the system, which can be determined by identifying the moment that the
system merges in the waveform.

The , :math:`\chirpmass`, can be determined if the frequency,
:math:`f_{\text{GW}}`, and the frequency derivative,
:math:`\dot{f}_{\text{GW}}`, with respect to time of the are
measured :cite:`2017AnP...52900209A`:

.. math::

   \label{eq:chirp-mass-frequency}
   \chirpmass = \frac{c^3}{G} \left[ \left( \frac{5}{96} \right)^{3} \pi^{-8} f_{\text{GW}}^{-11} \dot{f}_{\text{GW}}^{3} \right]^{1/5}.

This can be integrated with respect to time to remove the explicit
dependence on :math:`\dot{f}_{\text{GW}}`:

.. math::

   \label{eq:chirp-mass-frequency-int}
   f_{\text{GW}}^{-8/3} (t) = \frac{(8 \pi)^{8/3}}{5} \left( \frac{G \chirpmass}{c^3} \right)^{5/3} (t_{\text{c}} - t),

 where :math:`t_{\text{c}}` is the time at which the two objects
coalesce. Thanks to this equation it is possible to determine the chirp
mass using the time periods between zero-crossings of the signal.

The gives an important indicator that a system is a rather than a ,
since there are good physical reasons to believe neutron stars have an
upper mass limit (the Tolman-Oppenheimer-Volkoff limit) around
:math:`2.17\,\solMass`. It does not, however, exclude the system being
the result of two low-mass black holes coalescing. To exclude this
possibility we must calculate the compactness of the binary close to the
merger: black holes are physically denser and more compact than neutron
stars, and so can produce a more compact orbit before merging.

The compactness of the system will be affected by spin and orbital
eccentricity, but for simplicity we can consider the compactness of a
non-spinning system where the orbit close to the merger is almost
circular  [4]_. This can be determined by measuring the frequency of the
orbit immediately prior to the merger, :math:`\omega_{\text{max}}`,
which coincides with the time when the amplitude is greatest (recalling
that the frequency is **twice** the orbital frequency). The orbital
separation, :math:`R` of the objects in the binary is

.. math::

   \label{eq:oribital-separation}
   R = \left( \frac{GM}{\omega_{\text{max}}^2} \right)^{1/3},

 where :math:`M` is the total mass of the binary.

For a similar to GW150914, where :math:`M \approx 70\,\solMass` we find
that :math:`R = \SI{350}{\kilo\meter}`: this is small in comparison to
the normal diameters of stars, but it’s a little difficult to see the
implications of this for compact objects.

To help with this we introduce the compactness ratio,
:math:`\mathcal{R}`, which is the ratio of :math:`R` to the Schwarzchild
radius, which is the smallest possible radius of a compact object.

.. math:: r = \frac{2Gm}{c^{2}} \approx 2.95 \left( \frac{m}{\solMass} \right) \,\text{km}

In the GW150914-like case above :math:`\mathcal{R} \approx 1.7`, since
the Schwarzchild radius of the individual objects is
:math:`\SI{103}{\kilo\meter}`. For a system we expect
:math:`\mathcal{R}` between around :math:`2` and :math:`5`.

Transient astronomy
===================

Gamma-ray burst observatories
-----------------------------

There are currently four major gamma-ray burst observatories located on
Earth-orbitting satellites.

    A gamma ray detector on the Neil Gehrels *Swift* Observatory with a
    large field of view (over 1 steradian with high positional accuracy,
    and three with lower accuracy–the whole sky is :math:`4 \pi`
    steradians) which can roughly localise a within 15 seconds.

    A gamma ray detector on the Fermi Gamma-ray Space Telescope which is
    composed of twelve scintillation detectors giving whole-sky coverage
    (except for the part of the sky obscured by the Earth).

INTEGRAL
    The INTEGRAL satellite, like , provides all-sky coverage and
    localisation of .

AGILE
    A gamma ray telescope with a narrower field of view than the other
    three instruments which are dedicated to detection, but which has
    observed a large number of .

The proposed THESEUS mission, under development by the European Space
Agency is a and X-ray observatory planned for launch around 2032. The
timing of this mission’s launch would mean that both THESEUS and would
be observing simultaneously.

Optical surveys
---------------

Optical surveys are an important aspect of transient astronomy, and they
promise to allow very rapid detection of short-lived astrophysical
events such as supernovae and kilonovae. While sky surveys are nothing
new in the world of astronomy, dating back to the development of
catalogues such as Messier’s in the 18th Century, the ability to conduct
a survey over a very large area of the sky very rapidly has only become
possible thanks to development in both sensor technology and data
processing techniques in the last decade. A current example of such a
survey telescope is the :cite:`2014htu..conf...27B`, which
is capable of imaging a 47 square degree area of the sky in a single
exposure, allowing the entire Northern hemisphere sky to be imaged every
three nights, to a limiting magnitude around 20.5. The produces large
quantities of data every night, but this will be dwarfed by the quantity
of data produced by the . This facility, which has been designed
specifically for rapid all-sky surveys (compared to , which is an
instrument placed on an exisiting telescope) will produce around ten
times more data, around 15 terabytes per night, proving a formidable
challenge to both data processing and analysis. Other important
programmes in transient astronomy include the One-Meter Two-Hemisphere
collaboration (comprising the Swope Supernova Survey in Chile, and the
Nickel Telescope in California) who were the first to discover the
optical counterpart to GW170817 :cite:`2017Sci...358.1556C`,
and on a somewhat longer timescale, ESA’s *Gaia*
mission :cite:`2019IAUS..339...12B`.

Challenges for GW event follow-up
=================================

While preparing alerts based on observations is challenging, attempting
to make observations to follow these up is not without problems. The
localisation of most events is poor, meaning that the event could
originate anywhere within a large patch (or large patches) of the sky.
The majority of observatories can perform observations over only a small
field of view, however, and the emission related to a event may be
short-lived. As a result an observatory must be able to rapidly survey a
large area of sky with high sensitivity.

The sky localisations which are published by detectors are divided into
observing “tiles” by each follow-up observatory . The size of each tile
will vary depending on the sensitivity and field-of-view of the
telescope. Each tile is then prioritised using probability information
from the
analysis :cite:`2017ApJ...834...84C,2019MNRAS.489.5775C`,
and taking into account difficulties in moving the telescope and the
period of local night.

GW170817: A case-study
======================

[sec:gw170817]

|image|

On 17 August 2017, during the second observing run of advanced LIGO, and
a few days after advanced Virgo had started making observations a
signal, GW170817, was detected by both LIGO detectors and the Virgo
detector. In contrast to previous detections which had all been signals,
GW170817 was identified as being produced by a system.

Independently of the detection the Fermi and INTEGRAL satellites
detected a slightly less than two seconds after the time the was
detected in . GCN alerts were issued rapidly for both the Fermi
detection (within 14 seconds) and the LIGO/Virgo detection (within 40
minutes).

The (recently-expanded) three detector network initially localised the
signal to within 31 square degrees in the southern celestial hemisphere,
however later analysis allowed this to be reduced to a 28 square degree
patch of sky. The localisation areas from the various detections are
shown in figure [fig:gw170817-localisation] for the detections in green
and the detections in blue.

The three-detector localisation was calculated by around 17:54 UTC,
which allowed telescopes in South America to search the localisation
area for an optical transient  [5]_. The Swope supernova survey was the
first collaboration to observe the
transient :cite:`2017ApJ...848L..12A,2017Sci...358.1556C`
(although six observatories would independently discover the optical
counterpart :cite:`2017ApJ...848L..12A`). The optical
counterpart was observed in NGC 4993.

The highly-precise localisation which was produced by imaging the
optical counterpart allowed observations to be made across the entire
spectrum.

Ultraviolet emission was detected 15.3 hours after the event by Swift,
and 9 days later X-ray emission was detected by the Chandra X-ray
Observatory. 16 days after the was observed radio emission was observed
by the VLA in New Mexico.

observations continued until 2019, with the Hubble Space Telescope
unable to detect any optical afterglow after 584
days :cite:`2019ApJ...883L...1F`. Superluminal radio
emission was also reported :cite:`2018Natur.561..355M`
between 75 and 230 days after the merger.

Cosmology from multimessenger astronomy
=======================================

The observation of an counterpart to GW170817 allowed the galaxy it
originated in to be identified. In turn this allowed the recession
velocity of the to be determined with high precision from its redshift.
The detection allows the distance to the source to be measured directly
(although with a fairly large uncertainty, thanks to a degeneracy
between the distance to the source and the angle at which it is inclined
relative to the observer.

Since the distance, :math:`d`, and recession velocity, :math:`v`, are
related by Hubble’s Law,

.. math::

   \label{eq:hubble-law}
   v = H_{0} d

if we know both :math:`v` and :math:`d` we can infer :math:`H_{0}`.

The distance to the source of GW170817 inferred from the is
:math:`d = \SI[parse-numbers=false]{48.8^{+2.9}_{-6.9}}{\mega\parsec}`,
and the measured recession velocity is
:math:`v = \SI{3017\pm166}{\kilo\meter\ \second^{-1}}`.

This allowed :math:`H_{0}` to be inferred to be
:math:`\SI[parse-numbers=false]{70.0^{+12.0}_{-8.0}}{\kilo\meter\ \second^{-1}\ \mega\parsec^{-1}}`
 :cite:`2017Natur.551...85A`.

.. figure:: figures/H0-inference
   :alt: The posterior probability density function of the inferred
   value of the Hubble constant, :math:`H_{0}` using observations of
   GW170817, compared to the value inferred from Planck observations of
   the cosmic microwave background (green) and from supernovae (orange).
   The -based inference is not sufficiently precise to resolve the
   tension between these two estimates.

   The posterior probability density function of the inferred value of
   the Hubble constant, :math:`H_{0}` using observations of GW170817,
   compared to the value inferred from Planck observations of the cosmic
   microwave background (green) and from supernovae (orange). The -based
   inference is not sufficiently precise to resolve the tension between
   these two estimates. 

While we get the greatest amount of information from events which can be
localised by observations, it is also possible to infer the Hubble
constant using only observations. This means that events can be used,
which are much more frequently observed than events.

In order to make inferences without knowing which galaxy the event
occurred in we need accurate three-dimensional galaxy catalogues. By
identifying a list of galaxies which lie within the localised volume
(through the sky localisation and distance estimate of the ) we can use
a Bayesian analysis to combine the inferences from each plausible galaxy
to give an overall
estimate :cite:`2019arXiv190806050G,2019arXiv190806060T`.

From the first two observation runs’ detections it is possible to update
the GW170817-only estimate of :math:`H_{0}` to
:math:`\SI[parse-numbers=false]{68.0^{+14.0}_{-7.0}}{\kilo\meter\ \second^{-1}\  \mega\parsec^{-1}}`
 :cite:`2019arXiv190806060T`.

.. figure:: figures/H0-statistical
   :alt: The posterior probability density function for :math:`H_{0}`
   inferred using a statistical method and observations from the O1 and
   O2 observing runs for advanced LIGO and Virgo.
    :cite:`2019arXiv190806050G,2019arXiv190806060T`

   The posterior probability density function for :math:`H_{0}` inferred
   using a statistical method and observations from the O1 and O2
   observing runs for advanced LIGO and Virgo.
    :cite:`2019arXiv190806050G,2019arXiv190806060T`

GW follow-up of EM events
=========================

In addition to attempts to identify electromagnetic counterparts to
signals, there are ongoing efforts to identify signals produced by
events observed by observatories. Thanks to the near-continuous,
all-sky, broadband observations made by a network of detectors, it is
possible to conduct searches for counterparts in high-latency in
recorded data (whereas an observatory may need to be pointed to the
appropriate area of sky, for example).

There have been targeted searches for from , motivated by observations.
The sky localisation provided by the observation simplifies the process
of searching for the signal :cite:`2019arXiv190803584T`.

Pulsars are the most promising source of continuous , and since these
are observed by radio telescopes, which can determine their rotation
frequency we can target searches for from pulsars both by sky location
and frequency (the frequency is twice the rotation frequency, since are
emitted from the quadrupole mode). To date we’ve not been successful in
detecting from pulsars, but the non-detection allows us to place limits
on the physical properties of known
pulsars :cite:`2019PhRvD..99l2002A`. Pulsars are also
observed to *glitch* when observed in radio: a glitch is a sudden change
in the rotational frequency of the pulsar; the mechanism which causes
these is poorly understood, but may produce . The time at which these
glitches occur is well known from observations, so searches for these
can be carried out over a short stretch of
data :cite:`2019PhRvD.100f4058K`.

Observations are made of frequently, and events are known to be a
progenitor source for these events. These events are very well localised
in time, however gamma ray detectors are not normally able to give a
very precise sky localisation for an event, so a search can be made over
a short span of detector data, but a large sky
area :cite:`2019arXiv190701443T`.

The future: multi-band multimessenger astronomy
===============================================

The current generation of detectors are designed to operate in a
frequency range where the merger and ringdown components of a or
low-mass system will produce a detectable signal. However, space-based
detectors, such as , will be able to make observations at much lower
frequencies. As a result the inspiral of these events will be observable
for a much longer period of time than is currently possible.

For an inspiralling event the frequency of the inspiral signal can be
used to predict the time at which the two systems will
merge :cite:`1994PhRvD..50.7111S`. This means if the lowest
frequency a detector can measure an inspiral signal at is
:math:`f_{\text{low}}` then the time, :math:`t`, between observing the
start of the inspiral and the merger is approximately

.. math::

   \begin{aligned}
   \label{eq:sources:cbc:time-until-coalescence}
   t &\approx \frac{5}{256} \left( \frac{G \chirpmass}{c^3} \right)^{-\frac{5}{3}} ( \pi f_{\text{low}} )^{- \frac{8}{3}} \\
     &\approx 2.16 \left(\frac{\chirpmass}{1.22 \solMass} \right)^{-\frac{5}{3}} \left( \frac{f_{\text{low}}}{\SI{100}{\hertz}} \right)^{- \frac{8}{3}} \quad\text{sec}\end{aligned}

 where :math:`\chirpmass` is the . For a system the will be around
:math:`\SI{1.25}{\solMass}`.

.. figure:: figures/inspiral-time
   :alt: The physical time until coalescence for an inspiralling binary
   system, given a chirp mass (:math:`y`-axis), for the system, and a
   signal frequency (:math:`x`-axis).

   The physical time until coalescence for an inspiralling binary
   system, given a chirp mass (:math:`y`-axis), for the system, and a
   signal frequency (:math:`x`-axis).

.. [1]
   Within the solar system, and more broadly, the heliosphere, it’s
   possible to argue that additional messengers exist, for example,
   through sample return missions, or magnetometer measurements,
   however, these are not available for the vast majority of the
   universe, so I’ll not give them any further consideration here.

.. [2]
   Though it’s generally accepted that this was a coincidence, as no
   event following this one has been coincident with an event, and the
   poor localisation of the GW150914 signal provides little evidence
   that the two events were spatially coincident.

.. [3]
   If the Earth was equivalently spherical the highest mountains would
   be around :math:`\SI{25}{\meter}` high.

.. [4]
   For a fuller discussion of the effects of spin and the orbit on the
   determination of the orbital compactness see section 4
   of :cite:`2017AnP...52900209A`.

.. [5]
   The search was complicated by the proximity of the search region to
   the sun, which meant observations were only possible shortly after
   the onset of twilight for optical telescopes.

