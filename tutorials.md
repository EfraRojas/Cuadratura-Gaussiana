# Implementación en Python

A continuación, se presenta el código Python utilizado para implementar la cuadratura gaussiana, usando la librería `numpy`.

    import numpy as np

    def gaussxw(N):
        x, w = np.polynomial.legendre.leggauss(N)
        return x, w

    def gaussxwab(a, b, x, w):
        x_scaled = 0.5 * (b - a) * x + 0.5 * (b + a)
        w_scaled = 0.5 * (b - a) * w
        return x_scaled, w_scaled

    def gauss_integrate_sin_x2(a, b, N):
        x, w = gaussxw(N)
        x_scaled, w_scaled = gaussxwab(a, b, x, w)
        return np.sum(w_scaled * np.sin(x_scaled**2))

    resultado = gauss_integrate_sin_x2(0, np.pi, 30)
    print(resultado)

