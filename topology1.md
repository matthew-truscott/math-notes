# TOPOLOGY

### Chapter 1 - Set theory

#### 1 - Fundamental Concepts

Capital letters are sets, lowercase are objects or elements in the sets.
If object a belongs to set A, this can be written
$$a \in A$$ {#eq:set-1}

or if not in A,
$$a \notin A$$ {#eq:set-2}

Equality defined as labels referring to the same entity. Subset is defined
as: every element of A is also an element of B, or
$$A \subseteq B$$ {#eq:set-3}

If this holds and additionally A is not B, then one can call A a subset of
B, or write
$$A \subset B$$ {#eq:set-4}

To define a set, one can throw objects into curly braces like so,
$$A = \{a, b, c\}$$ {#eq:set-5}

So A contains the list specified, and nothing else. Often this list can
be impractically large so instead one can define a property to restrict
the elements of a set, say
$$B = \{x \mid x \text{ is an even integer}\}$$ {#eq:set-6}

The vertical bar is equivalent to saying "such that". One can now define
operators that act on multiple sets and return a single set. Two basic
ones are OR and AND. OR is also called the union and is written
$$A \cup B = \{x \mid x \in A \text{ or } x \in B\}$$ {#eq:set-7}

AND is the intersection and is formally defined
$$A \cap B = \{x \mid x \in A \text{ and } x \in B\}$$ {#eq:set-8}

The definition of an empty set is useful, $\emptyset$, which trivially
obeys
$$A \cup \emptyset = A$$ {#eq:set-9}

and
$$A \cap \emptyset = \emptyset$$ {#eq:set-10}

The difference of two sets is defined as the set of elements of A that
are not in B, or
$$A - B = \{x \mid x \in A \text{ and } x \notin B\}$$ {#eq:set-11}

Sets follow distributive laws:
$$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$$ {#eq:set-12}
$$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$$ {#eq:set-13}

and DeMorgan laws,
$$A - (B \cup C) = (A - B) \cap (A - C)$$ {#eq:set-14}
$$A - (B \cap C) = (A - B) \cup (A - C)$$ {#eq:set-15}

Given a set A, one can define a powerset as the set of all subsets of
A, or $\mathcal{P}(A)$. 

For multiple unions and intersections, one can now define
$$\bigcup_{A \in \mathcal{A}} A = \{x \mid x \in A \text{ for at least one } 
A \in \mathcal{A}\}$$ {#eq:set-16}
$$\bigcap_{A \in \mathcal{A}} A = \{x \mid x \in A \text{ for every }
A \in \mathcal{A}\}$$ {#eq:set-17}

Given two sets A and B, a cartesian product can be defined as the of all
ordered pairs (a, b) where a is in A and b is in B. This ordered pair can
be defined in terms of set operations but is more commonly thought of as
a primitive. 
$$A \times B = \{(a, b) \mid a \in A \text{ and } b \in B\}$$ {#eq:set-18}

#### 2 - Functions

A function assigns each each element of set A to an element in set B

Assignment is a subset r of a cartesian product C x D of two sets, where
each element of C appears as the first coordinate of at most one ordered
pair in r. 
$$[(c, d) \in r \text{ and } (c, d') \in r] \Rightarrow [d = d']$$ {#eq:set-19}

Under this definition, c is the domain and d is the image. 

For a given assignment, given A is the domain set and B is the image set,
a function is some operation that maps A to B. One can think of it as a
geometric transformation. 
$$f : A \rightarrow B$$ {#eq:set-20}

The value of $f$ at a can be written $f(a)$. It is the unique element of B
that $f$ assigns.

Define the restriction of $f$ to $A_0$ to be the mapping $A_0$ into $B$
whose rule is 
$$\{(a, f(a) \mid a \in A_0\}$$ {#eq:set-20}

Essentially this is, as the name suggests, restricting the possible inputs
to the function.

The composite $g \circ f$ where $f : A \rightarrow B$ and $g : B \rightarrow C$,
can be defined as a function that maps A onto C. Or formally,
$$\{(a, c) \mid \text{ For some } b \in B, f(a) = b \text{ and } g(b) = c\}$$ {#eq:set-21}

A function is injective or one-to-one, if for each pair of objects in A, the images
are distinct. If every element of B is the image of an element of A, the function
is surjective. If a function is both, it is bijective. Not only can one pass objects
into functions, but also sets, in the following way. If $A_0$ is a subset of A,
$$f(A_0) = \{b \mid b = f(a) \text{ for at least one } a \in A_0\}$$ {#eq:set-22}

If a function is bijective, it has an inverse function, $f^{-1}$.

#### 3 - Relations
A relation on a set A is a subset C of the cartesian product A x A. The special
case being a function whose image set is A. 

An equivalence relation has the following properties:

#) Reflexivity: $xCx$ for every $x$ in A
#) Symmetry: If $xCy$, then $yCx$
#) Transivity: If $xCy$ and $yCz$ then $xCz$

A partition is a way to split up a set into a bunch of smaller subsets such that
the union is the set, and the intersection of any pair is null.

An order relation has the following properties:

#) Comparability: For every $x$ and $y$ in A for which $x \neq y$, either $xCy$ or $yCx$
#) Nonreflexivity
#) Transivitiy

We use tilde, ~, as the generic symbol for an equivalence relation and, <, for an
order relation. 

If X is a set, and < is an order relation on X, and if $a < b$, then $(a, b)$ is 
defined as
$$\{x \mid a < x < b\}$$ {#eq:set-23}


