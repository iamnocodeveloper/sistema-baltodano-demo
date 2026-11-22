# sistema-baltodano-demo

Demo navegable del **sistema de gestión** del Bufete del Lic. Oscar Felipe Baltodano Valverde (San José, Costa Rica).

Es el complemento de la web pública: la web presenta el despacho y recibe consultas; este panel es lo que el bufete usa todos los días para agendar, seguir expedientes y cobrar honorarios.

## Qué incluye

Aplicación de una sola página (`index.html`, CSS y JS inline, sin backend ni dependencias externas salvo Google Fonts):

- **Entrada simulada**: usuario demo precargado y botón «Entrar en modo demostración» (sin autenticación real).
- **Escritorio**: citas del día, consultas nuevas sin asignar, plazos que vencen esta semana, facturación del mes, avisos del bufete y honorarios por abogado.
- **Agenda**: vista de día (calendario por abogado, ancho = duración, hora actual marcada) y de semana (bloques repartidos en carriles cuando hay citas simultáneas). Alta real de citas con control de cruce por abogado; detalle con cliente, tipo, abogado y estado (confirmada / pendiente / atendida / cancelada).
- **Consultas**: bandeja de 12 consultas entrantes (sitio web, WhatsApp, llamada, correo) con estados nuevo / contactado / cita agendada / descartado, nota de seguimiento y conversión a cita —al convertir, se crea la ficha del cliente si no existe—.
- **Expedientes**: 45 casos con buscador y filtro por estado; ficha con cliente, carátula, área, abogado a cargo, cuantía, juzgado, próximos vencimientos y bitácora de actuaciones (se pueden agregar).
- **Clientes**: 35 fichas con contacto, expedientes, citas, facturación e historial de comunicaciones.
- **Facturación**: honorarios de los últimos tres meses por cliente y concepto, con total, cobrado y pendiente del mes; estados pagado / pendiente (botón «Cobrar»).
- **Informes**: consultas por mes, áreas más frecuentes, horas de agenda por abogado, cobrado vs. pendiente y facturación de seis meses. Todo con SVG y CSS, sin librerías.
- **Ajustes**: tipos de consulta y su duración, abogados, horarios de atención, recordatorios (con vista previa del mensaje) y datos del bufete.
- Menú de usuario con acceso a la web pública y pie con la nota de demo.

Los datos son de ejemplo y se generan en el navegador, relativos a la fecha en que se abre el demo: 35 clientes, 45 expedientes, unas 80 citas del mes, 12 consultas, 10 vencimientos próximos y 48 facturas de tres meses. Montos en colones costarricenses (₡).

Áreas usadas como categorías genéricas: civil, laboral, familia y notarial. No se atribuyen especialidades ni casos reales al bufete.

## Despliegue

`Dockerfile` de dos líneas (`nginx:alpine` + copia de los archivos) publicado desde este repositorio en EasyPanel:

- Sistema: https://clientes-sistema-baltodano.rddxeh.easypanel.host/
- Web pública: https://clientes-demo-baltodano.rddxeh.easypanel.host/

## Nota

Demo de referencia hecho por Nocodeveloper. No envía mensajes, no cobra nada, no guarda datos y no incluye información real de terceros; en el sistema real se cargan los datos del bufete.