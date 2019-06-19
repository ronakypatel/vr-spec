ClinGen Allele Registry
!!!!!!!!!!!!!!!!!!!!!!!

ClinGen Allele Registry provides identifiers for more than 900 million variants. Each identifier (canonical allele identifiers: CAIds) is an abstract concept which represents a group of identical variants based on alignment. Identifiers are retrievable irrespective of the reference sequence and normalization status.

As a Driver Project for GA4GH, `ClinGen Allele Registry <https://reg.clinicalgenome.org>`__ implements two standards: RefGet and VR in the first implementation (**June 27, 2019**). 

The API endpoints that support data retrieval in this two key standards are summarized in the following table.

**HOST**: `https//reg.clinicalgenome.org/ <https://reg.clinicalgenome.org>`__

.. csv-table::
   :header: API Path, Parameters, Response Format, Example, 
   :align: left

   **RefGet**,,,
   [GET] /sequence/service-info, \-, Refget v1.0.0, `/sequence/service-info <https://reg.clinicalgenome.org/sequence/service-info>`
   [GET] /sequence/{id}, id => TRUNC512 digest for reference sequence, Refget v1.0.0, `/sequence/vYfm5TA_F-_BtIGjfzjGOj8b6IK5hCTx <https://reg.clinicalgenome.org/sequence/vYfm5TA_F-_BtIGjfzjGOj8b6IK5hCTx>`__ 
   [GET] /sequence/{id}/metadata, id => TRUNC512 digest for reference sequence, Refget v1.0.0, `/sequence/vYfm5TA_F-_BtIGjfzjGOj8b6IK5hCTx/metadata <https://reg.clinicalgenome.org/sequence/vYfm5TA_F-_BtIGjfzjGOj8b6IK5hCTx/metadata>`__
   **VR**,,,
   [GET] /vrAllele?hgvs={hgvs}, hgvs => HGVS expression, VR v1.0, `/vrAllele?hgvs=NC_000007.14:g.55181320A>T <https://reg.clinicalgenome.org/vrAllele?hgvs=NC_000007.14:g.55181320A%3ET>`__  `/vrAllele?hgvs=NC_000007.14:g.55181220del <https://reg.clinicalgenome.org/vrAllele?hgvs=NC_000007.14:g.55181220del>`__ 
   
Support for GA4GH refget and VR specs provided in ClinGen Allele Registry through implementation that is independent from VR-Python. Support for this community standards is implemented in ClinGen Allele Registry through extension of code written in C++.
