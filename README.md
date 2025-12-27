# ProContacto-Salesforce-Developer-Adriel

## Ejercicio 1: Instalación del Ambiente
Para el desarrollo de esta evaluación técnica, se ha configurado el siguiente entorno de trabajo:  

**IDE:** Visual Studio Code.  
<img width="1919" height="1040" alt="image" src="https://github.com/user-attachments/assets/a2a35b48-4ee3-47a0-abf8-6c08ffb3792e" /> 

**Extensiones:** Se instaló el Salesforce Extension Pack para el desarrollo de componentes Apex.  
<img width="1919" height="1040" alt="image" src="https://github.com/user-attachments/assets/0ea32416-9d0b-4f1d-b78c-9fc58b8d3e4d" />  

**Control de Versiones:** Git y Git Bash para la gestión del repositorio y despliegues.  
<img width="976" height="509" alt="image" src="https://github.com/user-attachments/assets/6f20eefc-5529-4a3d-8da2-5c2ac273f9c5" />  


## EJERCICIO 2: Comprensión del protocolo HTTP

**1. ¿Qué es un servidor HTTP?**  
Es un software que se ejecuta en un servidor que se encarga de escuchar y procesar las peticiones (requests) solicitadas por los clientes, para así devolver una respuesta (response) con la información solicitada.

**2. ¿Qué son los verbos HTTP? Mencionar los más conocidos**  
Son métodos que indican la acción que se desea realizar sobre un recurso específico. Los más conocidos son:
* **GET:** Solicitar datos de un recurso.
* **POST:** Enviar datos para ser procesados para un recurso.
* **PUT:** Actualizar o reemplazar un recurso existente.
* **DELETE:** Eliminar un recurso.
* **PATCH:** Modificar parcialmente un recurso.

**3. ¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?**  
* **Request (Petición):** Es el mensaje que envía el cliente al servidor solicitando una acción.
* **Response (Respuesta):** Es el mensaje que el servidor envía de vuelta al cliente con el resultado de la acción solicitada.
* **Headers (Encabezados):** Son los metadatos enviados en el request y en el response. Tienen información adicional sobre la transacción, como el tipo de contenido, la longitud del mensaje, etc.

**4. ¿Qué es un queryString? (En el contexto de una url)**  
Es una cadena de texto añadida al final de una URL para pasar parámetros al servidor. Comienza con un signo de interrogación `?` y los parámetros se separan por `&`.
* *Ejemplo:* `https://tiendaropa.com/busqueda?producto=remera&talla=m`

**5. ¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?**  
Es un código numérico de tres dígitos que el servidor envía en la respuesta para indicar el estado de la petición. Se agrupan en categorías:
* **1xx:** Informativos.
* **2xx:** Éxito (Ej. `200 OK`, `201 Created`).
* **3xx:** Redirección (Ej. `301 Moved Permanently`).
* **4xx:** Error del cliente (Ej. `400 Bad Request`, `404 Not Found`).
* **5xx:** Error del servidor (Ej. `500 Internal Server Error`).

**6. ¿Cómo se envía la data en un GET y cómo en un POST?**  
* **GET:** Los datos se envían visibles en la URL a través del **QueryString**. Tienen un límite de caracteres y no son seguros para información sensible.
* **POST:** Los datos se envían en el **cuerpo (body)** de la petición. No son visibles en la URL, no tienen límite de tamaño estricto y son más seguros para enviar información confidencial.

**7. ¿Qué verbo http utiliza el navegador cuando accedemos a una página?**  
Utiliza el verbo **GET**. Al escribir una dirección en la barra y presionar Enter, el navegador solicita "traer" ese recurso.

**8. Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.**  
Son formatos de texto para el intercambio de datos.
* **JSON (JavaScript Object Notation):** Es ligero y basado en pares clave-valor. Es el estándar más usado en APIs REST modernas.
    ```json
    {
      "nombre": "Juan",
      "edad": 30,
      "activo": true
    }
    ```
* **XML (eXtensible Markup Language):** Es un lenguaje de marcado basado en etiquetas. Es más verborrágico y estricto.
    ```xml
    <usuario>
      <nombre>Juan</nombre>
      <edad>30</edad>
      <activo>true</activo>
    </usuario>
    ```

**9. Explicar brevemente el estándar SOAP**  
**SOAP (Simple Object Access Protocol)** es un protocolo estándar basado estrictamente en XML para intercambiar información estructurada. Es conocido por su robustez, seguridad (WS-Security) y transaccionalidad (ACID), pero es más pesado y complejo de implementar que REST. Utiliza un archivo WSDL para definir la estructura del servicio.

**10. Explicar brevemente el estándar RESTful**  
**REST (Representational State Transfer)** no es un protocolo, sino un estilo arquitectónico. Un servicio RESTful utiliza los verbos HTTP estándar (GET, POST, PUT, DELETE) para manipular recursos identificados por URLs. Es "stateless" (sin estado), suele usar JSON como formato de transporte y es más ligero y flexible que SOAP.  

**11. ¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?**  
Son los metadatos que el cliente envía al servidor para darle contexto sobre la petición (quién la envía, qué acepta recibir, credenciales, etc.).
El key **Content-Type** es fundamental porque indica al servidor qué tipo de formato tienen los datos que se están enviando en el cuerpo del mensaje (body).
* *Ejemplo:* `Content-Type: application/json` avisa al servidor que el body contiene un objeto JSON.  

## EJERCICIO 4:
### Realizar los siguientes módulos de Trailhead:
https://www.salesforce.com/trailblazer/syl2zip2b0pbmidcc8

## EJERCICIO 5:

