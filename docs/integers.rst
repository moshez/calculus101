Building the Integers
----------------------

We are already one leg up on the ancient Greeks,
as we have a 0 in our natural numbers.
However, it turns out that we need some more numbers to be able to answer questions like
"If I have $3, and I spend $4, how much money do I have?" (answer: "$1 in debt", of course).

There are several ways to construct the integers.
The technique used here will also come in handy later: 
imagine they exist, figure out how they would look, and then formalize.
So, assume that there is an answer for
"I have :math:`X` things, and I spend :math:`Y` things.
How much do I have left?"
Call this answer :math:`A(X, Y)`.
Intuitively, imagine it to be :math:`X-Y`.
What properties will it have?

 * If :math:`X+W=Y+Z`, then :math:`X-Y=Z-W`, or :math:`A(X,Y)=A(Z,W)`.
 * :math:`(X-Y)+(Z-W)=(X+Z)-(Y+W)` or :math:`A(X, Y)+A(Z, W)=A(X+Z, Y+W)`
 * :math:`(X-Y)(Z-W)=(XZ+YW)-(XW+YZ)` or :math:`A(X,Y)A(Z,W)=A(XZ+YW,XW+YZ)`

In order to formalize this, another powerful technique is helpful -- equivalence classes.
Take the collection of all pairs of natural numbers :math:`(X, Y)`.

Definition: :math:`(X,Y)\tilde (Z,W)`
(read as ":math:`(X,Y)` is equivalent to :math:`(Z,W)`)
if :math:`X+W=Z+Y`.

In order for a definition of a relation to be a proper equivalence,
three things need to be proven: reflectivity, symmetry and transitivity.

Reflectivity: this means each thing should be equivalent to itself.
Indeed, :math:`(X,Y)~(X,Y)` because :math:`X+Y=X+Y`.

Symmetry: if one thing is equivalent to another,
then the other thing should be equivalent to the first thing.
Indeed, if :math:`(X,Y)~(Z,W)` then :math:`X+W=Z+Y`,
but then :math:`Z+Y=X+W`, and so :math:`(Z,W)~(X,Y)`.

Transititivity: Assume :math:`(X,Y)~(Z,W)` and :math:`(Z,W)~(U,V)`.
Then :math:`(X,Y)~(U,V)`, or :math:`X+V=Y+U`.
We know that :math:`X+W=Y+Z` and :math:`Z+V=U+W`.
Adding both sides, we get :math:`X+W+Z+V=Y+Z+U+W`.
Using the commutative law, :math:`X+V+W+Z=Y+U+W+Z`.
Now, use the eliminative property of addition,
and get :math:`X+V=Y+U`.

The other part of the technique is moving from the set of "things"
to the set of "equivalence classes of things".

Define an equivalence class as
"all elements that are equivalent to a given element"

Formally: :math:`[(X,Y)]={(Z,W): (Z,W)~(X,Y)}`.

TODO [Issue #4]: Show that :math:`(X,Y)~(Z,W)` iff
:math:`[(X,Y)]=[(Z,W)]`.

The set of the integers: :math:`\mathbb{Z}={[(X,Y)]: X,Y\in \mathbb{N}}`.
Just like the natural numbers, the integers need operations.

In order to inspire the definition, again informally view :math:`(X,Y)` as :math:`X-Y`.
So :math:`X-Y+Z-W=(X+Z)-(Y+W)`,
and :math:`(X-Y)(Z-W)=(XZ+YW)-(XW+YZ)`.

Formally:

.. math::
    [(X,Y)]+[(Z,W)]=[(X+Z,Y+W)]

For this definition to make sense, the following theorem is needed:

Theorem: If :math:`(X,Y)~(X',Y')` and :math:`(Z,W)~(Z',W')` then :math:`(X+Y,Z+W)~(X'+Y',Z'+W')`.

Proof:

.. math::
    X+Y'=X'+Y

.. math::
    Z+W'=Z'+W

Adding the equalities:

.. math::
    X+Y'+Z+W'=Z'+W+X'+Y

Rearrange:

.. math::
    X+Z+Y'+W'=X'+Z'+Y+W

Which is the definition of :math:`(X+Y,Z+W)~(X'+Y',Z'+W')`.

Because of this theorem,
it does not matter which elements of the equivalence class
are used to define addition,
and so the definition of addition makes sense.

Define multiplication by :math:`[(X,Y)][(Z,W)]=[(XZ+YW,XW+YZ)]`

Exercise: Prove that this definition makes sense.
Hint [Issue #5]: Follow the same steps as the proof above -- write down the equivalences.
This time, how about multiplying them?

Note that :math:`[(X,0)]+[(Y,0)]=[(X+Y,0)]` and :math:`[(X,0)][(Y,0)]=[(XY,0)]`.
Also note that if :math:`X\neq Y`, it is not the case that :math:`(X,0)~(Y,0)`,
and so :math:`[(X,0)]\neq [(Y,0)]`.

Therefore, the function :math:`i:\mathbb{N}\to\mathbb{Z}` preserves uniqueness,
addition and multiplication.
Functions that preserve uniquenes and structure are called "embeddings".
It is often convenient, and perfectly safe,
to consider the embedding as an identity, and confuse :math:`n` and :math:`[(n,0)]`.

Note :math:`[(X,Y)]+[(Y,X)]=[(X+Y,Y+X)]=[(0,0)]=e(0)`.
Define $-[(X,Y)]=[(Y,X)]$, and the equality above can be written as:

.. math::

   a+(-a)=0

The integers with addition and multiplication are called a ring for satisfying
the following axioms:

* :math:`a+0=a`
* :math:`a+(b+c)=(a+b)+c`
* :math:`a+b=b+a`
* For every :math:`a` there is a :math:`-a such that :math:`a+(-a)=0`
* :math:`a1=a`
* :math:`a(bc)=(ab)c`
* :math:`ab=ba`
* :math:`a(b+c)=ab+ac`

(Notice that above we wrote :math:`0` and :math:`1` for :math:`e(0)` and :math:`e(1)`).

Define :math:`a-b=a+(-b)`, and any two integers can be subtracted.

Note that for every :math:`X` and :math:`Y`,
either :math:`Y>X` in which case there is an number :math:`n` such that :math:`X=Y+n` or :math:`X+0=Y+n`,
which means :math:`[(X,Y)]=[(n,0)]`,
either :math:`Y>X` in which case there is an nteger :math:`n` such that :math:`Y=X+n` or :math:`n+X=0+Y`,
which means :math:`[(X,Y)]=[(0,n)]=-[(n,0)]`,
:math:`X=Y` which means :math:`[(X,Y)]=[(0,0)]`.

In other words, for every integer, :math:`z`, either :math:`z=n`, :math:`z=-n` or :math:`z=0`,
with :math:`n` a non-zero natural number.

This our structure theorem for the integers: every integer is either a natural number or the inverse of a negative number.
