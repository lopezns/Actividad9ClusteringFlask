# Implementacion de K-Means Clustering con Flask

Aplicacion web en Flask para segmentar clientes de un centro comercial usando el algoritmo K-Means Clustering.

## Dataset

El proyecto usa `Mall_Customers.csv`, con 200 registros y las siguientes columnas:

- `CustomerID`
- `Genre`
- `Age`
- `Annual Income (k$)`
- `Spending Score (1-100)`

Las variables seleccionadas para el agrupamiento son:

- `Annual Income (k$)`
- `Spending Score (1-100)`

## Instalacion

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Ejecucion

```bash
python app.py
```

Luego abrir:

```text
http://127.0.0.1:5000/
```

## Rutas principales

- `/`: pagina principal y descripcion del problema.
- `/dataset/`: descripcion, limpieza y muestra del dataset.
- `/conceptos/`: conceptos de K-Means y metodo del codo.
- `/modelo/`: ejecucion del modelo, graficas, centroides y tabla procesada.
- `/Cluster/`: ruta de resultados basada en el ejemplo del profesor.
- `/interpretacion/`: analisis de patrones y conclusiones.

## Estructura del proyecto

```text
.
├── app.py
├── Clustering.py
├── Mall_Customers.csv
├── requirements.txt
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── dataset.html
│   ├── conceptos.html
│   ├── modelo.html
│   ├── ClusterResults.html
│   └── interpretacion.html
└── static/
    ├── css/styles.css
    └── img/
```

## Resultado

Con K=5 se identifican segmentos como clientes de alto valor, clientes con potencial, compradores frecuentes, clientes conservadores y clientes promedio.
