# demo


oc new-build java --name=java-binary-build --binary=true


oc start-build bc/java-binary-build \

--from-file=./build/libs/hello-boot-0.1.0.jar \

--follow

---------------------------------------
url.properties
api.web.noauth.context.url=/upi/noaouth

----------------------------------------------

openssl verify -CAfile /etc/origin/master/ca.crt /etc/origin/master/master.server.crt
/etc/origin/master/master.server.crt: OK

-----------------------------------------------------------------------------------
As we are using Routes for external access to the cluster, we need the CA certs to enable TLS in the client. Extract the public certificate of the broker certification authority
$ oc extract secret/my-cluster-cluster-ca-cert --keys=ca.crt --to=- > src/main/resources/ca.crt

Import the trusted cert to a keystore
$ keytool -import -trustcacerts -alias root -file src/main/resources/ca.crt -keystore src/main/resources/keystore.jks -storepass password -noprompt
-----------------------------------------------------------------------------

http://gogs-.icd-ocpadmin.cloudapps.onlinesbi.com/sbi/sbi-demo.git
