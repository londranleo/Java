📚 Ruta completa de documentación Java
## 🟢 NIVEL 1 — Fundamentos de Java

### 01. Introducción a Java

- ¿Qué es Java?
- Características principales
- JDK
- JRE
- JVM
- Java SE
- Código fuente
- Compilación
- Bytecode
- Ejecución
- `.java`
- `.class`
- Cómo funciona un programa Java desde que se escribe hasta que se ejecuta
- `main`
- Argumentos de `main`

---

### 02. Variables

- Qué es una variable
- Declaración
- Inicialización
- Asignación
- Tipado estático
- Tipos primitivos
- Tipos de referencia
- Scope
- Lifetime
- `var`
- `final`
- Convenciones de nombres

---

### 03. Tipos de datos

- `byte`
- `short`
- `int`
- `long`
- `float`
- `double`
- `char`
- `boolean`
- `String`
- Valores por defecto
- Rango de cada tipo
- Literales
- Sufijos
- Overflow
- Underflow

---

### 04. Conversión de tipos

- Conversión implícita
- Conversión explícita
- Casting
- `widening`
- `narrowing`
- Conversión entre números
- Conversión `String`
- `parseInt`
- `parseDouble`
- `valueOf`
- Problemas de conversión

---

### 05. Strings

- Qué es `String`
- Inmutabilidad
- String Pool
- Índices
- Longitud
- Concatenación
- Comparación
- `equals`
- `equalsIgnoreCase`
- `substring`
- `charAt`
- `contains`
- `startsWith`
- `endsWith`
- `replace`
- `split`
- `trim`
- `strip`

---

### 06. StringBuilder y StringBuffer

- Diferencia con `String`
- Mutabilidad
- `StringBuilder`
- `StringBuffer`
- Rendimiento
- Cuándo utilizar cada uno
- `append`
- `insert`
- `delete`
- `reverse`

---

### 07. Caracteres y textos especiales

- `char`
- Unicode
- Escape sequences
- `\n`
- `\t`
- `\"`
- `\\`
- `\r`
- Text blocks

---

### 08. Entrada y salida

- `System.out`
- `System.in`
- `Scanner`
- Entrada de texto
- Entrada numérica
- Problemas de `nextLine`
- Formateo de salida
- `printf`

---

### 09. Operadores

- Aritméticos
- Unarios
- Incremento/decremento
- Asignación
- Asignación compuesta
- Comparación
- Lógicos
- Ternario
- Precedencia
- Asociatividad

---

### 10. Expresiones

- Qué es una expresión
- Operandos
- Operadores
- Evaluación
- Precedencia
- Conversión automática
- Expresiones booleanas
- Expresiones complejas

---

# 🟡 NIVEL 2 — Control de flujo

### 11. `if / else`

- Condiciones
- Bloques
- `else`
- `else if`
- Condiciones anidadas
- Expresiones booleanas

### 12. `switch`

- `case`
- `default`
- `break`
- Fall-through
- Switch moderno
- Arrow syntax
- Switch expressions
- `yield`

### 13. Bucles

- `for`
- `while`
- `do while`
- Inicialización
- Condición
- Actualización
- Bucles infinitos
- Bucles anidados

### 14. `break` y `continue`

- `break`
- `continue`
- Bucles anidados
- Labels

### 15. Arrays

- Declaración
- Inicialización
- Índices
- Longitud
- Arrays multidimensionales
- Recorrido
- Arrays de objetos
- `Arrays`
- Copias
- Ordenamiento
- Búsqueda

---

# 🟠 NIVEL 3 — Métodos

### 16. Métodos

- Declaración
- Parámetros
- Argumentos
- Retorno
- `void`
- `return`
- Scope
- Métodos estáticos
- Métodos de instancia

### 17. Sobrecarga

- Method overloading
- Reglas de resolución
- Parámetros
- Tipos de retorno
- Ambigüedad

### 18. Recursividad

- Qué es
- Caso base
- Caso recursivo
- Stack
- Riesgos
- Recursividad vs iteración

---

# 🔵 NIVEL 4 — Programación Orientada a Objetos

### 19. Clases y objetos

