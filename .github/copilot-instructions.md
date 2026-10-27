# Instrucciones para este repositorio

## Contexto del proyecto

- Este proyecto es una aplicación de Diseño Experimental desarrollada en Python y Streamlit para el curso de Diseño Experimental del programa de Ingeniería Agrícola de la Universidad de Sucre.
- La aplicación debe apoyar el aprendizaje de estudiantes de Ingeniería Agrícola y presentar los procedimientos estadísticos de forma comprensible y rigurosa.

## Estructura del proyecto

- `app.py`: portada y punto de entrada de la aplicación.
- `pages/`: una página por cada diseño experimental.
- `utils/`: funciones reutilizables; debe incluir `__init__.py`.
- `data/`: archivos CSV con datos de ejemplo.
- `verificacion/`: scripts de R para verificar los análisis.
- Mantén esta estructura y coloca cada archivo en el directorio correspondiente.

## Idioma y explicación pedagógica

- Escribe en español todo el código nuevo, los comentarios, los docstrings y los mensajes visibles de la interfaz.
- En cada paso estadístico, agrega un comentario que explique qué se calcula y por qué, con lenguaje adecuado para estudiantes de Ingeniería Agrícola.
- Presenta las decisiones y supuestos estadísticos de manera clara; no ocultes pasos relevantes del análisis.

## Código y documentación

- Declara anotaciones de tipo (`type hints`) en las funciones, incluidos sus parámetros y valores de retorno.
- Documenta las funciones con docstrings en español siguiendo el estilo Google, con secciones pertinentes como `Args`, `Returns` y `Raises`.
- Prefiere funciones pequeñas y reutilizables, ubicadas en `utils/` cuando su uso corresponda a más de una página.

## Dependencias permitidas

- Usa únicamente estas librerías: `streamlit`, `pandas`, `numpy`, `scipy`, `statsmodels`, `plotly` y `openpyxl`.
- No agregues dependencias, ni siquiera de desarrollo, sin pedir permiso primero.

## Análisis estadístico

- Ajusta los modelos de ANOVA con `statsmodels.formula.api.ols` y calcula la tabla con `statsmodels.stats.anova.anova_lm`, usando `typ=2`.
- Realiza las comparaciones de Tukey con `statsmodels.stats.multicomp.pairwise_tukeyhsd`.
- No inventes, estimes a mano ni codifiques como constantes resultados estadísticos. Los valores presentados deben provenir siempre del cálculo ejecutado con los datos disponibles.
- Usa las mismas observaciones y el mismo modelo al calcular y mostrar resultados relacionados; informa claramente los supuestos o limitaciones relevantes.

## Verificación antes de terminar

- Antes de dar por terminada una tarea, ejecuta el código pertinente, revisa los errores que aparezcan y corrige los relacionados con los cambios.
- Ejecuta la comprobación más específica disponible para los archivos modificados y confirma que la aplicación o el análisis pueda ejecutarse cuando corresponda.
- Si no existe código ejecutable o no es posible ejecutar una comprobación, indícalo claramente en el resumen de la tarea; no afirmes que se validó algo que no se ejecutó.