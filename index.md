Project Name : Filter Fasta Sequences
=====================================

Required Software:
------------------

Python: [pyfasta](https://pypi.python.org/packages/source/p/pyfasta/pyfasta-0.5.2.tar.gz)

Codes:
------

.. code-block:: bash

    $ cat -e fasta-ids.txt #Check the ends
    $ tr '\r' '\n' < fasta-ids.txt > test.txt #replace '\r' with newline character
    $ for l in $(cat test.txt); do grep  $l main-fasta.fasta >> temp_header.txt; done
    $ pyfasta extract  --fasta ./main-fasta.fasta --space --header --file temp_header.txt > filtered_seq.fasta