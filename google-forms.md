# Habla con un par — especificación para Google Forms

Se necesitan **dos formularios**: uno para la solicitud (enlazado desde el banner) y otro para la encuesta posterior a la conversación (lo envía el par al terminar).

> Configuración de ambos: **Desactivar** "Recopilar correos electrónicos" y "Limitar a 1 respuesta" (las dos cosas obligan a iniciar sesión con Google y rompen el anonimato).

---

## Formulario 1 — Solicitud

**Título:** Habla con un par
**Descripción:**
Si estás pasando por un momento difícil, puedes hablar con otro estudiante que se capacitó para escuchar. La conversación dura de 20 a 30 minutos, puede ser virtual o presencial y los pares cuentan con supervisión profesional. No reemplaza la atención psicológica.
*[Agregar aquí la línea o el servicio de emergencia que confirme la UCA]*

| # | Pregunta | Tipo | Obligatoria | Opciones / notas |
|---|---|---|---|---|
| 1 | ¿En qué año de la carrera estás? | Opción múltiple | Sí | 1.º · 2.º · 3.º · 4.º · 5.º o más |
| 2 | Facultad | Desplegable | Sí | Lista oficial de facultades UCA + "Prefiero no decir" |
| 3 | ¿Quieres que sea anónimo? | Opción múltiple | Sí | Sí, anónimo → saltar a la sección 3 · No → ir a la sección 2 |
| — | *Sección 2* | | | |
| 4 | ¿Cómo te llamamos? | Respuesta corta | No | |
| — | *Sección 3* | | | |
| 5 | ¿Dónde te escribimos para agendar? (correo o WhatsApp) | Respuesta corta | Sí | "Solo se usa para coordinar la conversación." |
| 6 | ¿Cómo prefieres conversar? | Opción múltiple | Sí | Virtual · Presencial · Me da igual |
| 7 | ¿Qué horario te queda mejor? | Casillas | No | Mañana · Mediodía · Tarde |
| 8 | ¿Quieres adelantarnos algo? | Párrafo | No | |
| 9 | Consentimiento | Casillas | Sí | "Entiendo que es una conversación de apoyo entre pares y no una consulta psicológica, y acepto que se use mi contacto solo para agendarla." |

**Mensaje de confirmación:** Listo, recibimos tu solicitud. Un par te va a escribir para acordar el día y la hora.

---

## Formulario 2 — Encuesta posterior

Agregar un campo oculto o una pregunta "Código de conversación" (el par lo escribe en el enlace con *Obtener vínculo prellenado*) para unir cada encuesta con su solicitud sin pedir datos personales.

| # | Pregunta | Tipo | Métrica del canvas |
|---|---|---|---|
| 1 | ¿Qué tan útil te resultó la conversación? | Escala lineal 1–5 | Valor percibido |
| 2 | ¿Te sentiste escuchado/a sin que te juzgaran? | Sí · En parte · No | Confianza |
| 3 | ¿Volverías a usarlo o se lo recomendarías a alguien? | Sí · Tal vez · No | Intención de uso |

---

## Cómo sale cada métrica

| Métrica | Fuente | Cálculo |
|---|---|---|
| Interés | **Analítica de la web de la UCA** (impresiones y clics del banner) | clics ÷ vistas del banner |
| Conversión | Clics del banner + respuestas del Formulario 1 | solicitudes ÷ clics |
| Valor percibido | Formulario 2, P1 | promedio 1–5 |
| Confianza | Formulario 2, P2 | % "Sí" |
| Intención de uso | Formulario 2, P3 | % "Sí" |
| Derivación | Registro interno de los supervisores | casos que llegan a un profesional ÷ casos derivados |

**Corte de primer año:** filtrar todas las métricas por P1 = "1.º" del Formulario 1.

**Para medir clics aunque la UCA no comparta su analítica**, el banner puede enlazar a una URL con parámetro, por ejemplo `…/viewform?usp=pp_url&entry.XXXX=banner_home`. Esto cuenta solo los clics que llegan al formulario, no las vistas del banner.

## Criterios de éxito (del canvas)
- Al menos el 20 % de quienes hacen clic completa la solicitud.
- Al menos el 70 % se siente escuchado sin ser juzgado **y** volvería a usarlo.
