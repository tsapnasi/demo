# demo


oc new-build java --name=java-binary-build --binary=true


oc start-build bc/java-binary-build \

--from-file=./build/libs/hello-boot-0.1.0.jar \

--follow

---------------------------------------
url.properties
api.web.noauth.context.url=/upi/noaouth
