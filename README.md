# cl-globals

A Common Lisp interface to "globals," the original NoSQL data storage engine before SQL even  
existed.

This project is core abstraction layer on which the concrete implementation wrappers will
be based, of which there are two: the open source YottaDB (a fork of GT.M), and InterSystems 
IRIS, the last commercial implementation still in use today.

## Overview

Globals are the storage engine of standard MUMPS implementations. MUMPS is a programming
language built originally for healthcare applications, and it powers many legacy EHRs to this
day. Examples include Epic, the VA's VistA, the Indian Health Service's RPMS.

The core abstraction at the heart of globals is the "sparse matrix." It's fundamentally a
heirarchical key-value datastore that has evolved with performance as the paramount engineering
goal, considering the hardware on which it ran decades ago.

Although the MUMPS programming language (sometimes simply referred to as "M") is becoming
obsolete, there is nothing obsolete about its storage engine, which competes with the best
NoSQL engines in existence today for speed, reliability, and paradigmatic flexibility. The
existence of fast C APIs for both the open source and commercial implementations of M globals
opens the possibility of building new kinds of databases on the rock-solid foundation of 
globals.

This is the goal of this interface of Common Lisp to M globals - to combine the "meta" 
programming power of the world's most flexible programming language with the paradigmatic
freedom of the world's fastest storage engine. What is old is new again, times two.
