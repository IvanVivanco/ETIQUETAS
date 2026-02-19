Deteco DTX - Sistema de Etiquetas y Visor de Inventario

Aplicación web desarrollada para la gestión logística y de bodega de Deteco IC SA. Esta herramienta permite generar etiquetas físicas con códigos QR inteligentes y visualizar el estado del inventario en tiempo real escaneando dichos códigos desde cualquier dispositivo móvil o PC.

🚀 Características Principales

Generador de Etiquetas (PDF e Impresión): * Diseño industrial minimalista y corporativo.

Ajuste de tamaños de fuente en tiempo real (Nombre, SKU, N° Organizador, Familia).

Auto-numeración de cajas/organizadores físicos.

Opciones de diseño en matriz (filas, columnas, orientación vertical/horizontal).

Códigos QR Inteligentes: Cada etiqueta generada contiene un QR que enlaza directamente a la ficha del producto dentro de la aplicación.

Visor de Inventario (Responsivo):

Búsqueda manual o automática (vía escaneo de QR).

Muestra información vital: Código, Nombre, Stock actual, Ubicación física (Organizador).

Descarga directa de Ficha Técnica (PDF) si está disponible en la base de datos.

Base de Datos en Tiempo Real: Conectado directamente a una hoja de cálculo de Google Sheets (vía CSV), permitiendo actualizaciones de stock e información sin necesidad de modificar el código.

🛠️ Instalación y Despliegue (GitHub Pages)

Esta aplicación no requiere servidores backend complejos. Funciona 100% en el navegador (Client-Side).

Clonar o subir archivos: Asegúrate de tener los archivos index.html y logo.png en la rama main de tu repositorio.

Activar GitHub Pages:

Ve a la pestaña Settings de tu repositorio.

En el menú izquierdo, haz clic en Pages.

En "Build and deployment", selecciona Deploy from a branch.

En "Branch", selecciona main y la carpeta /(root), luego guarda.

Listo: En un par de minutos, tu aplicación estará en línea en tu enlace de GitHub (ej. https://tu-usuario.github.io/tu-repo/).

📊 Configuración de la Base de Datos (Google Sheets)

Para que el buscador, el stock y las fichas técnicas funcionen, tu Google Sheet debe tener exactamente estas columnas (puedes tener más, pero estas son las leídas por el sistema):

CODIGO

NOMBRE

CATEGORIA

STOCK

ORGANIZADOR

FICHA

C-01-05

GUANTES MULTIFLEX

EPP

79

179

https://link-a-dropbox/pdf

C-02-12

DISCO CORTE 4.5"

HERRAMIENTA

150

C02-16

(vacío)

(Nota: Si no usas "ORGANIZADOR", el sistema buscará una columna llamada "UBICACION" como respaldo).

¿Cómo conectar el Google Sheets?

En Google Sheets, ve a Archivo > Compartir > Publicar en la web.

Selecciona la pestaña de tu inventario y elige el formato Valores separados por comas (.csv).

Copia el enlace generado y pégalo en la variable CSV_URL dentro del archivo index.html.

📂 Estructura de Archivos

index.html: Archivo principal. Contiene toda la estructura HTML, diseño (Tailwind CSS/Estilos propios) y la lógica JavaScript (conexión a BDD, generador de PDF, creador de QR).

logo.png: Logotipo oficial de Deteco que se incrusta en las etiquetas y en el visor.

👨‍💻 Créditos

Diseñado y programado por Iván Vivanco para uso interno en el área de adquisiciones y logística de Deteco IC SA.
