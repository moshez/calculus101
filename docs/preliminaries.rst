Preliminaries
-------------

This text covers things from the basics.
However, there are a few things that will be assumed without deep justification --
perhaps to be filled by a "Set Theory 101" text.

The first is sets.
A set is a collection of elements.
A set can be indicated by its elements: :math:`{2,5,9}`.
A set can also be indicated by a property of its elements: :math:`{x:x>5}`.

The second is functions.
The intuitive idea of a "function" is "something that assigns each element in its domain a value".
Making this notion more formal requires a surprise --
we do not have any rules of assignment or a way of calculating the result.
The formal definition of a function is
"a set of pairs :math:`(x, y)` such that there are no two pairs
:math:`(x, y)` and :math:`(z, w)` where :math:`x=z` but :math:`y\neq w`".
The intuition should be not the rules of assignment,
but the graph of a function as its true meaning.
When we specify a function like :math:`f(x)=x+5`,
what we are saying is
"the set of all pairs :math:`(x, y)` where, say,
:math:`x` is a rational number and
:math:`y=x+5`,
or :math:`{(x,y):y=x+5}`.

The third is the natural numbers.
For mathematicians, the natural numbers always include :math:`0` -- :math:`{0, 1, 2, ...}`.
The natural numbers come with addition and multiplication,
which obey the following rules:

* Neutrality of :math:`0`: :math:`x+0=x` for every :math:`x`
* Neutrality of :math:`1`: :math:`x1=x` for every :math:`x`
* Uniqueness of addition: :math:`x+y=x+z` implies :math:`y=z`
* Almost-uniqueness of multiplication:  :math:`xy=xz` implies :math:`y=z` or :math:`x=0`
* Associativity of addition: :math:`x+(y+z)=(x+y)+z`
* Associativity of multiplication: :math:`x(yz)=(xy)z`
* Commutativity of addition: :math:`x+y=y+x`
* Commutativity of multiplication: :math:`xy=yx`
* Distributive law: :math:`x(y+z)=xy+xz`
* Almost inverses: if :math:`x \neq y`, then either there is a :math:`z` such that :math:`x+z=y` or :math:`y+z=x`, but not both.

Definition: :math:`x\leq y` if there is a :math:`z` such that :math:`x+z=y`

Claim: If :math:`x\leq y` and :math:`y\leq z` then :math:`x<z`

Before proving this, note that even though it seems utterly obvious,
in math nothing is taken on faith.
Even things like this must be formally proven.

How can a proof proceed?
Clearly, this would not be true of any relationship,
so the definition of :math:`\leq` needs to be used.
When substituting the definition, the results are:

.. math::

  x + t = y

  y + s = z

Note that since we use :math:`y` and :math:`z` in the theorem statement,
different letters were used instead.

If :math:`x+t=y`, then :math:`x+t` can be subsituted
in the second equation for :math:`y`,
leading to :math:`(x+t)+s=z`.
Applying the associative law,

.. math
  x+(t+s) = z

And so :math:`x\leq z`

We write :math:`x<y` for :math:`x\leq y` and :math:`x\neq y`.

The last thing taken for granted for the natural numbers is the law of induction.
The law of induction says that if a property holds for :math:`0` and
whenever it holds for :math:`x` it holds for :math:`x+1`,
then it holds for all integers.
This is a powerful axiom: it can actually build addition, multiplication and order by itself.

Here is a simple example: "no numbers between :math:`0` and :math:`1`": there is no number :math:`x`
such that :math:`0<x<1`.

Proof:
Since :math:`0=0`, for :math:`x=0` it is not the case that :math:`0<x<1`.

Let :math:`y=x+1`. We prove that it is not the case that :math:`y<1`.
Indeed, since :math:`y=x+1`, we know that :math:`1\leq y`.
By the axioms on order, either :math:`y=1` or it is not the case that :math:`y\leq 1`,
and in either case, it is not the case that :math:`y<1`. QED

Notice that this was a simple application --
the fact that the inductive statement holds for :math:`x` was not even used. 

TODO: Write hint-along-exercises for:
 * Prove :math:`x\leq y` and :math:`y\leq x` implies :math:`x=y`
 * Prove :math:`0\leq x` for every :math:`x`
 * Prove order respects addition and multiplication, as an exercise
 * Prove "no numbers between :math:`x` and :math:`x+1`

Here is a more interesting example: every non-empty set of integers has a least element.

Now, this does not seem to be a statement where we can use the law of induction.
Instead, we transform it into a statement where we can use induction:
for every set :math:`A`, if :math:`x \in A` (read as ":math:`n` is in :math:`A`),
then :math:`A` has a least element.
Induction on this statement, however, will fail.
As is often the case, the hardest part is figuring out the correct inductive statement.

Proof:
The inductive statement is:
"for every :math:`x`,
if :math:`x\leq y` and :math:`x\in A`,
then :math:`A` has a least element".

First, verify for :math:`0`: if :math:`x\leq 0`, and :math:`x\in A`, then :math:`x=0`,
and since :math:`0\leq z` for all natural numbers :math:`z`, :math:`0` is the least element.

Assume the statement holds for :math:`x`.
Assume :math:`y=x+1\in A`.
If there is a :math:`z<y` and :math:`z\in A`,
then :math:`z\leq x` and 
by the assumption, :math:`A` has a least element.
Otherwise, for every :math:`z\in A`, :math:`y\leq z` and so
:math:`y` is the least element.
Either way, :math:`A` has a least element,
and so the induction is proven. QED

We write :math:`\mathbb{N}` for the set of natural numbers.

TODO: write hint-a-long exercise for:

* If :math:`A` is a set, and :math:`p\in A` is a member,
  :math:`B` is the set of all pairs :math:`(a, n)` for
  :math:`a\in A` and :math:`n` a natural number,
  and :math:`f:B\to A` is a function,
  then there is a unique function,
  :math:`s:\mathbb{N}\to A` such that
  :math:`s(0)=p` and :math:`s(n+1)=f(s(n), n)`

We call function from the natural numbers is also
called a "sequence",
and the technique above is called
"defining a sequence by recursion".
It is a powerful technique for generating sequences.
