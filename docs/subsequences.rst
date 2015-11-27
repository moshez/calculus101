Subsequences and convergence
============================

If :math:`a_n` is a sequence of real numbers,
and :math:`n_k` is a sequence of natural numbers that is increasing
(that is, `:math:`n_{k+1} > n_k`),
then we can define a sequence :math:`a_{n_k}`.
This is called a subsequence of :math:`a_n`.

Subsequences interact with convergence in a few interesting ways.
First, if :math:`a_n` converges to :math:`a`, then every subsequence
does as well.

To prove this, we will first show a useful lemma: if :math:`n_k` is an increasing sequence
of natural numbers, than :math:`n_k \geq k`.
We show this by induction: :math:`n_0` is a natural number, so by definition, :math:`n_0 \geq 0`.
Assume :math:`n_k \geq k`, then :math:`n_{k+1} > n_k \geq k`. Since :math:`n_{k+1} > k`,
then :math:`n_{k+1} \geq k+1`. 

Now, let :math:`\epsilon > 0`. Since :math:`a_n` converges to :math:`a`, there is an :math:`N`
such that :math:`n > N` implies :math:`|a_n - a| < \epsilon`. Now, if :math:`k > N`, then
:math:`n_k > N`, so :math:`|a_{n_k} - a| < \epsilon`. Since this is true for every :math:`\epsilon`,
we have proved the subsequence converges.

Since :math:`a_n` is a subsequence of itself (via :math`n_k = k`), if every subsequence converges
to :math:`a`, than so does :math:`a_n`. Note that if :math:`a_n` converges to :math:`a`,
then so does every subsequence as shown above, and therefore, so does every subsubsequence.
In fact, a weaker result is true: if every subsequence *has* a subsubsequence that converges to
:math:`a`, than so does :math:`a_n`.

In order to prove this, we need to master a technique that is mechanical
yet subtle: reversing complicated statements. We need to specify what it means for a sequence to
*not* converge to :math:`a`. If :math:`a_n` does not converge to :math:`a`, then there exists
an :math:`\epsilon > 0` such that for every :math:`N` there is an :math:`n>N` such that
:math:`|a_n - a| \geq \epsilon`.

The easiest way to approach the theorem is to prove the logical converse: if :math:`a_n` does
not converge to :math:`a`, then there is a subsequence with no subsubsequence that converges
to :math:`a`.

Let :math:`a_n` be a sequence, and let us assume :math:`a_n` does not converge to :math:`a`.
Let :math:`N = 0`. Then we can find, as above, :math`n_0`, so that :math:`|a_{n_0} - a| \geq \epsilon`.
Now we define a subsequence recursively: let :math:`N=n_k`, find :math:`n_{k+1} > N` such that
:math:`|a_{n_{k+1}} - a| \geq \epsilon`. Note that since every element of this subsequence is
:math:`\epsilon`-away from :math:`a`, than no subsubsequence can converge to :math:`a`.

We note that here we did not take advantage of the properties of real numbers, and indeed,
the above results are true for rational numbers as well. The following result is not (and,
indeed, it is possible to show that it is unique to the real numbers).

Let :math:`a_n` be a bounded sequence, `-M<a_n<M` for every :math:` n`.
Then it has a converging subsequence.
Since this result is so important, both for understanding real numbers and,
practically,
to prove results about real numbers,
there will be too proofs given.

We define two sequences, :math:`c_k` increasing and :math:`d_k` decreasing, by induction,
with the property that there is an infinite number of :math:`a_n` such that :math:` c_k\leq a_n\leq d_k` for every :math:` k`.
We set :math:` c_0=-M,d_0=M`. Since all :math:`a_n` satisfy that, an infinite number of them do.
Assume we have :math:`c_k<d_k`. Set :math:`m=(c_k+d_k)/2`.
Assume a finite number of :math:` a_n` have :math:` c_n\leq a_n\leq m`[1] and a finite nmber of :math:` a_n` have :math:` m\leq a_n\leq d_n`[2].
However every :math:` a_n` is either :math:` \leq m` or :math:` \geq m`, so only a finite number of :math:` a_n` have :math:`c_k\leq a_n\leq d_k`.
This contradicts the inductive assumption, so one of [1] or [2] is infinite. If [1] is infinite,
set :math:` c_{k+1}=c_k,d_{k+1}=m` otherwise :math:` c_{k+1}=m,d_{k+1}=d_k`.
We see that :math:`d_k-c_k=1/2^k` and so converges to :math:`0`.

We apply Cantor's lemma, and get :math:`c_k` and :math:`d_k` converge to :math:`a`.
Set :math:`n_0 = 0`. Then :math:`c_0 = -M < a_{n_0} < M = d_0`.
Recursively, find :math:`n_{k+1} > n_k` such that :math:`c_{k+1} \leq a_{n_{k+1}} \leq d_{k+1}`.
One such must exist, because there are infinite members of :math:`a_n` between :math:`c_{k+1}` and :math:`d_{k+1}`,
but only a finite number :math:`\leq n_k`.

By the Sandwich theorem, we have :math:` a_{n_k}` converging to :math:` a`.

Here is another proof for this: let :math:`a_n` be any sequence. We define a subsequence by induction:
let :math:`n_0` be such that `a_{n_0}` is less than any element in the sequence.
Let :math:`n_{k+1}` be such that it is :math:` >n_k` and the smallest element that is
:math:` \geq` than `a_{n_k}`. If this construction succeeds, we have an increasing subsequence.
This construction might fail: at any stage, the "smallest" element might not exist.
However, if the smallest element does not exist, we define a new subsequence, :math:`m_k`.
Without loss of generality, we assume that the smallest element does not exist in the first stage:
therefore, for every :math:`n`, :math:`a_n` is not the smallest element.
We take :math:`m_0` to be :math:`0`.
If we have :math:`m_k`, we notice there must be an infinite number of :math:`m`, :math:`a_m < a_{m_k}`.

This means for every sequence, we can either construct an increasing subsequence or a decreasing subsequence.
Since bounded increasing or decreasing sequences, we constructed a converging subsequence.
