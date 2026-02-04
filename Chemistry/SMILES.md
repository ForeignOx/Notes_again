SMILES stands for Simplified Molecular Input Line Entry System. It is a way of encoding molecular structure. SMILES notation is widely used in chem-informatics, molecular modelling, and drug design. I will be writing the SMILES in <span style="color:#21d07c">green</span> for easy distinguishing.
## 1. Atoms
* Atoms are represented by their atomic symbols, and should be enclosed in square brackets, <span style="color:#21d07c">[]</span>,  unless they are one of B, C, N, O, P, S, F, Cl, Br or I and have no formal charge and have the standard number of hydrogen atoms[^1] attached and are the normal [[Isotopes|isotopes]] and are not [[Chiral Centres|chiral centres]].
	* An atom of gold would be <span style="color:#21d07c">[Au]</span>
	* <span style="color:#21d07c">[C]</span> is a carbon atom, but <span style="color:#21d07c">C</span> is a methane molecule
	* Ammonia is <span style="color:#21d07c">N</span>
	* Water is <span style="color:#21d07c">O</span>
*  Atoms in [[Arenes|aromatic rings]] are specified by lower case letters, [[Aliphatic Compounds|aliphatic compounds]] use uppercase letters
	* <span style="color:#21d07c">c1ccccc1</span> is benzene, while <span style="color:#21d07c">C1CCCCC1</span> is hexane
* Formal charge is shown by either <span style="color:#21d07c">+</span> or <span style="color:#21d07c">-</span> followed by a digit
	* <span style="color:#21d07c">[HO-]</span> is a hydroxide ion
	* <span style="color:#21d07c">[OH3+]</span> is a hydronium ion
	* <span style="color:#21d07c">[O-2]</span> is an oxide ion
## 2. Bonds
* Single bonds are represented as <span style="color:#21d07c">-</span>, but they are implied, so there is no need to indicate them
	* <span style="color:#21d07c">CCO</span> is ethanol
* Double bonds are represented as <span style="color:#21d07c">=</span>
	* <span style="color:#21d07c">C=CCC</span> is but-1-ene
* Triple bonds are represented as <span style="color:#21d07c">#</span>
	* <span style="color:#21d07c">C#CC</span> is propyne
* Quadruple bonds are represented as <span style="color:#21d07c">$</span>
	* <span style="color:#21d07c">[Ga+]$[As-]</span> is gallium arsenide
* Aromatic "$3/2$" bonds are represented as <span style="color:#21d07c">:</span>
* "Non-bonds" used to show that two parts are not bonded together are represented as <span style="color:#21d07c">.</span>
	* <span style="color:#21d07c">[Na+].[Cl-]</span> is aqueous sodium chloride
* Single [[Stereoisomerism|stereoisomeric]] bonds around double bonds can be represented with <span style="color:#21d07c">\</span> and <span style="color:#21d07c">/</span>
	* <span style="color:#21d07c">F/C=C/F</span> is E-1,2-difluoroethene, whereas <span style="color:#21d07c">F/C=C\F</span> is Z-1,2-difluoroethene
## 3. Branches
* Branches are enclosed in <span style="color:#21d07c">()</span>, and can be nested or stacked, the connection to a branch is always to the left
	* <span style="color:#21d07c">CC(C)C</span> is methylpropane
	* <span style="color:#21d07c">CC(=O)C</span> is propanone
* If there are two branches around a ring, you can write parts of the ring as if they were branched
	* 3-cyanoanisole, depicted below, is written as <span style="color:#21d07c">COc(c1)cccc1C#N</span>
	```smiles 
	COc(c1)cccc1C#N 
	```
* Ring-closing bonds don't require <span style="color:#21d07c">(</span><span style="color:#21d07c">)</span>, choosing ring-closing closing bonds appropriately can reduce the number of () required
	* Methylbenzene can be written as <span style="color:#21d07c">Cc1ccccc1</span> or as <span style="color:#21d07c">c1cc(C)ccc1</span> or as <span style="color:#21d07c">c1cc(ccc1)C</span>, the first of which is the simplest
## 4. Cyclic structures
* Cyclic structures are represented by breaking a bond in each ring and writing ring opening and closing bonds by writing a digit immediately after the atomic symbol at the ring closure
	* <span style="color:#21d07c">C1CCC1</span> is cyclobutane
* The first ring will be labelled with <span style="color:#21d07c">1</span>, the second will be labelled with <span style="color:#21d07c">2</span> and so on
	* Decaline aka decahydronaphthalene, shown below, can be written as <span style="color:#21d07c">C1CCCC2C1CCCC2</span>
	```smiles
	C1CCCC2C1CCCC2
	```
* Multiple digits can represent ring-closing bonds, if two digit numbers are required, the label is preceded by <span style="color:#21d07c">%</span>
	* An alternate way of writing decaline is <span style="color:#21d07c">C1CCCC2CCCCC12</span>
	* <span style="color:#21d07c">C%12</span> is a single ring-closing bond of ring 12
## 5. Chirality
* An <span style="color:#21d07c">@</span> symbol following a the atomic symbol of the [[Chiral Centres|chiral centre]], means the other three atoms are listed anti-clockwise. The chiral centre and hydrogen if it is the first attached group go in <span style="color:#21d07c">[</span><span style="color:#21d07c">]</span>
* <span style="color:#21d07c">@@</span> means the atoms are listed clockwise instead
	* <span style="color:#21d07c">F[C@H](Cl)C</span> and <span style="color:#21d07c">F[C@@H](Cl)C</span> are the two enantiomers shown below
	```smiles
	C[C@H](Cl)F
	C[C@@H](Cl)F
	```
	
[^1]: Boron has 3, Carbon has 4, Nitrogen can have 3 or 5, Oxygen has 2, Phosphorous has 3 or 5, Sulphur has 2,4 or 6, Fluorine has 1, Chlorine has 1, Bromine has 1, Iodine has 1 

#Chemistry #Guide