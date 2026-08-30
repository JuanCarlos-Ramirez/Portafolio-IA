# compras-s-n-con-regresion-logistica

Predicción de compra S/N con regresión logística desde cero (solo NumPy). Proyecto pensado para aprendices: cada etapa está separada y graficada.

Responde a: ¿Si una persona de 45 años pasa 6h en la web, compra o no?

### El Pipeline (como en la vida real)

Este código sigue 6 etapas claras:

1.  **CARGA:** Si existe `data/empresaX.csv` lo usa (20+ columnas). Si no, genera 400 clientes lógicos.
2.  **VER:** Muestra `head()` y conteos. Total compraron: 278/400.
3.  **PREPARACIÓN:** Normalización automática `(X - mean)/std` que funciona para N características.
4.  **ENTRENAMIENTO:** Gradiente `dw = X.T @ (p - y) / n`. Loss: 0.693 (azar) -> 0.508
5.  **GRÁFICAS:** 3 vistas que explican todo.
6.  **PRUEBA:** Predicción para clientes nuevos.

### Las 3 Gráficas que genera

El código genera esto automáticamente:

**1. Datos crudos:** Puntos rojos (no compra) y verdes (compra). Vista humana para contar a mano.

**2. Frontera aprendida:** La famosa línea azul que divide. `w0*Edad + w1*Horas + b = 0`

**3. Curva de aprendizaje:** Cómo la IA baja el error iteración a iteración.

### Resultados Demo

- Cliente 45 años, 6h -> **88.3% -> COMPRA**
- Cliente 22 años, 1h -> 12.1% -> NO COMPRA

Pesos aprendidos: `w_edad=0.59, w_horas=0.82` -> El tiempo en web pesa más.

### Cómo ejecutarlo

```bash
git clone https://github.com/TU_USUARIO/compras-s-n-con-regresion-logistica.git
pip install -r requirements.txt
python src/modelo.py
```
### Presentación Grafica
logistica_02_frontera.png
