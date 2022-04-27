

Why3 files accompanying the paper "A verified VCGen based on Dynamic Logic: an exercise in meta-verification"

## Files 

* [dl.why]: formalization  of WhileDL
* [examples.why]: some examples involving validity and inference of update triples 
* [upd-simpl.mlw]: update simplifcation
* [dl-vcgen.mlw]: logic VCGen     
* [dl-exec-vcgen.mlw]: execution VCGen
* proof session folders for all of the above
* html proof summary files for all of the above

## Example commands

* `why3 ide x.why -L .`: (executed in the top-level folder) launches the Why3 IDE with file x.why 
* `why3 replay x -L .`: replays the proof session for x (assuming all the above SMT solvers are present in the local setup)
* `why3 replay --smoke-detector=top x -L .`: replays the proof session for x (assuming all the above SMT solvers are present in the local setup)


## Tool versions used in this development 

* Why3 platform, version 1.4.0
* Alt-Ergo 2.4.0
* CVC4 1.8
* Z3 4.8.6


## Paper Abstract 

  A verified VCGen based on Dynamic Logic: an exercise in meta-verification 

  With the incresasing importance of program verification, an issue
  that has been receiving more attention is the certification of
  verification tools, addressing the vernacular question: ``Who
  verifies the verifier?''. In this paper we approach this
  meta-verification problem by considering a fundamental component of
  program verifiers: the ``Verification Conditions Generator''
  (VCGen), responsible for producing a set of proof obligations from a
  program and a specification.

  The semantic foundations of VCGens lie in program logics, such as
  Hoare logic, Dynamic logic, or Separation logic, and related
  predicate transformers.  Dynamic logic is the basis of the KeY
  system, one of the foremost deductive verifiers, whose logic makes
  use of the notion of \emph{update}, which is quite intricate to
  formalize.  In this paper we derive systematically, based on a
  KeY-style dynamic logic, a correct-by-construction VCGen for a toy
  programming language.

  The workflow covers the entire process, from the logic to the
  VCGen. It is implemented in the Why3 tool, which is itself a program
  verifier. We prove soundness and (an appropriate notion of)
  completeness of the logic w.r.t. the programming language semantics,
  then write a VCGen for the logic and prove its soundness. The VCGen
  is written as a program in WhyML (the internal Why3 programming
  language), that can be extracted to OCaml code. With its specific
  logic and programming languages and its ability to interface with
  external proof tools, Why3 stands in a sweet spot, in terms of
  expressivity of logic language, degree of automation, and proof
  management, for the purpose of formalizing the different notions
  involved in this task. In particular, we reason about the (dynamic)
  program logic in Why3's logic language, but then use the programming
  language to actually implement the VCGen.

  Dynamic logic is one of a variety of research topics that our dear
  friend and colleague Luís Soares Barbosa has, over the years,
  initiated and promoted at the University of Minho. It is a pleasure
  for us to dedicate this work to him on the occasion of his 60th
  birthday.



