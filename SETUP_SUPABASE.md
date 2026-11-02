# Configuración de Mi Mes Compartido con Supabase

## Antes de publicar
- Use un correo personal para GitHub y Supabase.
- Defina primero el nombre exacto del repositorio: `mi-mes`.
- No suba datos reales de prueba dentro del código.
- No ejecute el SQL parcialmente. Si aparece un error, deténgase y conserve el mensaje completo.

## 1. Crear el proyecto
1. Ingrese a https://supabase.com y cree un proyecto.
2. Guarde la contraseña de base de datos en un lugar seguro.
3. Espere hasta que el proyecto quede activo.

## 2. Crear la base de datos
1. Abra `SQL Editor` en Supabase.
2. Cree una consulta nueva.
3. Copie todo el contenido de `supabase-setup.sql`.
4. Presione `Run` una sola vez.

## 3. Configurar autenticación
1. Abra `Authentication > URL Configuration`.
2. En `Site URL` coloque `https://TU-USUARIO.github.io/mi-mes/`.
3. Añada la misma dirección en `Redirect URLs`.
4. Mantenga habilitada la confirmación por correo.

## 4. Conectar la PWA
1. Abra `Project Settings > API`.
2. Copie `Project URL`.
3. Copie la clave `Publishable` (o `anon` si el panel aún usa ese nombre).
4. Abra `config.js` y reemplace los dos textos de ejemplo.
5. Nunca coloque la clave `service_role` o una secret key en GitHub.

## 5. Publicar
Suba todos los archivos a la raíz del repositorio GitHub Pages y active `main / (root)`.

## 6. Primer uso
1. José crea una cuenta y confirma el correo.
2. José crea el hogar compartido.
3. En Ajustes, José genera un código de invitación.
4. La segunda persona crea su propia cuenta, confirma el correo y usa el código.
5. Ambos teléfonos ven el mismo presupuesto.

## Seguridad
La aplicación utiliza cuentas separadas, RLS y membresía por hogar. El código de invitación vence en 48 horas y se utiliza una sola vez. La clave pública puede estar en el navegador; la seguridad depende de las políticas RLS. Nunca publique credenciales administrativas.

## Alcance offline de esta versión
La interfaz puede abrir después de la primera carga. La consulta y edición compartida requiere Internet. No se encolan gastos offline para evitar duplicados y conflictos entre teléfonos.


## Prueba obligatoria antes de ingresar datos reales
1. Cree dos cuentas de prueba con correos distintos.
2. Cree un hogar con la primera cuenta.
3. Genere un código e incorpore la segunda cuenta.
4. Registre un gasto desde un teléfono y confirme que aparece en el otro.
5. Cierre sesión y compruebe que no se muestran datos del hogar.
6. Cree una tercera cuenta que no pertenezca al hogar y confirme que no puede ver datos.
7. Solo después utilice información real.

## Si GitHub conserva una versión anterior
Cambie `mi-mes-shared-v2.0.0` en `sw.js` por un nombre nuevo, confirme el cambio en GitHub y vuelva a abrir la PWA con conexión.
