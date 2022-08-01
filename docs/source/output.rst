Output
=====

The directories and output files listed below can be found inside the the zip file. All paths are relative to the top-level **results** directory.

FastQC
++++++++++++++

FastQC (ver. 0.11.9) gives general quality metrics about your reads. It provides information about the quality score distribution across your reads and per base sequence content (%T/A/G/C). You get information about adapter contamination and other overrepresented sequences.

For further reading and documentation see the `FastQC help <https://www.bioinformatics.babraham.ac.uk/projects/fastqc/Help/>`_.

The FastQC plots displayed in the MultiQC report shows untrimmed reads. They may contain adapter sequences and potentially regions with low quality. 

**Output directory: `<RUNNAME>/fastqc/`**

    `<SAMPLE>_fastqc.html``
        FastQC report, containing quality metrics for your untrimmed raw fastq files
