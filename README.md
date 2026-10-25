# AlquilER · Dashboard de Proyecto

Tablero de control del proyecto **AlquilER** (alquiler de propiedades) al 25/10/2026.
Entregable de la *Actividad Práctica: Diseño del Dashboard* (página 8).

## Contenido

- `index.html` — tablero autocontenido (HTML + CSS + JS inline, sin dependencias).
- `AlquilER-Dashboard.pdf` — versión imprimible en A4 (9 páginas).

## Secciones

1. Resumen ejecutivo y veredicto.
2. 5 KPIs con fórmula, meta, fuente y decisión: alcance MVP, cobertura backend, velocidad de integración, defectos abiertos, cobertura E2E.
3. Evolución semana a semana (commits apilados + curva acumulada).
4. Sprints S0–S3 y código del proyecto.
5. Equipo y ritmo (participación por autor + histograma de horas).
6. Trazabilidad: 22 commits clave con hash, fecha, repo y autor.
7. Riesgos y decisiones.
8. Metodología, fuentes y comandos de reproducción.
9. Entrega: link de funcionamiento y pasos de publicación.

## Datos reales utilizados

- Período: 11/08/2026 → 23/10/2026 (74 días, 10,6 semanas).
- Commits del período: 762 (405 backend · 201 web · 156 mobile).
- 31 PRs mergeados, 0 abiertos; 3 issues, todos cerrados (promedio 63,5 h).
- 2.127 pruebas automatizadas; cobertura backend 97,83 % líneas (9.714/9.929), 98,71 % métodos, 95,10 % clases.
- Autores: Julián Pretz 385 commits (50,5 %), Mariano Fernández 377 (49,5 %).
- Deploy: https://alquilerr.alwaysdata.net · API health: https://alquiler.alwaysdata.net/api/health (200 OK).

## Publicación (link público)

Opción A — GitHub Pages (recomendada, gratis):

1. Crear repo `alquiler-dashboard` en GitHub.
2. Subir `index.html` (y opcionalmente el PDF) a la rama `main`.
3. Settings → Pages → Source: `main` / root.
4. URL resultante: `https://<usuario>.github.io/alquiler-dashboard/`.

Opción B — Netlify Drop (sin cuenta):

1. Ir a https://app.netlify.com/drop.
2. Arrastrar la carpeta `AlquilER-dashboard`.
3. URL instantánea tipo `https://<nombre>.netlify.app`.

Opción C — alwaysdata (ya usado por el proyecto):

Subir `index.html` a `~/www/` del hosting `alquilerr.alwaysdata.net`.

## Regenerar el PDF

Servir la carpeta y usar Edge/Chrome headless:

```powershell
# servidor local
python -m http.server 8765 --directory "C:\Users\Julip\Desktop\AlquilER-dashboard"

# PDF
"C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" `
  --headless=new --disable-gpu `
  --print-to-pdf="C:\Users\Julip\Desktop\AlquilER-dashboard\AlquilER-Dashboard.pdf" `
  --print-to-pdf-no-header --virtual-time-budget=6000 `
  "http://localhost:8765/index.html"
```

## Script de presentación (5 minutos)

1. **0:00–0:30** — Portada: "AlquilER, en una sola pantalla. 74 días, 762 commits, 31 PRs, 2.127 pruebas."
2. **0:30–1:30** — KPIs: 5 indicadores, 4 en meta y 1 en atención (E2E 50 %). Veredicto: MVP completo, listo para defender, no para producción.
3. **1:30–2:30** — Evolución: dos picos (W37–W38 refactor, W41 integración), cierre intenso en W43, ritmo sostenido 69 commits/semana.
4. **2:30–3:30** — Sprints S0→S3: contrato → núcleo → producto → calidad. 74 días, 4 releases internos.
5. **3:30–4:15** — Equipo: carga repartida 50,5/49,5, pero conocimiento concentrado; casi la mitad del trabajo después de las 20:00.
6. **4:15–4:45** — Trazabilidad: 22 commits clave con hash y fecha; riesgos R-01 a R-05 con mitigación y fecha objetivo.
7. **4:45–5:00** — Cierre: link público, PDF, metodología reproducible y próximos pasos (CI/CD, E2E, monitoreo).
