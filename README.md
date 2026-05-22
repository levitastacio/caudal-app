# 💰 Caudal — Finance Dashboard

App web de finanzas personales que se conecta a tu Google Sheet (alimentado por Google Apps Script que lee Gmail).

## Características

- 📊 Gráficas de gastos por categoría
- 🏦 Sincronización automática de transacciones bancarias vía Gmail
- 📱 Responsive - funciona en desktop, tablet y celular
- ➕ Agrega transacciones manualmente
- 🔐 Datos privados - todo corre en tu navegador + tu Google Drive

## Instalación rápida

1. **Configura el backend** (Google Apps Script):
   - Ve a `../caudal-apps-script/GUIA-INSTALACION.md`
   - Sigue los 4 pasos para crear el Sheet y el script de sincronización

2. **Abre esta app**:
   - Si ya está deployada en Netlify: abre la URL que se te proporcione
   - Localmente: abre `index.html` en tu navegador

3. **Conecta tu Sheet**:
   - Click en **⚙️ Conectar Sheet** (arriba a la derecha)
   - Pega la URL CSV de tu Google Sheet (obtenida en PASO 3 de la guía)
   - Click en **Conectar y sincronizar**

## Stack técnico

- **Frontend:** HTML5 + CSS3 + Vanilla JavaScript
- **Datos:** Google Sheets (CSV publicado)
- **Backend:** Google Apps Script (lee Gmail automáticamente)
- **Hosting:** Netlify (static)

## Estructura de archivos

```
caudal-app/
├── index.html      # Aplicación web (UI + lógica)
├── netlify.toml    # Configuración de Netlify
├── .gitignore      # Archivos a ignorar en git
└── README.md       # Esta documentación
```

## Para deployar manualmente

Si está en un repo git:

```bash
netlify deploy --prod --dir=.
```

O desde la raíz del proyecto:

```bash
./deploy.sh
```

## Troubleshooting

**"Error: No se puede conectar al Sheet"**
- Confirma que la URL termina en `output=csv`
- Verifica que el Sheet esté publicado en Google Drive

**"No aparecen transacciones"**
- Abre el Google Sheet directamente y verifica que tenga datos
- Revisa que el Apps Script se haya ejecutado (ve a Ejecuciones en script.google.com)

**"Me veo transacciones duplicadas"**
- A veces ocurre en las primeras sincronizaciones
- Puedes borrar filas directamente en el Sheet o desde la app

## Licencia

MIT — úsalo libremente.

## Preguntas o mejoras

Este es un proyecto en desarrollo. Para cambios o bug reports, contacta al desarrollador.
