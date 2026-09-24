# ☁️ Guía: Crear Cuenta y Proyecto en Supabase

[« Índice de la sección](./README.md) | [Siguiente: Credenciales de API »](../02-configuracion-basica/01-credenciales-api.md)

---

Esta guía detalla los pasos para crear una cuenta en **Supabase** y aprovisionar tu primera base de datos **PostgreSQL** en la nube.

## 1. Introducción

Supabase ofrece una base de datos PostgreSQL administrada, junto con una API generada automáticamente, autenticación y almacenamiento de archivos. Su plan gratuito es ideal para proyectos de aprendizaje y prototipos.

## 2. Registro y Verificación

1. Accede al sitio oficial: [supabase.com](https://supabase.com).
2. Haz clic en **Sign Up** o **Login**.
3. Regístrate con tu correo electrónico (o con tu cuenta de GitHub).
4. **Crítico:** Revisa tu bandeja de entrada y confirma tu correo haciendo clic en el enlace de **Confirm email address**.

## 3. Configuración de la Organización

Tras verificar tu cuenta, el sistema te pedirá crear una organización:

- **Nombre:** Elige un nombre representativo (ej. `Proyecto Geoportal`).
- **Tipo:** Selecciona `Personal`.
- **Plan:** Elige el **Plan Gratuito (Free)**.

![Creación de Proyecto en Supabase](./img/01-creacion-proyecto.png)
_Figura 1: Interfaz de creación de proyecto en Supabase._

> [!WARNING]
> En el plan gratuito, si la base de datos no tiene actividad durante **7 días**, Supabase la pausará. Deberás entrar al panel para reactivarla manualmente.

## 4. Creación del Proyecto

Configura los detalles técnicos de tu base de datos:

1. **Nombre del Proyecto:** Por ejemplo, `Geoportal`.
2. **Contraseña de la Base de Datos:**
   - **Importante:** Asigna una contraseña robusta y **guárdala inmediatamente**. La necesitarás para conectar herramientas externas como pgAdmin, QGIS o Power BI.
3. **Región:** Selecciona el servidor más cercano a tu ubicación para reducir la latencia (ej. `South America (São Paulo)` o `East US`).
4. Haz clic en **Create new project**.

---

### Resultado Esperado

Una vez finalizado el aprovisionamiento (puede tardar un par de minutos), tendrás una instancia de PostgreSQL lista para configurar.
