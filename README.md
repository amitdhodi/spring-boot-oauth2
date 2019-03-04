# spring-boot-oauth2
Spring boot Oauth2 projects for Authorization server along with Resource server and Oauth2 client showcasing the authorization code grant flow

# Authorization code grant flow:
This grant type is most appropriate for server-side web applications. After the resource owner has authorized access to their data, they are redirected back to the web application with an authorization code as a query parameter in the URL. This code must be exchanged for an access token by the client application. This exchange is done server-to-server and requires both the client_id and cli
ent_secret, preventing even the resource owner from obtaining the access token.

# How to test this example:
1. Clone the repo https://github.com/amitdhodi/spring-boot-oauth2.git and download the code locally
2. Import the projects: clientApplication & oauthServer as Maven projects in your IDE(Eclipse/IntelliJ)
3. Run the Oauth + Resource server by running the OauthServerApplication.java file
4. Run the client by running the ClientApplication.java
5. Open browser and hit the URL: http://localhost:8484/client
6. Enter authserver credentials mentioned in application.yml: username - authUser, password - authUserSecret
7. This would redirect automatically to a URL similar to the one listed here:
http://localhost:8282/authServer/oauth/authorize?client_id=testClient&redirect_uri=http://localhost:8484/client/login&response_type=code&state=Di4zM1 and would open an 
approval page which asks the resource owner to provide authorization to access protected resource hosted on the resource
server. Select "Approve" and click on "Authorize".
8. Once the authorization is done, user is redirected to http://localhost:8484/client/ page and prints "Hello authUser".


