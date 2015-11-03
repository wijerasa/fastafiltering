Project Name : Filter Fasta Sequences
=====================================

Required Software:
------------------

Python: [pyfasta](https://pypi.python.org/packages/source/p/pyfasta/pyfasta-0.5.2.tar.gz)

Codes:
------

.. code-block:: bash

    $ cat -e 15-1029_EAB_RNAseq2_diffp0.05.txt #Check the ends
    $ tr '\r' '\n' < 15-1029_EAB_RNAseq2_diffp0.05.txt > test.txt #replace '\r' with newline character
    $ for l in $(cat test.txt); do grep  $l M-G-RedundancyRemoved.fasta.txt >> 15_1025_EAB_RNAseq_latest.txt; done
    $ pyfasta extract  --fasta ./M-G-RedundancyRemoved.fasta.txt --space --header --file 15-1029_EAB_RNAseq2_diffp0.05.txt > filtered_seq_latest.fasta