# 🔷 Pionex Trading Terminal

Terminal de trading profesional para **Pionex** construida en HTML/JS puro. Funciona directamente en **GitHub Pages** sin backend ni instalación.

![Terminal Preview](https://img.shields.io/badge/Pionex-Terminal-00e5a0?style=for-the-badge)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Ready-blue?style=for-the-badge)

---

## 🚀 Deploy en GitHub Pages (5 minutos)

### Paso 1 — Crear repositorio
1. Ve a [github.com/new](https://github.com/new)
2. Nombre: `pionex-terminal` (o el que quieras)
3. Visibilidad: **Public**
4. Click **"Create repository"**

### Paso 2 — Subir archivos
1. En tu repositorio vacío, click **"uploading an existing file"**
2. Sube `index.html` (renombra `pionex-app.html` → `index.html`)
3. Opcionalmente sube este `README.md`
4. Click **"Commit changes"**

### Paso 3 — Activar GitHub Pages
1. Ve a **Settings** → **Pages**
2. En *Source* selecciona **"Deploy from a branch"**
3. Branch: **main** / Folder: **/ (root)**
4. Click **Save**

### Paso 4 — Acceder
En ~60 segundos tu terminal estará en:
```
https://TU-USUARIO.github.io/pionex-terminal
```

---

## ⚙️ Solución CORS integrada

La app incluye **3 modos de proxy CORS** seleccionables desde la interfaz:

| Proxy | URL | Notas |
|-------|-----|-------|
| **corsproxy.io** ✅ | `corsproxy.io` | Recomendado. Gratuito, sin registro |
| **allorigins.win** | `allorigins.win` | Alternativa si el primero falla |
| **Directo** | Sin proxy | Solo para entornos locales sin restricciones |

> El proxy **corsproxy.io** está seleccionado por defecto y funciona en GitHub Pages.

---

## ✨ Funcionalidades

### 📊 Datos de Mercado (sin API key)
- ✅ Lista de todos los pares SPOT de Pionex
- ✅ Ticker en tiempo real (strip animado)
- ✅ Gráfico de precios con área + volumen (100 velas)
- ✅ Intervalos: 1m, 5m, 15m, 1H, 4H, 1D, 1W
- ✅ Order book con profundidad visual y spread
- ✅ Trades recientes del par seleccionado
- ✅ Estadísticas 24h: máx, mín, volumen, quote vol

### 🔐 Trading y Cuenta (requiere API key)
- ✅ Autenticación con HMAC-SHA256 (estándar Pionex)
- ✅ Balances de cuenta por moneda
- ✅ Órdenes abiertas con cancelación
- ✅ Historial de órdenes cerradas
- ✅ Formulario compra/venta: LIMIT y MARKET
- ✅ Conexión WebSocket para feed en vivo

---

## 🔑 Cómo obtener tu API Key de Pionex

1. Inicia sesión en [pionex.com](https://www.pionex.com)
2. Ve a **Perfil** → **API Management**
3. Click **"Create API Key"**
4. Activa: **Read** + **Trade** (no actives Withdraw)
5. Añade tu IP o usa **"No IP Restriction"** para pruebas
6. Guarda la Key y el Secret en lugar seguro

> ⚠️ **Nunca compartas tu API Secret.** Esta app procesa todo en tu navegador; ningún dato sale a terceros salvo las llamadas directas a la API de Pionex.

---

## 🛡️ Seguridad

- Todo el código es **client-side** (HTML + JS puro)
- El signing HMAC-SHA256 ocurre en tu navegador
- Los proxies CORS solo reenvían la petición, no almacenan datos
- Código 100% auditable (un solo archivo `index.html`)

---

## 🛠️ Uso local (sin GitHub Pages)

```bash
# Opción 1: Python
python3 -m http.server 8080
# Abrir: http://localhost:8080/index.html

# Opción 2: Node
npx serve .
```

> En local puedes usar el modo **"Directo (sin proxy)"** si tu navegador no restringe CORS en localhost.

---

## 📄 Licencia

MIT — Úsalo libremente.
