README - Prueba de carga con K6

DESCRIPCIÓN GENERAL:
Este proyecto contiene una prueba de carga automatizada al servicio de autenticación de la API pública https://fakestoreapi.com/auth/login, utilizando la herramienta K6. 
El objetivo es evaluar el comportamiento del endpoint bajo condiciones de concurrencia moderada, validando tiempos de respuesta y tasa de errores.

REQUISITOS:
- K6 v1.1.0
- Sistema operativo: Windows, Linux o macOS
- Conexión a internet activa

INSTRUCCIONES DE EJECUCIÓN:

1. Clonar el repositorio:
   git clone https://github.com/juniorDeveloper8/login-performance-k6.git

2. Ubicarse en el directorio del script:
   cd k6-login-test/scripts

3. Ejecutar la prueba:
   k6 run login_test.js

ESTRUCTURA DEL PROYECTO:
- /data/users.csv → contiene las credenciales de prueba utilizadas en el test
- /scripts/login_test.js → script principal que ejecuta la prueba de carga
- readme.txt → instrucciones de instalación y ejecución
- conclusiones.txt → hallazgos técnicos y observaciones del ejercicio

Generación del resumen de resultados
- Si deseas guardar el resumen de la prueba en un archivo de texto para análisis posterior, puedes hacerlo ejecutando:
  k6 run scripts/login_test.js > textSummary.txt

NOTAS IMPORTANTES:
- El único usuario válido confirmado por la API es: mor_2314 / 83r5^_
- El endpoint probado fue: https://fakestoreapi.com/auth/login
- El servidor responde con código HTTP 201 (Created) en lugar de 200, lo cual fue ajustado en el script para validar correctamente las respuestas exitosas.

AUTOR:
Esta prueba fue desarrollada como parte de un ejercicio técnico personal. 
Todos los scripts y archivos están disponibles públicamente para su revisión y reproducción.
