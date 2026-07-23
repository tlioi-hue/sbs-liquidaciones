# CLAUDE.md

Instrucciones durables para Claude Code en este repositorio.

## Git: commit y push automáticos

El usuario autorizó de antemano que, después de cada cambio de código realizado por Claude,
se haga automáticamente:

1. `git add` de los archivos modificados (por nombre, nunca `-A`/`.` a ciegas).
2. `git commit` con un mensaje descriptivo.
3. `git push` a `main` — sin pedir confirmación en cada ocasión.

Esta autorización cubre el flujo normal de "hice un cambio, lo subo". Sigue aplicando el
criterio de cautela para cualquier otra operación destructiva o inusual (`--force`,
`reset --hard`, reescritura de historia, borrado de ramas, etc.) — esas SIEMPRE deben
confirmarse con el usuario antes de ejecutarse, esta autorización no las cubre.

Nota: este repo tiene `vercel.json` con rewrites de SPA, lo que sugiere que está conectado
a Vercel con auto-deploy desde `main`. Un push automático probablemente dispara un deploy
a producción. El usuario fue informado de esto y aun así prefirió el flujo automático.
