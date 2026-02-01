# EcoSolution_chatbot

El proyecto **EcoSolutions** consiste en el desarrollo de un chatbot basado en **Procesamiento de Lenguaje Natural (PLN)** que brinda información y soluciones relacionadas con problemas de contaminación ambiental.

El sistema utiliza modelos de inteligencia artificial desarrollados en **Python**, empleando técnicas como **Regresión Logística** y **Vectorización de texto**, que permiten interpretar preguntas realizadas por los usuarios y generar respuestas relacionadas con temas ambientales. Para el entrenamiento del modelo, se recopilan y procesan datos obtenidos de distintas fuentes relacionadas con el medio ambiente.

El proyecto incluye un **sistema web desarrollado en Angular**, el cual se comunica con un **backend construido en Python mediante una API**.

El sistema cuenta con **dos versiones del backend**:

* 🔹 Una API que entrena el modelo utilizando procesamiento tradicional (secuencial).
* 🔹 Una API que entrena el modelo utilizando **procesamiento paralelo**, con el objetivo de mejorar el tiempo de entrenamiento del modelo.

Es importante destacar que el paralelismo se aplica únicamente durante el proceso de entrenamiento del modelo, no durante la ejecución ni en la generación de respuestas del chatbot.

La solución está estructurada mediante **submódulos**, donde se separan los componentes del proyecto, incluyendo ambas versiones del backend y la aplicación web en Angular.

<br>

# 📦 Componentes del Proyecto

El proyecto está compuesto por:

* 🌐 Frontend desarrollado en Angular
* ⚙️ Backend Python — Entrenamiento secuencial del modelo
* ⚙️ Backend Python — Entrenamiento paralelo del modelo
* 🧠 Modelo de IA basado en PLN
* 📦 Uso de submódulos Git para organizar los componentes


<br>

# ✅ Requisitos Previos

Antes de instalar el proyecto debes tener instalado:

* Git
* Python 3.9 o superior
* Node.js (versión 18 o superior recomendada)
* Angular CLI

Instalar Angular CLI:

```bash
npm install -g @angular/cli
```

<br>

# ✅ Cómo descargar el proyecto con submódulos

Existen varias formas de hacerlo.

<br>

## ⭐ Forma 1 — Clonar todo desde el inicio (Recomendada)

Este método descarga el repositorio principal junto con todos los submódulos.

```bash
git clone --recurse-submodules URL_DEL_REPO
```

Luego entra al proyecto:

```bash
cd EcoSolution_chatbot
```

<br>

## ⭐ Forma 2 — Si ya clonaste el repositorio sin submódulos

Si ejecutaste solo `git clone`, debes inicializar los submódulos manualmente.

Entra al proyecto:

```bash
cd EcoSolution_chatbot
```

Luego ejecuta:

```bash
git submodule update --init --recursive
```

Esto descargará todos los submódulos faltantes.

<br>

## ⭐ Forma 3 — Actualizar submódulos a la última versión

Si los submódulos ya existen pero deseas actualizarlos:

```bash
git submodule update --recursive --remote
```

<br>

# ✅ Instalación del Backend (Python API)

Entrar al submódulo del backend:

```bash
cd backend_python
```

Crear entorno virtual:

```bash
python -m venv venv
```

Activar entorno virtual:

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

Instalar dependencias:

```bash
pip install -r requirements.txt
```

Ejecutar la API:

```bash
python app.py
```

<br>

# ✅ Instalación del Frontend (Angular)

Entrar al submódulo del frontend:

```bash
cd frontend_angular
```

Instalar dependencias:

```bash
npm install
```

Ejecutar el proyecto Angular:

```bash
ng serve
```

El sistema estará disponible en:

```
http://localhost:4200
```

<br>

# ✅ Notas Importantes

* El backend debe estar ejecutándose antes de iniciar el frontend.
* Verificar que la URL de la API esté configurada correctamente en Angular.
* Los submódulos contienen:

  * Backend con procesamiento paralelo
  * Backend con procesamiento no paralelo
  * Sistema web Angular
