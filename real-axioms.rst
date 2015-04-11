Axiomatizing the Real Numbers
-----------------------------

Building the real numbers is a bit more difficult.
Instead, a different route will be taken --
first, the real numbers will be treated axiomatically.
On the assumption that the real numbers exist,
and obey certain axioms,
theorems will be proven.
After getting experience with the real numbers,
and some related techniques,
it will be more easier to understand the construction.

The real numbers are assumed to be a *complete*
*ordered* *field*. 

The axioms for ordered field have been given already,
but here they are repeated:

Addition is an abelian group

 * :math:`a+0=a`
 * :math:`a+(b+c)=(a+b)+c`
 * For every :math:`a`, there is a :math:`-a` such that :math:`a+(-a)=0`
 * :math:`a+b=b+a`

Multiplication is almost an abelian group

 * :math:`a1=a`
 * :math:`a(bc)=(ab)c`
 * For every :math:`a\ne 0`, there is a :math:`a^{-1}` such that :math:`aa^{-1}=1`
 * :math:`ab=ba`

Multiplication distributes over addition

 * :math:`a(b+c)=ab+ac`

Ordered field

There exist a subset of the field, :math:`P` (the positive numbers), such that:

 * For every :math:`a`, exactly one of :math:`a\in P`, :math:`-a\in P` or :math:`a=0` is true
 * If :math:`a,b\in P` then :math:`ab, a+b\in P`

Before defining the axioms of completeness,
the concept of bounds needs to be introduced.
If :math:`A` is a subset of an ordered field,
:math:`q` is an upper bound if :math:`a\leq q`
for every :math:`a\in q`.
Sometimes, an upper bound will not exist.
For example, in the field of rational numbers,
the set of embedded natural numbers has no
upper bound.
Sometimes, an upper bound will exist.
For example, the set :math:`{1,2,3}`
has :math:`5` as an upper bound.

An ordered field will be called complete if whenever a set :math:`A` does have
an upper bound, it has a least upper bound.

 * For every :math:`A`, if there exists a :math:`q` upper bound,
   then there exists an upper bound :math:`p` such that
   if :math:`r` is also an upper bound, :math:`p\leq r`

If :math:`p` is the least upper bound of a set,
then it is the only least upper bound of the set.
Because of that, we call such a number "the supremum" of the
set, and denote :math:`p=\mathtext{sup} A`

The rational numbers, as we have seen, are not complete.
Specifically, the set of values that :math:`a_n`,
defined previously,
does not have an least upper bound.
Here is a proof:
assume there was a least upper bound :math:`a`.
Then because every :math:`b_n` is an upper bound,
:math:`0<a_n\leq a\leq b_n<2` for every :math:`n`.
Because of that,
:math:`a_n^2\leq a\leq b_n^2`.
Recall that :math:`b_n-a_n=2^{-n}`, and so 
:math:`a_n^2\leq a^2\leq b_n^2` and
:math:`b_n^2-a_n^2=(b_n-a_n)(b_n+a_n)\leq 2^{-n}*4`,
and so
:math:`b_n^2-a^2\leq 2^{-n}*4` and
:math:`a^2-a_n^2\leq 2^{-n}*4` and
If :math:`a^2>2`, then write :math:`d=a^2-2>0`.
Since :math:`d` is a rational number,
:math:`d=m/n\geq 1/n > 2^{-n} = 2^{-(n+3)}*4`
and now :math:`a^2-a_n^2< d`,
so :math:`a^2 < d+a_n^2 < d+2 = a^2`
which is a contradiction.
A similar argument shows :math:`a^2<2`
cannot be true, using :math:`b_n`.
So :math:`a^2=2`, but such an :math:`a` cannot
be a rational number. 
This shows that :math:`a_n` does not have a
least upper bound in the field of rational numbers.

So it turns out the rationals are *not* a complete ordered field.
Maybe there is no complete ordered field?
It would not be surprising to know that some axioms have no
structures that satisfy them.
However, maybe there is a complete ordered field.
Just as the natural numbers have been taken up on faith,
the consequences of the axiom "there exists a complete ordered field".

It has already been shown that the natural numbers embed in every ordered
field. 
However, complete ordered fields have a stronger property.

Theorem: (Archimedean property) If :math:`\mathbb{F}` is a complete ordered field,
then for every :math:`a\in F` there is a natural number :math:`n`,
such that :math:`a<n`.

Proof:
Suppose there is an :math:`a` without such a natural number.
Then :math:`n\leq a` for every :math:`n`,
and so the natural numbers have an upper bound.
By completeness, they have a least upper bound, :math:`b`.
Since :math:`n+1` is a natural number if :math:`n` is,
:math:`n+1\leq b` for every natural number :math:`n`.
Therefore, :math:`n\leq b-1<b` for every :math:`n`,
so :math:`b-1` is also an upper bound.
Since :math:`b` was a least upper bound,
this cannot be.

If a field is Archimedean, and :math:`x>0`,
then for any :math:`y>0` there is a natural number :math:`n>y/x`
or :math:`y<nx`.
This is known as the "hair grows at some amount of miles per hour"
consequence:
no matter how some small some number is,
and how big another number is,
they are commensurable:
if we add the small one to itself enough times,
we will overtake the bigger one.

Assume :math:`a<b` in an Archimedean field.
Then there is a rational number :math:`a<q<b`.
First the case :math:`0<a<b`.
Pick a natural number :math:`n` such that :math:`n>(b-a)^{-1}`.
Therefore, :math:`1/n<(b-a)`.
Using the Archimedian property again,
there is a natural number :math:`k` such that :math:`k/n>a`.
Any set of natural numbers has a first element,
so there is a smallest number :math:`m` such that :math:`m/n>a`.
Now, if :math:`m/n\geq b`,
then :math:`(m-1)/n\geq b-1/n>b-(b-a)=a`,
and so :math:`m` is not the smallest number.
Therefore :math:`q=m/n` satisfies the condition.
If :math:`a<0<b`, then :math:`0` satisfies the condition.
Lastly, if :math:`a<b<0`, find a :math:`q` such that :math:`-b<q<-a` (by the first part),
and so :math:`a<-q<b` and :math:`-q` satisfies the condition.

This result can be summarized as "in an Archimedean field, there is a rational number between any
two elements", or "the rationals are dense in any Archimedean field".

Assume :math:`\mathbb{F}` and :math:`\mathbb{G}` are complete ordered fields.
If :math:`A` is the set of all rationals :math:`q<f` for some :math:`f\in\mathbb{F}`.
There is a natural number :math:`n>f` and so :math:`A` is bounded from above by :math:`n` in :math:`\mathbb{G}` as well.
Therefore, there is a least upper bound in :math:`\mathbb{G}`.
Define :math:`g(f)` to be this upper bound.
This defines a function :math:`g` from
:math:`\mathbb{F}` to :math:`\mathbb{G}`.

It is straight-forward to see that this function preserves addition, multiplication and order.
It is also straight-forward to verify that the same function defined from
:math:`\mathbb{G}` to :math:`\mathbb{F}`.
Therefore, any two complete ordered fields are one and the same.

So given that a complete ordered field does exist,
it is Archimedean and unique.
Therefore, under the axiom that it exists,
it is fine to talk about "the complete ordered field",
and for short, this will be referred to as "the real number field".
