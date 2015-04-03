Irrationals -- the Secret Pythagoras Kept
------------------------------------------

The integers allow solving equations like :math:`a+x=b`.
The rationals allow solving equations like :math:`ax=b`.
What other numbers are needed?

In Ancient Greece, Pythagoras and his followers did two things:
they built the rationals to understand music
and they taught each other what is now known in Pythagoras's theorem:
if a right-angled triangle has sides :math:`a`, :math:`b` and a hypotanuse :math:`c`
then :math:`a^2+b^2=c^2`.
Students were taught to keep those secrets, on pain of death.
Why the secrets and the threats?

Consider a right-angled triangle with sides of length :math:`1`.
Call the hypotenuse :math:`c`.
:math:`1^2+1^2=c^2`, or :math:`2=c^2`.

Can :math:`c` be rational?
Assume it is.
We can assume :math:`c` is positive (because :math:`(-c)^2=c^2`),
so :math:`cm=n`, and :math:`2m^2=c^2m^2=n^2`.
If we write :math:`n=(2^k)p`, with :math:`p` odd,
then :math:`n^2=2^(2k)p^2`, and :math:`p^2` is odd.
If we write :math:`m=(2^l)q`, with :math:`q` odd,
then :math:`m^2=2^(2l)q^2`, and :math:`q^2` is odd.
In other words: 
:math:`(2^2k)p^2=2*2^(2l)q^2=2^(2l+1)q^2`
Since :math:`2k\ne 2l+1:`
then :math:`2^{2k}\ne 2^{2l+1}`
If :math:`2^{2k}<2^{2l+1}`,
then
:math:`p^2=2^{2l+1-2k}q^2`, and so :math:`p^2` is even,
and so :math:`p` is even.
If :math:`2^{2l+1}<2^{2k}`, for similar reasons,
:math:`q` is even.

Since both :math:`p` and :math:`q` are odd,
neither can be the case,
so the assumption is wrong: :math:`c` is not "rational".

That is why the Pythagoreans kept those secrets -- they knew the side of the hypotenuse could not be rational.
Indeed the word "irrational" comes from that era,
where it was "illogical" that this would be the case.

It would be nice to be able to solve equations like :math:`c^2` so that triangles' sides will have length.
How can the answers be calculated?

If :math:`0<x<y`, then :math:`x^2<y^2`.

Define two sequences: :math:`a_n` and :math:`b_n`
so that :math:`a_n^2<2<b_n^2`.

 * :math:`a_0=1` and :math:`b_0=2`
 * After having :math:`a_n` and :math:`b_n`, calculate :math:`t=(a_n+b_n)/2`.
   If :math:`t^2<2` set :math:`a_{n+1}=t,b_{n+1}=b_n`. Otherwise, set :math:`a_{n+1}=a_n,b_{n+1}=t`.

Note:
 * :math:`a_n\leq a_{n+1}`
 * :math:`b_{n+1}\leq b_n`
 * :math:`a_n<b_n`.
 * :math:`b_{n+1}-a_{n+1}=1/2(b_n-a_n)`

So :math:`a` and :math:`b` seem to be growing closer,
trying to find the square root of 2.
