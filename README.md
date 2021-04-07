# [ls4](#)

> A PLTL-prover based on labelled superposition with partial model guidance


**LS4** : A PLTL-prover based on labelled superposition with partial model guidance.

**LS4**  [1] is a prover for Propositional Linear Temporal Logic (PLTL). On the logic side, it is based on the calculus LPSup [2]. 
However, instead of saturating the given clause set, it uses partial models to guide the inference process.

**LS4** uses the Minisat 2.2 SAT-solver as its internal solving engine. 

**[1] PLTL-Prover Based on Labelled Superposition with Partial Model Guidance** <br>
Suda M., Weidenbach C., in IJCAR 2012 (eds. B. Gramlich, D. Miller, and U. Sattler), LNAI 7364, pp. 537-543. Springer, Heidelberg (2012) 

**[2] Labelled Superposition for PLTL** <br>
Suda M., Weidenbach C., in LPAR-18 (eds. N. Bjorner and A. Voronkov), LNCS 7180, pp. 391-405. Springer, Heidelberg (2012)

### To compile:

```bash
cd core
make         # for an optimized version, but with asserts and debug info
make r       # for a release version (optimized, no asserts, no debug info)
make d       # for a debug version (unoptimized, asserts, debug info)
````

> Note: Although the sources of the used aiger library are provided, they are not compiled automatically by the makefile. That's why  a compiled module aiger.o is also included. It is a 64bit version of the library. If you need to compile ls4 for 32bit, either rename the provided file aiger.o_32 to aiger.o and then run make, or persuade the makefile to compile aiger.o for you from the sources.

### To run:

```bash
./ls4 spec_cl_5.trp

./ls4 -format=aiger cuhanoi4.aig

./ls4 --help
```

The relevant options are:
<pre>
INPUT OPTIONS, 
(AIGER OPTIONS) and 
MAIN OPTIONS.
</pre>
The other categories are inherited from Minisat and their effect on ls4 has not been tested.
