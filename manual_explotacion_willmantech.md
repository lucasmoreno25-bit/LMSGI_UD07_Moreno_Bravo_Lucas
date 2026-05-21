# Proyecto: Sistema de Gestión para WillmanTech S.L.

Este proyecto sirve para poner en marcha y organizar el sistema de gestión de ventas y facturas de la empresa WillmanTech S.L. Todo el sistema funciona dentro de contenedores de Docker para que sea fácil de instalar.


## Carpetas y Archivos del Proyecto

Los archivos están organizados de la siguiente manera:

* report_invoice_willmantech.xml: Plantilla para diseñar las facturas (QWeb XML).
* interoperabilidad/invoice_ubl.xml: Factura electrónica oficial en formato XML (UBL).
* manual_explotacion_willmantech.md: Manual de instrucciones para el ordenador y el usuario.

## Explicación Sencilla de cada Parte

### 1. Plantilla de Factura (report_invoice_willmantech.xml)
Es el diseño de la factura. Usa un código llamado QWeb que hace lo siguiente:
* Coge automáticamente los datos de la base de datos, como el nombre del cliente o el total.
* Tiene un bucle que escribe todas las cosas que ha comprado el cliente, una debajo de otra.
* Tiene un truco: si el cliente no tiene ningún descuento, la columna de "Descuento" desaparece sola para que la factura quede más limpia.

### 2. Compartir Datos con otros Sistemas (Carpeta interoperabilidad)
Sirve para enviar las facturas a Hacienda o a otros programas de forma automática:
* invoice_ubl.xml: Es un archivo XML especial que sigue las normas de la Unión Europea para las facturas electrónicas obligatorias.

### 3. Manual Técnico (manual_explotacion_willmantech.md)
Es el libro de instrucciones para la persona encargada de los ordenadores. Explica:
* Cómo funciona Docker y la base de datos por dentro.
* Los pasos para instalar todo el programa desde cero.
* Quién puede entrar al sistema (jefes, contables o comerciales) y qué cosas tienen permiso para tocar.
* Cómo hacer copias de seguridad para no perder los datos si se rompe el ordenador.
* Cómo el programa convierte la factura de una pantalla web a un archivo PDF listo para imprimir.


