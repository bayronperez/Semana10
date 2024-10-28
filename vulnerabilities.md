# Vulnerabilidades Identificadas en GPSMapApp

## 1. Permitir Respaldo de Datos
- **Descripción**: El atributo `android:allowBackup` está configurado en `true`, lo que permite que los datos de la aplicación sean respaldados sin control.
- **Impacto**: Exposición de datos sensibles, que podría ser accedida por aplicaciones maliciosas.
- **Recomendación**: Cambiar `allowBackup` a `false` en el archivo `AndroidManifest.xml`.

## 2. Vulnerabilidad de StrandHogg 2.0
- **Descripción**: La actividad principal permite la superposición de actividades, facilitando ataques de phishing mediante el secuestro de tareas.
- **Impacto**: Potenciales ataques de phishing que pueden comprometer la información del usuario.
- **Recomendación**: Configurar adecuadamente `launchMode` y `taskAffinity` en el archivo `AndroidManifest.xml`.

## 3. Conexiones No Seguras (HTTP)
- **Descripción**: La aplicación realiza conexiones mediante HTTP, exponiendo los datos a interceptaciones.
- **Impacto**: Riesgo de interceptación de datos sensibles durante la transmisión.
- **Recomendación**: Usar exclusivamente HTTPS para el tráfico de red y eliminar todas las conexiones HTTP inseguras.

## 4. Uso de Permisos de Ubicación en Segundo Plano
- **Descripción**: La aplicación accede a la ubicación en segundo plano, lo que puede violar la privacidad del usuario.
- **Impacto**: Riesgo de privacidad y consumo innecesario de batería.
- **Recomendación**: Limitar el uso de permisos en segundo plano a las funcionalidades esenciales.

## 5. Abuso de Permisos Sensibles
- **Descripción**: Se utilizan permisos sensibles (`ACCESS_FINE_LOCATION`, `INTERNET`) sin justificación adecuada.
- **Impacto**: Riesgo de abuso de permisos y posible explotación por parte de aplicaciones maliciosas.
- **Recomendación**: Justificar el uso y restringir los permisos en el archivo `AndroidManifest.xml`.
