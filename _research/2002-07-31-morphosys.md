---
title: 'MorphoSys'
subtitle: 'SIMD Predication'
date: 2002-07-31 00:00:00
description: A novel branch predication scheme for the MorphoSys reconfigurable cell array.
featured_image: '/images/research/morphosys/morphosys.png'
---

[MorphoSys](http://www.eng.uci.edu/morphosys/) is a [reconfigurable computer architecture](http://en.wikipedia.org/wiki/Reconfigurable_computing) that is composed of a software programmable processing unit called TinyRISC and a reconfigurable hardware unit called Reconfigurable Cell Array (RC Array). The Reconfigurable Cell Array has 64 reconfigurable cells arranged in an 8 by 8 array. Each cell has an ALU/MAC unit and a register file. RC Array functionality and the interconnection network are configured through context words. Context words are stored in a context memory in two blocks (one for the rows and the other one for the columns). Each block has eight sets of sixteen context words.

I developed a novel [branch predication](http://en.wikipedia.org/wiki/Branch_predication) scheme for the MorphoSys Reconfigurable Cell Array by improving and combining the unrestricted predication model and the guarded execution model. It could be shown that significant execution autonomy was added to the SIMD processing elements and that the code size was reduced considerably. The implemented predication scheme enables more efficient if-conversion compilations than previous predication schemes of general purpose processors.

This work was supported by the [Defense Advanced Research Projects Agency (DARPA)](http://en.wikipedia.org/wiki/Darpa) ([DoD](http://en.wikipedia.org/wiki/United_States_Department_of_Defense)) under contract F-33615-97-C-1126 and the [National Science Foundation](http://en.wikipedia.org/wiki/National_Science_Foundation) under grant CCR-0083080.
