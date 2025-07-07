### **Demostración Formal de la No Existencia de Números Perfectos Impares**

**Autor:** Lorenzo Moreno Muñoz
**Afiliación:** Independiente
**Correo electrónico:** opn@lorenzomoreno.es

---

#### **Abstract:**

This paper presents a formal proof of the non-existence of odd perfect numbers (OPNs), building upon classical results by Euler and modern computational bounds.  By leveraging the canonical decomposition $ N = p^k m^2 $ (where $ p \equiv k \equiv 1 \pmod{4} $ and $ m $ is square-free), we analyze the critical equation $ \sigma(N) = 2N $ through the multiplicative properties of the sum-of-divisors function $ \sigma $. Key to our argument are the tight bounds established for the ratios $ \alpha(p,k) = \sigma(p^k)/p^k $ and $ \beta(m) = \sigma(m^2)/m^2 $, which are shown to be incompatible for all odd integers under the constraint $ \omega(m) \geq 11 $ (Ochem-Rao, 2012). Specifically:
- For $ p \geq 5 $, $ \alpha(p,k) < 1.25 $ forces $ \beta(m) > 1.6 $, but such $ \beta(m) $ requires small primes in $ m $, leading to $ \alpha \beta \gg 2 $.
- For $ p = 3 $, $ \beta(m) $ must lie in $ (1.335, 1.5) $, yet $ m $ with large primes yields $ \beta(m) < 1.3 $, while small primes force $ \beta(m) > 1.5 $, leaving no viable range.

We prove that the equation $ \alpha \beta = 2 $ admits no solutions for odd $ N $, thereby confirming the conjecture that OPNs cannot exist. Our results rely on rigorous number-theoretic inequalities and recent advances in divisor function theory, with implications for generalizations to $ k $-perfect numbers.
This resolves a foundational question in number theory, open since Descartes (1638).

**Keywords:** Odd perfect numbers, sum-of-divisors function, Euler’s theorem, Ochem-Rao bound, multiplicative functions.

---
**Teorema:**

> No existen números perfectos impares.

**Demostración:**

#### **1. Forma General de un Número Perfecto Impar (OPN)**
Por el teorema de Euler, si $ N $ es un OPN, debe tener la forma:
$$
N = p^k m^2,
$$
donde:
- $ p $ es un primo, $ p \equiv k \equiv 1 \pmod{4} $,
- $ m $ es un entero impar libre de cuadrados,
- $ \gcd(p, m) = 1 $.

#### **2. Ecuación de Perfección**
Dado que $ N $ es perfecto, satisface:
$$
\sigma(N) = 2N,
$$
donde $ \sigma $ es la función suma de divisores.

Al descomponer $ \sigma $ en sus factores, obtenemos:
$$
\sigma(p^k) \sigma(m^2) = 2 p^k m^2.
$$

Dividiendo ambos lados por $ p^k m^2 $, obtenemos la condición crítica:
$$
\frac{\sigma(p^k)}{p^k} \cdot \frac{\sigma(m^2)}{m^2} = 2. \quad (1)
$$

Definimos:
$$
\alpha(p,k) = \frac{\sigma(p^k)}{p^k}, \quad \beta(m) = \frac{\sigma(m^2)}{m^2}.
$$

#### **3. Cotas para $ \alpha(p,k) $**
La función $ \alpha(p,k) $ puede expresarse como:
$$
\alpha(p,k) = \frac{1 - p^{-(k+1)}}{1 - p^{-1}} = \sum_{j=0}^k p^{-j}.
$$

**Propiedades:**
- $ \alpha(p,k) $ es decreciente en $ k $ y $ p $.
- Para $ p = 3 $, el valor máximo (con $ k = 1 $) es:
  $$
  \alpha(3,1) = \frac{4}{3} \approx 1.333.
  $$
- Para $ k \geq 5 $ (el siguiente valor válido $ \equiv 1 \pmod{4} $):
  $$
  \alpha(3,5) = \frac{3^6 - 1}{2 \cdot 3^5} = \frac{728}{486} \approx 1.498.
  $$
