# 🚀 Guía Completa: Crear tu Portafolio en GitHub

## Paso 1: Crear Cuenta en GitHub (Si no tienes)

1. Ve a https://github.com/signup
2. Usa email profesional (preferiblemente tu nombre)
3. Completa los datos
4. Verifica tu email
5. Crea tu primer repositorio

---

## Paso 2: Crear Repositorio en GitHub

### Opción A: Desde la web (MÁS FÁCIL PARA PRINCIPIANTES)

1. Inicia sesión en https://github.com
2. Haz clic en **"+"** en esquina superior derecha
3. Selecciona **"New repository"**
4. Rellena los datos:

```
Repository name: wine-quality-ml
Description: Machine Learning classification model for wine quality prediction with imbalanced data handling using LightGBM and SMOTE
Public: ✓ Selecciona PUBLIC (para portafolio)
Add a README file: ✗ No (ya tienes README.md)
Add .gitignore: ✗ No (ya tienes .gitignore)
Choose a license: ✗ No (ya tienes LICENSE)
```

5. Haz clic en **"Create repository"**

---

## Paso 3: Configurar Git en Tu Máquina

### 3.1: Instalar Git (Si no tienes)

Descarga desde: https://git-scm.com/download/win

Abre PowerShell como **Administrador** y ejecuta:
```powershell
# Verificar que Git está instalado
git --version
```

### 3.2: Configurar tu Identidad Git

```powershell
# Abre PowerShell en tu carpeta de proyecto
# Luego ejecuta:

git config --global user.name "Tu Nombre"
git config --global user.email "tu_email@ejemplo.com"

# Verificar:
git config --global --list
```

**Ejemplo:**
```powershell
git config --global user.name "Diego García"
git config --global user.email "diego@ejemplo.com"
```

---

## Paso 4: Crear Token de Autenticación (IMPORTANTE)

GitHub ya no acepta contraseña por línea de comandos. Necesitas un **Personal Access Token (PAT)**.

### Crear el Token:

1. Ve a https://github.com/settings/tokens
2. Haz clic en **"Generate new token"** → **"Generate new token (classic)"**
3. Nombre del token: `wine-quality-ml-upload`
4. Selecciona estos permisos (checkboxes):
   - ✓ repo (acceso completo)
   - ✓ workflow
   - ✓ admin:repo_hook
5. Haz clic en **"Generate token"**
6. **COPIA el token** (aparece solo una vez)
7. Guárdalo en un lugar seguro (lo usarás pronto)

---

## Paso 5: Inicializar Git Local y Subir Archivos

Abre **PowerShell** y navega a tu carpeta del proyecto:

```powershell
# Navega a tu carpeta
cd "c:\Users\diego_garciaar\OneDrive - Future It Firm\Documentos\Python\Wine Quality"

# Verifica que estás en el lugar correcto
Get-ChildItem  # Deberías ver tus archivos (.md, .csv, .ipynb, etc.)
```

Luego ejecuta estos comandos (UNO POR UNO):

### 5.1: Inicializar repositorio local

```powershell
git init
```

### 5.2: Agregar todos los archivos

```powershell
git add .
```

Verifica:
```powershell
git status
```

Deberías ver algo como:
```
On branch master
No commits yet

Changes to be committed:
  new file:   .gitignore
  new file:   CHANGELOG.md
  new file:   LICENSE
  new file:   MODELO_DOCUMENTACION.md
  new file:   PORTAFOLIO_GUIDE.md
  new file:   Practica_ML.ipynb
  new file:   README.md
  new file:   RESUMEN_FINAL.md
  new file:   requirements.txt
  new file:   winequality-red.csv
  new file:   wine_model_documentation.json
```

### 5.3: Crear primer commit

```powershell
git commit -m "Initial commit: Complete Wine Quality ML portfolio project"
```

### 5.4: Cambiar rama a main (estándar moderno)

```powershell
git branch -M main
```

### 5.5: Agregar el repositorio remoto

Reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub:

```powershell
git remote add origin https://github.com/TU_USUARIO/wine-quality-ml.git
```

**Ejemplo:**
```powershell
git remote add origin https://github.com/diego-garcia/wine-quality-ml.git
```

### 5.6: Empujar (Push) los archivos a GitHub

```powershell
git push -u origin main
```

