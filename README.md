


The size of the Docker Image without Multi-Stage is much larger. 

Golang is a statically typed language. So for executing a Golang application, we do not need a Golang Runtime.

During Multi-Stage Build of Docker images, there are two stages namely :

1) Build Stage
   
2) Run Stage (Final Image)

The Final Image will have Runtime Environment, Binary (which has been built in the Build Stage) and Executable. 


To, reduce the size of the Docker Image significantly, the contents of the Build Stage should not be present in the Final Image.



So, we are using DISTROLESS IMAGES. 

### DISTROLESS IMAGES :

Very Minimalistic Image that will hardly have any packages.

The Minimalistic Image (or) Light weight Docker Image will have only the Runtime Environment.

Another important thing to be noted about Distroless Images is that they provide the HIGHEST SECURITY.




During this Journey, I have used scratch - One of the official Distroless images from the Docker Hub as the base image.


### Conclusion :

The main purpose of choosing a golang based applciation to demostrate this example is golang is a statically-typed programming language that does not require a runtime in the traditional sense. Unlike dynamically-typed languages like Python, Ruby, and JavaScript, which rely on a runtime environment to execute their code, Go compiles directly to machine code, which can then be executed directly by the operating system.

So the real advantage of multi stage docker build and distro less images can be understand with a drastic decrease in the Image size.





