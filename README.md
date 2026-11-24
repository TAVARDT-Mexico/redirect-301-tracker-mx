# Verificador de Redirecciones HTTP 301/302 y Cadenas de Saltos

[![Verificador Redirecciones](https://img.shields.io/badge/TAVARDT-Redirect%20301-5b3cf5.svg)](https://tools.tavardt.com/mx/verificador-redirecciones-301/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Auditoria de cadenas de redireccion, deteccion de bucles infinitos y conservacion de autoridad digital en Mexico.

Desarrollado y mantenido por la division de ingenieria de rastreo y plataformas web de **TAVARDT**.

***

## Capacidades de Auditoria de Redirecciones HTTP

* **Rastreo Completo de Cadenas de Saltos**: Inspeccion de codigos HTTP (301, 302, 307, 308) y tiempos de transicion.
* **Deteccion de Bucles Infinitos**: Identificacion de rutas circulares que provocan fallos de carga en navegadores y buscadores.
* **Conservacion de Autoridad y PageRank**: Alertas contra cadenas excesivas que consumen presupuesto de rastreo en plataformas digitales.
* **Control de Seguridad de Protocolo**: Deteccion de degradaciones temporales a HTTP inseguro.
* **Puntuacion de Eficiencia de Redireccion**: Indice cuantitativo de 0 a 100 con recomendaciones tecnicas priorizadas.

***

## Instalacion y Ejecucion

Requiere Python 3.8 o superior sin dependencias externas.

```bash
git clone https://github.com/TAVARDT/redirect-301-tracker-mx.git
cd redirect-301-tracker-mx
python redirect_tracker.py https://empresa.com.mx
```

Para generar salida estructurada JSON:

```bash
python redirect_tracker.py https://empresa.com.mx -json
```

***

## Diagnostico Completo en la Web

Para revision profunda de cadenas de redireccion:

* **Verificador de Redirecciones 301 Oficial**
* **[Portal Corporativo TAVARDT](https://ag.tavardt.com/mx/)**

***

## Consultoria en Migraciones y SEO Tecnico

Para migraciones seguras y conservacion de trafico bajo directrices de Estandares W3C y Mejores Practicas Tecnicas, consulte al equipo de **TAVARDT**.

***

## Enlaces Útiles

* **Portal Corporativo:** https://ag.tavardt.com/mx/
* **Suite de Diagnósticos:** https://tools.tavardt.com/mx/
* **Contacto Técnico:** https://ag.tavardt.com/mx/contacto/

***

© 2026 TAVARDT. Todos los derechos reservados.
