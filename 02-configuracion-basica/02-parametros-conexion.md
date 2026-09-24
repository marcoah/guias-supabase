# 🔌 Guía: Obtención de Datos de Conexión PostgreSQL

[« Índice de la sección](./README.md) | [Anterior: Credenciales de API](./01-credenciales-api.md) | [Siguiente: Conexión desde pgAdmin »](./03-conexion-pgadmin.md)

---

Para conectar aplicaciones de escritorio como **pgAdmin, QGIS o Power BI** directamente a PostgreSQL, necesitas los parámetros técnicos de acceso al servidor.

## 1. Localizar el Menú de Conexión

1. En la parte superior de tu proyecto en Supabase, haz clic en el botón **Connect**.
2. Verás una lista de métodos de conexión.

## 2. Seleccionar el Método de Conexión

| Método | Puerto | Cuándo usarlo |
| :-- | :-- | :-- |
| **Direct connection** | `5432` | Solo funciona en redes con **IPv6**. Muchas redes domésticas y de oficina no lo soportan. |
| **Transaction pooler** | `6543` | Muchas conexiones cortas y simultáneas. Es el que usamos en estas guías para QGIS y pgAdmin. |
| **Session pooler** | `5432` | Alternativa compatible con IPv4 para herramientas que mantienen la conexión abierta. |

> [!TIP]
> Si una herramienta muestra errores como `prepared statement "..." already exists` con el **Transaction pooler**, cambia al **Session pooler** (mismo host, puerto `5432`).

## 3. Parámetros de Conexión Clave

Haz clic en **View parameters** y copia los siguientes datos:

- **Host:** La dirección del servidor (ej. `aws-0-sa-east-1.pooler.supabase.com`).
- **Port:** `6543` (Transaction pooler) o `5432` (Session pooler / conexión directa).
- **Database name:** Generalmente `postgres`.
- **User:** El nombre de usuario (ej. `postgres.xxxxxxx`). Con el pooler, el usuario incluye el identificador del proyecto después del punto.

## 4. Gestión de la Contraseña

- **Seguridad:** Supabase **nunca** mostrará tu contraseña en este panel.
- Debes usar la contraseña que definiste al [crear el proyecto](../01-registro/01-crear-cuenta-y-proyecto.md).
- **¿La olvidaste?** Cámbiala en: `Project Settings` > `Database` > `Reset database password`. Recuerda actualizarla después en todas las herramientas conectadas.

---

### 🚀 Aplicaciones Compatibles

Con estos datos podrás conectar aplicaciones SIG y herramientas de BI como:

- **pgAdmin:** Para administración avanzada de SQL ([siguiente guía](./03-conexion-pgadmin.md)).
- **QGIS:** Para gestión de capas vectoriales ([Datos espaciales](../03-datos-espaciales/02-conexion-qgis.md)).
- **Power BI / Tableau:** Para análisis y tableros ([Conexión con Power BI](../05-power-bi/README.md)).
