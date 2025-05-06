# ¿Qué es la cuadratura gaussiana?

La cuadratura gaussiana es un método numérico que nos ayuda a calcular aproximaciones de integrales definidas sin necesidad de dividir el intervalo en muchas partes iguales. En lugar de eso, selecciona de manera inteligente los puntos (nodos) y los pesos que mejor aproximan el valor de la integral, logrando una mayor precisión incluso con pocos puntos.

## Ventajas:
- Es muy precisa aunque utilicemos pocos puntos.
- Es especialmente útil para funciones suaves, donde la curva no tiene cambios bruscos.

## Fórmula principal:

Para una función `f(x)`, la integral de `a` a `b` se puede aproximar así:

∫ de a a b de f(x) dx ≈ suma desde i=1 hasta n de (w_i * f(x_i))

markdown
Copiar
Editar

Aquí:
- `x_i` son los nodos (puntos)
- `w_i` son los pesos
- ambos están ajustados al intervalo `[a, b]`.

## Cambio de intervalo:

Como los nodos y pesos estándar se calculan en el intervalo `[-1, 1]`, es necesario hacer una transformación para escalarlos a cualquier intervalo `[a, b]`:

x = ((b - a)/2) * ξ + (a + b)/2

css
Copiar
Editar

Y la integral en `[a, b]` se calcula como:

∫ de a a b de f(x) dx ≈ (b - a)/2 * suma desde i=1 hasta n de (w_i * f(((b - a)/2) * ξ_i + (a + b)/2))

css
Copiar
Editar

De esta manera, podemos aplicar la cuadratura gaussiana a diferentes intervalos de forma sencilla y eficiente.

[3. Código en Python con explicación](tutorials.md)


