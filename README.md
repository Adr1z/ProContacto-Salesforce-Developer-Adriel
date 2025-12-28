# ProContacto-Salesforce-Developer-Adriel

## EJERCICIO 1: Instalación del Ambiente
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
Utiliza el verbo **GET**.

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
**SOAP (Simple Object Access Protocol)** es un protocolo estándar basado en XML para intercambiar información estructurada. Es conocido por su robustez, seguridad (WS-Security) y transaccionalidad (ACID), pero es más pesado y complejo de implementar que REST. Utiliza un archivo WSDL para definir la estructura del servicio.

**10. Explicar brevemente el estándar RESTful**  
**REST (Representational State Transfer)** es un estilo de arquitectura para sistemas distribuidos en red, que define restricciones para la comunicación cliente-servidor.  
**RESTFul** es un servicio que implementa los principios de la arquitectura **REST**, usando HTTP para interactuar con recursos (datos) identificados por URLs.

**11. ¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?**  
Son los metadatos que el cliente envía al servidor para darle contexto sobre la petición (quién la envía, qué acepta recibir, credenciales, etc.).
El key **Content-Type** es fundamental porque indica al servidor qué tipo de formato tienen los datos que se están enviando en el cuerpo del mensaje (body).
* *Ejemplo:* `Content-Type: application/json` avisa al servidor que el body contiene un objeto JSON.  

## EJERCICIO 4:
### Realizar los siguientes módulos de Trailhead:
https://www.salesforce.com/trailblazer/syl2zip2b0pbmidcc8

## EJERCICIO 5:
**1. Lead (Candidato)**
<ins>Concepto</ins>:  
Un Lead representa un prospecto no calificado: alguien que mostró interés pero todavía no se sabe si será cliente. El objetivo de este objeto es convertirse en una Account, Contacto u Opportunity.  

<ins>Datos Estándar (Campos)</ins>:  
FirstName, LastName  
Company   
Status  
LeadSource   
Rating  
Email, Phone  

**2. Account (Cuenta)**
<ins>Concepto</ins>:  
Una Account representa una empresa o cliente.  

<ins>Datos Estándar (Campos)</ins>:  
Name  
AccountNumbe  
Type  
Industry  
BillingAddress, ShippingAddress  
AnnualRevenue  

**3. Contact (Contacto)**  
<ins>Concepto</ins>:  
Representa a una persona física asociada o que trabaja para una Account.  

<ins>Datos Estándar (Campos)</ins>:  
AccountId  
FirstName, LastName  
Email, Phone, MobilePhone  
Title  
Department  

**4. Opportunity (Oportunidad)**  
<ins>Concepto</ins>:  
Representa una venta potencial en progreso.  

<ins>Datos Estándar (Campos)</ins>:  
Name   
AccountId  
StageName  
CloseDate  
Amount   
Probability  

**5. Product**  
<ins>Concepto</ins>:  
Un Product es un bien o servicio que la empresa vende.  

<ins>Datos Estándar (Campos)</ins>:  
Name
ProductCode  
IsActive  
Family  
Description

**6. PriceBook**  
<ins>Concepto</ins>:  
Un PriceBook define una lista de precios para productos.   

<ins>Datos Estándar (Campos)</ins>:   
Name  
IsActive  
IsStandard  

**7. Quote (Presupuesto)**  
<ins>Concepto</ins>:  
Una Quote es un presupuesto enviado a un cliente.  

<ins>Datos Estándar (Campos)</ins>:   
OpportunityId  
QuoteNumber  
Status  
ExpirationDate  
Subtotal, GrandTotal  

**8. Asset (Activo)**  
<ins>Concepto</ins>:  
Representa un producto específico que un cliente ya ha comprado y posee.  

<ins>Datos Estándar (Campos)</ins>:  
AccountId  
ProductId  
SerialNumber  
InstallDate, PurchaseDate  
Status  

**9. Case (Caso)**  
<ins>Concepto</ins>:  
Un Case es un ticket de soporte o atención al cliente.  

<ins>Datos Estándar (Campos)</ins>:  
CaseNumber  
Subject, Description  
Status  
Priority  
Origin  
AccountId, ContactId  

