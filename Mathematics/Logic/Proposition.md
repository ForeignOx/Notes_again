## Definition
A proposition is a statement which has a truth value. It is either true or false. Questions are not statements and are thus not propositions
Often propositions depend on a variable $x$. This is called a conditional statement or statement frame, $A(x)$. We can turn a conditional statement into an unconditional statement using the quantifiers "for all" ($\forall$), the universal quantifier and "there exists" ($\exists$), the existential quantifier
The statement $(\forall x)(x<4)$ still contains the variable '$x$', but $x$ is no longer free to be given values, and is now called a bound variable. Roughly speaking, quantified variables are bound and unquantified variables are free
Suppose we have a sentence $A(x,y)$ containing $\hspace{0pt}2$ free variables, we can use two quantifiers to obtain a statement. Importantly, if quantifiers of both types are used, then the order in which they are written affects the meaning of the statment;
$$
(\exists y)(\forall x)P(x,y)\text{ and }(\forall x)(\exists y)P(x,y)
$$
Are different things. with the first being the stronger statement.
If two quantifiers are of the same type, the order does not affect their meaning. We abbreviate $(\forall x)(\forall y)$ to $(\forall x,y)$
Combinations of frame variables and logical connectives such as [[And|and]], [[Or|or]] and [[Not|not]] are called truth-functional forms. A truth-functional form that is always true is called a tautology or a tautologous form
### Negation of Quantifiers
The combinations $\sim(\forall x)$ and $(\exists x)\sim$ have the same meanings: something is not always true if and only if it is sometimes false
Similarly $\sim(\exists y)$ and $(\forall y)\sim$
We can summarise in a rule:
    In taking the negation of a statement beginning with a string of quantifiers, we can simply change each quantifier to the opposite kind and move the negation sign to the end of the string
Thus:
$$
\sim(\forall x)(\exists y)(\forall z)P(x,y,z) \iff (\exists x)(\forall y)(\exists z)\sim P(x,y,z)
$$


#Mathematics #Logic 