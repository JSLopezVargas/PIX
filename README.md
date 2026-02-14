# **Automation: Stock Management & Reporting (PIX RPA)**

Este proyecto automatiza de extremo a extremo el procesamiento de inventarios diarios de una tienda, integrando bases de datos locales, almacenamiento en la nube de Microsoft, reportes de Excel y envío de reportes por GForms.

## **📝 Descripción del Proyecto**

El bot ejecuta un flujo de trabajo modular diseñado para la integridad y trazabilidad de datos:

1. Limpieza de entorno: Cierre automático de procesos (Google Chrome, Excel) para evitar bloqueos de ejecuciones por programas abiertos previamente.

2. Sincronización de Datos: Procesamiento de información técnica y carga en base de datos SQLite.

3. Cálculo de Métricas: Ejecución de consultas SQL para obtener estadísticas de negocio (promedios y conteos).

4. Generación de Reportes: Exportación de resultados a un archivo Excel dinámico.

5. Integración Microsoft Graph: Carga del reporte y archivo JSON a OneDrive mediante autenticación OAuth2 (Método PUT).

6. Cierre de Proceso: Registro de actividad y envío de evidencias en Google Forms.

## **🚀 Pasos para la Ejecución **

1. Configuración de Entorno: Verificar que el Client Secret y Tenant ID en el archivo Config.xlsx sean válidos.

2. Preparación del Navegador: * Abrir Google Chrome en una ventana normal (No incógnito).

3. Asegurarse de tener la sesión de Google/Gmail iniciada, ya que el llenado del formulario requiere acceso a la cuenta.

4. Lanzamiento: Ejecutar el archivo Main.pix desde PIX Studio.

## **🛠 Requisitos y Dependencias **

- Software: PIX RPA Studio.

- Navegador: Google Chrome con la extensión de PIX RPA instalada y habilitada.

- Sesión Activa: Cuenta de Google abierta en el navegador (Requisito para el acceso a GForms).

- Base de Datos: Motor SQLite 3.

- Permisos Azure: Aplicación registrada con permisos Files.ReadWrite.

## **🔗 Enlace del Formulario **

El formulario de Google utilizado para la recolección de métricas es:

👉 https://docs.google.com/forms/d/1nOAeCra_aGSJHlwpi3Hc5JRtWN-PKx7yXhqazd4S4qQ

## **💡 Nota de BA para el desplegador **

Para garantizar que el bot interactúe correctamente con los elementos web:

- No minimices la ventana de Chrome mientras el bot esté interactuando con el formulario.

- Verifica que el bloqueador de anuncios (si tienes uno) no esté afectando la carga del formulario de Google.

- En el repositorio se encuentra el diagrama BPMN del proceso en formato PNG y bpmn.
