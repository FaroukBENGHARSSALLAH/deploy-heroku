Spring MVC Template
==========================

A set of steps to deploy in the heroku cloud v7.

What you need: 

- [x] Procfile, 
- [x] Webapp-runner

For a procfile, you can the in-folder file.

For the webapp runner, it's a maven pluguin; add it in the POM file



 You can use my API using this maven dependency : 
 
  ```
  
       <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-dependency-plugin</artifactId>
			<version>2.3</version>
            <executions>
                <execution>
                    <phase>package</phase>
                    <goals><goal>copy</goal></goals>
                    <configuration>
                        <artifactItems>
                            <artifactItem>
                                <groupId>com.heroku</groupId>
                                <artifactId>webapp-runner</artifactId>
                                <version>9.0.30.0</version>
                                <destFileName>webapp-runner.jar</destFileName>
                            </artifactItem>
                        </artifactItems>
                    </configuration>
                </execution>
            </executions>
        </plugin>
```


