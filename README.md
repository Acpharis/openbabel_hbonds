openbabel_hbonds
================

This uses openbabel to detect hydrogen bonds between a receptor
and ligand in a PDB file. It attempts to flip or spin hydrogens to make some hydrogen bonds.

Dependencies
------------

This requires having the pybel and openbabel python extensions installed.

It also currently targets python 2.7 , modifications to support python 3 are very welcome.

Usage
-----

`openbabel_hbonds_native` uses openbabel's native definition of a hydrogen bond acceptor and donor.

`openbabel_hbonds_smarts` uses smarts to define h-bond donors and acceptors. You may modify it to meet your preferred definition.

Both scipts output a list of h-bonds as Donor (chain, residue id, residue name, atom name) then Acceptor (chain, residue id, residue name, atom name)

```
A  137 ARG  NH2 A  394 CC3  O27
A  143 LYS  NZ  A  394 CC3  F10
A  213 ALA  N   A  394 CC3  N15
A  394 CC3  N25 A  214 PRO  O  
A  394 CC3  N18 A  213 ALA  O  
```

Future Work
-----------
[] H-bonds to aromatic rings
[] Tautomers of residues
[] Tautomers of ligands
[] Flip possibly mis-assigned residues
[] Factor out common code between the two scripts
