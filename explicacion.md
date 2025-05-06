<script type="text/javascript"
  async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# ¿Qué es la cuadratura gaussiana?

La cuadratura gaussiana es un método numérico que nos ayuda a calcular aproximaciones de integrales definidas sin necesidad de dividir el intervalo en muchas partes iguales. En lugar de eso, selecciona de manera inteligente los puntos (nodos) y los pesos que mejor aproximan el valor de la integral, logrando una mayor precisión incluso con pocos puntos.

## Ventajas:
- Es muy precisa aunque utilicemos pocos puntos.
- Es especialmente útil para funciones suaves, donde la curva no tiene cambios bruscos.

## Fórmula principal:

Para una función \( f(x) \), la integral de \( a \) a \( b \) se puede aproximar así:

$$
\int_a^b f(x)\, dx \approx \sum_{i=1}^n w_i f(x_i)
$$

Aquí:
- \( xi \) son los nodos (puntos)
- \( wi \) son los pesos
- ambos están ajustados al intervalo \([a, b]\).

## Cambio de intervalo:

Como los nodos y pesos estándar se calculan en el intervalo \([-1, 1]\), es necesario hacer una transformación para escalarlos a cualquier intervalo \([a, b]\):

$$
x = \frac{b - a}{2} x_i + \frac{a + b}{2}
$$

Y la integral en \([a, b]\) se calcula como:

$$
\int_a^b f(x)\, dx = \frac{b - a}{2} \sum_{i=1}^n w_i f\left( \frac{b - a}{2} x_i + \frac{a + b}{2} \right)
$$

De esta manera, podemos aplicar la cuadratura gaussiana a diferentes intervalos de forma sencilla y eficiente.

[3. Código en Python con explicación](tutorials.md)




