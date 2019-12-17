# Big-Endian Support for BoringSSL

## Description

BoringSSL is a fork of OpenSSL that is designed to meet Google's needs.

Programs ship their own copies of BoringSSL when they use it and we update everything as needed when deciding to make API changes. This allows us to mostly avoid compromises in the name of compatibility. It works for us, but it may not work for you.

BoringSSL arose because Google used OpenSSL for many years in various ways and, over time, built up a large number of patches that were maintained while tracking upstream OpenSSL. As Google's product portfolio became more complex, more copies of OpenSSL sprung up and the effort involved in maintaining all these patches in multiple places was growing steadily.

One of the key deficencies of BoringSSL is that it is a little-endian only implementation. 

This project aims to add support for Big Endian systems such as Z. Some work has already been done that has implemented some of this support. However, a couple of the key ciphers are still little endian only. 

The project is constrained by the fact that Google will not accept big-endian-enabled code. Therefore, instead: 

* We will use the hardware acceleration and associated libraries (libica).
* The project will provide a generic hardware acceleration interface such that other architectures can plug into it.
* If h/w isn’t available it default to the existing little-endian code
* For Z there are two libraries which provide access to the hardware and if it’s not available will implement things in software
* This project will require you to research and understand the hardware acceleration libraries and how they are invoked
* Take the latest BoringSSL code and enable it to invoke a generic layer of h/w acceleration routines
* For Z, have that generic layer invoke the APIs in the libraries

## Additional Information

* [Google's BoringSSL git site](https://boringssl.googlesource.com/boringssl/)
* [libica Programmers' Reference](http://public.dhe.ibm.com/software/dw/linux390/docu/l33xci10.pdf)
* [Secure Key Solution with the Common Cryptographic Architecture Application Programmer's Guide])http://public.dhe.ibm.com/software/dw/linux390/docu/l60xcc08.pdf)
* [Exploiting Enterprise PKCS #11 using openCryptoki 3.10](http://public.dhe.ibm.com/software/dw/linux390/docu/l39xce01.pdf)

## Desirable Skills

* C coding skills
* Familiarity with encryption
* Familiarity with openSSL or BoringSSL an advantage

## Expected Outcome

* Set of patches to boringssl TLS 1.2 and 1.3 implementations
* Log of run of testsuite to verify operation

## Difficultly

*Medium*

## Mentors

  * Neale Ferguson <neale@sinenomine.net>

## Additional Contacts
