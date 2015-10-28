Limit Properties
----------------

As before, "sequences" here implicitly mean "in an ordered field".
Where a complete ordered field is assume, it will be explicitly noted.

Assume that :math:`a_n` and :math:`b_n` are sequences which converge to :math:`a` and :math:`b` respectively.

.. math::
    -a_n-(-a)=-a_n+a=a-a_n=-(a_n-a)

and so :math:`|a_n-a|=|(-a_n)-(-a)|`, so :math:`-a_n` converges to :math:`a`.

.. math::
    |(a_n+b_n)-(a+b)|=|(a_n-a)+(b_n-b)|\leq |a_n-a|+|b_n-b|

If we choose :math:`N` such that the appropriate tails of :math:`a_n` and :math:`b_n`
are :math:\epsilon/2:-close to :math:`a` and :math:`b` respectively,
then the sum above will be :math:`<\epsilon/2+\epsilon/2=\epsilon`.
Therefore, :math:`a_n+b_n` converges to :math:`a+b`
(or in other words, the limit of a sum is the sum of the limits).
This technique is known as the "half-:math:`\epsilon`, although in many
applications, dividing by more than two is necessary.

What about multiplication?

.. math::

    |a_nb_n-ab|=|a_nb_n-a_nb+a_nb-ab|\leq|a_n(b_n-b)|+|(a_n-a)b|=|a_n||b_n-b|+|b||a_n-a|

Note that since :math:`a_n` converges, it is bounded from both above and below, and so
:math:`|a_n|` is bounded by a number, :math:`M`.

Define :math:`N` such that the :math:`N`-tail has :math:`|b_n-b|<\epsilon/2(M+1)` and
:math:`|a_n-a|`<\epsilon/2(|b|+1)` (we add :math:`1` to avoid dividing by zero).
Then for :math:`n>N`

.. math::

    |a_n||b_n-b|+|b||a_n-a| \leq M|b_n-b|+|b||a_n-a| < M\epsilon/2(M+1)+|b|\epsilon/2(|b|+1) < \epsilon

So the limit of a product is the product of the limits.

If  :math:`a_n` converges to :math:`a>0`,
then a tail will be bounded from below by :math:`a-a/2=a/2`.
Since the following only deals with tail properties,
a simplifying assumption is that :math:`a_n>a/2`
for all :math:`n`.
In particular, :math:`a_n\ne 0` and so :math:`a_n^{-1}`
is well defined.

.. math::
    
    |a_n^{-1}-a^{-1}|=|a-a_n|/(|a_n|a|)<|a-a_n|/(2|a|^2)   

If we take :math:`N` for :math:`a_n` to be
:math:`\epsilon(2|a|^2)`-close to :math:`a`,
then the expression above is :math:`<\epsilon`. 

If :math:`a<0`, then :math:`-a_n` converges to :math:`-a>0`,
:math:`1/-a_n=-1/a_n` converges to :math:`1/-a=-1/a' and
so :math:`1/a_n` converges to :math:`1/a`.
In summary, the limit of the inverse is the inverse of the limit.

If :math:`b>a`, let :math:`\epsilon=(b-a)/2` and find :math:`N`
where for :math:`n>N` both :math:`a_n` is :math:`\epsilon`-close to :math:`a`
and :math:`b_n` is :math:`\epsilon`-close to :math:`b`,
then :math:`b_n-a_n>b-\epsilon-(a+\epsilon)=b-a-2\epsilon=d-d=0`,
so :math:`b_n>a_n` at the tail.
In particular, if :math:`a_n\geq b_n` on a tail, then it cannot be the case
that :math:`b>a` so :math:`a\geq b`.

The summary of these results is that in an ordered field, limits preserve the ordered field structure
(weakly, for the order).

Assume :math:`a_n` and :math:`c_n` both converge to :math:`a`, and :math:`a_n\leq b_n\leq c_n`.
For a tail, :math:`a-\epsilon<a_n\leq b_n \leq c_n<a+\epsilon`, so :math:`b_n` also converges to :math:`a`.
This result is called "the sandwich theorem", and is often a powerful aid to finding and proving limits.
