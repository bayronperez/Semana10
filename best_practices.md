# Mejores Prácticas Implementadas en GPSMapApp

## 1. Cifrado de Datos Sensibles
- **Descripción**: Se implementa el cifrado para proteger datos sensibles (como contraseñas y datos personales) utilizando AES (Advanced Encryption Standard).
- **Impacto**: Aumenta la seguridad de los datos en reposo, protegiéndolos de accesos no autorizados.

## 2. Implementación de HTTPS
- **Descripción**: Todas las conexiones de red se realizan a través de HTTPS, asegurando la confidencialidad e integridad de los datos transmitidos.
- **Impacto**: Protege la información del usuario durante la transmisión, evitando ataques de intermediarios (MITM).

## 3. Validación y Sanitización de Entradas
- **Descripción**: Todas las entradas del usuario son validadas y sanitizadas para prevenir ataques como inyección de SQL y XSS (Cross-Site Scripting).
- **Impacto**: Reduce el riesgo de ataques maliciosos y mejora la seguridad general de la aplicación.

## 4. Minimización de Permisos
- **Descripción**: La aplicación solicita solo los permisos estrictamente necesarios para su funcionamiento.
- **Impacto**: Minimiza el riesgo de abuso de permisos y protege la privacidad del usuario.