- Qué es una clase
- Qué es un objeto
- Estado
- Comportamiento
- Instanciación
- Referencias

### 20. Constructores

- Constructor
- Constructor por defecto
- Parámetros
- Sobrecarga
- `this`

### 21. Atributos y métodos

- Atributos de instancia
- Atributos estáticos
- Métodos de instancia
- Métodos estáticos

### 22. Encapsulación

- `private`
- `public`
- `protected`
- Package-private
- Getters
- Setters
- Control del estado

### 23. `static`

- Variables estáticas
- Métodos estáticos
- Bloques estáticos
- Inicialización
- Limitaciones

### 24. `final`

- Variables
- Métodos
- Clases
- Constantes
- Inmutabilidad vs `final`

### 25. Herencia

- `extends`
- Superclase
- Subclase
- `super`
- Constructor de la superclase
- Reutilización
- Limitaciones

### 26. Polimorfismo

- Upcasting
- Downcasting
- Overriding
- Dispatch dinámico
- Tipo declarado
- Tipo real

### 27. Clases abstractas

- `abstract`
- Métodos abstractos
- Métodos concretos
- Cuándo utilizar una clase abstracta

### 28. Interfaces

- `interface`
- `implements`
- Métodos abstractos
- `default`
- `static`
- Interfaces múltiples
- Contratos

### 29. Composición y agregación

- Asociación
- Agregación
- Composición
- Relación entre objetos
- Herencia vs composición

### 30. `Object`

- `toString`
- `equals`
- `hashCode`
- Contrato entre `equals` y `hashCode`

---

# 🟣 NIVEL 5 — Java avanzado

### 31. Packages

- `package`
- `import`
- Organización
- Visibilidad entre packages
- Convenciones

### 32. Modificadores de acceso

- `public`
- `private`
- `protected`
- package-private
- Cómo funcionan entre clases y paquetes

### 33. Enumeraciones

- `enum`
- Valores
- Métodos
- Campos
- Constructores
- `switch`
- Comportamiento asociado

### 34. Excepciones

- Qué es una excepción
- Jerarquía
- `Throwable`
- `Exception`
- `RuntimeException`
- `Error`

### 35. `try / catch / finally`

- Captura
- Múltiples `catch`
- `finally`
- Multi-catch
- Try-with-resources

### 36. `throw` y `throws`

- Lanzar excepciones
- Declarar excepciones
- Diferencias
- Propagación

### 37. Checked y unchecked

- Checked exceptions
- Unchecked exceptions
- Cuándo utilizar cada una
- Buenas prácticas

---

# 🔴 NIVEL 6 — Generics

### 38. Conceptos de Generics

- Por qué existen
- Type safety
- Generic types
- Type parameters
- Erasure

### 39. Clases genéricas

- `<T>`
- Múltiples parámetros
- Restricciones

### 40. Métodos genéricos

- `<T>`
- Inferencia de tipos
- Métodos estáticos genéricos

### 41. Tipos acotados

- `extends`
- Upper bounds
- Multiple bounds
- `super`

### 42. Wildcards

- `?`
- `? extends`
- `? super`
- Producer
- Consumer
- PECS

---

# 🟤 NIVEL 7 — Collections Framework

### 43. Collection Framework

- `Collection`
- `List`
- `Set`
- `Queue`
- `Deque`
- `Map`

### 44. List

- `ArrayList`
- `LinkedList`
- Acceso
- Inserción
- Eliminación
- Complejidad

### 45. Set

- `HashSet`
- `LinkedHashSet`
- `TreeSet`
- Unicidad
- Orden

### 46. Map

- `HashMap`
- `LinkedHashMap`
- `TreeMap`
- Claves
- Valores
- Colisiones

### 47. Queue y Deque

- `Queue`
- `Deque`
- `PriorityQueue`
- FIFO
- LIFO

### 48. Iterators

- `Iterator`
- `ListIterator`
- `hasNext`
- `next`
- `remove`

### 49. Comparación

- `Comparable`
- `Comparator`
- `compareTo`
- `compare`
- Orden natural
- Orden personalizado

### 50. Utilidades de Collections

- `Collections`
- `Arrays`
- Ordenamiento
- Búsqueda
- Inmutabilidad

