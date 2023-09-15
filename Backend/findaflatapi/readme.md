# Find a flat Api readme

### Application.yml

```yml
spring:
  output:
    ansi:
      enabled: ALWAYS
  datasource:
    url: ${FIND_A_FLAT_API_SPRING_DATASOURCE_URL}
    username: ${FIND_A_FLAT_API_SPRING_DATASOURCE_USERNAME}
    password: ${FIND_A_FLAT_API_SPRING_DATASOURCE_PASSWORD}
    driver-class-name: ${FIND_A_FLAT_API_SPRING_DATASOURCE_DRIVER_CLASS_NAME}
    hikari:
      maximumPoolSize: ${FIND_A_FLAT_API_SPRING_HIKARI_MAXIMUM_POOL_SIZE}

  h2:
    console:
      enabled: ${FIND_A_FLAT_API_SPRING_H2_CONSOLE_ENABLED}
      path: /h2-console

  sql:
    init:
      mode: ${FIND_A_FLAT_API_SPRING_SQL_INIT_MODE}

  jpa:
    defer-datasource-initialization: ${FIND_A_FLAT_API_SPRING_JPA_DEFER_DATASOURCE_INITIALIZATION}
    open-in-view: ${FIND_A_FLAT_API_SPRING_JPA_OPEN_IN_VIEW}
    show-sql: ${FIND_A_FLAT_API_SPRING_JPA_SHOW_SQL}
    properties:
      default-schema: ${FIND_A_FLAT_API_SPRING_API_JPA_PROPERTIES_DEFAULT_SCHEMA}
      hibernate:
    database-platform: ${FIND_A_FLAT_API_SPRING_JPA_DATABASE_PLATFORM}
    generate-ddl: ${FIND_A_FLAT_API_SPRING_JPA_GENERATE_DDL}
    hibernate:
      ddl-auto: ${FIND_A_FLAT_API_SPRING_JPA_HIBERNATE_DDL_AUTO}
      naming:
        physical-strategy: org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl

springdoc:
  writer-with-default-pretty-printer: true
  api-docs:
    path: /api-docs
    resolve-schema-properties: false
  swagger-ui:
    path: /docs
    operationsSorter: method
    enabled: ${FIND_A_FLAT_API_ENABLE_SWAGGER}
    filter: true
    display-request-duration: true

server:
  port: ${FIND_A_FLAT_API_SERVER_PORT}

logging:
  level:
    com:
      bitbox:
        law:
          api: ${FIND_A_FLAT_API_LOGGING_LEVEL_COM_BITBOX_LAW_API}
    org:
      springframework: ${FIND_A_FLAT_API_LOGGING_LEVEL_ORG_SPRINGFRAMEWORK}
    root: ${FIND_A_FLAT_API_LOGGING_LEVEL_ROOT}
```

### Intelli j development environment variables

```textile
FIND_A_FLAT_API_ENABLE_SWAGGER=true;FIND_A_FLAT_API_LOGGING_LEVEL_COM_BITBOX_LAW_API=info;FIND_A_FLAT_API_SERVER_PORT=9100;FIND_A_FLAT_API_SPRING_API_JPA_PROPERTIES_DEFAULT_SCHEMA=find_a_flat_api;FIND_A_FLAT_API_SPRING_DATASOURCE_DRIVER_CLASS_NAME=org.postgresql.Driver;FIND_A_FLAT_API_SPRING_DATASOURCE_PASSWORD=find_a_flat_api;FIND_A_FLAT_API_SPRING_DATASOURCE_URL=jdbc:postgresql://localhost:5432/find_a_flat_api;FIND_A_FLAT_API_SPRING_DATASOURCE_USERNAME=ubuntu;FIND_A_FLAT_API_SPRING_H2_CONSOLE_ENABLED=false;FIND_A_FLAT_API_SPRING_HIKARI_MAXIMUM_POOL_SIZE=10;FIND_A_FLAT_API_SPRING_JPA_DATABASE_PLATFORM=org.hibernate.dialect.PostgreSQLDialect;FIND_A_FLAT_API_SPRING_JPA_DEFER_DATASOURCE_INITIALIZATION=false;FIND_A_FLAT_API_SPRING_JPA_HIBERNATE_DDL_AUTO=none;FIND_A_FLAT_API_SPRING_JPA_OPEN_IN_VIEW=enable;FIND_A_FLAT_API_SPRING_JPA_SHOW_SQL=true;FIND_A_FLAT_API_SPRING_SQL_INIT_MODE=never;FIND_A_FLAT_API_LOGGING_LEVEL_ORG_SPRINGFRAMEWORK=3;FIND_A_FLAT_API_LOGGING_LEVEL_ROOT=root
```