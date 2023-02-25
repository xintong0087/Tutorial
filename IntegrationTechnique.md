# Integration Techniques

Reflecting back to calculus, taking derivative is relatively straightforward. However, its reverse calculation, integration is not as easy. There are many techniques for integration, and many functions do not have close-form anti-derivatives. In today's tutorial, we will learn some of the most common integration techniques that demystefy the process.

We consider functions of the form $f(x)$ and their antiderivates $F(x) = \int f(x) dx$. 
* Note that it is just a generic notation, and it does not necessarily mean the probability density function nor the cummulative density function. 

## Common Antiderivatives

There are many functions with simple antiderivatives. We can solve them literally in seconds.

### Power Functions

Consider a function of the form 
    $$f(x) = x^k, \quad k \neq -1,$$ 
its anti-derivative is 
    $$F(x) = \int f(x) dx = \frac{1}{k+1} x^{k+1} + C,$$
where $C$ is a constant.

We have left the special case when $k=1$. 
    $$f(x) = \frac{1}{x}, $$
its anti-derivative is 
    $$F(x) = \ln(|x|) + C. $$

### Exponential Functions

Consider a function of the form 
    $$f(x) = e^x, $$
its anti-derivative is 
    $$F(x) = e^x + C,$$

### Trigonometric Functions

Consider a function of the form 
    $$f(x) = \sin(x), $$
its anti-derivative is 
    $$F(x) = -\cos(x) + C,$$

Consider a function of the form 
    $$f(x) = \cos(x), $$
its anti-derivative is 
    $$F(x) = \sin(x)+ C,$$

## Technique 1: u-substitution
With only knowing the common anti-derivatives will still give us trouble in integrating problems like

$$\int e^{kx} dx.$$

What can we do about the constant $k$?

The u-subtitution method reduces the above problem to simply solving common anti-derivatives. As it name suggests, the u-subtitution changes the variable $x$ to a variable $u = g(x)$. Here, we want to select $u$ as a functions of $x$ such that the integration becomes easy.

In the above problem of integrating $e^{kx}$, a natural choice is $u = kx$, and the integration becomes

$$\int e^{u} dx.$$

Since one can't directly integrate a function of $u$ with respect to $x$, we will need to find an expression of $dx$ so we can integrate with respect to $u$.

We start by finding what is $du$, which can be directly solved from $u = kx$. We can take derivatives on both sides, and get

$$du = k dx.$$

Hence, the original problem now becomes a common antiderivative

$$\int e^u \frac{1}{k} du = \frac{1}{k} \int e^u du = \frac{1}{k} e^u + C = \frac{1}{k} e^{kx} +C$$

### Summary for u-substitution

There are four steps for u-substitution:

1. Determine $u$ as a function of $x$
2. Find $dx$ in terms of $du$ by taking derivatives on both sides for the result obtained in step 1.
3. Conduct integration with respect to $u$.
4. Plug $x$ back.

Note that, one can only efficiently use u-substitution when constants are in play, or if $du$ is conveniently in integrand. See the following examples.

### Examples:

* Solve the integration problem:
$$\int (3-x)^{10} dx $$

* Solve the integration problem:
$$\int \sqrt{7x+9} dx $$

* Solve the integration problem:
$$\int (2x+2) e^{x^2 + 2x +3} dx $$

<!-- * Solve the integration problem:
$$\int \frac{x^2+1}{x^3+3x} dx $$ -->


## Technique 2: integration by parts

Integration by parts is also a technique that reduce integration of products back to the commonly known antiderivatives. 

$$ \int u(x) v(x) dx = u(x) \int v(x) dx - \int u'(x) \left( \int v(x) dx \right) dx$$

Don't be turned down by the complex formula, let's take a look at an example

$$\int x \sin(x) dx$$

Let $u = x$, $v = \sin(x)$. To follow the formula, we still need to calculate the derivative of $u$ and integral of $v$.

$$u'(x) = 1, \quad \int v(x) dx = -\cos(x) $$

Then we can transform the original problem to the following

$$\int x \sin(x) = x (-\cos(x)) - \int 1 (-\cos(x)) dx = -x\cos(x) + \sin(x) + C$$

### Summary for integration by parts

There are three steps for integration by parts:

1. Determine $u(x)$ and $v(x)$.
2. Find derivative of $u$, $u'(x)$, and integral of $v$.
3. Conduct integration normally.

Note that, one can only efficiently use integration by parts on product of things with known derivatives/antiderivatives.

### Examples:

* Solve the integration problem:
$$\int x e^x dx $$

* Solve the integration problem:
$$\int x \cos(4x) dx $$

* Solve the integration problem:
$$\int x^2 e^{-x}  dx $$


