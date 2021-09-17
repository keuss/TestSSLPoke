# TestSSLPoke
TestSSLPoke


With `test.com` domain (get cer first, from browser for example) :

 - `mvn clean package`
 - Import : `keytool -import -trustcacerts -alias test -file test.cer -keystore trustStore.jks`
 - List : `keytool -v -list -storetype jks -keystore trustStore.jks`
 - Test : `java -Djavax.net.ssl.trustStore=trustStore.jks -Djavax.net.ssl.trustStorePassword=changeit -jar target/ssl-poke.jar test.com 443`
