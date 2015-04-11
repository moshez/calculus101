Sequences and Convergance
-------------------------

Recall the definition of a sequence:
a sequence of :math:`X`s is a function from the natural numbers to :math:`X`.
Usually, instead of :math:`f(n)` it is written as :math:`a_n`.
In this chapter, unless mentioned otherwise,
sequences will be sequences in an ordered field.

Let :math:`a` and :math:`b` real numbers,
and :math:`\epsilon>0` be a real number
(informally, think of it as "small").
If :math:`x<y+\epsilon`, define it as :math:`x` is
:math:`\epsilon`-almost smaller than :math:`y`.
If :math:`a` is :math:`\epsilon`-smaller than :math:`b` and
:math:`b` is :math:`\epsilon`-smaller than :math:`a`, then
:math:`a-\epsilon<b<a+\epsilon`, or
:math:`-\epsilon<b-a<\epsilon`.

Definition: In an ordered field, the absolute value :math:`|x|` is defined as

.. math::
    |x| = \text{max}{x,-x}

Since 

.. math::
    b-a<\epsilon

and 

.. math::
    a-b<\epsilon

then

.. math::
    |b-a| < \epsilon

Call this ":math:`b` and :math:`a` are :math:`\epsilon`-close".
Note that since :math:`|b-a|=|a-b|`, this relationship is symmetric
(though not, in general, transitive).
An alternative way of saying it is "within :math:`epsilon` of each other".
The reason this relationship has no many ways is because this,
above all else, defines calculus.

If :math:`a_n` and :math:`b_n` are sequences,
and there exists :math:`N` such that
for all :math:`n>N`, :math:`a_n=b_n`,
then they "share a tail".
Sharing a tail is obviously a reflexive
and symmetric condition.
It is also transitive:
if :math:`a_n` shares a tail with :math:`b_n`, starting at :math:`N`,
and :math:`b_n` shares a tail with :math:`c_n`, starting at :math:`M`,
then if :math:`n>\text{max}{N,M}`,
:math:`a_n=b_n=c_n`,
and so :math:`a_n` shares a tail with :math:`c_n`.

A property of sequences is called a tail property if it is the same
for sequences sharing a tail.

Here is an example: the property of having all the elements in a sequence bounded from above
is a tail property, though it is not immediately obvious that it is.

Lemma: Every finite set has an upper bound

Proof: By induction on the size of the set. If the size is 0, the set is empty and so any number (say, :math:`1`) is an upper bound.
Assume every set of size :math:`n` is bounded.
If :math:`A` is a set of :math:`n+1` elements, let :math:`x\in A`.
:math:`A-{x}` is a set of :math:`n` elements,
so it has an upper bound, :math:`b`.
If :math:`b\geq x`, then :math:`b` is an upper bound for :math:`A`.
Otherwise :math:`b<x`, and so :math:`x` is an upper bound for :math:`A`.
Either way, :math:`A` is bounded from above.

Now, if :math:`a_n` is a sequence which shares a tail with :math:`b_n`,
and the latter is bounded from above by :math:`b`,
then for :math:`n>N`, :math:`a_n=b_n\leq b`.
If :math:`a` is an upper bound for :math:`{a_1,...,a_{N-1} }`,
then :math:`\text{max}{a,b}` is an upper bound for all of :math:`a_n`.

Being bounded from above by a particular number is not, of course, a tail property.
It can be explicitly transformed to a tail property by looking only at tails:
a sequence :math:`a_n` will be said to be "eventually bounded from above" by :math:`a`
if there exists a :math:`N` such that for all :math:`n>N`, :math:`a_n\leq a`.
It is straightforward to verify that this is a tail property.
Similarly, a sequence is defined to be "eventually bounded from below" by :math:`a`
if there exists a :math:`N` such that for all :math:`n>N`, :math:`a_n\geq a`.

A sequence, :math:`a_n` is eventually :math:`\epsilon`-close to :math:`a`
if it is both eventually bounded from above by :math:`a+\epsilon` and
eventually bounded from below by :math:`a-\epsilon`.
If :math:`a_n` is :math:`\epsilon`-close to :math:`a` for all :math:`\epsilon>0`,
then :math:`a_n` converges to :math:`a`.

Note that any sequence that converges has a bounded tail, and therefore it is bounded.
In other words, an unbounded sequence will not converge to anything.

A sequence is said to be increasing if for all :math:`n`, :math:`a_n\leq a_{n+1}`.
A sequence is said to be decreasing if for all :math:`n`, :math:`a_n\geq a_{n+1}`.
A sequence is said to be monotonic if it is either increasing or decreasing.

Theorem: in a complete ordered field, every monotonic sequence converges.

Proof:
First assume that :math:`a_n` is increasing. Let :math:`a` be a least upper bound.
Then :math:`a_n\leq a<a+\epsilon` for every :math:`n` and :math:`\epsilon`.
Since :math:`a` is a least upper bound, and :math:`a-\epsilon<a`, then
:math:`a-\epsilon` is not an upper bound.
So there is a :math:`N`, :math:`a-\epsilon<a_N`.
If :math:`n>N`, :math:a-\epsilon<a_n<a+\epsilon`.

Now if :math:`a_n` is decreasing, then :math`-a_n` is increasing and converges
to :math:`a`.
Note that :math:`|-a_n-a|=|a_n-(-a)|`, and so :math:`a_n` converges to :math:`-a`.

QED

Note that this theorem is only true in complete ordered fields.
