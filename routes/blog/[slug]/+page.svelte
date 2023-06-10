<script>
  import { marked } from 'marked';
  const source = `
  # Gradient Descent
- Have *some* function $J(w, b)$
- Want $min_w,_b(J(w,b))$

1. Start with some $w, b$.
2. Keep changing $w, b$ to reduce $J(w, b)$ until a minimum is settled on:
	- $w = w - \alpha \frac{d}{dw}J(w)$
	- $b = b - \alpha\frac{d}{db}J(b)$
	where:
	- $\alpha$ is the [[Learning Rate]].
	- $\frac{d}{dw}$ and $\frac{d}{db}$ are derivatives. Hence, if a curve of a cost function is going up, the derivative of two points is positive. Hence $w$ and $b$ become smaller.
3. As gradient descent gets closer to a local minimum, the derivative becomes smaller, hence the steps become smaller too - although the learning rate $\alpha$ would be a constant value.`
</script>

{@html marked(source)}
