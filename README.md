lingva
======

Repository for Lingva

Lingva is compiled for Linux x64. Folder contains : 

Lingva = front end that allows fine control over what and how to analyze code. Makes use of all the files.
core = modified version of Vampire that can work with program analysis and Symbol elimination 
infXpostFx.py = infix to postfix transformation of tptp 
insertInv.py = insert a set of invariants at different locations in source code
symels = bash script that implements strategies for minimizing the set of invariants. Makes use of core

README.md = this file 

Usage
=======
./Lingva [-h] [-o OUTPUTFILE] [-v] [-t TIMELIMIT]
              [-f [FUNCNO [FUNCNO ...]]] [--format FORMAT] [--tVamp TVAMP]
              [--completeOutput] [--folderFEC FOLDERNAME]
              INPUT-FILENAME

Annotate C code with invariants

positional arguments:
  INPUT-FILENAME        input file to be processed.

optional arguments:
  -h, --help            show this help message and exit
  -o OUTPUTFILE, --output OUTPUTFILE
                        output filename -- by default if no output is
                        specified, the output will be printed in a file
                        $(INPUT-FILENAME).annotated and also on the screen.
  -v, --verbose
  -t TIMELIMIT, --time_limit TIMELIMIT
                        time limit for invariant generation , default value 10
                        seconds
  -f [FUNCNO [FUNCNO ...]], --fun [FUNCNO [FUNCNO ...]]
                        Name of the function to process and the while/whiles
                        to process. We support the * operator, with the
                        constraint that if * is the first part of the argument
                        it must be escaped ( \* ). In case there is no while
                        specified after . then we consider the default option
                        * - all the whiles in the function. \*.* represents
                        the default value for this option
  --format FORMAT       format of the invariants. Values can be either tptp or
                        framac. Default value framac
  --tVamp TVAMP         Time limit for the minimization of the set of
                        invariants. Default 20 seconds. 0 seconds - no
                        minimization is done!
  --completeOutput      flag that tells the tool to output also complete
                        output for each of the whiles analysed. This can be
                        used in combination with the --folderFEC option
  --folderFEC FOLDERNAME
                        folder where to save individual files that come from
                        complete output. If left empty, than no files will be
                        saved.

Licence
======

Lingva has the same Licence as Vampire. For the licence file see: http://vprover.org/license.cgi

Vampire Licence: 

Our licence is quite liberal. In short, we do not allow modification and distribution of Vampire and the use of Vampire to compete against Vampire. To obtain a copy of Vampire you will be required to accept the terms of the licence. If you require any other licence, please contact Andrei Voronkov.
Vampire Software Licence Agreement
This is a Licence Agreement for use of Computer Software known as Vampire ('the Software') supplied by the University of Manchester ('the University').
Please carefully read through this Licence prior to using the Software as it sets out the obligations between you ('the Licensee') and the University which is binding and enforceable. If you are not prepared to accept the terms of this Licence then do not use the Software. Installation or use of the Software shall constitute acceptance of the terms set out below.
THE SOFTWARE

The software is distributed in binary form only as a set of executable binaries and it is the Licensee's sole responsibility to integrate it into appropriate applications.
The University does not warrant that the Software is free from errors and shall not be liable in any way for any loss consequent upon the existence of errors.
THIS LICENCE

This Licence entitles the Licensee to a royalty-free non-exclusive end-user licence to use the Software. The Licence does not permit Licensee incorporating the Software in any system entering a competition.
If you wish to use the software for competition purposes or want to have access to the source code used to create the Software, please contact us at the address at the end of this licence to obtain an appropriate licence.
RE-DISTRIBUTION

The Licencee may not distribute the Software.
MODIFICATION

The Licensee may not modify, disassemble, translate, reverse engineer, or decompile the Software.
COPYRIGHT

Ownership of the copyright in the Software and supporting documentation shall remain at all times vested in the University.
DISCLAIMER AND LIMITATION OF LIABILITY

THIS MATERIAL IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS ``AS IS'' AND ANY EXPRESSED OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDERS OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS MATERIAL, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
THIRD PARTY RIGHTS

It is the Licensee's responsibility to secure all necessary licences to third party software for the purposes of using the Software with the third party software. The Licensee acknowledges that University's obligations relate solely to the Software supplied.
TERMINATION

The University shall have the right to terminate this Licence forthwith should the Licensee be in breach of any of its terms. The Licensee shall forthwith delete any copies of the Software.
SEVERABILITY

If any of the terms in this Licence are found to be unenforceable then the terms shall be severed from this Licence to the extent that it shall be necessary for this Licence to remain enforceable.
COMPLETE AGREEMENT

This Licence sets out the complete terms under which the Licensee shall have the right to use the Software unless one party has made fraudulent or negligent misrepresentations inducing the other to enter into this Licence.
WAIVER

Any waiver of rights under this Licence must be in writing.
ENGLISH LAW

This Licence shall be construed and interpreted in accordance with the laws of England and the English courts shall have non-exclusive jurisdiction over any disputes.
GENERAL

You acknowledge that you have read this Agreement, you understand it, and that by installing and using the Software you agree to be bound by its terms and conditions. You assume full responsibility for the use of the Software and agree to use it legally and responsibly.
QUERIES

If you have any questions relating to this Licence then please contact: Andrei Voronkov, The Kilburn Building, University of Manchester, Oxford Road, Manchester, M13 9PL. Telephone: 0161 275 6116.