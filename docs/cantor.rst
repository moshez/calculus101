Cantor's Lemma
--------------

A (closed) interval, :math:`[a,b]` is a set of numbers: :math:`\{x: a\leq x\leq b\}`.
Intervals can contain other intervals: :math:`[a,b]\subset [c,d]` if and only if
:math:`a\leq c` and :math:`d\leq b`.

The next lemma allows defining limits without knowing what they are,
or showing that a sequence of intervals has a point in common.

Assume :math:`a_n\leq b_n` are two sequences,
:math:`a_n` monotonically increasing and :math:`b_n` monotonically decreasing.
Also assume that the sequence :math:`b_n-a_n` converges to :math:`0`.

These sequences can be thought of a sequence of intervals.
The monotonicity requirements mean that each interval contains all following ones.
The convergence requirement says that the limit of the lengths of the intervals is :math:`0`.

Since :math:`b_n` is decreasing, :math:`b_n\leq b_1`, and so :math:`a_n\leq b_1`.
Therefore, :math:`a_n` is bounded, and so has a limit, :math:`a`.
For similar reasons, :math:`b_n` is bounded and so has a limit, :math:`b`.

By the results on the limits of addition and negation,
:math:`b-a=0`, so :math:`b=a`.
Call the limit :math:`c`.
Limits for monotnic sequences are the bounds,
so :math:`a_n\leq c\leq b_n` for every :math:`n`.

If :math:`d<c` the because :math:`c` is the least upper bound on :math:`a_n`,
for some :math:`n`, :math:`d < a_n`,
and therefore :math:`d\notin [a_n,b_n]`.
Similarly, if :math:`d>c`, some :math:`b_n` is smaller than :math:`d`,
and therefore :math:`d\notin [a_n,b_n]`.

The only number that is common to all intervals is :math:`c`.

This result is known as "Cantor's Lemma".

Here is an application of this lemma:
if :math:`f:N\to [0,1]` is a function
there is a number :math:`x`, :math:`f(n)\neq x` for every :math:`n`.

Define a sequence by induction.

:math:`a_0=0` and :math:`b_0=1`.

look at :math:`f(n)`.
For :math:`n+1`, define :math:`c_n=b_n-a_n`.
:math:`[a_n,b_n]` is the union of three intervals:

 * :math:`[a_n,a_n+c_n/3]`
 * :math:`[a_n+c_n/3,a_n+2c_n/3]`
 * :math:`[a_n+2c_n/3,b_n]`

Not all of them can contain :math:`f(n)`,
because the intersection of all three is empty.
For :math:`[a_{n+1},b_{n+1}]`,
choose the smallest that does not contain :math:`f(n)`

Note that by induction, :math:`0<=b_n-a_n = 3^{-n}<1/n`
and so the conditions for Cantor's Lemma are fullfilled.

Let :math:`c` be the common limit.
By the :math:`n+1`-st stage, :math:`c!=f(n)`.
This proves the result.

This result is often summarized as "there are more
real numbers between :math:`0` and :math:`1` than
integers.
