Build docker image using buildpacks:

First, the dev needs to add the image tag in pom xml 

```
<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
				<configuration>
					<image>
						<name>dimk10/${project.artifactId}:s4</name>
					</image>
					<excludes>
						<exclude>
							<groupId>org.projectlombok</groupId>
							<artifactId>lombok</artifactId>
						</exclude>
					</excludes>
				</configuration>
			</plugin>
		</plugins>
	</build>
```


Then, run the following maven command:

```mvn spring-boot:build-image```
