---
{"dg-publish":true,"permalink":"/analysis-maths-2/"}
---

<iframe src="/img/user/Xournal++/Ana1+2_EN_live.pdf" width="100%" height="900px" title="Xournal++/Ana1+2_EN_live.pdf" style="border:1px solid #ccc;"></iframe>

<iframe src="/img/user/Attachments/Ana1+2_EN.pdf" width="100%" height="900px" title="Ana1+2_EN.pdf" style="border:1px solid #ccc;"></iframe>

# Elementary Rules of Integration
<iframe src="/img/user/Xournal++/Integration%20Rules.pdf" width="100%" height="900px" title="Integration Rules" style="border:1px solid #ccc;"></iframe>

## Additional rules
### The u-Substitution Rule (Change of Variables)
This is used to simplify an integral by replacing a portion of the function with a single variable, u.
- **Rule**: $∫f(g(t))⋅g'(t)dt=∫f(u)du$, where $u=g(t)$.

### The Inverse Trigonometric Rule (Arctangent)
This is a "table" integral, meaning it is a standard derivative form.

-  **Rule**: $∫\frac{1}{1+u^2}du=arctan(u)+C$.

### Integration by Parts (trigonometric specialization)
For the product of an exponential and a trigonometric function, you use a rule derived from the Product Rule of differentiation.

- **Rule**: $∫udv=uv−∫vdu$.
- **Application**: To integrate eatcos(bt), you typically apply Integration by Parts twice or use the resulting "elementary" formula:
$$∫e^{at}cos(bt)dt= \frac{e^{at}}{a^2+b^2}(acos(bt)+bsin(bt)$$