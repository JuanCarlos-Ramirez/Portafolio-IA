# 03 - SVR Auditoria Salarial

Detectar sueldos que se salen de la politica salarial de la empresa usando Support Vector Regression.

### ¿Que hace?
No predice sueldos futuros. Audita los actuales.

1. Aprende cual deberia ser el sueldo normal segun los años de experiencia.
2. Crea un tubo de tolerancia de +/- $600 (epsilon).
3. Clasifica empleados dentro y fuera de banda.

### Resultado visual
![auditoria](svr_puntos_bonitos.png)

- **Verde (Dentro del tubo):** Sueldo dentro de la banda permitida. Ej: 50 de 60 empleados.
- **Rojo (Fuera del tubo):** Sueldo atipico para revision de RRHH. Son los vectores de soporte.
    - Rojo arriba: posible sobrepago
    - Rojo abajo: posible subpago / riesgo de fuga

### El modelo
```python
epsilon = 600
svr = SVR(kernel='rbf', gamma=0.3, C=10.0, epsilon=epsilon)

##------------------------------------------
## epsilon: ancho del tubo. Si el error es menor, lo perdonamos.
## C: que tan estricto soy con los que se salen.
## Gamma: que tan curva es la banda salarial.
