#Docker environment instead Vagrant for labs in Mongodb University

For some reasons I cannot run Vagrant on my host machine.
Also I would like to run labs in my favorite virtualization tools - Docker.

Project Structure
-----------------

Each Course has separate folder.
I tried to rework Vagrant environment to the same Docker environment.
So it is all You need in one place!

####Get Started
After each changes in Dockerfile you should rebuild docker image `docker-compose build`.
Run needed lab for command `docker-compose up` optional You can run it as daemon `docker-compose up -d`
Next: run `docker ps` command in free terminal window to get container ID. 
run `docker exec -it %container_id% bash` to enter inside container. it like `vagrant ssh` command.
#####Hint:
Database stored inside docker. so in each rebuild you should recreate users.

M103    Basic Cluster Administration
-------------------------

Open M103 folder.
For labs you need to change command inside docker-compose file to manage mongod instance.
Also one note: do not use --fork because it allows successful docker shutdowning.


M310    MongoDB Security
--------------------

It is recommended to connect MFlix with MongoDB Atlas, so you do not need to
have a MongoDB server running on your host machine. The lectures and labs in
this course will assume that you are using an Atlas cluster instead of a local
instance.

M312    Diagnostics and Debugging
--------------------