**Se abrirá una ventana de autenticación de GitHub:**
- Usuario: Tu usuario de GitHub
- Contraseña: **PEGA EL TOKEN** que copiaste en Paso 4 (no tu contraseña)

---

## Paso 6: Verificar en GitHub

1. Ve a tu repositorio: `https://github.com/TU_USUARIO/wine-quality-ml`
2. Deberías ver:
   - ✓ Todos tus archivos
   - ✓ El README.md renderizado abajo
   - ✓ Verde "main" branch

---

## Paso 7: Mejorar tu Repositorio (Opcional pero Recomendado)

### 7.1: Agregar Topics

En GitHub, ve a **Settings** → **Topics** y añade:
- `machine-learning`
- `wine-quality`
- `lightgbm`
- `smote`
- `python`
- `data-science`
- `classification`

### 7.2: Hacer el README Visible

El README.md ya se ve automáticamente. Verifica que incluya todo.

### 7.3: Agregar Badge de Python

En tu README.md, añade esto al inicio:

```markdown
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)
![Status](https://img.shields.io/badge/Status-Complete-green?style=flat)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)
```

---

## Paso 8: Actualizaciones Futuras (Push/Pull)

Cuando hagas cambios locales:

```powershell
# Ver cambios
git status

# Agregar cambios
git add .

# Commit
git commit -m "Descripción de cambios"

# Push
git push origin main
```

---

## Paso 9: Verificar en GitHub Pages (Portafolio Web)

Si quieres tener el notebook visible en web:

1. Ve a **Settings** → **Pages**
2. Source: Deploy from a branch
3. Branch: **main** → **/(root)**
4. Save

Tu repositorio tendrá URL: `https://TU_USUARIO.github.io/wine-quality-ml`

---

## ✅ Checklist Final

- [ ] Cuenta GitHub creada
- [ ] Repositorio creado en GitHub
- [ ] Git instalado en tu máquina
- [ ] Git configurado (user.name, user.email)
- [ ] Token creado y guardado
- [ ] Archivos inicializados (git init)
- [ ] Archivos agregados (git add .)
- [ ] Primer commit hecho (git commit)
- [ ] Rama renombrada a main (git branch -M main)
- [ ] Remote añadido (git remote add origin)
- [ ] Push completado (git push -u origin main)
- [ ] Verificado en GitHub
- [ ] Topics agregados
- [ ] README visible
- [ ] GitHub Pages configurado (opcional)

---

## 🔧 Troubleshooting

### Error: "fatal: not a git repository"
```powershell
# Asegúrate de estar en la carpeta correcta
Set-Location "c:\Users\diego_garciaar\OneDrive - Future It Firm\Documentos\Python\Wine Quality"
git init
```

### Error: "permission denied" o "authentication failed"
- Verifica que usaste el TOKEN (no contraseña)
- Verifica que el TOKEN tiene permisos de "repo"
- Crea un nuevo TOKEN si no funciona

### Error: "remote origin already exists"
```powershell
git remote remove origin
git remote add origin https://github.com/TU_USUARIO/wine-quality-ml.git
```

### Error: "branch main not found"
```powershell
git branch -M main
git push -u origin main
```

---

## 🎯 Siguientes Pasos Después de GitHub

Una vez que subas a GitHub:

1. **Actualiza LinkedIn**
   - Añade el link a tu portafolio
   - Escribe post sobre el proyecto

2. **Crea tu Portafolio Web**
   - GitHub Pages te da uno gratis
   - O usa template profesional

3. **Comienza a Aplicar**
   - Usa PORTAFOLIO_GUIDE.md
   - Incluye link a GitHub en tu CV

4. **Continúa Aprendiendo**
   - Segundo proyecto (diferente tipo)
   - Open source contributions
   - Certificaciones

---

## 📞 Comandos Rápidos de Referencia

```powershell
# Estado actual
git status

# Ver commits
git log

# Ver ramas
git branch -a

# Cambiar rama
git checkout nombre-rama

# Crear rama nueva
git checkout -b nueva-rama

# Ver cambios
git diff

# Deshacer cambios locales
git restore nombre-archivo

# Ver URL remota
git remote -v
```

---

**Última edición**: 6 de Diciembre, 2025
**Para**: Tu Portafolio ML
**Estado**: 🟢 Listo para usar
