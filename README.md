# Academia Infra · Ingeniero de Infraestructura y Plataformas

Plataforma de estudio tipo **LMS** para preparar la prueba de **Ingeniero de Infraestructura y Plataformas**.
HTML, CSS y JavaScript puros — sin build, sin dependencias. Se publica en **GitHub Pages**.

🌐 Sitio: `https://jpatehor.github.io/academia-infra-plataformas/`

## Origen del contenido

Generado a partir del archivo **INVENTARIO PRUEBAS INGENIERO DE INFRA PLATAFORMAS.xlsx**:

- **13 temas** · **87 preguntas** · **790 puntos**
- 6 áreas: Infraestructura · Nube · DevOps · Comunicaciones (Redes) · Seguridad · Programación
- Prioridad por tema según el inventario (**Alto / Medio / media / baja**)

| Área | Preg. | Temas |
|---|---|---|
| INFRAESTRUCTURA | 38 | Plataformas, Teoría Linux, Shell, Virtualización |
| NUBE | 15 | AWS, AWS SysOps |
| DEVOPS | 16 | CI, CD, CM, RM |
| PROGRAMACION | 8 | Webservers |
| COMUNICACIONES | 5 | Redes de TI |
| SEGURIDAD | 5 | Seguridad de TI |

## Modos

- **KPIs** — dominio global, dominio por área (barras), racha de días, simulacros.
- **Plan de estudio flexible** — orden oficial por prioridad → puntaje, con casilla *Estudiado*.
- **Práctica por tema** — corrección inmediata con pista y explicación.
- **Simulacro** — las 87 preguntas en orden aleatorio con cronómetro (1 min/pregunta).
- **Repaso de falladas** — se repiten hasta acertarse.

## Datos

`data/questions.json` — esquema:

```json
{
  "meta":   { "titulo": "...", "totalPreguntas": 87, "totalPuntaje": 790 },
  "temas":  [ { "id","area","tema","preguntas","puntaje","prioridad" } ],
  "questions": [ { "id","area","tema","enunciado","opciones":[4],"correcta","pista","explicacion" } ]
}
```

## Avance

Todo el progreso vive en `localStorage` (`academia-infra.v1`). No hay backend ni cuentas.

> Nota: el sitio se sirve por HTTP (GitHub Pages). Si abres `index.html` con `file://`, el navegador bloquea la
> lectura del JSON por CORS; publícalo o sírvelo con un servidor local.
