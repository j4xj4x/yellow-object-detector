# Yellow Object Detector

## Descripción

Yellow Object Detector es un proyecto de visión artificial que detecta objetos de color amarillo en tiempo real utilizando una cámara web. El programa procesa cada frame del video, identifica las regiones que contienen el color amarillo y dibuja un rectángulo alrededor del objeto detectado.

Este proyecto utiliza procesamiento de imagen basado en el espacio de color **HSV**, lo que permite detectar colores de forma más robusta que usando directamente RGB.

## Tecnologías utilizadas

* Python 3.12.1
* OpenCV
* NumPy
* Pillow (PIL)

## Requisitos

* Python 3.12.1
* Cámara web
* Entorno virtual (recomendado)

## Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/j4xj4x/yellow-object-detector.git
cd yellow-object-detector
```

2. Crea un entorno virtual:

```bash
python -m venv venv
```

3. Activa el entorno virtual:

**Windows**

```bash
venv\Scripts\activate
```

**Mac / Linux**

```bash
source venv/bin/activate
```

4. Instala las dependencias:

```bash
pip install -r requirements.txt
```

## Uso

Ejecuta el programa con:

```bash
python main.py
```

El programa abrirá la cámara web y comenzará a analizar el video en tiempo real.
Cuando detecte un objeto amarillo, dibujará un rectángulo verde alrededor del área detectada.

Para cerrar la aplicación, presiona la tecla **Q**.

## Cómo funciona

El programa sigue estos pasos:

1. Captura video en tiempo real desde la cámara.
2. Convierte cada frame del espacio de color **BGR a HSV**.
3. Genera una máscara que filtra únicamente los píxeles dentro del rango de color amarillo.
4. Detecta la región donde aparece el color.
5. Calcula el área delimitadora del objeto.
6. Dibuja un rectángulo alrededor del objeto detectado.

## Estructura del proyecto

```
yellow-object-detector
│
├── main.py
├── util.py
├── requirements.txt
└── README.md
```