---

# 🟢 NIVEL 8 — Functional Java

### 51. Interfaces funcionales

- Qué son
- SAM
- `@FunctionalInterface`
- `Predicate`
- `Function`
- `Consumer`
- `Supplier`
- `UnaryOperator`
- `BinaryOperator`

### 52. Lambda

- Sintaxis
- Parámetros
- Return
- Inferencia
- Captura de variables
- Variables efectivamente finales

### 53. Method References

- Referencia a método estático
- Método de instancia
- Método de objeto
- Constructor

### 54. Stream

- Qué es
- Pipeline
- Source
- Intermediate operations
- Terminal operations
- Lazy evaluation

### 55. `filter`

- Predicados
- Filtrado
- Evaluación lazy

### 56. `map`

- Transformación
- `map`
- `flatMap`

### 57. `sorted`

- Orden natural
- Comparator
- Ordenamiento personalizado

### 58. `collect`

- Collectors
- `toList`
- `toSet`
- `joining`
- `groupingBy`
- `partitioningBy`

### 59. `reduce`

- Reducción
- Identity
- Accumulator
- Combiner

### 60. Optional

- `Optional`
- `of`
- `ofNullable`
- `empty`
- `map`
- `flatMap`
- `orElse`
- `orElseGet`
- `orElseThrow`

---

# 🔷 NIVEL 9 — Java moderno

### 61. Date & Time API

- `LocalDate`
- `LocalTime`
- `LocalDateTime`
- `Instant`
- `Duration`
- `Period`
- `ZoneId`
- `ZonedDateTime`

### 62. Records

- Qué son
- Componentes
- Constructor
- Accesores
- Inmutabilidad
- Cuándo utilizarlos

### 63. Sealed Classes

- `sealed`
- `permits`
- `final`
- `non-sealed`

### 64. Pattern Matching

- `instanceof`
- Pattern variables
- Pattern matching para `switch`

### 65. Text Blocks

- Strings multilínea
- Formateo
- Uso práctico

---

# ⚫ NIVEL 10 — Archivos y recursos

### 66. File API

- `File`
- `Path`
- `Paths`
- `Files`

### 67. Lectura y escritura

- Texto
- Bytes
- Streams de archivos
- Buffers

### 68. NIO

- Channels
- Buffers
- Filesystem
- Paths

### 69. Serialización

- `Serializable`
- Serialización
- Deserialización
- Problemas de serialización

---

# 🔥 NIVEL 11 — Concurrencia

### 70. Threads

- Thread
- Runnable
- Ciclo de vida
- Estados
- `start`
- `run`

### 71. Sincronización

- Race conditions
- `synchronized`
- Locks
- Deadlocks
- Atomicidad

### 72. Concurrency API

- `ExecutorService`
- Thread pools
- `Callable`
- `Future`

### 73. CompletableFuture

- Asincronía
- `thenApply`
- `thenAccept`
- `thenCompose`
- `thenCombine`
- Manejo de errores

### 74. Atomic y concurrent collections

- Atomic variables
- `ConcurrentHashMap`
- `CopyOnWriteArrayList`
- Blocking queues

---

# 🚀 NIVEL 12 — Java profesional

Aquí ya empezamos a conectar Java con el desarrollo de backend.

### 75. Maven

- `pom.xml`
- Dependencies
- Plugins
- Lifecycle
- Scopes
- Repositories

### 76. Gradle

- `build.gradle`
- Dependencias
- Tasks
- Plugins
- Diferencias con Maven

### 77. Testing

- Unit testing
- JUnit
- Assertions
- Test lifecycle
- Parameterized tests

### 78. Mockito

- Mocks
- Stubs
- Verify
- Argument matchers
- Unit testing con dependencias

### 79. JDBC

- Driver
- Connection
- Statement
- PreparedStatement
- ResultSet
- Transactions
- Connection pooling

---

# 🌐 NIVEL 13 — Spring

### 80. Spring Framework

- IoC
- DI
- Beans
- ApplicationContext
- Component scanning
- Configuration

### 81. Spring Boot

- Spring Boot
- Starters
- Auto-configuration
- Configuration
- Profiles
- Actuator

