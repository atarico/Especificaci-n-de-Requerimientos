<h1 align="center" style="font-size: 24px; font-weight: bold; text-decoration: underline;"> Especificación de Requerimientos</h1>

<p style="font-size: 18px; font-weight: bold;">
  Software de seguridad para la empresa "Audoglio".
</p>
<p>
  Fecha: 04/05/2025
</p>
<p>
  Lugar: UTN - (Presencial).
</p>
<p>
  Participantes:
</p>
<p>
  • Equipo:
  <ul style="list-style-type: square;">
    <li>Abril, Sottini. (Lider)</li>
    <li>Julia, Gaeto. (Analista)</li>
    <li>Velozo, Joan. (Analista)</li>
    <li>Cordero, Ignacio. (Minutero)</li>
    <li>Tarico, Agustin. (Especialista)</li>
    <li>Gonzalez, Antonio. (Especialista)</li>
  </ul>
</p>
<p>
• Cliente: Audoglio, Pablo.
</p>

# 🧾 1. Objetivo General

Desarrollar una aplicación de gestión para una empresa dedicada a compras y ventas, que incluya control de accesos, permisos por sector, y funcionalidades internas de capacitación, con un fuerte enfoque en seguridad.

---

## ✅ 2. Requerimientos Funcionales

### 2.1. Autenticación de Usuarios

- RF1: El sistema deberá permitir la autenticación de usuarios mediante credenciales locales (usuario/contraseña).

- RF2: El sistema deberá soportar autenticación externa (por ejemplo, mediante proveedores OAuth como Google, Microsoft u otro sistema corporativo).

- RF3: El sistema deberá proporcionar una opción para recuperación de contraseña, la cual enviará un enlace de reseteo al correo electrónico registrado del usuario.

### 2.2. Gestión de Usuarios y Permisos

- RF4: El sistema deberá agrupar usuarios por sectores (por ejemplo: Ventas, Gestión, Operarios).

- RF5: El sistema deberá permitir asignar permisos específicos a los usuarios, basados en su sector.

- RF6: El sistema deberá contar con un sistema de permisos finos que limite el acceso a funciones (como comprar o vender) dependiendo del permiso asignado.

- RF7: El sistema deberá mostrar solo las funcionalidades habilitadas para cada usuario, ocultando o deshabilitando aquellas no permitidas.

### 2.3. Capacitación de Usuarios

- RF8: Una vez autenticado, el usuario deberá tener acceso a un módulo de capacitación donde podrá ver materiales, guías o tutoriales sobre el uso del sistema.

- RF9: El sistema deberá registrar el avance del usuario en su capacitación.

### 2.4. Funcionalidades de Gestión de Compras y Ventas

- RF10: El sistema deberá permitir registrar operaciones de compra y venta, solo para usuarios con permisos habilitados.

- RF11: Las operaciones deberán registrar fecha, productos, cantidades, usuario responsable y sector que ejecuta la operación.

---

## 🔒 3. Requerimientos de Seguridad

- RS1: El sistema deberá implementar control de acceso a nivel de función, validando cada acción contra los permisos del usuario.

- RS2: Las contraseñas deberán almacenarse de forma segura (con hashing y salt).

- RS3: El sistema deberá invalidar sesiones inactivas luego de un período configurable.

- RS4: Toda la comunicación con el servidor deberá utilizar HTTPS.

- RS5: Las funciones sensibles (ej. compras, ventas, gestión de usuarios) deberán estar protegidas de accesos no autorizados mediante validaciones adicionales del lado del servidor.

---

## 📊 4. Requerimientos No Funcionales

### 4.1. Usabilidad

- RNF1: La interfaz deberá ser clara y adaptable al nivel técnico de los usuarios.

- RNF2: El sistema deberá ser accesible desde distintos dispositivos (PC, tablets).

### 4.2. Mantenibilidad

- RNF3: El sistema deberá estar desarrollado de forma modular para facilitar actualizaciones y ampliaciones.

### 4.3. Rendimiento

- RNF4: Las operaciones comunes (autenticación, acceso a funciones, carga de módulos) no deberán superar los 2 segundos en condiciones normales de uso.
