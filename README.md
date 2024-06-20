# Av2SistemaAutenticacaoAutorizacao
Este é um sistema desenvolvido para realizar a AV2 da Disciplina Arquitetura de aplicações WEB, autenticação e autorização utilizando Spring Boot e JWT para gerenciar usuários com diferentes tipos de contas (ADMIN, GERENTE, VENDEDOR, CLIENTE etc.).

## Funcionalidades

- **Login**: Geração de token JWT ao efetuar login.
- **Buscar nome**: Retorna o nome do usuario através do token.
- **Buscar nome ADMIN**: Retorna nome do usuario através do token enviado, apenas usuarios ADMIN
- **Buscar nome GERENTE**: Retorna nome do usuario através do token enviado, apenas usuarios GERENTE

- ### Configuração de Segurança(`SecurityConfig`)

```java
@Configuration
@EnableWebSecurity
public class SecurityConfig {
    // Configurações de segurança
}
```
### Controller (`Controller`)
```java
@RestController
public class UsuarioController {
    // Endpoints de login,buscar nome etc.
}
```

## Endpoints
`Realizar Login: /login`
`"/gerente/{token}"`
`/nomeusuario/{token}`

`/admin/{token}`
