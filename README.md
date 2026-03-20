# Protocolo Fortaleza v2.0

Sistema de Capacitacion NRD-2 para CONRED / IGSS.

## Como subir a GitHub Pages

### Paso 1: Crear repositorio
1. Ve a github.com y crea una cuenta (o inicia sesion)
2. Haz clic en "New Repository"
3. Nombre: `protocolo-fortaleza`
4. Selecciona "Public"
5. Clic en "Create Repository"

### Paso 2: Subir archivos
1. En tu repositorio nuevo, haz clic en "uploading an existing file"
2. Arrastra TODOS los archivos .html y .md de esta carpeta
3. Clic en "Commit changes"

### Paso 3: Activar GitHub Pages
1. Ve a Settings > Pages
2. En "Source" selecciona "Deploy from a branch"
3. En "Branch" selecciona "main" y carpeta "/ (root)"
4. Clic en "Save"
5. Tu sitio estara en: `https://TU-USUARIO.github.io/protocolo-fortaleza/`

### Como modificar una fase sin afectar las demas
- Cada fase es un archivo independiente (fase-1.html, fase-2.html, etc.)
- Edita SOLO el archivo de la fase que necesitas cambiar
- Sube ese archivo individual a GitHub
- Las demas fases NO se ven afectadas

## Estructura de archivos
```
index.html      -> Portal principal (dashboard)
fase-1.html     -> Fase 1: Diagnostico de Amenazas
fase-2.html     -> Fase 2: Arquitectura de Respuesta
fase-3.html     -> Fase 3: Ingenieria de Seguridad (NRD-2)
fase-4.html     -> Fase 4: Gestion Final y Certificacion
README.md       -> Este archivo
MARCO-PEDAGOGICO.md -> Fundamentos cientificos
```

## Codigos de acceso
Los codigos validos son: 2025, CONRED, NRD2, FORTALEZA
(Puedes cambiarlos en el archivo index.html, busca VALID_CODES)
