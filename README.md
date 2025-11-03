# Aula Conecta — Repositorio Educativo
Plataforma formativa para organizar, publicar y evaluar **Recursos Educativos Digitales (RED)**: documentos, imágenes, videos y actividades con rúbricas y control de entregas.

## Propósito
Centralizar materiales, facilitar entregas de estudiantes y evaluación por parte de docentes, con gestión de roles y metadatos.

## Alcance
- **Institución:** Instituto Técnico-Formativo “San Martín”
- **Área de ejemplo:** Ciencias Sociales · Historia
- **Niveles/etiquetas:** adaptable a básica primaria, secundaria y superior

## Roles y permisos (resumen)
- **Administrador:** cuentas, políticas, estructura, reportes
- **Docente:** crea recursos y tareas, plazos, rúbricas, califica
- **Alumno:** accede a recursos, entrega tareas, ve retro y notas
- **Invitado (opcional):** acceso a materiales públicos

## Tipos de recurso
PDF, DOCX, PPTX, JPG, PNG, SVG, MP4. Metadatos: título, autor, fecha, palabras clave, licencia, idioma, grado, asignatura, tema.

## Estructura sugerida
```
/SanMartin/Secundaria/3ro/Historia/Imperio_Romano
  ├─ recursos
  ├─ tareas
  └─ evaluaciones
```

## Flujo docente (carga de recursos)
1. Inicia sesión → selecciona curso
2. Navega a tema → **Subir recurso**
3. Completa metadatos → **Subir**
4. (Opcional) **Notificar** estudiantes

## Flujo alumno (entrega de tarea)
1. Inicia sesión → Tareas
2. Revisa instrucciones y rúbrica
3. Sube archivo(s) o enlace
4. Confirma entrega (se registra fecha/hora)

## Demo mínima incluida
- **/src/frontend**: prototipo HTML/JS para listar recursos desde `/src/data/resources.json`.
- **/src/data/metadata-schema.json**: esquema de metadatos.
- **/docs**: lineamientos, roles y permisos, políticas, wireframes.
- **/resources/ejemplos**: place-holders.

## Cómo ejecutar el prototipo (estático)
Sin dependencias: abre `src/frontend/index.html` en tu navegador o sirve el folder con un servidor simple:
```bash
# Opción 1: Python 3
python -m http.server 8000 -d src/frontend
# Opción 2: Node (si lo tienes)
npx http-server src/frontend -p 8000
```
Luego visita http://localhost:8000

## Cómo subir esto a GitHub (línea de comandos)
```bash
git init
git add .
git commit -m "Aula Conecta: scaffold inicial"
git branch -M main
# crea el repo vacío en GitHub y copia su URL, por ej.:
git remote add origin https://github.com/TU-USUARIO/aula-conecta.git
git push -u origin main
```

## Licencia
MIT
