# GitHub Deployment Workflow

Este proyecto demuestra cómo usar GitHub Actions para implementar un flujo de trabajo de CI/CD básico.

El objetivo es desplegar automáticamente un sitio web estático a GitHub Pages **solo cuando se modifica el archivo `index.html`** en la rama `main`.

---

## 🛠️ Tecnologías utilizadas

- [GitHub Actions](https://docs.github.com/actions)
- [GitHub Pages](https://pages.github.com/)
- HTML (sitio estático)

---

## 🚀 ¿Cómo funciona?

El repositorio contiene un archivo `index.html` simple con contenido estático.

Se utiliza un archivo de workflow en `.github/workflows/deploy.yml` que:
- Se activa solo con `git push` a la rama `main`
- Solo si se modificó `index.html`
- Usa la acción `peaceiris/actions-gh-pages` para desplegar el sitio a la rama `gh-pages`

Una vez desplegado, el sitio es accesible en:

📎 https://athaly.github.io/gh-deployment-workflow/

---

## 📂 Estructura del repositorio

gh-deployment-workflow/
├── .github/

│ └── workflows/

│ └── deploy.yml

├── index.html

└── README.md

---

## ✅ Resultado

Cada vez que se modifica `index.html` y se hace `git push` a `main`, GitHub Actions ejecuta automáticamente el workflow y actualiza el sitio en GitHub Pages.

