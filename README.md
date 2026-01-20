# 📂 Estructura de Datos (JSON Portfolio)

Este repositorio contiene la información dinámica para el portafolio personal. Los datos están organizados en archivos JSON y se sirven mediante GitHub Raw.

## 📌 Reglas Generales

* **Idioma**: Cada archivo debe tener un sufijo de idioma: `_es.json` para español y `_en.json` para inglés.
* **Formato de Fechas**: Se recomienda usar el formato `"Mes Año"` (ej. `"Enero 2024"`) o simplemente el año como string.

---

## 🛠 Estructuras de los Archivos

### 1. Información Personal (`about_{lang}.json`)

Contiene los datos principales, redes sociales, educación y stack tecnológico.

```json
{
  "name": "Nombre Completo",
  "role": "Título profesional",
  "exp": "Años de experiencia (ej: '1.5')",
  "image": "URL de la foto de perfil",
  "education": {
    "center": "Nombre de la institución",
    "title": "Título obtenido",
    "location": "Ciudad, País",
    "date": { "start": "2020", "end": "2023" },
    "description": "Breve resumen de la formación"
  },
  "languages": ["Idioma 1", "Idioma 2"],
  "phone": "Número de contacto",
  "location": "Ubicación actual",
  "professionalAboutMe": "Bio corta con HTML permitido (ej: <strong>React</strong>)",
  "largeAboutMe": ["Párrafo 1 de la bio larga", "Párrafo 2..."],
  "shortAboutMe": ["Frase impactante 1", "Frase impactante 2"],
  "technologies": {
    "frontend": ["React", "Next.js"],
    "backend": ["Node.js", "Supabase"],
    "devops": ["Git", "Docker"]
  },
  "social": {
    "github": "URL",
    "linkedin": "URL",
    "email": "correo@ejemplo.com"
  }
}

```

### 2. Experiencia Laboral (`job_experience_{lang}.json`)

Define la trayectoria profesional en empresas o como freelance. Se renderiza en una línea de tiempo.

```json
[
  {
    "company": "Nombre de la Empresa",
    "role": "Tu cargo",
    "date": {
      "start": "Mes Año",
      "end": "Mes Año o Presente"
    },
    "description": "Descripción de logros y responsabilidades.",
    "technologies": ["Tecnología 1", "Tecnología 2"],
    "location": "Remoto / Presencial",
    "link": "URL opcional de la empresa"
  }
]

```

### 3. Proyectos / Portafolio (`experience_{lang}.json`)

Lista de proyectos realizados con sus respectivos enlaces a código y demo.

```json
[
  {
    "name": "Nombre del Proyecto",
    "slug": "nombre-del-proyecto-url",
    "description": "Resumen breve del proyecto.",
    "advancedDescription": [
      "Punto clave 1",
      "Punto clave 2"
    ],
    "technologies": ["React", "Tailwind CSS"],
    "links": {
      "code": "URL de GitHub o null",
      "demo": "URL de la Live Demo o null"
    },
    "image": "URL de la imagen/mockup",
    "role": "Tu rol en el proyecto",
    "date": { "start": "2024", "end": "2024" }
  }
]

```

---

## 🚀 Cómo actualizar los datos

1. Edita el archivo correspondiente en este repositorio.
2. Realiza el **Commit** de los cambios.
3. La web se actualizará automáticamente en la siguiente carga (gracias al SSR) o cuando expire la caché del CDN de GitHub.

> [!IMPORTANT]
> Asegúrate de no dejar comas sueltas al final de los arrays u objetos, ya que esto invalidará el JSON y el servicio activará el modo de "datos por defecto" (vacío).
