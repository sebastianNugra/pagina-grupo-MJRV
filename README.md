# Página del Equipo N

Mini web estática donde cada integrante presenta su propia sección. Es el proyecto de la práctica de **Git, GitHub, Tailscale y Gitea**: lo construimos primero en GitHub y luego en un servidor Gitea propio. El foco está en aprender Git, no en el código.

## Integrantes y roles

| # | Nombre | Rol | Archivo |
|---|--------|-----|---------|
| 1 | Sebastian Nugra | Líder | `sebastian.html` |
| 2 | Jefferson Farez | Anfitrión del servidor | `jefferson.html` |
| 3 | Andres Buestan | Documentador | `andres.html` |
| 4 | Damian Guiñansaca | Revisor | `damian.html` |

## Estructura del proyecto

```
pagina-grupo-MJRV/
├── index.html        # Página principal con la lista de integrantes
├── sebastian.html    # Sección de Sebastian Nugra (Líder)
├── jefferson.html    # Sección de Jefferson Farez (Anfitrión)
├── andres.html       # Sección de Andres Buestan (Documentador)
├── damian.html       # Sección de Damian Guiñansaca (Revisor)
├── LICENSE
└── README.md
```

## Cómo empezar

1. Clona el repositorio:
   ```bash
   git clone https://github.com/sebastianNugra/pagina-grupo-MJRV.git
   cd pagina-grupo-MJRV
   ```
2. Abre `index.html` en tu navegador para ver la página.

## Flujo de trabajo

Nadie hace push directo a `main`. Cada tarea sigue este camino:

**Issue → Rama → Commits → Push → Pull Request → Revisión → Merge**

1. Trae lo último de `main`:
   ```bash
   git switch main
   git pull
   ```
2. Crea tu rama:
   ```bash
   git switch -c feature/seccion-tunombre
   ```
3. Trabaja, revisa y guarda cambios (commits convencionales):
   ```bash
   git status
   git diff
   git add archivo.html
   git commit -m "feat: add Jefferson's section"
   ```
4. Sube la rama y abre un Pull Request en GitHub:
   ```bash
   git push -u origin feature/seccion-tunombre
   ```
5. Un compañero revisa (mínimo un comentario) y aprueba. El Líder fusiona.

### Convenciones

- **Ramas:** `feature/<descripcion-corta>`, por ejemplo `feature/seccion-ana`.
- **Commits:** pequeños y en Conventional Commits, en inglés (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`). Evitar mensajes como "cambios".
- **Pull Requests:** enlazar el Issue con `Closes #N` en la descripción.
- **Revisión cruzada:** 1→2, 2→3, 3→4, 4→1.
- **Nunca subir:** contraseñas, tokens, archivos `.env` ni carpetas como `node_modules`.

## Progreso de la práctica

**Parte A: GitHub**
- [ ] Repositorio creado y colaboradores invitados
- [ ] Rama `main` protegida (PR + 1 aprobación)
- [ ] 4 Issues creados y asignados
- [ ] Estructura base fusionada
- [ ] 4 secciones fusionadas mediante PR
- [ ] Conflicto provocado y resuelto
- [ ] Historia verificada con `git log --oneline --graph --all`

**Parte B: Tailscale**
- [ ] Tailnet creada por el Anfitrión
- [ ] Los 4 integrantes conectados
- [ ] Ping exitoso al Anfitrión

**Parte C: Gitea**
- [ ] Gitea instalado y configurado con la IP de Tailscale
- [ ] Cuentas creadas y organización `equipo-MJRV`
- [ ] Repositorio vacío creado

**Parte D: Trabajo en Gitea**
- [ ] Remoto `gitea` añadido por los 4
- [ ] Historia de GitHub subida a Gitea
- [ ] 4 PR fusionados en Gitea
- [ ] Prueba de desconexión realizada

## Licencia

Este proyecto se distribuye bajo la licencia [MIT](LICENSE).