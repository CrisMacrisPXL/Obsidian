## container management
oplossing vraag 1:
docker run --rm --name ex-1 alpine:3.23 echo "Hello form inside the container!"

docker container ls -a

oplossing vraag 2:
1. docker run -d --name mgmt-ubuntu ubuntu:24.04 sleep infinity
2. docker exec -it mgmt-ubuntu bash
3. apt-get install -y curl
echo "Hello, World!"
exit
4. docker logs mgmt-ubuntu
5. docker top mgmt-ubuntu

- What do the logs show? Why?
commando: docker logs mgmt-ubuntu
deze is leeg. de sleep infinity commando is het hoofdproces en die print niks. 
- Which process is the main process of the container?
commando: docker top mgmt-ubuntu
Sleep infinity is het hoofdproces
- Is `curl` still installed after you leave the shell? Why?
commando : docker exec mgmt-ubuntu curl --version
Ja curl is nog steeds geinstalleerd. Zolang de container bestaat blijft ook curl geinstalleerd zelfs na een stop en een start van de container. Pas na een rm word alles verwijdert.

oplossing vraag 3:
1. docker run --name mgmt-httpd -d -p 8080:80 httpd:2.4
2. docker logs  -f mgmt-httpd

-What does the default page show?
It works!
-What does each refresh add to the logs?
Een get van de default page.
-Does Ctrl+C stop the container?
Nee



