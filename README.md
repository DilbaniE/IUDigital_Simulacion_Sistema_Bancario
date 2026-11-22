# 🏦 Simulación de atención al cliente en un banco

## 1. Descripción del proyecto

Este proyecto desarrolla una simulación de un sistema de atención bancaria mediante el uso de Python. Se busca analizar el comportamiento de las filas de clientes, los tiempos de espera y la utilización de los cajeros, evaluando diferentes configuraciones de atención.

El banco cuenta inicialmente con tres cajeros que atienden operaciones de retiro y pagos o depósitos. Se propone evaluar diferentes escenarios para determinar cuál ofrece un mejor servicio a los clientes y permite aprovechar adecuadamente los recursos disponibles.

## 2. Objetivo

Simular el funcionamiento de un banco durante una jornada de 8 horas, con el propósito de analizar los tiempos de espera de los clientes y comparar diferentes distribuciones de cajeros.

A partir de los resultados, se busca identificar la configuración que ofrece mejores condiciones de atención y determinar si es conveniente incorporar un cajero adicional.

## 3. Descripción del problema

El banco atiende dos tipos de operaciones:

- **Retiros:** representan el 70 % de las operaciones.
- **Pagos y depósitos:** representan el 30 % de las operaciones.

Los clientes presentan diferentes velocidades de atención, clasificadas en cuatro tipos:

| Tipo de usuario | Tiempo de servicio (retiros) | Tiempo de servicio (pagos) |
|---|---:|---:|
| Rápido | 1 minuto | 3 minutos |
| Normal | 2 minutos | 3 minutos |
| Lento | 3 minutos | 5 minutos |
| Muy lento | 4 minutos | 7 minutos |

El modelo considera los tiempos entre llegadas y los tiempos de servicio definidos para cada tipo de usuario y operación.

## 4. Metodología

La simulación se desarrolla mediante los siguientes pasos:

1. Definición de los parámetros del sistema bancario.
2. Generación de clientes y asignación del tipo de operación.
3. Clasificación de los clientes según su velocidad de atención.
4. Generación de los tiempos entre llegadas y de servicio.
5. Asignación de los clientes a los cajeros según la disponibilidad.
6. Simulación de diferentes configuraciones de cajeros.
7. Ejecución de 10 réplicas para cada escenario.
8. Cálculo y comparación de los indicadores de desempeño.
9. Elaboración de gráficas y tablas para analizar los resultados.

## 5. Escenarios evaluados

Se evaluaron cuatro configuraciones del sistema:

| Escenario | Distribución de cajeros |
|---|---|
| Modelo 1 | 3 cajeros mixtos |
| Modelo 2 | 1 cajero para retiros y 2 para pagos y depósitos |
| Modelo 3 | 2 cajeros para retiros y 1 para pagos y depósitos |
| Modelo 4 | 4 cajeros mixtos |

Los cajeros mixtos pueden atender tanto retiros como pagos y depósitos.

## 6. Indicadores analizados

Se calcularon los siguientes indicadores:

- Cantidad de clientes atendidos.
- Cantidad de clientes por tipo.
- Tiempo promedio de espera.
- Tiempo máximo de espera.
- Tiempo de espera según tipo de operación.
- Utilización de los cajeros.
- Comparación entre los diferentes escenarios.
- Variabilidad de los resultados entre réplicas.

## 7. Tecnologías utilizadas

- **Python:** lenguaje de programación utilizado para desarrollar la simulación.
- **NumPy:** generación de datos aleatorios y cálculos numéricos.
- **Pandas:** organización, procesamiento y análisis de los resultados.
- **Matplotlib:** elaboración de gráficas y visualización de resultados.
- **Google Colab:** entorno de ejecución del notebook.
- **Git y GitHub:** almacenamiento, organización y versionamiento del proyecto.

## 8. Estructura del repositorio

```text
Simulacion-Banco/
│
├── README.md
├── Actividad_M3_Banco_corregida.ipynb
│
└── evidencias/
    ├── resultados_generales.png
    ├── comparacion_tiempos_espera.png
    ├── espera_por_operacion.png
    └── utilizacion_cajeros.png
```

