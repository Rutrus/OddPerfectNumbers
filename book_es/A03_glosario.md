### **Glosario de Términos Matemáticos**
*(Ordenado alfabéticamente para una consulta rápida)*

---

#### **A**
**Números amigos**
Dos números distintos $ (a, b) $ son *amigos* si la suma de los divisores propios de uno es igual al otro (y viceversa):
$$ \sigma(a) - a = b \quad \text{y} \quad \sigma(b) - b = a. $$
*Ejemplo*: $ (220, 284) $, ya que:
$$ \sigma(220) - 220 = 284 \quad \text{y} \quad \sigma(284) - 284 = 220. $$

---

#### **C**
**Cota inferior**
Valor mínimo que puede tomar una cantidad en un problema. Para los OPN, se sabe que deben ser mayores que $ 10^{1500} $.

---

#### **E**
**Función $\sigma(n)$ (Sigma)**
Suma de **todos** los divisores positivos de $ n $ (incluyendo $ 1 $ y $ n $):
$$ \sigma(6) = 1 + 2 + 3 + 6 = 12. $$
- Clave para definir números perfectos: $ \sigma(n) = 2n $.

---

#### **H**
**Hipótesis de Riemann (HR)**
Conjetura no demostrada sobre los ceros no triviales de la función zeta de Riemann. Relacionada con la distribución de primos y, indirectamente, con propiedades de $ \sigma(n) $.

---

#### **N**
**Número $k$-perfecto**
Entero $ N $ que cumple $ \sigma(N) = kN $.
- *Perfecto clásico*: $ k=2 $.
- *Triperfecto*: $ k=3 $ (ejemplo par: 120).

**Números perfectos impares (OPN)**
Números perfectos que además son impares. No se conoce ninguno, y se ha demostrado su no existencia bajo ciertas condiciones.

**Números primos perfectos**
*No confundir con números perfectos*. Son primos $ p $ tales que $ \sigma(p) = p + 1 $ es también primo.
*Ejemplo*: $ p = 2 $ (pues $ \sigma(2) = 3 $, que es primo).

---

#### **O**
**Función $\omega(n)$ (Omega)**
Cantidad de **primos distintos** que dividen a $ n $.
- Para OPN, se sabe que $ \omega(n) \geq 101 $.

---

#### **P**
**Primos de Mersenne**
Números primos de la forma $ M_p = 2^p - 1 $. Relacionados con números perfectos pares mediante el teorema de Euclides-Euler.

**Números perfectos**
Enteros iguales a la suma de sus divisores propios: $ \sigma(n) = 2n $.
- *Pares*: Siguen la forma $ 2^{p-1}(2^p - 1) $ (si $ 2^p - 1 $ es primo).
- *Impares*: No se conocen.

---

#### **T**
**Teorema de Euclides-Euler**
Caracteriza todos los números perfectos pares:
$$ n = 2^{p-1}(2^p - 1), $$
donde $ 2^p - 1 $ es un primo de Mersenne.

---

### **Términos Adicionales**
**Libre de cuadrados**
Número que no es divisible por ningún cuadrado perfecto mayor que 1 (ej. $ 30 = 2 \times 3 \times 5 $).

**Multiplicativa (función)**
Propiedad de funciones como $ \sigma(n) $, donde $ \sigma(ab) = \sigma(a)\sigma(b) $ si $ a $ y $ b $ son coprimos.

---

### **¿Por qué este glosario?**
- **Claridad**: Define términos técnicos usados en el libro.
- **Conexiones**: Muestra cómo conceptos como $ \sigma(n) $ y primos de Mersenne se entrelazan.
- **Invitación a profundizar**: Términos como "Hipótesis de Riemann" abren puertas a otros problemas.
