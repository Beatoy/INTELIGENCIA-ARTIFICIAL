# INTELIGENCIA-ARTIFICIAL
ES UN REPOCITORIO DEL CONGLOMERADO DE TEMAS QUE SE HAN VISTO A LO LARGO DEL SEMESTRE
Clasificación de dígitos con una CNN (imágenes 8x8)
---------------------------------------------------

Este proyecto utiliza el dataset Digits de scikit-learn, que contiene imágenes de 8x8 píxeles de números escritos a mano. El código carga los datos, los normaliza y entrena una red convolucional sencilla para reconocer los dígitos del 0 al 9. También incluye la parte para probar una imagen externa llamada “mi_numero.png”.

Contenido del script
--------------------
- Carga del dataset Digits
- División en entrenamiento y prueba
- Normalización con StandardScaler
- Conversión a one-hot
- Preparación de los datos para la CNN
- Construcción del modelo (Conv2D, MaxPooling, Dense)
- Entrenamiento con validación
- Gráfica de la pérdida
- Evaluación final con accuracy
- Matriz de confusión
- Sensibilidad por clase
- Prueba con una imagen externa 8x8

Requisitos
----------
numpy
matplotlib
tensorflow
scikit-learn
seaborn
pillow

Ejecución
---------
Ejecutar:

    python cnn_digits.py

Si existe el archivo mi_numero.png en la misma carpeta, el código intentará clasificarlo. La imagen se convierte a escala de grises y se ajusta a 8x8 para que la red pueda procesarla.

Sobre la imagen externa
-----------------------
Para obtener un resultado razonable:
- fondo claro
- número en color oscuro
- preferentemente centrado
- formato PNG

Arquitectura del modelo
-----------------------
La red es pequeña debido al tamaño reducido de las imágenes:
- Capa Conv2D con 32 filtros
- MaxPooling 2x2
- Flatten
- Capa densa de 128 neuronas
- Capa de salida con 10 clases (softmax)

Resultados esperados
--------------------
El modelo suele obtener una exactitud mayor al 95% en este dataset. La matriz de confusión permite revisar dónde se presentan los errores.

Estructura sugerida del proyecto
--------------------------------
proyecto_cnn_digits/
    cnn_digits.py
    mi_numero.png   (opcional)
    requirements.txt
    README.md

Licencia
--------
Proyecto libre de uso educativo.
