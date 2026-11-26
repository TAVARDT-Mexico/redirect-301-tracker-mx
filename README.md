<p align="center">
  <a href="https://ag.tavardt.com/mx/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Auditor de Redirecciones HTTP 301 y Cadenas de Saltos

[![Verificador Redirecciones](https://img.shields.io/badge/TAVARDT-Redirect%20301-5b3cf5.svg)](https://tools.tavardt.com/mx/verificador-redirecciones-301/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de rutas de redireccion, deteccion de bucles infinitos, conservacion de autoridad y presupuesto de rastreo.

Desarrollado y mantenido por la division de ingenieria de indexacion e infraestructura de busqueda de **TAVARDT**.

***

## Vectores de Riesgo e Impacto Operativo en Redirecciones HTTP

Las cadenas excesivas de redireccionamiento erosionan la autoridad transferida, encarecen el rastreo y anaden latencia en plataformas digitales. Las secuencias circulares provocan fallos de carga en dispositivos moviles e impiden el rastreo.

El enrutamiento intermedio hacia HTTP sin cifrado compromete la privacidad de la sesion y debilita la confianza del usuario. La revision periodica asegura que las migraciones de dominio transfieran el valor organico con maxima solvencia tecnica.

***

## Capacidades Centrales de Auditoria Tecnica

* **Rastreo Paso a Paso No Automatizado**: Intercepcion controlada de codigos 301, 302, 303, 307 y 308 sin seguimiento ciego del cliente.
* **Deteccion Instantanea de Bucles Infinitos**: Identificacion de rutas circulares mediante historico de URLs visitadas, cancelando la traza y anulando la puntuacion.
* **Validacion del Estado del Destino Final**: Comprobacion del codigo HTTP de respuesta final, deduciendo 60 puntos si el destino devuelve un estado distinto de 200 OK.
* **Control de Extension y Link Equity**: Penalizacion de cadenas largas con 15 puntos por cada salto adicional sobre 3 para proteger el presupuesto de rastreo.
* **Auditoria de Degradacion Insegura**: Alerta inmediata ante transiciones de HTTPS a HTTP sin cifrar, con deduccion automatica de 20 puntos.
* **Medicion de Latencia Acumulada**: Registro del tiempo de transicion de cada salto y duracion total de la cadena en milisegundos.
* **Puntuacion de Eficiencia de Redireccion**: Metrica cuantitativa de 0 a 100 categorizando la ruta en OPTIMISED, LONG CHAIN (WARNING) o FAILURE / LOOP (CRITICAL).

***

## Instalacion y Ejecucion

Requiere Python 3.8 o superior sin librerias adicionales.

```bash
git clone https://github.com/TAVARDT-Mexico/redirect-301-tracker-mx.git
cd redirect-301-tracker-mx
python redirect_tracker.py https://empresa.com.mx
```

Para generar la salida en formato JSON estructurado en flujos de integracion continua:

```bash
python redirect_tracker.py https://empresa.com.mx -j
```

***

## Preguntas Frecuentes (FAQ Tecnico)

### 1. Como afectan las cadenas largas de redirecciones a la transmision de autoridad?
Cada salto adicional en una secuencia disipa una fraccion de la autoridad transmitida y retrasa la indexacion por parte de los rastreadores. Si la ruta supera el umbral tolerable, los buscadores pueden abandonar la navegacion antes de alcanzar el destino.

### 2. De que manera detecta la herramienta los bucles infinitos sin bloquearse?
El algoritmo registra cada URL consultada en un conjunto interno y gestiona las respuestas mediante un controlador sin seguimiento automatico. Al detectar una URL repetida, la ejecucion se aborta de inmediato y la puntuacion se establece en cero.

### 3. Que riesgos operativos introduce una degradacion de protocolo de HTTPS a HTTP?
La transicion intermedia hacia HTTP desprotegido compromete el cifrado de datos y expone las cabeceras a posibles manipulaciones de red. Este fallo anula las garantias de seguridad y activa advertencias en los navegadores modernos.

### 4. Cual es la diferencia tecnica entre codigos de redireccion permanente y temporal?
Las respuestas 301 y 308 transmiten la autoridad historica y consolidan el indice hacia la nueva ruta de forma definitiva. Por contra, los estados 302 y 307 marcan situaciones temporales que indican a los buscadores retener la URL de origen.

### 5. Por que resulta imprescindible validar la respuesta HTTP del destino final?
Una cadena que culmina en un error 4xx o 5xx anula cualquier beneficio de migracion y conduce a la desindexacion del recurso. El verificador comprueba la respuesta en tiempo real para garantizar que el destino devuelva un estado 200 OK.

***

## Consultoria en SEO Tecnico y Migracion de Portales

Para diseno de planes de migracion y cumplimiento de estandares W3C, consulte al equipo tecnico de **TAVARDT**.

***

## Enlaces Utiles

* **Portal Corporativo:** https://ag.tavardt.com/mx/
* **Suite de Diagnosticos:** https://tools.tavardt.com/mx/
* **Contacto Tecnico:** https://ag.tavardt.com/mx/contacto/

***

### Licencia
Distribuido bajo la Licencia MIT. Consulte el archivo LICENSE para conocer los terminos completos.

***

© 2026 TAVARDT. Todos los derechos reservados.
