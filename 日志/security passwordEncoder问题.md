# 单独使用security 的passwordEncoder加密问题

引入包
```java
<dependency>
            <groupId>org.springframework.security</groupId>
            <artifactId>spring-security-crypto</artifactId>
            <version>5.5.0</version>
        </dependency>
        <dependency>
            <groupId>org.bouncycastle</groupId>
            <artifactId>bcprov-jdk15on</artifactId>
            <version>1.64</version>
        </dependency>
```

注册到容器中
```java


@Configuration
public class PasswordEncoderConfig {
    @Bean
    public PasswordEncoder passwordEncoder() {
        return new Argon2PasswordEncoder();
    }
}
```

使用
```java
 passwordEncoder.matches(password,miningUser.getCashPassword());
```
