Building the Rationals
----------------------

The integers allow addition and subtration -- however, division is still tricky.
For example, there is no :math:`x` such that, :math:`2x=1`.
If :math:`2x=1`, then :math:`x+x=1`, and so :math:`x<=1`.
Since :math:`1+1=2\ne 1`, :math:`x<1`.
However, :math:`0+0=1`, so :math:`0<x<1`.

Much like the integers, first consider how :math:`X/Y` should behave and then formalize.
Much like we did with the rationals, we want to think how $latex X/Y$ behave, and then formalize it.

 * :math:`X/Y=Z/W` if and only if :math:`XW=ZY`
 * :math:`X/Y+Z/W=(XW+YZ)/YW`
 * :math:`(X/Y)(Z/W)=(XZ)/(YW)`

Formally define: for two pairs of integers, :math:`(X,Y)~(Z,W)` if :math:`XW=ZY`.

Exercise:
 * Prove this relationship is reflective, symmetric and transitive.

Let :math:`\mathbb{Q}` be the set of equivalence classes under this relationship.

Define multiplication and addition based on the earlier inspiration as:

.. math::
    [(X,Y)]+[(Z,W)]=[(XW+YZ,YW)]

.. math::
    [(X,Y)][(Z,W)]=[(XZ,YW)]

Exercise:
 * Prove these definitions depend only on the equivalence classes.

Note that :math:`[(X,1)]+[(Y,1)]=[(X+Y,1)]` and :math:`[(X,1)][(Y,1)]=[(XY,1)]`
and so :math:`e:\mathbb{Z}\to\mathbb{Q}` defined by :math:`e(X)=[(X,1)]` is an embedding.
Much like earlier, it is sometimes useful to confuse :math:`e(X)` and :math:`X`.

Note that if :math:`[(X,Y)]\ne 0` (or, really, :math:`e(0)`), than :math:`X\ne 0`.
In this case, :math:`[(Y,X)]\in\mathbb{Q}` and :math:`[(X,Y)][(Y,X)]=[(XY,YX)]=[(1,1)]=e(1)`
So every element different from :math:`0` has a multiplicative inverse.

In conclusion, the field axioms are satisfied:

 * :math:`a+0=a`
 * :math:`a+(b+c)=(a+b)+c`
 * :math:`a+b=b+a`
 * For every :math:`a` there is a :math:`-a` such that :math:`a+(-a)=0`
 * :math:`a1=a`
 * :math:`a(bc)=(ab)c`
 * :math:`ab=ba`
 * For every :math:`a\ne 0` that is a :math:`a^{-1}` such that :math:`aa^{-1}=1`
 * :math:`a(b+c)=ab+ac`

The field of rationals is called :math:`\mathbb{Q}`.

The embedding of the natural numbers into the integers,
combined with the embedding of the integers into the rationals,
gives an embedding of the natural numbers into the rationals.
Define a rational number, :math:`r` to be "positive" if there are
natural numbers that are not :math:`0`, :math:`n` and :math:`m`, such that
:math:`n=rm`. 

Theorem: for every rational, :math:`r`, exactly one of those is true:
 * :math:`r=0`
 * :math:`r` is positive
 * :math:`-r` is positive

Proof:
Assume :math:`r=[(X,Y)]` for :math:`X` and :math:`Y` integers.
Since :math:`Y\ne 0`, by the structure of integers,
either :math:`Y` is natural or :math:`-Y` is natural.
If :math:`-Y` is natural, by the definition of equivalence,
:math:`r=[(-X,-Y)]`, so we can assume :math:`Y` is natural.

If :math:`X=0`, then :math:`r=0`,
and :math:`rm=0` for every natural number :math:`m`.

If :math:`X` is natural,
then :math:`rY=X`.

If :math:`-X` is natural,
then :math:`-rY=-X`.

QED

Theorem: If :math:`r` and :math:`s` are positive,
then so are :math:`r+s` and `rs`.

Proof:
If :math:`rm=n` and `sl=k`,
then :math:`(rs)ml=nk` and

.. math::
    (r+s)ml=rml+sml=rml+slm=nl+km

And :math:`ml` and :math:`nl+km` are natural numbers,
since the natural numbers are closed under addition
and multiplication.

QED

Note that :math:`1`

Define :math:`r\leq s` if :math:`r=s`
or :math:`s-r` is positive.

It is straightforward to verify that

 * :math:`x\leq y` or :math:`y\leq x` and if both are true, :math:`x=y`
 * If :math:`x\leq y` then :math:`(x+z)\leq (x+z)`
 * If :math:`x\leq y: and :math:`0\leq z` then :math:`xz\leq yz`

Togther with the field axioms, those are the axioms of an "ordered field".

Exercise: Assume :math:`F` is an ordered field, there is an embedding
:math:`e:\mathbb{Q}\to F`.

Hint-a-long:
Define a sequence by recursion:

 * :math:`e(0)=0_F`
 * :math:`e(n+1)=e(n)+1_F`

Prove that :math:`n<m` implies :math:`e(n)<e(m)`

Define :math:`e(-n)=-e(n)`, and :math:`e(n/m)=e(n)/e(m)`.

The rationals, therefore, are the smallest ordered field.
