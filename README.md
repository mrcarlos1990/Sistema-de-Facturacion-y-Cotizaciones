# Sistema Corporativo de Facturacion y Cotizaciones AFCyber SOLUTIONS

Aplicacion profesional de escritorio para Windows creada con Python 3, Tkinter, SQLite y ReportLab.

## Ejecucion

1. Instalar dependencias:

```powershell
pip install -r requirements.txt
```

2. Ejecutar:

```powershell
python -m app.main
```

Tambien puede abrir `ejecutar_sistema.bat`.

## Acceso inicial

- Usuario: `admin`
- Contrasena: `admin pass`

En el primer inicio tambien se muestra la activacion local de licencia para seleccionar el periodo de uso.
Antes de la activacion se muestra la pantalla de terminos y condiciones, con aceptacion obligatoria.
Luego se solicita la contrasena maestra antes de permitir seleccionar el periodo de licencia.
En el primer inicio el sistema solicita cambiar las credenciales.

## Carpetas y datos

- Base de datos: `app/config/facturacion_afcyber.sqlite3`
- PDFs de facturas: `Facturas/`
- PDFs de cotizaciones: `Cotizaciones/`

## Funciones incluidas

- Login con contrasenas cifradas por hash PBKDF2.
- Roles basicos: Administrador y Usuario.
- Dashboard con indicadores y documentos recientes.
- Sistema de licencia local con vencimiento, renovacion e historial.
- Recuperacion de contrasena maestra mediante preguntas de seguridad con respuestas cifradas por hash.
- Terminos legales antes del primer uso y modulo Legal / Licencia.
- CRUD de clientes.
- CRUD de productos y servicios.
- Facturas con numeracion automatica, ITBIS, descuentos, observaciones, anulacion, PDF e impresion.
- Cotizaciones con vigencia, condiciones comerciales, PDF, impresion y conversion a factura.
- Centro de Ayuda con guias rapidas y carga de datos demo.
- Modulo Acerca de corporativo.
- Panel administrativo con usuarios, logs, licencia y respaldos.
- Administracion de preguntas de seguridad y logs de seguridad.
- Configuracion de impresora de Windows, vista previa, copias, papel y margenes.
- Impresoras por tipo de documento: facturas, cotizaciones y tickets/POS, con tamanos Carta, Media carta, A4, Ticket 80mm y Ticket 58mm.
- Productos con codigo de barras, categoria, existencia, precio de compra y precio de venta.
- Escaneo rapido con lectores USB tipo teclado en facturas y cotizaciones.
- Modulo de respaldos profesional: SQLite `.db`, Excel, CSV, PDF de reportes, ZIP completo y restauracion.
- Backup automatico opcional con frecuencia diaria, semanal o mensual y carpeta destino configurable.
- Configuracion editable de empresa, logo, colores, margenes, formato, pie de pagina y firma.
- Pantallas con navegacion atras, ventanas redimensionables y scroll en areas largas.
- Auditoria de acciones principales.

Firma obligatoria en documentos:

`Desarrollado por AFCyber SOLUTIONS por el Ing. Amauri Feliz`

## Preparacion futura para EXE

Ejemplo base con PyInstaller:

```powershell
pip install pyinstaller
pyinstaller --noconsole --name "AFCyber Facturacion" --add-data "app;app" app/main.py
```
