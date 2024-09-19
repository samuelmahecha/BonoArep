## Bono Arep
## Project Setup

This guide outlines the steps to set up and run your project.

**Prerequisites**

Before proceeding, ensure you have the following software installed on your system:

* **Java** (version 1.8.0 or higher): Download and install Java from the official website: https://www.oracle.com/java/technologies/downloads/
    * Verify your installation by running:
        ```bash
        mvn -version
        ```
      You should see output similar to:

        ```
        Apache Maven 3.x.x (unique identifier)
        Maven home: /path/to/maven
        Java version: 1.8.0, vendor: Oracle Corporation
        Java home: /path/to/java/jdk1.8.0.jdk/Contents/Home
        ...
        ```
* **Git:** Install Git by following the instructions on the official Git website: https://git-scm.com/downloads
    * Verify your installation by running:
        ```bash
        git --version
        ```
      This should output your Git version, for example:

        ```
        git version 2.34.1
        ```

**Installing the Project**

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/samuelmahecha/BonoArep.git
    ```
2. **Navigate to the Project Directory:**
    ```bash
    cd BonoArep
    ```

**Building the Project**

1. **Compile and Package:**
    * Run the following command to build the project using Maven:
        ```bash
        mvn package
        ```
    * This will compile your code and create a JAR file in the `target` directory. You should see output similar to:

        ```
        [INFO] Building jar:(https://github.com/samuelmahecha/ProyectoArepParcial.git-1.0-SNAPSHOT.jar
        [INFO] BUILD SUCCESS
        ```

**Functionalities tests**

  * CalcReflexBEServer and CalcReflexFacade working on differents ports

  ![image](https://github.com/user-attachments/assets/023de28a-1413-42f9-8a4e-f150907d1498)


  * Implementation of Bubble Sort
    
![image](https://github.com/user-attachments/assets/ecd379b2-e9f1-4bc3-9905-aef59aed58f6)


## Generating Project Documentation

1. **Generate the Site**
    - Run the following command to generate the site documentation:
      ```sh
      mvn site
      ```

2. **Add Javadoc Plugin for Documentation**
    - Add the Javadoc plugin to the `reporting` section of the `pom.xml`:
      ```xml
      <project>
        ...
        <reporting>
          <plugins>
            <plugin>
              <groupId>org.apache.maven.plugins</groupId>
              <artifactId>maven-javadoc-plugin</artifactId>
              <version>2.10.1</version>
              <configuration>
                ...
              </configuration>
            </plugin>
          </plugins>
        </reporting>
        ...
      </project>
      ```

    - To generate Javadoc as an independent element, add the plugin in the `build` section of the `pom.xml`:
      ```xml
      <project>
        ...
        <build>
          <plugins>
            <plugin>
              <groupId>org.apache.maven.plugins</groupId>
              <artifactId>maven-javadoc-plugin</artifactId>
              <version>2.10.1</version>
              <configuration>
                ...
              </configuration>
            </plugin>
          </plugins>
        </build>
        ...
      </project>
      ```

3. **Generate Javadoc Commands**
    - Use the following commands to generate Javadocs:
      ```sh
      mvn javadoc:javadoc
      mvn javadoc:jar
      mvn javadoc:aggregate
      mvn javadoc:aggregate-jar
      mvn javadoc:test-javadoc
      mvn javadoc:test-jar
      mvn javadoc:test-aggregate
      mvn javadoc:test-aggregate-jar
      ```

---------

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.

----------
## Author
Jose Samuel Mahecha Alarcon - @samuelmahecha

 
