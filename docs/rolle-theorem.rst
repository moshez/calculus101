Rolle's Theorem
===============
We note here that if :math:`f(x)=ax+b`, then :math:`f(x)-f(x_0)=a(x-x_0)` and so :math:`[f(x)-f(x_0)]/[x-x_0]=a`, and so :math:`f'(x)=a` for every :math:`x`.

Let :math:`f` be a derivable function on a segment :math:`A=[a,b]`, and assume that :math:`f(a)=f(b)`, then there is a number :math:`c` such that :math:`a<c<b` and :math:`f'(c)=0`. Why?

Since :math:`f` is derivable, it is continuous. So it attains its minimum :math:`m` and its maximum, :math:`M`. If :math:`m=M` then all values of :math:`f` are the same, and a constant function has derivative :math:`0` at all points. Otherwise, on e of those is not equal to :math:`f(a)`. The point where the one not equal to :math:`f(a)` is attained, is not :math:`b`, and so it is a :math:`c` such that :math:`a<c<b`. But at this point, a minimum or a maximum is attained not on an endpoint, so that :math:`f'(c)=0`.

Now let :math:`f` be any derivable function on :math:`[a,b]`. Define :math:`S=[f(b)-f(a)]/[b-a]`, the slope of :math:`f`. Define :math:`g` by :math:`g(x)=f(x)-[Sx-Sa]`. Then :math:`g(a)=f(a)`, and :math:`g(b)=f(b)-Sb=f(b)-S[b-a]=f(b)-[f(b)-f(a)]/[b-a][b-a]=f(b)-[f(b)-f(a)]=f(b)-f(b)+f(a)=f(a)`. Therefore, by the previous discussion, there is :math:`c`, :math:`g'(c)=0`. But :math:`g'(x)=f'(x)-S`, and so :math:`f'(c)=S=[f(b)-f(a)]/[b-a]`. So we see that if a function is derivable on an interval there is a point where the derivative is equal to the slope.

Here is a simple use: if :math:`f'(x)\geq 0` for every :math:`x` if :math:`a<x<b`, then :math:`f` is increasing. In order to see why, let `a\leq cf(c)`. For similar reasons, if the derivative is always negative, the function is decreasing.

Another way to write the same equation, by the way, is :math:`f(b)=f(a)+f'(c)[b-a]` for some :math:`c`, :math:`a<c<b`.
