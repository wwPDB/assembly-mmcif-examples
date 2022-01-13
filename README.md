# Sample assembly files in PDBx/mmCIF Format

 
Starting May 3rd 2022, the PDB archive will distribute assembly files in PDBx/mmCIF format for every entry, allowing direct access and visualisation of the curated assemblies for all PDB entries.

These updated PDBx/mmCIF format assembly files will have improved organization of assembly data to support usage by the community. These files will include all symmetry generated copies of each chain within a single model, with distinct chain IDs (*\_atom\_site.auth\_asym\_id* and *\_atom\_site.label\_asym\_id*) assigned to each. Generation of distinct chain IDs in assembly files are based upon the following rules:

* Chain IDs of the original chains from the atomic coordinate file will be retained (e.g., A)

* Assign unique chain ID (*atom\_site.label\_asym\_id* and *atom\_site.auth\_asym\_id*) for each symmetry copy within a single model. Rules of chain ID assignments:
  * The applied index of the symmetry operator (*pdbx\_struct\_oper\_list.id*) will be appended to the original chain ID separated by a dash (e.g., A-2, A-3, etc.)

  * If there are more than one type of symmetry operators applied to generate symmetry copy, a dash sign will be used between two operators (e.g., A-12-60, A-60-88, etc.)

In addition, entity ID and chain ID mapping categories, *\_pdbx\_entity\_remapping* and *\_pdbx\_chain\_remapping* will be provided. 
 
Within this repository are sample files. In May, the assembly files for the entire PDB archive will be available to the public under a new directory **https://ftp.wwpdb.org/pub/pdb/data/assemblies/mmCIF**.