# 🍽 TPV Restaurante Profesional

[![Desarrollado por secTF Labs](https://img.shields.io/badge/Desarrollado%20por-secTF%20Labs-8E44AD?style=for-the-badge&logo=github)](https://github.com/secTF-Labs)
[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-2ECC71?style=for-the-badge)](LICENSE)
[![NET Version](https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet)](https://dotnet.microsoft.com/)

Sistema de Punto de Venta (**TPV / POS**) de alta gama diseñado para la gestión integral de restaurantes, cafeterías y bares. Desarrollado en **C# con WPF (.NET 8)** y **SQLite / Entity Framework Core**, optimizado para pantallas táctiles y preparado para entornos multiusuario.

---

## 🌟 Novedades y Mejoras Recientes

- **🔒 Persistencia Segura y Permisos en Windows:**
  - La base de datos SQLite (`tpv_restaurante.db`) y la generación de archivos de tickets se han trasladado a la ruta del sistema `%LocalAppData%\TPVRestaurante`.
  - **Ejecución sin privilegios de Administrador:** Elimina los bloqueos de permisos en `C:\Program Files`, permitiendo que cualquier usuario estándar ejecute la aplicación con total fluidez.
- **📦 Módulo de Almacén y Compras Ampliado:**
  - Integración en tiempo real con SQLite para consultar, actualizar y dar de alta materias primas e insumos (Kilos, Litros, Cajas, Unidades).
  - Control de recepción de pedidos de compra que incrementa automáticamente el stock y actualiza el histórico de costes por unidad.
- **✏ Gestión Avanzada de Precios y Carta Extendida:**
  - Carta precargada con más de **40 productos organizados por familias** (*Primeros, Segundos, Postres y Bebidas*).
  - Módulo de Gerencia que permite seleccionar cualquier producto de la carta y modificar su precio o familia en vivo.
- **✂ División de Cuentas (Split Bill) y Promociones:**
  - Posibilidad de separar una comanda para cobrar un sub-ticket parcial (en efectivo o tarjeta) con aplicación de descuentos independientes en porcentaje (%).

---

## 🚀 Características Principales

- **🔐 Control de Acceso por Roles (PIN):**
  - Fichaje e inicio de sesión mediante teclado numérico táctil (*Keypad*).
  - Perfiles diferenciados con interfaz adaptable: *Camarero*, *Gestor de Almacén*, *Gerente* e *IT*.
- **🗺 Mapa de Sala Interactivo:**
  - Gestión de mesas y barra en tiempo real con indicadores visuales de estado (🟢 Libre | 🔵 Seleccionada | 🔴 Con pedido).
  - Modo edición *Drag & Drop* para organizar el plano de la sala.
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
| **Administrador** | Admin IT | `1234` | Acceso Total + Alta de Usuarios en Base de Datos |

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

* **Desarrollador:** Gustavo Ucar de Armas
* **Organización:** SecTF labs
* **Fecha de Lanzamiento:** 28/09/2026
* **Versión:** 1.0.0

