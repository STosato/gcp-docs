# REST
Achronym for **RE**presentational **S**tate **T**ransfer.

REST is a set of **architectural principles** or ***guidelines***, 
SOAP, instead is a W3C protocol. So REST is **not a protocol**

Because it's a set of guidelines, it leaves the implementation of these recommendations to developers

## How it works
When a **request is sent**, it is done trough <u>HTTP</u>.
The **response** messages can be sent in a variety of formats: HTML, XML, plain text, and JSON.

## RESTful applications
Must follow this guidelines:
1. A **client-server architecture** composed of clients, servers, and resources
2. [Stateless](https://www.redhat.com/en/topics/cloud-native-apps/stateful-vs-stateless) client-server communication = <u>no client content is stored</u> on the server between requests. 
	Information about the session’s state is instead held with the client.
3. **Cacheable data** to eliminate the need for some client-server interactions
4. A **uniform interface between components** so that <u>information is transferred in a standardized form</u> instead of specific to an application’s needs.
5. A l**ayered system constraint**, where client-server interactions can be mediated by hierarchical layers.
6. **Code on demand**, allowing servers to extend the functionality of a client by <u>transferring executable code</u> (though also reducing visibility, making this an optional guideline).

## SOAP
SOAP is a standard protocol, it imposes built-in rules that increase its complexity and overhead, which can lead to longer page load times.

However, these standards also offer **built-in compliances** that can make it **preferable for enterprise scenarios**.
These include security, atomicity, consistency, isolation, and durability (ACID), which is a set of properties for ensuring reliable database transactions.

Common web service specifications include:

-   **Web services security (WS-security)**: Standardizes how messages are secured and transferred through unique identifiers called tokens.
-   **WS-ReliableMessaging**: Standardizes error handling between messages transferred across unreliable IT infrastructure.
-   **Web services addressing (WS-addressing)**: Packages routing information as metadata within SOAP headers, instead of maintaining such information deeper within the network.
-   **Web services description language (WSDL)**: Describes what a web service does, and where that service begins and ends.

## REST vs SOAP
**REST** APIs are **lightweight**, making them ideal for newer contexts like IOT, mobile application development, and serverless computing. 

**SOAP** web services offer **built-in security** and transaction compliance that align with many enterprise needs, but that also makes them **heavier**.
