# 🛒 Sistema de Ventas e Inventario — Tienda Local

> Sistema web para la gestión de ventas e inventario de una tienda de barrio ubicada en el municipio de Bello, Antioquia.

---

## 1. Contextualización del Proyecto

### Descripción del Problema

Las tiendas de barrio en Colombia, y en particular en el municipio de **Bello (Antioquia)**, operan en su mayoría de forma manual: el registro de ventas se hace en cuadernos, el control de inventario depende de la memoria del tendero y no existe visibilidad sobre las ganancias reales del negocio. Esto genera pérdidas por productos vencidos, desabastecimiento, errores en el cobro y dificultad para tomar decisiones informadas sobre el negocio.

### Solución Propuesta

Este proyecto busca digitalizar los procesos clave de una tienda local mediante una aplicación que permita:

- **Registrar ventas** de forma rápida y sencilla desde el mostrador.
- **Controlar el inventario** en tiempo real, con alertas de stock bajo.
- **Gestionar productos**: agregar, editar, eliminar y categorizar artículos.
- **Consultar reportes** básicos de ventas diarias, semanales y mensuales.
- **Administrar proveedores** y entradas de mercancía.

### Contexto

| Atributo | Detalle |
|---|---|
| Tipo de negocio | Tienda de barrio (miscelánea / minimercado) |
| Ubicación | Bello, Antioquia, Colombia |
| Usuarios objetivo | Tendero / propietario y sus colaboradores |
| Modalidad | Aplicación web local (puede correr sin internet) |

---

## 2. Herramientas y Versiones de Software

### Frontend

| Herramienta | Versión | Descripción |
|---|---|---|
| HTML5 / CSS3 | — | Estructura y estilos base |
| JavaScript | ES2020+ | Lógica del cliente |
| React | 18.x | Librería de interfaz de usuario |
| Vite | 5.x | Herramienta de build y servidor de desarrollo |
| Tailwind CSS | 3.x | Framework de estilos utilitarios |

### Backend

| Herramienta | Versión | Descripción |
|---|---|---|
| Node.js | 20.x LTS | Entorno de ejecución JavaScript |
| Express.js | 4.x | Framework para el servidor HTTP / API REST |
| Sequelize | 6.x | ORM para manejo de base de datos |

### Base de Datos

| Herramienta | Versión | Descripción |
|---|---|---|
| MySQL | 8.x | Motor de base de datos relacional |

### Herramientas de Desarrollo

| Herramienta | Versión | Descripción |
|---|---|---|
| Git | 2.x | Control de versiones |
| npm | 10.x | Gestor de paquetes de Node.js |
| Postman | — | Pruebas de la API REST |
| VS Code | — | Editor de código recomendado |

---

## 3. Paso a Paso de Instalación

### Prerrequisitos

Antes de comenzar, asegúrate de tener instalado en tu equipo:

- [Node.js v20 LTS](https://nodejs.org/)
- [MySQL 8](https://dev.mysql.com/downloads/mysql/)
- [Git](https://git-scm.com/)

### Paso 1 — Clonar el repositorio

```bash
git clone https://github.com/usuario/tienda-bello.git
cd tienda-bello
```

### Paso 2 — Configurar las variables de entorno

Copia el archivo de ejemplo y edítalo con tus datos locales:

```bash
cp .env.example .env
```

Abre el archivo `.env` y ajusta los siguientes valores:

```env
# Base de datos
DB_HOST=localhost
DB_PORT=3306
DB_NAME=tienda_inventario
DB_USER=root
DB_PASSWORD=tu_contraseña

# Servidor
PORT=3001
NODE_ENV=development

# Seguridad
JWT_SECRET=clave_secreta_larga_y_segura
```

### Paso 3 — Crear la base de datos

Ingresa a MySQL y crea la base de datos:

```sql
CREATE DATABASE tienda_inventario CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### Paso 4 — Instalar dependencias del Backend

```bash
cd backend
npm install
```

### Paso 5 — Ejecutar migraciones y datos iniciales (seeders)

```bash
npx sequelize-cli db:migrate
npx sequelize-cli db:seed:all
```

### Paso 6 — Instalar dependencias del Frontend

```bash
cd ../frontend
npm install
```

### Paso 7 — Levantar el proyecto en modo desarrollo

Abre **dos terminales** de forma simultánea:

**Terminal 1 — Backend:**
```bash
cd backend
npm run dev
```

**Terminal 2 — Frontend:**
```bash
cd frontend
npm run dev
```

### Paso 8 — Acceder a la aplicación

Abre tu navegador y dirígete a:

```
http://localhost:5173
```

Las credenciales por defecto del administrador (seeder) son:

```
Usuario: admin@tienda.com
Contraseña: admin1234
```

> ⚠️ **Importante:** Cambia la contraseña del administrador inmediatamente después del primer inicio de sesión.

---

## 4. Información del Autor

| Campo | Detalle |
|---|---|
| **Nombre** | [Tu Nombre Completo] |
| **Correo electrónico** | tucorreo@email.com |
| **GitHub** | [@tu_usuario](https://github.com/tu_usuario) |
| **LinkedIn** | [linkedin.com/in/tu_perfil](https://linkedin.com/in/tu_perfil) |
| **Institución / Empresa** | [Nombre de tu institución o empresa] |
| **Ciudad** | Bello, Antioquia, Colombia |
| **Año** | 2024 |

---

## Licencia

Este proyecto está bajo la licencia **MIT**. Consulta el archivo [LICENSE](./LICENSE) para más información.

---

*Desarrollado con ❤️ para las tiendas de barrio de Bello.*