Origen: https://github.com/pbakaus/impeccable (carpeta plugin/)
Commit: 3671d50f0ac9a662ce0615e85a256110c9cd720b
Licencia: Apache 2.0

Aviso: este plugin descarga su motor (engine v0.1.17) desde los releases de GitHub del autor
la primera vez que se usa, ejecuta hooks en SessionStart / PostToolUse(Edit|Write) / Stop,
y envía telemetría anónima a impeccable.style (desactivable con DO_NOT_TRACK=1 o
IMPECCABLE_NO_TELEMETRY=1).
