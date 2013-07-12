## PLEASE NOTE:
This is an archive of code originally created by
<a href="mailto:tc@gauss.muc.de">Matthias Hölzl</a>
in 1998. [Quid-Pro-Quo](https://github.com/sellout/quid-pro-quo) is a notably 
more advanced Design By contract library based, long ago, on this same
source code. I'd recommend that you go check that out before spending 
any time in this repo.

# Common Lisp - Design by Contract

## What is it all about?

One main goals of every program is reliability, that is, correctness and
robustness. A program is correct if it performs according to its specification,
it is robust if it handles situatios that were not covered in the specification
in a graceful manner. One way to prove the correctness of a program with respect
to a (formal) specification is the Hoare calculus. Based on this formal method
Bertrand Meyer developed a method of software engeneering called Design
by Contract.

The principal idea of Design by Contract (DBC) is that a class and its clients
have a contract with each other: The client must guarantee certain conditions
before calling a method specialized on the class (the preconditions), the class
guarantees certain properties after the call (the postconditions). If the pre-
and postconditions are included in a form that the compiler can check, then any
violation of the contract between caller and class can be detected immedeately.

## Support for Design by Contract in Programming Languages

The language that offers the best support for DBC is Eiffel, designed by
Bertrand Meyer. It is rather difficult to add support for DBC to most other
languages, but not so for Common Lisp: I have written a package for Common Lisp
that provides support for DBC. It is still very new and not too well tested so
you should expect some rough edges and changes in its future design. There is no
larger program depending on this package available, only some silly test cases.
Since I intend to use the dbc package for my own programs this should change in
the not so distant future.