**10. Article (Artículo / Knowledge)**  
<ins>Concepto</ins>:  
Documentos de conocimiento (FAQs, manuales) que ayudan a los agentes a resolver Casos o a los clientes a auto-servirse.  

<ins>Datos Estándar (Campos)</ins>:  
Title  
UrlName  
Summary  
ValidationStatus  
PublishStatus   

**Diagrama UML:**  
<img width="2516" height="4356" alt="image" src="https://github.com/user-attachments/assets/781571c9-5161-4610-af90-55f1fb4a05f5" />  

## EJERCICIO 6: 

**Soluciones de Salesforce**  

A. ¿Qué es Salesforce?  
Es una plataforma CRM en la nube para gestionar ventas, servicios, marketing y relaciones con clientes.  

B. ¿Qué es Sales Cloud?  
Es un software que automatiza el ciclo de ventas para ayudar a las empresas a vender de forma más rápida y eficiente, proporcionándoles una plataforma integrada con todo lo que necesitan.  

C. ¿Qué es Service Cloud?  
Es una plataforma de atención al cliente diseñada para ayudar a las empresas a gestionar y resolver las consultas y problemas de sus clientes de forma eficiente.  

Ofrece herramientas para la gestión de casos, bases de conocimiento, soporte omnicanal, automatización y análisis.  

D. ¿Qué es Health Cloud?  
Es una plataforma CRM en la nube para el sector salud que unifica datos clínicos y no clínicos, creando una vista centralizada del paciente para una atención personalizada y eficiente; permitiendo la coordinación entre equipos, automatizando procesos e integrando historiales, dispositivos y sistemas en un lugar.  

E. ¿Qué es Marketing Cloud?  
Es la solución para automatización de marketing, campañas multicanal y personalización de comunicaciones.  

---

**Funcionalidades de Salesforce**  

A. ¿Qué es un Record Type?  
Es una función de Salesforce que permite agrupar registros similares dentro de un objeto y personalizarlos según las necesidades específicas.  

B. ¿Qué es un Report Type?  
Es una plantilla que define qué objetos, campos y relaciones estarán disponibles al crear un reporte.  

C. ¿Qué es un Page Layout?  
Es una herramienta que controla qué campos, botones y secciones ve el usuario en un registro.  

D. ¿Qué es un Compact Layout?  
Es una configuración que define los campos clave que se muestran en el encabezado de un registro (highlights) y en la vista resumida de la aplicación móvil.  

E. ¿Qué es un Perfil?  
Es una plantilla que define el nivel base de acceso y permisos de un usuario, determinando qué puede ver (objetos, campos) y qué puede hacer (crear, leer, editar, eliminar - CRED) dentro de la plataforma.  

F. ¿Qué es un Rol?  
Es una herramienta que define la jerarquía de visibilidad de datos dentro de la organización.  

G. ¿Qué es un Validation Rule?  
Es una regla que impide guardar datos inválidos según una condición.  

H. Diferencia entre Master-Detail y Lookup  

Master-Detail: Dependencia total; el hijo hereda seguridad del padre y se borra en cascada si el padre desaparece.  

Lookup: Relación flexible y opcional; el registro hijo puede existir de forma independiente.  

I. ¿Qué es un Sandbox?  
Es un entorno de prueba separado del entorno de producción.  

J. ¿Qué es un Change Set?  
Es una herramienta para migrar configuraciones entre entornos Salesforce.  

K. ¿Para qué sirve el Import Wizard?  
Para importar datos masivos fácilmente desde archivos externos a objetos.  

L. ¿Para qué sirve Web to Lead?  
Sirve para capturar automáticamente la información de visitantes de tu sitio web y crear registros de prospectos (leads) en tu CRM sin intervención manual.  

M. ¿Para qué sirve Web to Case?  
Sirve para capturar automáticamente solicitudes de soporte al cliente directamente desde tu sitio web, creando registros de Casos en Salesforce sin intervención manual.  

N. ¿Para qué sirve Omnichannel?  
Para distribuir casos/chats/tareas entre agentes según reglas y disponibilidad.  

