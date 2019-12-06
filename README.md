# Maven-Hello-World

# First Maven Project
I will guide you to create your first Maven project by creating a POM file and the standard directory layout.
It is just a Java code which is what we are going to built with Maven.

# Creating the POM File
Inside the pom.xml file we are going to write the XML code:
    
    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-shade-plugin</artifactId>
                <version>2.1</version>
                <executions>
                    <execution>
                        <phase>package</phase>
                        <goals>
                            <goal>shade</goal>
                        </goals>
                        <configuration>
                            <transformers>
                                <transformer
                                    implementation="org.apache.maven.plugins.shade.resource.ManifestResourceTransformer">
                                    <mainClass>hello.HelloWorld</mainClass>
                                </transformer>
                            </transformers>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>

# Creating a Java Source File
Inside the Java root source directory, create a new directory (java package) called helloworld.

Inside the helloworld directory (java package) insert a file named HelloWorld.java. Inside the HelloWorld.java file you put the following Java code:

package helloworld;
public class HelloWorld {

	public static void main(String args[]){

		System.out.println("Hello World, Maven");

	}
}

Save the file.

# Building the Project
When you have created the Java source file, open a command prompt and change directory into the project root directory. And Build the project.
Now you are good to go!
