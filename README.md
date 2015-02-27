Constituent-parser-nl
=======

Introduction
------------

This is a parser for Dutch text using the Alpino parser (http://www.let.rug.nl/vannoord/alp/Alpino/). The input for this module has to be a valid
KAF file with at least the text layer. The output will be the constituent trees in pennTreebank format for each of the sentences in the input KAF/NAF.
The tokenization and sentence splitting is taken from the input KAF file, so if your input file has a wrong tokenization/splitting, the output could
contain errors. The number of output constituent trees will be exactly the same as the number of sentences in your input KAF/NAF

Requirements
-----------
* KafNafParserPy: parser in python for KAF/NAF files (https://github.com/cltl/KafNafParserPy)
* lxml: library for processing xml in python
* Alpino parser:http://www.let.rug.nl/vannoord/alp/Alpino/

Installation
-----------
Clone the repository to your local machine and set the varible ALPINO_HOME in the file core/alpino_parser.py
to point to your local folder of the Alpino parser.

How to run the module with Python
---------------------------------

You can run this module from the command line using Python. The main script is core/alpino_parser.py. This script reads the KAF from the standard input
and writes the output to the standard output, generating some log information in the standard error output. To process one file just run:
````shell
cat examples/file1.in.kaf | alpino_parser.py > output.kaf
cat examples/file1.in.naf | alpino_parser.py > output.naf
````


Contact
----------------------------------
* Ruben Izquierdo
* Vrije University of Amsterdam
* ruben.izquierdobevia@vu.nl  rubensanvi@gmail.com
* http://rubenizquierdobevia.com/
