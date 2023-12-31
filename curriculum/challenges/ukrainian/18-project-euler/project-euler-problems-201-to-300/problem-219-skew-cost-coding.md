---
id: 5900f4481000cf542c50ff5a
title: 'Завдання 219: розрахунок асиметричної ціни'
challengeType: 1
forumTopicId: 301861
dashedName: problem-219-skew-cost-coding
---

# --description--

Нехай $A$ та $B$ будуть бітовими рядками (послідовності з 0 та 1).

Якщо $A$ дорівнює бітам <u>найлівішої</u> частини $B$, то $A$ називають префіксом $B$.

Наприклад, 00110 є префіксом <u>00110</u>1001, а не 00111 або 100110.

Код без префіксу розміру $n$ — це набір $n$ окремих бітових рядків, де жоден рядок не є префіксом іншого. Наприклад, ось код без префіксу розміру 6:

$$0000, 0001, 001, 01, 10, 11$$

Припустимо, за 1 копійку можна передати 0, а за 4 копійки — 1. Тоді загальна вартість даного коду без префіксів становитиме 35 копійок, що є найдешевшою можливою ціною при асиметричній ціновій політиці. Скорочено запишемо $Cost(6) = 35$.

Чому дорівнює $Cost(10^9)$?

# --hints--

`skewCostCoding()` має повернути `64564225042`.

```js
assert.strictEqual(skewCostCoding(), 64564225042);
```

# --seed--

## --seed-contents--

```js
function skewCostCoding() {

  return true;
}

skewCostCoding();
```

# --solutions--

```js
// solution required
```
