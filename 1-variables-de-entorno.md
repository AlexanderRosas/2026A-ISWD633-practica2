# Variables de Entorno
### ¿Qué son las variables de entorno?
Son valores dinámicos que pueden afectar el comportamiento de los procesos en ejecución dentro de un contenedor. Se utilizan para configurar aplicaciones (como credenciales de base de datos o puertos) sin necesidad de modificar el código fuente o la imagen.
# COMPLETAR

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```
<img width="828" height="452" alt="image" src="https://github.com/user-attachments/assets/1f65b859-6800-4645-91b6-32a428a71f5b" />


### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR

### Crear un contenedor con la imagen de mysql, mapear todos los puertos
<img width="828" height="452" alt="image" src="https://github.com/user-attachments/assets/bb7e9658-4a8b-41ea-9310-55225b1c4025" />

# COMPLETAR

### ¿El contenedor se está ejecutando?
No se esta ejecutando
# COMPLETAR

### Identificar el problema
# COMPLETAR
El contenedor falla porque la imagen oficial de MySQL requiere obligatoriamente que se defina una variable de entorno para la contraseña del usuario root (como MYSQL_ROOT_PASSWORD) para poder inicializar la base de datos. Sin esto, el proceso principal termina con error.

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
<img width="1153" height="252" alt="image" src="https://github.com/user-attachments/assets/f327a0b8-0e91-4726-80b7-ebcaecd7933f" />
