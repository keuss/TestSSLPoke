# TestSSLPoke
TestSSLPoke


 - keytool -import -trustcacerts -alias test -file test.cer -keystore trustStore.jks
 - keytool -v -list -storetype jks -keystore trustStore.jks
 - java -Djavax.net.ssl.trustStore=trustStore.jks -Djavax.net.ssl.trustStorePassword=changeit -jar target/ssl-poke.jar test.com 443
