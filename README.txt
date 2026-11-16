SENDA EDUCATIVA — PROYECTO PARA GITHUB PAGES
=============================================

CONTENIDO
---------
- index.html: aplicación web completa. Incluye cuestionarios, reglas de análisis,
  currículo, sesiones y autenticación Supabase.
- consentimiento_informado.pdf: documento original adjunto.
- consentimiento_informado.png: representación en imagen PNG del documento.
- INSTRUCCIONES_SUPABASE.txt: configuración de autenticación y creación de cuentas.

ANTES DE PUBLICAR
-----------------
1. Configura Supabase siguiendo INSTRUCCIONES_SUPABASE.txt.
2. En index.html, busca las dos constantes:
   SUPABASE_URL
   SUPABASE_PUBLISHABLE_KEY
   y reemplaza sus textos PEGA_AQUI... por los valores del proyecto.
3. No uses una clave service_role ni una secret key en index.html.
4. Sube los cuatro archivos a la raíz del repositorio GitHub.
5. Activa GitHub Pages desde Settings > Pages > Deploy from a branch > main > /(root).

AUTENTICACIÓN
-------------
La aplicación usa Supabase Auth con correo y contraseña. No incluye formulario de
registro. El administrador debe crear las cuentas desde el panel de Supabase.
Desactiva el registro público en la configuración de autenticación del proyecto.

PRIVACIDAD Y ALCANCE
--------------------
- Las respuestas de educadores y estudiantes se mantienen en memoria mientras
  la pestaña está abierta. No se envían a una base de datos ni se guardan en Supabase.
- El SDK de Supabase conserva la sesión de autenticación en el almacenamiento
  del navegador para que el usuario no tenga que iniciar sesión en cada recarga.
  Esto guarda la sesión de acceso, no las respuestas ni el currículo.
- Si se cierra o recarga la pestaña, las respuestas no persistidas se pierden.
- El currículo se genera en el navegador y puede imprimirse/guardarse como PDF.
- No se deben introducir nombres ni datos que identifiquen directamente al estudiante.
- El repositorio público permite que cualquiera consulte y descargue el código y
  los documentos publicados. No subir información real de estudiantes ni secretos.

IMPORTANTE
----------
La app debe someterse a pruebas funcionales y revisión pedagógica antes de un uso
institucional con estudiantes. La lógica reproduce las reglas implementadas en la
matriz de trabajo, pero el equipo responsable debe validar los resultados y las
rutas con casos de prueba representativos.
