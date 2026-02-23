# 📘 DAM M10 – Sistemes de Gestió Empresarial  
## Desarrollo e implantación de módulos en Odoo

**Ciclo:** DAM2 – Desarrollo de Aplicaciones Multiplataforma  
**Centro:** Ilerna  
**Asignatura:** M10 – Sistemes de Gestió Empresarial  

---

## 📌 Descripción

Este repositorio recoge el trabajo realizado durante la asignatura **Sistemes de Gestió Empresarial**, donde se ha trabajado la implantación y personalización de un ERP utilizando **Odoo** como plataforma principal.

El objetivo de la asignatura ha sido comprender cómo se estructura, desarrolla e implanta un sistema ERP en una empresa, aplicando conceptos de:

- Modelado de datos  
- Arquitectura MVC  
- Desarrollo modular  
- Seguridad y control de accesos  
- Personalización de vistas  
- Exposición de datos mediante controladores web  

Este repositorio documenta los avances prácticos realizados a través de distintos laboratorios progresivos.

---

## 🛠 Tecnologías utilizadas

- Odoo (v18)  
- Python  
- XML (vistas y configuración)  
- PostgreSQL  
- Docker & Docker Compose  
- Arquitectura MVC de Odoo  

---

# 🏗 Estructura del módulo desarrollado

```text
school/
│
├── __init__.py
├── __manifest__.py
│
├── models/
│   └── models.py
│
├── views/
│   └── views.xml
│
├── security/
│   └── ir.model.access.csv
│
└── controllers/
    └── controllers.py
```

---

# 📚 Competencias trabajadas

Durante el desarrollo de los laboratorios se han trabajado las siguientes competencias técnicas:

---

## 🔹 1. Modelado de datos en Odoo

- Creación de modelos personalizados (`models.Model`)
- Definición de campos:
  - `Char`
  - `Date`
  - `Boolean`
  - `Selection`
  - `Text`
- Relaciones:
  - `Many2one`
  - `One2many`
  - `Many2many`
- Restricciones SQL
- Campos calculados con `@api.depends`

**Ejemplo aplicado:**

Cálculo automático de la edad a partir de la fecha de nacimiento.

---

## 🔹 2. Diseño de vistas (XML)

Implementación de:

- Vista Lista (`<list>`)
- Vista Formulario (`<form>`)
- Vista Calendario (`<calendar>`)
- Vista Búsqueda (`<search>`)

Incluyendo:

- Agrupaciones dinámicas  
- Filtros personalizados  
- Organización con `<sheet>`, `<group>`, `<notebook>`  
- Uso de `widget="badge"` y `many2many_tags`  

---

## 🔹 3. Seguridad y control de accesos

- Configuración de `ir.model.access.csv`
- Gestión de permisos por grupo
- Control de:
  - Lectura  
  - Escritura  
  - Creación  
  - Eliminación  

---

## 🔹 4. Personalización del comportamiento del modelo

- Sobrescritura del método `name_get()`
- Eliminación del campo `name` en `school.event`
- Generación dinámica del nombre visible de los registros

**Ejemplo:**

```text
Tipo - Clase
```

---

## 🔹 5. Desarrollo de controladores HTTP

Creación de rutas web personalizadas mediante:

```python
@http.route('/school/events/', auth='public', website=True)
```

Funcionalidades implementadas:

- Acceso público  
- Consulta de registros mediante `request.env`  
- Uso de `sudo()`  
- Devolución de respuesta HTML simple  

Esto permite exponer datos del ERP vía navegador:

```text
http://localhost:8069/school/events/
```

---

# 🧠 Objetivos de aprendizaje alcanzados

- ✔ Comprensión de la arquitectura interna de Odoo  
- ✔ Desarrollo modular sobre un ERP real  
- ✔ Manipulación del ORM de Odoo  
- ✔ Personalización de interfaz  
- ✔ Gestión de seguridad  
- ✔ Exposición de datos mediante controladores  

---

# 🚀 Instalación del módulo

1. Clonar el repositorio.  
2. Copiar el módulo dentro de la carpeta `addons`.  
3. Reiniciar el servidor Odoo.  
4. Activar modo desarrollador.  
5. Actualizar lista de aplicaciones.  
6. Instalar el módulo.  

---

# 📈 Evolución del proyecto

El proyecto se ha desarrollado de forma progresiva a través de laboratorios numerados, permitiendo una evolución desde:

- Comprensión básica del ERP  
- Creación de modelos simples  
- Diseño de vistas  
- Gestión de permisos  
- Implementación de lógica calculada  
- Creación de endpoints web  

Este repositorio refleja el crecimiento técnico en el desarrollo sobre Odoo.

---

# 💼 Enfoque profesional

Aunque se trata de un entorno académico, el desarrollo se ha realizado aplicando buenas prácticas:

- Estructura modular limpia  
- Separación clara entre modelos, vistas y controladores  
- Código legible y mantenible  
- Uso correcto del ORM  
- Uso adecuado de decoradores y dependencias  

El objetivo ha sido no solo cumplir con los laboratorios, sino desarrollar una base sólida en personalización de sistemas ERP empresariales.

---

# 📌 Conclusión

La asignatura **M10 – Sistemes de Gestió Empresarial** ha permitido adquirir experiencia práctica en la implantación y personalización de un ERP real, comprendiendo tanto su estructura interna como su aplicación en un entorno empresarial.

El desarrollo sobre Odoo proporciona una visión directa de cómo funcionan los sistemas de gestión utilizados en empresas reales.
