# DGL Data Talent · ERP

Sistema ERP interno para gestión de búsquedas ejecutivas especializadas en datos, privacidad e IA — Data Governance Latam.

## Stack
- HTML + CSS + JS puro (sin frameworks, sin build step)
- Persistencia: `localStorage` (client-side, sin backend)
- Deploy: Vercel como sitio estático

## Módulos
| Tab | Descripción |
|-----|-------------|
| **Dashboard** | KPIs generales: candidatos, clientes, posiciones, score promedio |
| **Candidatos** | Base de candidatos evaluados con filtros y detalle |
| **Clientes** | Empresas clientes activas y potenciales |
| **Posiciones** | Búsquedas abiertas, en proceso o cerradas |
| **Evaluación** | Formulario de feedback de entrevistas con análisis IA |

## Archivos
- `index.html` — App principal (single-page, todos los módulos)
- `vercel.json` — Configuración de deploy estático
- `dgl-platform.html` — Versión anterior Sales CRM (archivo histórico)
- `CLAUDE.md` — Este archivo

## Deploy
Push a `main` en GitHub → Vercel auto-despliega en https://proyecto-dgl.vercel.app/

## Claves localStorage
```
dgl_cands_v2      — candidatos evaluados
dgl_clients_v1    — empresas clientes
dgl_positions_v1  — posiciones abiertas
```

## AI Feature
El botón "Analizar con IA" llama a `api.anthropic.com/v1/messages` directamente.
**Para producción:** mover a un endpoint serverless (Vercel Function) para no exponer la API key en el frontend.

## Personas del equipo
- Sofía Mónaco (Directora)
- Daniel Monastersky
- Facundo Malaureille
- Pablo Mlynkiewicz
