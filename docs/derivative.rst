Derivative
==========
Let :math:`f` be a function. For :math:`x_0`, and :math:`x`, we can define a function on :math:`h` as :math:`[f(x)-f(x_0)]/[x-x_0]`. That measures the average change in :math:`f` between :math:`x_0` and :math:`x`. It is not well-defined, of course, at :math:`x_0` itself. However, that does not stop us from asking about what limit it has at :math:`x_0`. There might, of course, not be a limit. If there is one, however, we call that limit "the derivative of :math:`f` at :math:`x_0`", and write :math:`f'(x_0)`.

We note that if :math:`f'(x_0)` exists, then :math:`f` must be continuous at :math:`x_0`.

From the definition, and the fact that limits of sums are sums of limits, we see that :math:`(f+g)'=f'+g'`. With a bit of algebra, it is easy to see that :math:`(fg)'=f'g+fg'`. If :math:`f` and :math:`g` are functions, we define :math:`(f\circ g)(x)=f(g(x))`. With this definition, and the kind of :math:`\epsilon`/:math:`\delta` games we are used to, it is straightforward to show that `(f\circ g)'(x_0)=f'(g(x_0))g'(x_0)`.

Assume :math:`f'(x_0)>0`. Let :math:`\epsilon=f'(x_0)/2`. Then by definition of limit, there is a :math:`\delta`, :math:`0<|x-x_0|<\delta` implies that :math:`|[f(x)-f(x_0)]/[x-x_0]-f'(x_0)|f'(x_0)-\epsilon=f'(x_0)/2>0`. If :math:`0<x-x_0f(x_0)`, and if :math:`0<x_0-x<\delta` then :math:`f(x)<f(x_0)`. Therefore, on any segment that contains :math:`x_0` (except as an endpoint) :math:`f(x_0)` is not a minimum or a maximum. For analogous reasons, if :math:`f'(x_0)<0`, it is neither a minimum or a maximum. In other words, if :math:`f'(x_0)` is a minimum or a maximum, even if only on a short segment that includes :math:`x_0` not as an endpoint, then :math:`f'(x_0)=0`.