La carpeta `evidencias` contiene imágenes de los resultados obtenidos durante la ejecución de la simulación. Los nombres de los archivos pueden ajustarse a las evidencias que finalmente se incorporen al repositorio.

## 9. Instrucciones de ejecución

### Opción 1. Ejecutar en Google Colab

1. Ingresar al repositorio de GitHub.
2. Abrir el archivo `Actividad_M3_Banco_corregida.ipynb`.
3. Descargar el notebook o abrirlo directamente en Google Colab.
4. Seleccionar el entorno de ejecución de Python.
5. Ejecutar las celdas en orden, desde el inicio hasta el final.
6. Esperar a que se generen las tablas, estadísticas y gráficas de los resultados.

### Opción 2. Ejecutar localmente

Se requiere tener instalado Python 3 y Jupyter Notebook.

Instalar las librerías necesarias:

```bash
pip install numpy pandas matplotlib jupyter
```

Clonar el repositorio:

```bash
git clone URL_DEL_REPOSITORIO
```

Ingresar a la carpeta del proyecto:

```bash
cd Simulacion-Banco
```

Iniciar Jupyter Notebook:

```bash
jupyter notebook
```

Abrir el archivo `Actividad_M3_Banco_corregida.ipynb` y ejecutar las celdas en orden.

## 10. Resultados obtenidos

La simulación se ejecutó utilizando 10 réplicas para cada configuración.

Los resultados obtenidos para el tiempo promedio de espera fueron:

| Escenario | Tiempo promedio de espera |
|---|---:|
| 3 cajeros mixtos | 0,42 minutos |
| 1 cajero de retiros y 2 de pagos | 4,78 minutos |
| 2 cajeros de retiros y 1 de pagos | 3,21 minutos |
| 4 cajeros mixtos | 0,08 minutos |

La configuración de cuatro cajeros mixtos presentó el menor tiempo promedio de espera, con aproximadamente 0,08 minutos por cliente.

Por otra parte, el modelo de tres cajeros mixtos presentó un tiempo promedio de espera de 0,42 minutos, lo que demuestra que también ofrece un buen desempeño en las condiciones simuladas.

### Utilización de los cajeros

| Escenario | Utilización promedio |
|---|---:|
| 3 cajeros mixtos | 47,14 % |
| 4 cajeros mixtos | 35,35 % |

La incorporación de un cuarto cajero disminuye los tiempos de espera, pero también reduce el porcentaje de utilización de los recursos, por lo que es importante considerar los costos asociados a mantener un cajero adicional.

## 11. Evidencias de resultados

En el notebook se encuentran las tablas y gráficas que permiten visualizar los resultados de la simulación.

Las principales evidencias son:

- Comparación de los tiempos promedio de espera entre escenarios.
- Tiempos de espera para retiros y pagos o depósitos.
- Utilización de los cajeros.
- Distribución de clientes por tipo.
- Resultados de las réplicas realizadas.
- Comparación de las configuraciones de atención.

Estas evidencias permiten verificar el comportamiento del sistema y respaldar las conclusiones obtenidas.

## 12. Conclusiones

La simulación permitió evaluar diferentes configuraciones de atención bancaria y analizar su efecto sobre los tiempos de espera de los clientes.

Los resultados muestran que la configuración de cuatro cajeros mixtos presenta el menor tiempo promedio de espera. Sin embargo, el escenario de tres cajeros mixtos también ofrece un buen desempeño, con tiempos de espera relativamente bajos y una mayor utilización de los recursos.

Los escenarios con cajeros exclusivos para retiros y pagos presentaron mayores tiempos de espera promedio, debido a la distribución de la demanda y a la capacidad de atención asignada a cada operación.

Por lo tanto, se concluye que mantener cajeros mixtos permite una mayor flexibilidad en la atención de los clientes. La decisión de incorporar un cuarto cajero debe considerar no solamente la reducción de los tiempos de espera, sino también los costos operativos y la utilización de los recursos disponibles.

---

**Proyecto académico — Simulación | Módulo 2, Actividad didáctica 2-M3**  
Desarrollado con Python y Google Colab.

Dilbani EB
