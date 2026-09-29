# 🍽 TPV Restaurante Profesional

[![Desarrollado por secTF Labs](https://img.shields.io/badge/Desarrollado%20por-secTF%20Labs-8E44AD?style=for-the-badge&logo=github)](https://github.com/secTF-Labs)
[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-2ECC71?style=for-the-badge)](LICENSE)
[![NET Version](https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet)](https://dotnet.microsoft.com/)

Sistema de Punto de Venta (**TPV / POS**) de alta gama diseñado para la gestión integral de restaurantes, cafeterías y bares. Desarrollado en **C# con WPF (.NET 8)** y **SQLite / Entity Framework Core**, optimizado para pantallas táctiles y preparado para entornos multiusuario en red local.

---

## 🌟 Novedades y Mejoras Recientes

- **🌐 Arquitectura Cliente-Servidor y Conexión en Red:**
  - Posibilidad de alojar la base de datos en un equipo servidor o unidad compartida en red local (rutas UNC como `\\SERVIDOR\TPVData\tpv_restaurante.db`) y conectar múltiples TPVs simultáneamente.
  - Módulo de prueba de conexión en caliente desde la pestaña de administración.
- **📦 Programador Automático de Copias de Seguridad (Backups):**
  - Servicio en segundo plano para programar copias de seguridad automáticas de la base de datos con intervalos configurables (1, 6, 12 o 24 horas).
  - Opción de forzar una copia de seguridad manual en cualquier momento hacia rutas locales o unidades externas (USB/NAS).
- **🔒 Persistencia Segura y Permisos en Windows:**
  - Guardado por defecto en `%LocalAppData%\TPVRestaurante` para garantizar ejecución inmediata sin requerir privilegios de Administrador en Windows.
- **📦 Almacén y Gestión de Compras:**
  - Control de stock de materias primas e insumos (Kilos, Litros, Cajas, Unidades) sincronizado con la base de datos.
  - Recepción de pedidos de compra con actualización de stock e historial de costes por unidad.
- **✏ Gestión Avanzada de Carta y Precios:**
  - Carta precargada con más de **40 productos organizados por familias** (*Primeros, Segundos, Postres y Bebidas*).
  - Módulo de Gerencia para modificar precios o familias en vivo y dar de alta nuevos platos.
- **✂ División de Cuentas (Split Bill) y Promociones:**
  - Separación de comandas para cobros parciales con aplicación de descuentos en porcentaje (%) independientes.

---

## 🚀 Características Principales

- **🔐 Control de Acceso por Roles (PIN):**
  - Fichaje e inicio de sesión mediante teclado numérico táctil (*Keypad*).
  - Perfiles diferenciados con interfaz adaptable: *Camarero*, *Gestor de Almacén*, *Gerente* e *IT*.
- **🗺 Mapa de Sala Interactivo:**
  - Gestión de mesas y barra en tiempo real con indicadores visuales de estado (🟢 Libre | 🔵 Seleccionada | 🔴 Con pedido).
  - Modo edición *Drag & Drop* para reorganizar el plano del salón.
- **💳 Módulo de Cobro, Tickets y Caja:**
  - Calculadora de cambio a devolver, emisión de ticket comercial en pantalla y guardado en disco.
  - Arqueo de caja diario con generación de **Informe Z** (cuadre de efectivo y tarjeta).

---

## 🔑 Usuarios y PINs Predeterminados

| Rol | Usuario | PIN Predeterminado | Acceso y Permisos |
|---|---|---|---|
| **Camarero** | Juan | `1111` | Sala, Comandas, Cobros Totales/Parciales y Descuentos |
| **Almacén** | María | `2222` | Control de Stock, Recepción de Compras e Insumos |
| **Gerente** | Carlos | `3333` | Edición de Precios, Alta de Platos, Plano de Sala y Cierre Z |
| **Administrador** | Admin IT | `1234` | Conexión Red, Backups, Permisos y Alta de Usuarios |

---

## 📥 Instalación y Despliegue

### Opción A: Instalador Autónomo (.exe)
1. Descarga el archivo de instalación `TPV_Restaurante_Setup_v1.0.0.exe` generado con **Inno Setup**.
2. Ejecuta el asistente de instalación.
3. Inicia la aplicación directamente desde el acceso directo del Escritorio sin necesidad de permisos de administrador.

### Opción B: Ejecución desde el Código Fuente
1. Clona este repositorio:
   ```bash
   git clone [https://github.com/secTF-Labs/TPVRestaurante.git](https://github.com/secTF-Labs/TPVRestaurante.git)
