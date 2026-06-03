# Quiniela Mundial 2026 (Cloud + PWA)

Esta version ya permite:
- Cuentas reales (registro/login)
- Multiples quinielas por nombre (ej: Familia, Amigos)
- Entrar a quinielas buscando el nombre
- Datos compartidos entre todos los miembros de cada quiniela
- Instalable como app (PWA)

## 1) Crear proyecto en Supabase
1. Crea proyecto en https://supabase.com
2. En `SQL Editor`, ejecuta completo `supabase-schema.sql`
3. En `Authentication > Providers`, deja Email habilitado
4. En `Project Settings > API`, copia:
- Project URL
- anon public key

## 2) Configurar la app
En [index.html](index.html), reemplaza:
- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`

## 3) Publicar
Sube estos archivos a tu repo de GitHub Pages:
- [index.html](index.html)
- [manifest.webmanifest](manifest.webmanifest)
- [sw.js](sw.js)

## 4) Uso
1. Cada persona crea su cuenta.
2. Tu creas una quiniela (ej: `Quiniela Familia Garcia`).
3. Los demas la buscan por nombre y presionan `Entrar`.
4. Puedes crear otra quiniela para amigos y usarla en paralelo.

## Notas
- Cada quiniela tiene su propia tabla y resultados.
- El admin de la quiniela es quien la crea (mas tu email ADMIN si quieres superadmin).
- Si cambias estructura SQL, vuelve a revisar politicas RLS.
