## Ejecutar los test

Para ejecutar los tests en los notebooks de este proyecto, sigue estos pasos:

1. **Abre el notebook**: Navega hasta el archivo `.ipynb` que deseas ejecutar (por ejemplo, `TallerEsp.Vect-Hermitian-Unitary-Tensor-Circuits.ipynb`).
2. **Ejecuta las celdas**: Haz clic en el botón de ejecución que se encuentra en la parte superior izquierda de cada bloque de código. Asegúrate de ejecutar las celdas en orden, ya que algunas dependen de resultados previos.
3. **Observa los resultados**: Los tests generarán salidas en forma de texto, gráficos o valores numéricos, dependiendo del ejercicio. Asegúrate de revisar cada resultado para verificar que coincide con lo esperado.

### Requisitos adicionales
- **Kernel de Python**: Asegúrate de que el kernel de Python esté correctamente configurado en Jupyter Notebook.
- **Dependencias instaladas**: Verifica que todas las librerías necesarias (`numpy`, `matplotlib`, etc.) estén instaladas antes de ejecutar los tests.

## Cómo funcionan los test

Cada test en este proyecto está diseñado para validar conceptos específicos relacionados con números complejos, espacios vectoriales, matrices y circuitos cuánticos. Aquí te explicamos cómo funcionan:

1. **Tests de verificación**: Algunos tests verifican propiedades matemáticas, como si una matriz es Hermitiana o Unitaria. Estos tests comparan los resultados calculados con los valores esperados y muestran un mensaje de éxito o error.
   
   Ejemplo:
    ```python
    is_hermitian = np.allclose(matrix, matrix.conj().T)
    print("Es Hermitiana:" , is_hermitian)
    ```

2. **Tests gráficos**: Algunos ejercicios generan gráficos para visualizar resultados, como la evolución de estados en un circuito cuántico. Estos tests no tienen una salida de "éxito" o "error", pero debes verificar que los gráficos coincidan con lo esperado teóricamente.

3. **Tests de cálculo**: Otros tests realizan cálculos numéricos, como encontrar valores propios o productos tensoriales. Estos tests imprimen los resultados en la salida, y debes compararlos con tus cálculos manuales o teóricos.

4. **Interpretación de resultados**:
   - Si el test muestra un mensaje de éxito (por ejemplo, "Es Hermitiana: True"), significa que el resultado coincide con lo esperado.
   - Si el test muestra un error o un resultado inesperado, revisa el código y verifica si hay errores en la implementación o en los cálculos.

### Ejemplo de un test típico
En el archivo `TallerEsp.Vect-Hermitian-Unitary-Tensor-Circuits.ipynb`, encontrarás tests como el siguiente:

 ```python
   Verificar si una matriz es Hermitiana
   hermitian_matrix = np.array([[2+0j, 2-1j], [2+1j, 3+0j]])
   is_hermitian = np.allclose(hermitian_matrix, hermitian_matrix.conj().T)
   print("Es Hermitiana:", is_hermitian)
   ```

Este test verifica si la matriz `hermitian_matrix` es igual a su transpuesta conjugada, lo que confirma si es Hermitiana.

### Consejos para ejecutar los tests
- **Ejecuta en orden**: Algunos tests dependen de variables o resultados de celdas anteriores. Asegúrate de ejecutar las celdas en el orden correcto.
- **Compara con papel y lápiz**: Para ejercicios más complejos, como el cálculo de valores propios o productos tensoriales, es útil verificar los resultados manualmente.
- **Revisa los gráficos**: En ejercicios que involucran visualizaciones, asegúrate de que los gráficos coincidan con lo esperado teóricamente.