---
id: 5900f3e61000cf542c50fef9
title: 'Problema 122: esponenziazione efficiente'
challengeType: 1
forumTopicId: 301749
dashedName: problem-122-efficient-exponentiation
---

# --description--

Il modo più semplice di calcolare $n^{15}$ richiede quattordici moltiplicazioni:

$$n × n × \ldots × n = n^{15}$$

Ma usando un metodo "binario" è possibile calcolarlo in sei moltiplicazioni:

$$$\start{align}   & n × n = n^2\\\\
  & n^2 × n^2 = n^4\\\\   & n^4 × n^4 = n^8\\\\
  & n^8 × n^4 = n^{12}\\\\   & n^{12} × n^2 = n^{14}\\\\
  & n^{14} × n = n^{15} \end{align}$$

Tuttavia è possibile calcolarlo anche in sole cinque moltiplicazioni:

$$\begin{align}   & n × n = n^2\\\\
  & n^2 × n = n^3\\\\   & n^3 × n^3 = n^6\\\\
  & n^6 × n^6 = n^{12}\\\\ & n^{12} × n^3 = n^{15} \end{align}$$

Definiremo $m(k)$ in modo che sia il numero minimo di moltiplicazioni per calcolare $n^k$; per esempio $m(15) = 5$.

Per $1 ≤ k ≤ 200$, trova $\sum{m(k)}$.

# --hints--

`efficientExponentiation()` should return `1582`.

```js
assert.strictEqual(efficientExponentiation(), 1582);
```

# --seed--

## --seed-contents--

```js
function efficientExponentiation() {

  return true;
}

efficientExponentiation();
```

# --solutions--

```js
// solution required
```
