Mhchem is a latex package that allows you to write chemical equations quickly and easily. It is recommended you disable "Latex suite" package when using it. I will display mhchem formulas in <span style="color:#21d07c">green</span>
If ever needed, [this](https://mhchem.github.io/MathJax-mhchem/) is a good guide
## Chemical Formulae
These are fairly simple, to enter the mhchem format, inside of "math mode", type <span style="color:#21d07c">\ce{}</span>. Then, to write the formula, simply write each element and their number to the left.
* <span style="color:#21d07c">$\ce{H2O}$</span> is how you write $\ce{H2O}$ 
To write multiple moles of a chemical, write the number in front of the chemical
* <span style="color:#21d07c">$\ce{2H2O}$</span> is $\ce{2H2O}$ 
* <span style="color:#21d07c">$\ce{1/2 Sb2O3}$</span> is $\ce{\frac{1}{2}Sb2O3}$
To use a variable such as $x$ or $n$, you can usually just put it in the formula as it is, although if it is a subscript you do need to do the subscript
* <span style="color:#21d07c">$\ce{nH2O}$</span> is  $\ce{nH2O}$ 
* <span style="color:#21d07c">$\ce{C_nH_{2n}}$</span> is $\ce{C_nH_{2n}}$
To insert Greek characters, do so as you would normally i.e. <span style="color:#21d07c">\mu</span>, to insert regular text, put it in <span style="color:#21d07c">{}</span>
* <span style="color:#21d07c">$\ce{{Gluconic Acid} + H2O2}$</span> is $\ce{{Gluconic Acid} + H2O2}$ 
* <span style="color:#21d07c">$\ce{\beta +}$</span> is $\ce{\beta +}$
For charges, if it is a 1+ or a 1- charge, you can simply put <span style="color:#21d07c">+</span> or <span style="color:#21d07c">-</span> after the symbol, for higher charges, put a <span style="color:#21d07c">^</span> then the number then the charge, if it is a complex ion, the compound in <span style="color:#21d07c">[]</span>
* <span style="color:#21d07c">$\ce{H+}$</span> is $\ce{H+}$
* <span style="color:#21d07c">$\ce{CrO4^2-}$</span> is $\ce{CrO4^2-}$
* <span style="color:#21d07c">$\ce{[AgCl2]-}$</span> is $\ce{[AgCl2]-}$
For [[Isotopes|isotopes]] of an element, do it as you would expect it to be in normal "math mode", but without the <span style="color:#21d07c">{}</span>
* <span style="color:#21d07c">$\ce{^227_90Th+}$</span> is $\ce{^227_90Th+}$
[[Oxidation States|Oxidation states]] are done by writing <span style="color:#21d07c">^{n}</span>, where n is the roman numeral of the state
* <span style="color:#21d07c">$\ce{Fe^{II}Fe^{III}2O4}$</span> is $\ce{Fe^{II}Fe^{III}2O4}$
[[Radicals]] are done by writing <span style="color:#21d07c">^.</span>
* <span style="color:#21d07c">$\ce{Cl^.}$</span> is $\ce{Cl^.}$
State symbols are done how they might be done in regular "math mode"
- <span style="color:#21d07c">$\ce{Cl_{(aq)}-}$</span> is $\ce{Cl_{(aq)}-}$
## Bonds
 <span style="color:#21d07c">-</span> is a single bond, <span style="color:#21d07c">=</span> is a double bond, <span style="color:#21d07c">#</span> is a triple bond, <span style="color:#21d07c">.</span> is a non-bond
 - <span style="color:#21d07c">$\ce{H3C-CH3}$</span> is $\ce{H3C-CH3}$
 - <span style="color:#21d07c">$\ce{O=O}$</span> is $\ce{O=O}$
 - <span style="color:#21d07c">$\ce{HC#N}$</span> is $\ce{HC#N}$
 - <span style="color:#21d07c">$\ce{KCr(SO4)2.12H2O}$</span> is $\ce{KCr(SO4)2.12H2O}$
 These next ones are more complex, so you need to use the command <span style="color:#21d07c">\bond{}</span> to make them be recognised. <span style="color:#21d07c">~</span> is a half bond and can be combined with <span style="color:#21d07c">-</span> or <span style="color:#21d07c">=</span> to form $1 \frac{1}{2}$ or $2 \frac{1}{2}$ bonds respectively, the ~ can also be put in between two - if that's what you want.
 - <span style="color:#21d07c">$\ce{A\bond{~-}B}$</span> is $\ce{A\bond{~-}B}$
 - <span style="color:#21d07c">$\ce{A\bond{~=}B}$</span> is $\ce{A\bond{~=}B}$
 - <span style="color:#21d07c">$\ce{A\bond{-~-}B}$</span> is $\ce{A\bond{-~-}B}$
[[Hydrogen Bonds]] can be represented by using ... or .... in the <span style="color:#21d07c">\bond{}</span> command, depending on how many dots you want
- <span style="color:#21d07c">$\ce{H2O\bond{...}HOH}$</span> is $\ce{H2O\bond{...}HOH}$
- <span style="color:#21d07c">$\ce{H2O\bond{....}HOH}$</span> is $\ce{H2O\bond{....}HOH}$
[[Dative Covalent bond|Dative bonds]] can be represented by using <span style="color:#21d07c">-></span> or <span style="color:#21d07c">&#60-</span> in the <span style="color:#21d07c">\bond{}</span> command
- <span style="color:#21d07c">$\ce{H3N\bond{->}H+}$</span> is $\ce{H3N\bond{->}H+}$
## Reactions
Reaction arrows are how you might expect:
- <span style="color:#21d07c"><span style="color:#21d07c">$\ce{A->B}$</span></span> is $\ce{A->B}$
- <span style="color:#21d07c">$\ce{A&#60-B}$</span> is $\ce{A<-B}$
- <span style="color:#21d07c">$\ce{A&#60->B}$</span> is $\ce{A<->B}$
- <span style="color:#21d07c">$\ce{A&#60=>B}$</span> is $\ce{A<=>B}$
- <span style="color:#21d07c">$\ce{A&#60=>>B}$</span> is $\ce{A<=>>B}$
- <span style="color:#21d07c">$\ce{A&#60&#60=>B}$</span> is $\ce{A<<=>B}$ 
You can put text above or below a reaction arrow using <span style="color:#21d07c">[][]</span> immediately after the arrow, where the first set of <span style="color:#21d07c">[]</span> is for the text above and the second set is for the text below
- <span style="color:#21d07c">$\ce{A->[H2O]B}$</span> is $\ce{A->[H2O]B}$
- <span style="color:#21d07c">$\ce{A->[][H2O]B}$</span> is $\ce{A->[][H2O]B}$
- <span style="color:#21d07c">$\ce{A->[{text above}][{text below}]B}$</span> is $\ce{A->[{text above}][{text below}]B}$

#Chemistry #Guide

