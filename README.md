# keycloak-java-client
Example of how to integrate Keycloak with Java Spring Boot Application


1. Run Keycloak<br>
	A. For default configuration with embedded H2 database run this command in terminal
`docker run -p 8080:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:18.0.2 start-dev`<br>
	B. For custom keycloak configuration with accessible mysql database run `keycloak-mysql.yml` file.
`docker-compose -f keycloak-mysql.yml up`
2. Access keycloak administration console at `localhost:8080` and prepare some configuration or import configuration which was used in this application by importing `real-export.json` file.
3. Define keycloak properties in `application.properties` file.
4. Start client application. It's running on `localhost:8081`.