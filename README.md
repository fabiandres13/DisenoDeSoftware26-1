# 🍽️ Sistema de Gestión de Inventarios para Pequeñas Empresas (Orientado a Restaurante)

![Estado: Finalizado](https://img.shields.io/badge/Estado-Finalizado-success)
![Curso: Diseño de Software](https://img.shields.io/badge/Curso-Diseño_de_Software-blue)
![Universidad de Talca](https://img.shields.io/badge/Institución-Universidad_de_Talca-red)

Aplicación web centralizada diseñada para automatizar y asegurar la trazabilidad del ciclo de vida de los productos en un restaurante, desde la compra al proveedor hasta el registro de la venta, controlando el stock en tiempo real mediante un sistema de roles seguros.

## 👥 Equipo de Trabajo: Grupo 3 "Los Sin Nombre"
* **Miguel Aliaga Vera** - *Líder de equipo*
* **Fabián Paredes Lagos**
* **Esteban Guzmán Cañete**

**Información Académica:**
* **Asignatura:** Diseño de Software
* **Profesor:** Ernesto Pereiras García
* **Facultad:** Ingeniería Civil en Computación, Universidad de Talca.

---

## 📌 Enlaces a Entregables Finales
Aquí puedes encontrar toda la documentación, informes y recursos generados durante el ciclo de desarrollo del proyecto:

### 📄 Informes
* **[Informe Unidad 1](https://docs.google.com/document/d/124NoD6csEitwZ_y5miStTJKufE1O5dAuuq0hI5yB6L8/edit?usp=sharing)**
* **[Informe Unidad 2](https://docs.google.com/document/d/1APk7WTtPP5vSeq0aE45QLme-I3uMD2b1AnN2hsrj__c/edit?usp=sharing)**
* **[Informe Unidad 3](https://docs.google.com/document/d/1MjOQkOiO6TpdmdkL2i6YidfDz6Mk9T0MBFvakts-DXU/edit?usp=sharing)**

### 🎯 Entregables Finales (Archivos en el Repositorio)
* 📊 **[Presentación Final (PDF)](./Presentacion_final_grupo_3.pdf)**
* 📑 **[Informe Final del Proyecto (PDF)](./Informe_final_grupo_3%20(1).pdf)**

### 🛠️ Recursos de Diseño y Prototipado
* 🗂️ **[Diagrama de Clases UML (Lucidchart)](https://lucid.app/lucidchart/d793510c-e990-43a7-8e57-6116b90dd468/edit?viewport_loc=-3525%2C-1838%2C9096%2C4590%2C0_0&invitationId=inv_a7beeb9b-08d0-4e25-9132-c16500c83666)**
* 🎨 **[Prototipo Navegable (Figma)](https://www.figma.com/design/7l5xmhpBemYKpRmee8LWLK/RESTAURANTE?node-id=0-1&t=EdeNszBVCXZzYhn0-1)**
* 📸 **Capturas de Pantalla:** Disponibles en los commits recientes del repositorio (UML y Prototipo).

---

## 🏗️ Arquitectura y Patrones de Diseño Aplicados

El sistema fue diseñado con un fuerte enfoque en la escalabilidad y las buenas prácticas de ingeniería de software, utilizando una **Arquitectura Cliente-Servidor Monolítica por Capas**. 

Para resolver problemas específicos de diseño y reducir el acoplamiento, se implementaron los siguientes patrones:

1. **Singleton (Patrón Creacional):** Implementado en la clase `Control (stock)` para centralizar el estado del inventario. Garantiza que módulos como Ventas, Compras y Alertas consulten una única instancia, evitando inconsistencias de datos en concurrencia.
2. **Proxy (Patrón Estructural):** Utilizado para mejorar la seguridad y el control de accesos. Verifica los permisos del usuario (Administrador vs. Empleado) antes de permitir la ejecución de transacciones de venta o modificaciones críticas.
3. **Observer (Patrón de Comportamiento):** Implementado para automatizar el control de stock. Descuenta automáticamente los productos tras cada venta y dispara alertas tempranas en el Dashboard cuando los niveles de inventario alcanzan un umbral crítico.

---

## 🚀 Funcionalidades Principales (Requerimientos)

* **Control de Stock en Tiempo Real (RF-01):** Actualización inmediata de cantidades (</= 2 segundos) tras registrar una venta o compra.
* **Alertas Inteligentes:** Notificaciones visuales automáticas cuando un producto entra en estado crítico de inventario.
* **Gestión de Transacciones:** Registro fluido de compras a proveedores y ventas a clientes, optimizado para una baja carga cognitiva (</= 5 clics por transacción).
* **Control de Accesos:** Diferenciación clara de vistas y operaciones según el rol de usuario autenticado.

---
*Proyecto desarrollado para la evaluación final de la asignatura Diseño de Software - Semestre 1, 2026.*
