# Practice and Internship Themes

## Improve Java AWS Lambda for Project CRaC

Keywords: Engineering, Opensource, Java, C, networking,

A serverless function is a piece of code that gets are requests from the cloud for execution, while the cloud manages client connections, workload distributions, etc.
We are developing OpenJDK Project CRaC (https://github.com/CRaC) which aims to improve Java start-up and warm-up, which are especially important in serverless environments.
The Java code of applications needs to be changed a little to support the new CRaC programming model.
We've done modifications for the official Java client of AWS Lambda (https://github.com/aws/aws-lambda-java-libs) for Project CRaC
It's possible to do some improvements, like better management of connection with the cloud.
Also, AWS X-ray support is missing.
The concrete scope is yet to be defined, it can grow or shrink.

## Static Analyzer based on Graal VM

Keywords: Engineering, Research, Compilers, Java

There is a powerful toolbox for Java program analysis and compilation collected at https://www.graalvm.org.
One of the possible applications is Java programs static analysis with a greater understanding of the language and runtime semantics.
There is a prototype that can detect possible changes in the behavior of Java programs without actually executing them.
However, the prototype is limited and we need a change in how Graal VM assumes some aspects of the runtime behavior.

## Improvement of Quarkus build system for projects targeting OpenJDK CRaC

Keywords: Engineering, Opensource, Java, Maven,

To develop a universal build step to create CRaC images, available for all Quarkus users.
It's expected that the step will be very similar to existing Quarkus support of CDS archives.
The step should perform the documented actions expected by CRaC: running, providing some workload, triggering the image creation, and placing the image in the Docker image.
An example for manual execution: https://github.com/CRaC/example-quarkus#preparing-the-image.


## macOS/Aarch64 (Apple M1) OpenJDK Port development

Keywords: Engineering, Opensource, OpenJDK, C, assembler

There are a few open tasks remaining after the port was done:
https://bugs.openjdk.java.net/issues/?jql=cpu%20%3D%20aarch64%20AND%20os%20%3D%20os_x%20AND%20status%20not%20in%20(resolved%2C%20closed)

Some of them can be a subject for a separate track, alone.

For example, JNI calls optimization on small argument type.
It's required to change the call generator, and measure the improvement.