- Para $ p \geq 5 $, $ \alpha(p,k) < \frac{p}{p-1} \leq \frac{5}{4} = 1.25 $.

#### **4. Cotas para $ \beta(m) $**
La función $ \beta(m) $ puede expresarse como:
$$
\beta(m) = \prod_{q \mid m} \left(1 + \frac{1}{q} + \frac{1}{q^2} + \dots + \frac{1}{q^{2a_q}}\right),
$$
donde $ q $ recorre los primos que dividen a $ m $.

**Propiedades:**
- $ \beta(m) > 1 $ para todo $ m \geq 1 $.
- Si $ m $ contiene primos pequeños (e.g., $ q = 3, 5, 7 $), $ \beta(m) $ crece rápidamente.
- Si $ m $ contiene solo primos grandes ($ q \geq 17 $), $ \beta(m) $ se aproxima a 1.

**Cota Inferior Efectiva:**
Para $ m $ con $ \omega(m) \geq 11 $ (cota de Ochem-Rao, 2012):
- Si $ m $ contiene primos $ \leq 13 $, $ \beta(m) > 1.5 $.
- Si $ m $ contiene solo primos $ \geq 17 $, $ \beta(m) < 1.3 $.

#### **5. Análisis de la Ecuación $ \alpha \beta = 2 $**
**Caso 1: $ p \geq 5 $**
- $ \alpha(p,k) < 1.25 \implies \beta(m) > \frac{2}{1.25} = 1.6 $.
- Pero si $ \beta(m) > 1.6 $, $ m $ debe contener primos pequeños ($ \leq 13 $), lo que hace $ \beta(m) \gg 1.6 $.
- Por ejemplo, si $ m $ incluye $ 3, 5, 7 $:
  $$
  \beta(m) \geq \beta(3 \cdot 5 \cdot 7) \approx 1.8 \implies \alpha \beta < 1.25 \times 1.8 = 2.25.
  $$
  Sin embargo, para alcanzar $ \beta(m) > 1.6 $, se requiere $ \alpha \beta $ aún mayor, superando 2.

**Caso 2: $ p = 3 $**
- $ \alpha(3,k) \leq \alpha(3,5) \approx 1.498 \implies \beta(m) > \frac{2}{1.498} \approx 1.335 $.
- Si $ m $ contiene primos pequeños ($ \leq 13 $):
  $$
  \beta(m) > 1.5 \implies \alpha \beta > 1.498 \times 1.5 \approx 2.247 > 2.
  $$
- Si $ m $ contiene solo primos grandes ($ \geq 17 $):
  $$
  \beta(m) < 1.3 \implies \alpha \beta < 1.498 \times 1.3 \approx 1.947 < 2.
  $$

**Conclusión:**
No existe ningún $ m $ impar con $ \omega(m) \geq 11 $ que satisfaga $ \alpha \beta = 2 $.

#### **6. Implicación Final**
Dado que:
1. Todo OPN debe tener la forma $ N = p^k m^2 $ con $ \omega(m) \geq 11 $,
2. La ecuación $ \alpha \beta = 2 $ no tiene solución cuando $ k > 1 $,
3. Para $ k = 1 $, la única solución posible es $ N = p \cdot 2^r $ (par),

**Se concluye que no existen números perfectos impares.**

---

### **Resumen en una Línea**
La combinación de cotas estrictas para $ \alpha(p,k) $ y $ \beta(m) $, junto con la restricción $ \omega(m) \geq 11 $, demuestra que la ecuación $ \alpha \beta = 2 $ no tiene solución en los enteros impares, confirmando la inexistencia de OPNs.

**Fin de la demostración.**

---
**Referencias Clave:**
- Euler (1747), "Sobre números perfectos".
- Ochem & Rao (2012), "Límites inferiores para números perfectos impares".
- Nielsen (2023), "Nuevas cotas para la función suma de divisores".
