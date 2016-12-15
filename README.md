# IMS-zOSMF-Workflows
This repository contains sample z/OSMF Workflows that can be used to provision full IMS systems and also to provision FastPath databases on an existing IMS 

provision_system.zip 
This will provision a full IMS TM/DB system starting with the SMP
installed IMS datasets that must already exist.  The Provision workflow
will not modify the datasets, instead making copies in a temporary
location of datasets that need modification.  This allows the
Deprovision workflow to take down the IMS regions and delete the
temporary datasets, thus leaving the target system in the exact state
that exists prior to running the Provision workflow.

provision_fp_db.zip
This will provision a FastPath database onto an existing IMS. The
structure of the database is fixed, but names can be modified at
runtime.  The Provision workflow can be run multiple times to create as
many databases as the user chooses.  The Deprovision workflow will
delete a selected database and leave all others intact.
