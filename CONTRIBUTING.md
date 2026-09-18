# Cómo contribuir

Este documento define el flujo de trabajo del equipo para todo cambio en el repositorio. Corresponde a la historia `HUT1`.

## Estrategia de ramas

Trabajamos con trunk based. `main` es la única rama de larga vida y siempre debe quedar en un estado demostrable.

Cada historia se resuelve en una rama corta que sale de `main` y vuelve a `main` por pull request.

Formato del nombre

`<id-historia>-<descripcion-corta>`

Ejemplos

- `hu1-registrar-tratamiento`
- `hut2-arquitectura-modelo-de-datos`
- `hut13-app-web-ingreso`

Reglas

- El identificador va en minúsculas, por ejemplo `hu1`.
- La descripción usa minúsculas y guiones medios entre palabras.
- Una rama atiende una sola historia.
- La rama se elimina después de fusionar el pull request.

No hay protecciones de rama. Todo integrante puede fusionar su propio pull request. La revisión de un par es recomendada y no bloqueante.

## Mensajes de commit

Formato

`tipo: descripción`

Tipos

- `feat` para funcionalidad nueva.
- `fix` para corrección de errores.
- `docs` para documentación.
- `test` para pruebas.
- `refactor` para cambios internos sin cambio de comportamiento.
- `chore` para mantenimiento, plantillas y configuración.

Reglas

- La descripción va en minúsculas, en español y en presente.
- La primera línea no supera 72 caracteres.
- Cada commit resuelve un cambio concreto.

Ejemplos

- `docs: convencion de ramas y mensajes de commit`
- `feat: registro de tratamiento de un paciente`
- `fix: recalculo de dosis futuras al editar un tratamiento`

## Pull requests

- Todo cambio entra a `main` por pull request.
- Se usa la plantilla `.github/pull_request_template.md`.
- El campo "Como se verifico" es obligatorio.
- El cuerpo cierra la historia con `Closes #<numero>`.
- La revisión de un par es recomendada. El autor puede fusionar su pull request.
- Antes de fusionar se verifica la Definition of Done de `README.md`.

## Issues

- Toda historia nueva se crea con la plantilla `.github/ISSUE_TEMPLATE/historia-de-usuario.yml`.
- La plantilla pide historia, criterios de aceptación, prioridad MoSCoW, estimación, dependencias y Definition of Ready.
- El issue mantiene la versión vigente de la historia. `docs/product-backlog.md` la resume.

## Tablero

El trabajo se sigue en el GitHub Project 1 "Vision Care · Product Backlog". Las columnas del campo Status son Backlog, Ready, In Progress, In Review, QA / Testing, Blocked y Done.

Reglas de uso

- Una persona mantiene como máximo una historia en In Progress.
- Una historia pasa a In Review cuando el pull request está abierto.
- Una historia pasa a Done cuando cumple la Definition of Done y el Product Owner la acepta.

## Definition of Done

Está publicada en `README.md` y en `docs/product-backlog.md`.
