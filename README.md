# INTELIGENCIA-ARTIFICIAL
ES UN REPOCITORIO DEL CONGLOMERADO DE TEMAS QUE SE HAN VISTO A LO LARGO DEL SEMESTRE
Clasificación de dígitos con una CNN (imágenes 8x8)

Este proyecto trabaja con el dataset Digits de scikit-learn (son imágenes pequeñas, de 8x8 píxeles), y se entrena una red convolucional sencilla para reconocer los números del 0 al 9.
El archivo principal incluye todo: carga de datos, normalización, construcción del modelo, entrenamiento, gráficas y pruebas con una imagen externa.

Objetivo del código

La idea es tomar los dígitos escritos a mano del dataset, entrenar una CNN y verificar qué tan bien reconoce números.
También se agregó la parte para cargar una imagen aparte (mi_numero.png) para comprobar si el modelo responde bien fuera del dataset.

Lo que incluye el script

Carga del dataset Digits

Normalización usando StandardScaler

Conversión de etiquetas a one-hot

Preparación del formato para CNN

Construcción del modelo

Entrenamiento con validación

Gráfica de la pérdida

Evaluación en test

Matriz de confusión

Sensibilidad por clase

Clasificación de una imagen externa 8x8

Todo en un solo archivo para facilitar pruebas.

Requisitos

Crea un archivo requirements.txt así:

numpy
matplotlib
tensorflow
scikit-learn
seaborn
pillow

Cómo ejecutarlo

Solo correr:

python cnn_digits.py


Si tienes un archivo mi_numero.png en la misma carpeta, el script también lo intenta clasificar. La imagen se convierte a escala de grises y se ajusta a 8x8 para que el modelo la pueda interpretar.

Si no existe la imagen, solo se omite esa parte (o la puedes comentar).

Notas sobre la imagen externa

Para que la predicción tenga sentido:

fondo claro

número en negro

idealmente centrado

formato PNG

el código lo ajusta a 8x8, así que no importa el tamaño original

Modelo usado

El modelo es pequeño por el tamaño de las imágenes:

Conv2D de 32 filtros

MaxPooling

Flatten

Dense de 128

Dense final de 10 clases con softmax

Es un modelo básico, suficiente para este dataset.

Resultados esperados

Normalmente la exactitud ronda arriba del 95%.
La matriz de confusión y las sensibilidades por clase ayudan a ver en qué dígitos falla más.

Estructura sugerida del proyecto
proyecto_cnn_digits/
│
├── cnn_digits.py
├── mi_numero.png   (opcional)
├── requirements.txt
└── README.md

Licencia

Este proyecto se puede usar libremente con fines educativos o demostrativos.