O. ¿Para qué sirve Chatter?  
Para colaboración interna, comentarios, menciones y seguimiento de registros.  

---

**Conceptos Generales**  

A. ¿Qué significa SaaS?  
Software as a Service: software accesible vía internet, sin instalación local.  

B. ¿Salesforce es SaaS?  
Sí, Salesforce es una plataforma SaaS.  

C. ¿Qué significa que una solución sea Cloud?  
Que se ejecuta en servidores remotos accesibles por internet.  

D. ¿Qué significa On-Premise?  
Que el software se instala y ejecuta localmente en servidores propios.  

E. ¿Qué es un pipeline de ventas?  
Es el conjunto de oportunidades activas y su estado en el proceso comercial.  

F. ¿Qué es un funnel de ventas?  
Es la representación del proceso de conversión, desde prospectos hasta clientes.  

G. ¿Qué significa Customer Experience?  
Es la experiencia total del cliente en todas sus interacciones con la empresa.  

H. ¿Qué significa omnicanalidad?  
Integrar todos los canales de atención (web, chat, mail, teléfono) de forma unificada.  

I. ¿Qué significa que un negocio sea B2B?¿Qué significa que un negocio sea B2C? ¿Qué es un KPI?  

B2B: Bussiness to Bussiness (negocio entre empresas).  

B2C: Bussiness to Client (negocio empresa → consumidor final).  

KPI: Key peformance indicator (indicador clave para medir rendimiento).  

J. ¿Qué es una API y diferencia con REST API?  

API: interfaz para comunicación entre sistemas.  

REST API: API que usa HTTP y principios REST.  

K. ¿Qué es un Proceso Batch?  
Proceso que ejecuta grandes volúmenes de datos de forma asincrónica.  

L. ¿Qué es Kanban?  
Método visual para gestionar tareas por estados.  

M. ¿Qué es un ERP?  
Sistema que integra finanzas, logística, compras, RRHH, etc.  

N. ¿Salesforce es un ERP?  
No. Salesforce es un CRM, aunque puede integrarse con ERPs.  

## EJERCICIO 7:  
**A.** Consultar tu ID haciendo un GET con POSTMAN a este WS:  
https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json  
<img width="760" height="398" alt="image" src="https://github.com/user-attachments/assets/d63d6ade-ebb9-4931-81b3-f5a3088ea73e" />  

**B.** Agregar un campo al objeto Contact llamado idprocontacto de tipo texto de 255 caracteres.
<img width="1877" height="452" alt="image" src="https://github.com/user-attachments/assets/a5eec156-3a3d-40f0-97a0-f6dddc65f045" />  

**C.**  
```apex
trigger ContactTrigger on Contact (after insert, after update) {

    Set<Id> contactIds = new Set<Id>();

    for (Contact con : Trigger.new) {
        if (con.idprocontacto__c != null) {
            contactIds.add(con.Id);
        }
    }

    if (!contactIds.isEmpty()) {
        ContactIntegrationHandler.processContacts(contactIds);
    }
}
```
```apex
public class ContactIntegrationHandler {

    @future(callout=true)
    public static void processContacts(Set<Id> contactIds) {

        List<Contact> contactsToUpdate = new List<Contact>();

        for (Contact iteratedContact : [
            SELECT Id, idprocontacto__c
            FROM Contact
            WHERE Id IN :contactIds
        ]) {

            Http http = new Http();
            HttpRequest request = new HttpRequest();
            request.setEndpoint(
                'https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts/' +
                iteratedContact.idprocontacto__c + '.json'
            );
            request.setMethod('GET');

            HttpResponse response = http.send(request);

            if (response.getStatusCode() == 200) {
                Map<String, Object> results =
                    (Map<String, Object>) JSON.deserializeUntyped(response.getBody());

                if (results.containsKey('email')) {
                    iteratedContact.Email = (String) results.get('email');
                    contactsToUpdate.add(iteratedContact);
                }
            }
        }

        if (!contactsToUpdate.isEmpty()) {
            update contactsToUpdate;
        }
    }
}
```
