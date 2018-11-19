# sequencingDB
Store HTS results with dramatically reduced storage.

## Initiative
Organizations and sequencing centers store large amount of HTS 
sequencing data (e.g. thousands of or even tens of thousands WGS samples). This requires large amount of storage. This
makes exploring the storage a headache. Transfering the sequencing data through internet is always "a watched pot".

## Design
* Create "hash table" of reference genome
* Sample table links to "hash table"
* Store only the difference if no exact match
* Need API for swift rebuilding of the original fastq(.gz)
