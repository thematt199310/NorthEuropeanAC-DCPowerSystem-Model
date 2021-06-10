# Northen European AC/DC Power SystemModel

Detailed phasor-approximated, time-domain model of the Nordic countries (Denmark, Norway, Sweden and Finland).

This document contains some information about the model "Northern European AC/DC Power System" and how to use it.
Note that the document does not provide any tutorial on how to use the software DigSilent PowerFactory, and 
user's proficiency with it is assumed. For that you can visit: https://www.digsilent.de/en/


*------------------------------------------------------------------------------------------------------------------*

List of files:

** NEACDCPS.pfd\
This file contains all the data associated to the model topology and control of elements, and is provided in the
Digsilent PowerFactory project file format *.pfd. Note: the file was produced with 2018 version and there might be
performance issues associated with different software versions.

*------------------------------------------------------------------------------------------------------------------*

The model contains 38 grid elements distributed across several folders. Each grid elementcontains specific part of 
the system:

** HVDC_LCC folder contains HVDC-LCC type links\
** HVDC_VSC folder contains HVDC-VSC type links\
** Kriegers-Flak Interconnector contains Kriegers-Flak link and related objects, controls\
** Nordic Power System contains Country level modeling\
** Three-island Topology contains North Sea Wind Power Hub (NSWPH) modeling

At any time, 37 out of 38 grids must be active. If it is not the case, load-flow errors might occur.

Two study cases are created: 

** Scenario 1 with NSWPH low-inertia scenarion active\
** Scenario 2 with NSWPH zero-inertia scenarion active

Study cases contain information about parts of the network model(s) considered for calculation, calculation setting,
study time and calculation result file to be stored for reporting.

The result file contains the following variables:

** >300kV bus voltage\
** Active power between >300kV buses\
** Active power for HVDC links\
** Frequency of 10 machines involved in Frequency Containment Reservers in Nordic Power System\
** Frequency for Continental Europe and Great Britain equivalent grids\
** NSWPH related variabels: active power of the offshore converters, hub voltage and frequency, WPP active power