### 82. Spring MVC

- HTTP
- Request
- Response
- Controllers
- Routing
- Parameters
- Headers
- Status codes

### 83. REST API

- REST
- Resources
- CRUD
- JSON
- DTO
- HTTP methods
- HTTP status codes

### 84. Spring Data JPA

- Entity
- Repository
- Persistence
- Query methods
- JPQL

### 85. Hibernate

- ORM
- Persistence Context
- Entity lifecycle
- Lazy loading
- Eager loading
- Relaciones
- N+1

### 86. Transacciones

- `@Transactional`
- Commit
- Rollback
- Propagation
- Isolation

### 87. Spring Security

- Authentication
- Authorization
- Password encoding
- Roles
- Permissions
- JWT
- Filters

---

# 🐘 NIVEL 14 — Bases de datos

### 88. SQL

- SELECT
- INSERT
- UPDATE
- DELETE
- JOIN
- GROUP BY
- HAVING
- Subqueries
- Indexes

### 89. MySQL

- Configuración
- Bases
- Tablas
- Relaciones
- Índices

### 90. PostgreSQL

- Tipos
- Constraints
- JSON
- Índices
- Transactions

### 91. Diseño de bases de datos

- Normalización
- Relaciones
- Claves primarias
- Claves foráneas
- Integridad
- Índices

---

# 🐳 NIVEL 15 — DevOps para Java

### 92. Git

- Repository
- Working tree
- Staging
- Commit
- Branch
- Merge
- Rebase
- Remote
- Fetch
- Pull
- Push
- Revert
- Reset
- Reflog
- HEAD
- Hashes

### 93. GitHub

- Repository
- SSH
- Pull Requests
- Branch protection
- Issues
- Actions

### 94. Docker

- Images
- Containers
- Dockerfile
- Volumes
- Networks
- Docker Compose

---

# 📨 NIVEL 16 — Arquitectura backend

### 95. Arquitectura por capas

- Controller
- Service
- Repository
- Entity
- DTO
- Mapper

### 96. SOLID

- SRP
- OCP
- LSP
- ISP
- DIP

### 97. Design Patterns

- Singleton
- Factory
- Builder
- Strategy
- Observer
- Adapter
- Decorator
- Template Method

### 98. Clean Architecture

- Domain
- Application
- Infrastructure
- Dependency Rule
- Use Cases

### 99. DDD

- Entity
- Value Object
- Aggregate
- Repository
- Domain Service
- Bounded Context

---

# 📡 NIVEL 17 — Sistemas distribuidos

### 100. Microservicios

- Monolito
- Microservicios
- Comunicación
- Service discovery
- API Gateway
- Configuración
- Resiliencia

### 101. Kafka

- Producer
- Consumer
- Topic
- Partition
- Offset
- Consumer group
- Event-driven architecture

### 102. Redis

- Cache
- Key/value
- TTL
- Sessions
- Distributed locks

### 103. Mensajería

- Sincronía vs asincronía
- Eventos
- Colas
- Reintentos
- Dead-letter queues

---

# ☁️ NIVEL 18 — Cloud

### 104. AWS

- EC2
- S3
- RDS
- IAM
- VPC
- CloudWatch
- Load Balancer

### 105. Kubernetes

- Pod
- Deployment
- Service
- ConfigMap
- Secret
- Ingress
- Scaling
- Health checks

---

# 🏆 NIVEL 19 — Ingeniería profesional

### 106. Logging

- Logs
- Log levels
- SLF4J
- Logback
- Structured logging

### 107. Observabilidad

- Metrics
- Tracing
- Monitoring
- Health checks
- Actuator

### 108. Seguridad

- OWASP
- SQL Injection
- XSS
- CSRF
- CORS
- Password hashing
- Secrets
- JWT
- OAuth2

### 109. Rendimiento

- Complejidad
- Memoria
- Garbage Collector
- JVM
- Profiling
- Caching
- Database optimization

### 110. Buenas prácticas

- Clean Code
- SOLID
- DRY
- KISS
- YAGNI
- Code review
- Refactoring
- Naming
- Documentation📚 Ruta completa de documentación Java