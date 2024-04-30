---
marp: true
---

# Hibernate: Mapeo objeto-relacional

## Introducción

- ¿Qué es Hibernate?
- Ventajas del mapeo objeto-relacional
- Funcionamiento de Hibernate

---

## Componentes principales de Hibernate

### Sesiones y transacciones

- Sesiones de Hibernate
- Obtención y cierre de sesiones
- Administración de transacciones

--- 

### Obtención y cierre de sesiones
Es importante obtener y cerrar las sesiones correctamente para liberar recursos y garantizar la integridad de la aplicación.

Ejemplo de obtención y cierre de sesión:

```java
Session session = HibernateUtil.getSessionFactory().openSession();
try {
    // Realizar operaciones con la sesión
} finally {
    session.close();
}

```

---

### Configuración de Hibernate

- Archivo de configuración (hibernate.cfg.xml)
- Propiedades de configuración
- Dialectos y conexiones a la base de datos


---

## Mapeo de objetos y relaciones

### Clases de entidad

- Anotaciones y/o archivos de mapeo XML
- Asociaciones entre entidades
- Propiedades y relaciones bidireccionales

### Tipos de datos personalizados

- Mapeo de tipos básicos
- Conversores de tipos personalizados
- Tipos de datos especiales de Hibernate

---

## Consultas y criterios

### Consultas HQL (Hibernate Query Language)

- Sintaxis básica de HQL
- Parámetros y consultas parametrizadas
- Consultas con múltiples entidades y asociaciones

### Criterios de Hibernate

- Creación de criterios
- Restricciones y condiciones
- Ordenamiento y proyecciones

---

## Optimización y rendimiento

### Estrategias de carga

- Lazy loading vs. Eager loading
- Carga selectiva y carga anticipada
- Uso de @Fetch para controlar la carga

### Caché de Hibernate

- Tipos de caché (primera, segunda y consulta)
- Configuración de la caché de entidades y colecciones
- Gestión de la caché para mejorar el rendimiento

---

## Transacciones y concurrencia

### Gestión de transacciones

- Inicio y finalización de transacciones
- Control de transacciones mediante anotaciones
- Transacciones distribuidas y propagación

### Bloqueo y concurrencia

- Optimistic locking
- Pessimistic locking
- Resolución de conflictos y control de concurrencia

---

## Conclusiones

- Hibernate simplifica el acceso a bases de datos relacionales
- Proporciona un mapeo transparente entre objetos y tablas
- Ofrece opciones de optimización y rendimiento

---

## Recursos adicionales

- Documentación oficial de Hibernate: [hibernate.org](https://hibernate.org)
- Tutoriales y ejemplos en el sitio web de Hibernate: [hibernate.org/orm/documentation](https://hibernate.org/orm/documentation)
- Repositorio de ejemplos de Hibernate en GitHub: [github.com/hibernate/hibernate-orm](https://github.com/hibernate/hibernate-orm)
