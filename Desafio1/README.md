Se realiza un pipeline de Jenkins con tres etapas principales: "Input", "Passtemporal" y "Creacion del Usuario".
En la primera etapa, "Input", se solicita al usuario ingresar los datos del nuevo usuario, como el nombre, el apellido y el departamento.
Estos datos se recopilan mediante un cuadro de diálogo de entrada proporcionado por Jenkins.

Construcción del login: Una vez que el usuario proporciona el nombre y el apellido, se concatenan para formar el login del nuevo usuario.
Esto se realiza dentro de la etapa "Input" mediante la creación de la variable login, que es la combinación del nombre y el apellido.

Generación de contraseña temporal: En la etapa "Passtemporal", se genera una contraseña temporal para el nuevo usuario.
Esta contraseña se crea concatenando el nombre y el apellido, y luego convirtiendo todo a minúsculas.
La contraseña temporal se guarda en la variable env.TEMPORAL_PASSWORD para que esté disponible en otras etapas.

Creación del usuario: En la etapa "Creacion del Usuario", se utilizan los datos ingresados por el usuario (nombre, apellido, departamento) y la contraseña temporal generada para crear el usuario en el sistema.


Salida de información: Finalmente, se utiliza la función echo para imprimir un mensaje informativo en la consola de Jenkins. Este mensaje proporciona detalles sobre el usuario recién creado, como su nombre, apellido, departamento, login y contraseña temporal. Esto facilita a los operadores o desarrolladores verificar que el usuario se haya creado correctamente y obtener información relevante sobre él.

















