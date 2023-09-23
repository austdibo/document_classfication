## maven打包会自动执行test方法，如何skipTests关闭maven自动执行test
```
方案1
使用spring-boot-maven-plugin方式打包，可以增加参数 <skipTests>true</skipTests>
    <properties>
        <skipTests>true</skipTests>
    </properties>
    
方案2
使用maven-surefire-plugin方式打包，可以增加配置<skip>true</skip>
  <build>
        <plugins>                    
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-surefire-plugin</artifactId>
                <configuration>
                    <skip>true</skip>
                </configuration>
            </plugin>
        </plugins>
    </build>
方案3
idea中设置关闭

方案4
在执行命令中增加 -DskipTests=true，跳过test。
```

## test
