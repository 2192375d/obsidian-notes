# languages
### alphabet
alphabet: set of all symbols
	Ex:   $\sum$ = $\{0, 1\}$
		$\sum^*$= set of all finite strings over $\sum$
		 $\epsilon$ = empty string

### language (over $\sum$)
A language is a subset of $\sum^*$

###### language operations
<u>basic ones</u>
complementation: $\overline{L}=\{x\in\sum^*\\:x\notin L\}$ 
union: $L_1\cup L_2=\dots$
intersection: $L_1\cap L_2=\dots$
concatenation: $L_1\cdot L_2=\{xy:x\in L_1,y\in L_2\}$

A result of concatenation is $L_1\cdot\emptyset=\emptyset=L_2\cdot\emptyset$

<u>Kleene Star</u>
$L^*=\{x:x=\epsilon\text{ or } x=y_1\dots y_k,\text{where }k>0\text{ and } y_1,...,y_k\in L\}$

<u>reversal</u>
$L^R=\{x^R:x\in L\}$

### regular expresions (regex)
-strings
-strings with special alphabet $\sum\cup\{\emptyset,\epsilon,+,*,(,)\}$

However, special alphabets have a problem:
	$\emptyset$ can represent '$\emptyset$' as a symbol, "$\emptyset$" as a sting, or $\{\}$ as a set

###### definition of set of regexes over $\sum$
Let $\mathcal{RE}$ be the smallest set such that:
	basis: $\emptyset,\epsilon,a,\forall a\in\sum$
	inductive step: $\text{if }R,S\in\mathcal{RE},\text{ then}(R+S),(RS),(R^*)\in\mathcal{RE}$

Note that similar to $\emptyset$, $\epsilon$ can be written as a symbol, or a string, or an empty string. However, since regex can't include empty string, $\epsilon$ can't be an empty string.

_example_
$(0+(1\ 1))^*$ is a regex
() is not regex

### languages denoted by a regex R
Consdider $\mathcal{L}(R)\coloneqq\text{set of strings that R matches}$
$\mathcal{L}(R)=\begin{cases}\emptyset,&R=\emptyset\\\{\epsilon\},&R=\epsilon\\\{a\},&R=a,\text{where }a\in\sum\end{cases}$

Here is another example:
$\mathcal{L}(R)=\begin{cases}\mathcal{L}(S)\cup\mathcal{L}(T)&,R=(S+T)\\\mathcal{L}(S)*\mathcal{L}(T)&,R=(ST)\\\mathcal{L}(S)^*&,R=S^*\\\end{cases}$

###### precedence (highest to lowest)
- *
- $\cdot$ (concatenation)
- +
For good convention, omit external parentheses

| language $L$                                              | regex $R\ S.T.\mathcal{L}(R)=L$ |
| --------------------------------------------------------- | ------------------------------- |
| $L=\sum^*$                                                | $R=(0+1)^*,R=(0^*1^*)^*$        |
| $L=\{x\in\sum^*:x\text{ starts with 1 and ends with 1}\}$ | $R=1(1+0)^*1+1$                 |

### equivalence between regex
<u>commutativity of union</u>
$(R+S)=(S+R)$
<u>associativity of union</u>
$((R+S)+T)=(R+(S+T))$
<u>associativity of concatenation</u>
$((RS)T)=(R(ST))$
<u>left distributivity</u>
$(R(S+T))=((RS)+(RT)$
<u>right distributivity</u>
$((S+T)R)=((SR)+(TR))$
<u>identity for union</u>
$(R+\emptyset)=R$
<u>identity for concatenation</u>
$(R\epsilon)=R\text{ and }(\epsilon R)=R$
<u>annihilator for concatenation</u>
$(\emptyset R)=\emptyset\text{ and }(R\emptyset)=\emptyset$
<u>Idempotence of Kleene star</u>
${R^*}^*=R^*$

_How to prove equivalence of two regex?_
To prove $R=S$
Show 
	$\mathcal{L}(R)\subset\mathcal{L}(S)$
	$\mathcal{L}(S)\subset\mathcal{L}(R)$

_example_
$L=\{x\in\sum^*:111\text{ is a substring of }x\}$
Then, $R=(1+0)^*111(1+0)^*$

### regular language
A language is __regular__ if there is a regex $\mathcal{R}$ S.T. $L=\mathcal{L}(R)$

_example_
Let $P(R)$ be $$P(R):\text{}$$

### closure of regular language
Let $f(L)$ be an arbitrary language operation
Let $P(R)$: There exists a regex $R'$ S.T. $\mathcal{L}(R')=f(\mathcal{L}(R))$
WTS: $P(R)$ holds for every regex $R$

_proof_
	Let $A$ be an arbitrary regular language
	Then, $A=\mathcal{L}(R)$ for some regex $R$
	Thus, $\mathcal{L}(R')=f(\mathcal{L}(R))=f(A)$
	Thus, $A$ is regular