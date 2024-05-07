# Spring Security Cheatsheet

## Getting Started

### Add Spring Security Dependency
Include the Spring Security dependency in your project's build configuration.

### Configuration
Create a security configuration class by extending `WebSecurityConfigurerAdapter`.

### Enable Security
Use the `@EnableWebSecurity` annotation on your main application class.

## Basic Configuration

### Authentication
Configure authentication mechanisms:
```java
@Override
protected void configure(AuthenticationManagerBuilder auth) throws Exception {
    auth.inMemoryAuthentication()
        .withUser("user").password("{noop}password").roles("USER")
        .and()
        .withUser("admin").password("{noop}adminpassword").roles("USER", "ADMIN");
}
```

### Authorization
Define authorization rules:
```java
@Override
protected void configure(HttpSecurity http) throws Exception {
    http.authorizeRequests()
        .antMatchers("/public").permitAll()
        .antMatchers("/admin").hasRole("ADMIN")
        .anyRequest().authenticated()
        .and()
        .formLogin();
}
```

### Password Encoding
Use password encoding to securely store passwords:
```java
@Bean
public PasswordEncoder passwordEncoder() {
    return new BCryptPasswordEncoder();
}
```

## Form-Based Authentication

### Login Form
```java
@Override
protected void configure(HttpSecurity http) throws Exception {
    http.formLogin()
        .loginPage("/login")
        .defaultSuccessUrl("/dashboard")
        .permitAll();
}
```

### Logout
```java
@Override
protected void configure(HttpSecurity http) throws Exception {
    http.logout()
        .logoutUrl("/logout")
        .logoutSuccessUrl("/login?logout")
        .permitAll();
}
```

## OAuth2 Authentication

### OAuth2 Client Configuration
```java
@Configuration
@EnableOAuth2Client
public class OAuth2Config extends WebSecurityConfigurerAdapter {
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
            .antMatchers("/", "/login**", "/error**")
            .permitAll()
            .anyRequest()
            .authenticated()
            .and()
            .oauth2Login();
    }
}
```

### OAuth2 Resource Server
```java
@Configuration
@EnableResourceServer
public class ResourceServerConfig extends ResourceServerConfigurerAdapter {
    @Override
    public void configure(HttpSecurity http) throws Exception {
        http.authorizeRequests()
            .antMatchers("/api/**").authenticated();
    }
}
```

## Best Practices

- Always use strong password encoding mechanisms like BCrypt.
- Implement roles and authorities to manage access control.
- Use HTTPS to secure data transmission.
- Use CSRF protection to prevent cross-site request forgery attacks.
- Keep sensitive configuration (like OAuth2 secrets) in external properties.
- Regularly update your Spring Security version to benefit from security patches.

Remember, Spring Security is a powerful and complex topic. It's essential to refer to the official Spring Security documentation and community resources to ensure you are following best practices and staying up to date with security recommendations.