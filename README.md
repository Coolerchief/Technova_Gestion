
<p align="center">
  <img src="assets/img/tecmilenio_logo.png" alt="TecMilenio" width="150"/>
  &nbsp;&nbsp;&nbsp;
  <img src="assets/img/Technova_logo.png" alt="TechNova" width="150"/>
</p>

# 🖥️⚙️ Sistema de Gestion de Tareas TechNova

Proyecto académico para la materia de **Estructuras de Datos** - Sistema de gestión de tareas administrativas, marketing y soporte técnico, implementado en **Java**.

🚧 **Estado:** En desarrollo - Documentación y diseño completados, implementación funcional en progreso.

---

## 🧾 INFORMACIÓN DEL PROYECTO

### Datos Académicos
- **Universidad**: TecMilenio
- **Materia**: Estructuras de Datos
- **Profesora**: Blanca Aracely Aranda Machorro
- **Ubicación**: Monterrey, Nuevo León

---

## 📑 ÍNDICE DE CONTENIDO

1. [ Descripción del Caso](#-descripción-del-caso)
2. [ Sistema de clasificación de Tareas por Prioridad](#-sistema-de-clasificación-de-tareas-por-prioridad)
3. [Tecnologías usadas en el proyecto](#-Tecnologias-usadas-en-el-proyecto)
4. [ Arquitectura](#-arquitectura-del-sistema)
5. [ Diseño UML](#-diseño-uml)
6. [ Estructuras de Datos](#-estructuras-de-datos-aplicadas)
7. [ Análisis del Problema](#-análisis-del-problema)
8. [ Caso de Estudio: Organización de Tareas en TechNova](#-caso-de-estudio-organización-de-tareas-en-technova)
9. [ Roles del Sistema](#-roles-del-sistema)
10. [ Avance del Proyecto](#-avance-del-proyecto)
11. [ Glosario de Términos](#-glosario-de-términos)
12. [ Bibliografía](#-bibliografía-formato-apa)
13. [ Objetivos de Aprendizaje Alcanzados](#-objetivos-de-aprendizaje-alcanzados)
14. [Desarrolladores](#-Desarrolladores)
15. [ Conclusiones y Agradecimientos](#-conclusiones-y-agradecimientos)
---

## 🔍📝 Descripción del Caso

### Estudio de caso
En TechNova, el equipo de Soporte Técnico notó que constantemente se generaba caos durante los turnos: mientras algunos técnicos atendían tickets urgentes de clientes con problemas críticos, otras solicitudes importantes quedaban olvidadas o se realizaban en desorden. Por ejemplo, un cliente podía reportar que su servidor estaba caído, pero al mismo tiempo llegaban varias solicitudes de mantenimiento que, aunque menos urgentes, también necesitaban seguimiento.
Además, los departamentos de Administración y Marketing enfrentaban dificultades similares: los reportes financieros se retrasaban porque los responsables estaban ocupados con tareas imprevistas, y las campañas publicitarias a veces no se ejecutaban a tiempo por falta de organización. Esto generaba ineficiencia, estrés en el personal y retrasos en la atención a clientes.


### 📩 Solicitudes del cliente para el programa
- ✅(COMPLETADO) - Persistencia de Datos: Implementar un sistema de almacenamiento para guardar las tareas y que no se pierdan al cerrar el programa.
- ✅(COMPLETADO) - Interfaz Gráfica (GUI): Desarrollar una interfaz gráfica para mejorar la experiencia del usuario, permitiendo una mejor interacción.
- ⏳(EN PROCESO) - Notificaciones y Recordatorios: Añadir la funcionalidad de notificaciones o recordatorios para tareas urgentes.
- ✅(COMPLETADO) - Mejorar la Gestión de Usuarios: Agregar un sistema para asignar tareas a diferentes usuarios o equipos dentro de los departamentos.


### 📈 Alcance del programa
**Funciones:**
- Registro y clasificación de tareas.
- Asignación de tareas a usuarios y departamentos.
- Control de estados (pendiente, en proceso, completada).
- Reportes básicos de productividad.


**Limitaciones:**
- Reportes estadísticos avanzados  
- Notificaciones externas  

---

## 📊 Sistema de clasificación de Tareas por Prioridad

| Color | Tipo de tarea | Descripción | Tiempos Requeridos
|-------|-------|-------------|--------------------------|
| 🔴 **Rojo** | Urgente | Tareas que requieren un enfoque total | Inmediata |
| 🟢 **Verde** | Colaborativa | Proyectos/Campañas de la empresa | Plazos especificados |
| 🔵 **Azul** | Regular | Tareas diarias y ocasionales | Programable |

---

## 🛠️ Tecnologías usadas en el proyecto

- **Java 17+** - Lenguaje principal de desarrollo  
- **Swing** - Interfaz gráfica  
- **Estructuras de Datos:** Pilas, Colas, Listas  
- **Patrón de diseño:** MVC (Modelo-Vista-Controlador)  

---

## 📂 Arquitectura del Sistema


### Estructura de Capas (MVC)
<p align="center">
  <img src="assets/img/diagrama.png" alt="Foto Evidencia" width="950" height="950">
</p>


### 🧩 Componentes del Sistema

- **Capa de Presentación (View / UI)**  
  - 📂 `view/` → Contiene las interfaces gráficas para la interacción del usuario.  
  - 🖥️ `interfaz.java` → Clase principal de interfaz para mostrar y capturar información.  

- **Capa de Control (Controller)**  
  - 📂 `controller/` → Coordina la lógica entre modelo, servicio y vista.  
  - ⚙️ Clases que gestionan las operaciones del sistema desde la UI.  

- **Capa de Lógica de Negocio (Service)**  
  - 📂 `service/` → Implementa la lógica del negocio (manejo de triage/tareas, clasificación, validaciones).  
  - 📝 `GestorTareasMain.java` → Punto de ejecución del sistema que conecta las funciones de servicio con los controladores.  

- **Capa de Acceso a Datos (DAO)**  
  - 📂 `dao/` → Se encarga de la conexión con la base de datos y operaciones CRUD.  
  - 🔗 `DBConnection.java` (o similar) → Clase para gestionar la conexión.  

- **Capa de Modelo (Model)**  
  - 📂 `model/` → Clases que representan las entidades principales.  
  - 👤 Ejemplo: `Paciente.java`, `RegistroAtencion.java`, `NivelTriage.java`.  

- **Capa de Utilidades (Util)**  
  - 📂 `util/` → Herramientas y clases auxiliares para estructuras de datos personalizadas.  
  - 📌 `cola.java`, `pilas.java`, `listas.java` → Implementaciones de estructuras de datos.  

- **Otros Archivos Importantes**  
  - 🚀 `main.java` → Punto de entrada alternativo al sistema.  
  - ✅ `TODO.md` → Lista de pendientes y funcionalidades en desarrollo.  
  - 📄 `readme.txt` → Notas rápidas o documentación básica.  
  - 📦 `lib/` → Librerías externas necesarias para correr el sistema.  
  - 🗂️ `bin/` → Archivos compilados.  

---

## 📊 Diseño UML

### Diagrama de Clases


<p align="center">
  <img src="assets/img/mvc.jpg" alt="Foto Evidencia" width="800" height="800">
</p>


## 🎓 Estructuras de Datos Aplicadas

**Pila (Stack):**
- Propósito: Gestionar incidencias críticas  
- Operaciones: `push`, `pop`, `peek`  
- Uso: Priorizar atención inmediata a problemas críticos  

**Cola (Queue):**
- Propósito: Gestionar tareas administrativas y de marketing  
- Operaciones: `offer`, `poll`, `peek`  
- Uso: Procesar tareas en orden de llegada  

**Lista (LinkedList):**
- Propósito: Gestionar tareas generales de departamentos  
- Operaciones: `add`, `remove`, `contains`  
- Uso: Mantener secuencia de tareas por departamento 

---

## 🔍 Análisis del Problema

**Problemática Identificada:**  
- Difícil priorizar incidencias críticas sobre tareas regulares  
- Falta de un registro ordenado de tareas por departamento  
- Necesidad de un sistema rápido, confiable y fácil de usar  

**Requisitos Funcionales:**  
- Registrar incidencias críticas  
- Registrar tareas administrativas y de marketing  
- Registrar tareas por departamento  
- Consultar próximas tareas  
- Atender tareas según prioridad  

**Requisitos No Funcionales:**  
- Estructuras de datos eficientes para alta concurrencia  



---

## 📌 Caso de Estudio: Organización de Tareas en TechNova

La empresa TechNova necesita organizar las tareas internas para no retrasar proyectos ni incidencias críticas. Se aplican **Pilas para incidencias críticas**, **Colas para tareas administrativas/marketing** y **Listas para tareas de departamentos**.

- Las incidencias críticas se mezclaban con tareas regulares, dificultando priorizar lo urgente.  
- Tareas administrativas y de marketing se procesaban de manera desordenada, generando retrasos en entregas y proyectos.  
- Cada departamento llevaba su propia lista de tareas sin un registro centralizado, lo que provocaba duplicidad y pérdida de información.  

### ❌ Problemática
Estos problemas generaban retrasos en la atención de incidencias críticas, confusión en la gestión de tareas y pérdida de productividad en toda la empresa. Por ejemplo:

- Una incidencia crítica de soporte técnico podía permanecer sin atención horas, mientras tareas menos urgentes eran realizadas primero.  
- Una tarea importante de marketing para un lanzamiento podía quedar retrasada porque se registró en una lista sin prioridad.  
- Los supervisores tenían dificultad para generar un resumen confiable de todas las tareas pendientes de cada departamento.  


### 💡 Solución Propuesta
Nuestro sistema digital de gestión de tareas implementa **estructuras de datos especializadas** para optimizar el flujo y la atención según prioridad:

- **Pilas (Stack)** → Gestionan **incidencias críticas** de soporte técnico.  
  - Ejemplo: Si un servidor cae, esta incidencia se agrega al tope de la pila y se atiende inmediatamente, garantizando que los problemas más urgentes sean resueltos primero.  
- **Colas (Queue)** → Gestionan **tareas administrativas y de marketing**.  
  - Ejemplo: Una campaña de redes sociales se agrega al final de la cola y se atiende en orden de llegada, asegurando que todas las tareas regulares se procesen de manera justa.  
- **Listas (LinkedList)** → Gestionan **tareas de departamentos específicos**.  
  - Ejemplo: Tareas de desarrollo, finanzas o recursos humanos se agregan a la lista correspondiente, permitiendo consultar, eliminar o reordenar tareas según las necesidades de cada equipo.  


### 📊 Ejemplo de Flujo
1. Incidencia crítica llega → Se agrega a la Pila → Urgente 
2. Tarea administrativa llega → Se agrega a la Cola → Tareas diarias y ocasionales
3. Tarea de departamento llega → Se agrega a la Lista → Colaborativa

### ✅ Beneficios
- Organización eficiente de tareas según prioridad  
- Interfaz amigable y profesional  
- Facilita seguimiento y gestión interna  
- Base para futuras mejoras y persistencia de datos  

---


## 👥 Roles del Sistema

| Rol | Función Principal | Acceso |
|-----|-----------------|--------|
| Gerente | Supervisar tareas y cerrar el sistema | Panel completo |
| Empleado | Agregar, consultar y atender tareas | Panel principal |

---

## 📈 Avance del Proyecto

**✅ Completado:**  
- Análisis de requisitos  
- Diseño de arquitectura MVC  
- Diagramas UML y diseño de clases  
- Implementación de clases `Pilas`, `Colas`, `Listas`  
- Interfaz básica de usuario  

**🔄 En Desarrollo:**  
- Mejoras en validaciones de entrada  
- Guardado y recuperación de datos (futuro)  
- Mejoras en layout de la interfaz  

**📅 Por Hacer:**  
- Pruebas unitarias   
- Optimización y refactorización de código  
- Publicación en GitHub y despliegue 

---

## 📚 Glosario de Términos

### Términos de Gestión de Tareas
- **Incidencia Crítica**: Problema o fallo que requiere atención inmediata, gestionado mediante una **pila (Stack)** para garantizar prioridad máxima.  
- **Tarea Administrativa/Marketing**: Actividad que debe procesarse en orden de llegada, gestionada con una **cola (Queue)** para respetar el flujo FIFO.  
- **Tarea por Departamento**: Actividad específica de un departamento, gestionada mediante **listas (LinkedList)**, permitiendo agregar, eliminar o consultar según necesidad.  
- **Prioridad de Tarea**: Criterio que determina qué tarea atender primero, implementado mediante la posición en la pila o cola y validaciones internas.  

### Términos de Estructuras de Datos
- **Pila (Stack)**: Estructura LIFO (Last In, First Out), usada para incidencias críticas; la última tarea agregada se atiende primero.  
- **Cola (Queue)**: Estructura FIFO (First In, First Out), usada para tareas administrativas y de marketing; la primera tarea en entrar es la primera en atenderse.  
- **Lista (LinkedList)**: Estructura dinámica que permite agregar, eliminar y consultar tareas por departamento de manera flexible.   
- **Complejidad Temporal**: Tiempo que tarda una operación según el tamaño de la estructura de datos; útil para analizar eficiencia de la pila, cola y lista.  

### Términos de Ingeniería de Software
- **MVC (Model-View-Controller)**: Patrón que separa la lógica de negocio, la interfaz y los datos, aplicado en nuestro proyecto para mantener código organizado.  
- **DAO (Data Access Object)**: Patrón para acceder a datos de manera abstracta; en nuestro caso, puede usarse para persistencia futura de tareas en base de datos.  
- **JDBC**: API de Java que permitirá conectarse a bases de datos para almacenar tareas de manera permanente (implementación futura).  
- **UML**: Lenguaje de modelado usado para diagramar clases (`Pilas`, `Colas`, `Listas`, `Interfaz`) y casos de uso del sistema.  

### Abreviaturas Técnicas
- **ED**: Estructuras de Datos  
- **CRUD**: Create, Read, Update, Delete (operaciones que se aplicarán a tareas y registros en base de datos futura)  
- **API**: Conjunto de funciones para interactuar con sistemas o módulos del programa  
- **GUI**: Graphical User Interface, en nuestro caso implementada con **Swing**  
- **FIFO / LIFO**: First In First Out / Last In First Out, principios de funcionamiento de colas y pilas  

---

## 📖 Bibliografía (Formato APA)

### 📚 Referencias Académicas
1. **Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, R. L. (2022).** *Introduction to Algorithms* (4th ed.). MIT Press.  
   _Utilizado para el estudio de algoritmos y estructuras de datos aplicadas en la gestión de tareas._

2. **Weiss, M. A. (2020).** *Data Structures and Algorithm Analysis in Java* (3rd ed.). Pearson Education.  
   _Referencia principal para la implementación de pilas, colas y listas en Java._

3. **Silberschatz, A., Galvin, P. B., & Gagne, G. (2018).** *Operating System Concepts* (10th ed.). John Wiley & Sons.  
   _Consultado para entender conceptos de concurrencia y manejo de procesos en sistemas._

### 💻 Referencias Técnicas
1. **Oracle Corporation. (2024).** *Java SE 17 Documentation: Collections Framework*.  _Documentación oficial de Java para el manejo de colecciones, listas, colas y pilas._

2. **Fowler, M. (2018).** *Patterns of Enterprise Application Architecture* (2nd ed.). Addison-Wesley Professional.  
   _Consultado para aplicar patrones de diseño como MVC en la organización del proyecto._

---

## 🎯 Objetivos de Aprendizaje Alcanzados

### Conceptos de Estructuras de Datos
- **Implementación práctica de pilas, colas y listas** para la gestión de tareas internas y incidencias críticas.  
- **Análisis de complejidad temporal y espacial** de operaciones en Stack, Queue y LinkedList, evaluando eficiencia en escenarios de alta concurrencia de tareas.  
- **Diseño de estructuras de datos eficientes** adaptadas a distintos tipos de tareas: urgentes (Stack), regulares (Queue) y departamentales (LinkedList).  
- **Optimización del rendimiento** mediante selección de la estructura de datos correcta para cada tipo de tarea y flujo de trabajo.  

### Habilidades de Ingeniería de Software
- **Aplicación de patrones de diseño** básicos y buenas prácticas para mantener el código organizado y modular.  
- **Documentación técnica clara y profesional**, incluyendo diagramas UML y explicación de estructuras y flujo de tareas.  
- **Metodología de desarrollo estructurada**, planificando fases de análisis, diseño, implementación y pruebas de manera ordenada.  

### Competencias Interdisciplinarias
- **Comprensión del dominio de gestión de proyectos internos**, adaptando conceptos de priorización a escenarios de trabajo real.  
- **Trabajo en equipo y coordinación** al gestionar múltiples tipos de tareas y usuarios en el sistema.  
- **Comunicación técnica efectiva**, explicando flujos de tareas, estructuras utilizadas y resultados a compañeros o evaluadores.  

---

## 👨‍💻 Desarrolladores  

<table>
  <tr>
    <td width="160" align="center">
      <img src="assets/img/Andres.jpg" alt="Andres" width="120" height="120">
    </td>
    <td width="160" align="center">
      <img src="assets/img/Samu.png" alt="Samu" width="120" height="120">
    </td>
    <td width="160" align="center">
      <img src="assets/img/Pablo.jpg" alt="Pablo" width="120" height="120">
    </td>
    <td width="160" align="center">
      <img src="assets/img/Gael.jpg" alt="Gael" width="120" height="120">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Andres Abarca</b></td>
    <td align="center"><b>Samuel Martínez</b></td>
    <td align="center"><b>Pablo Núñez</b></td>
    <td align="center"><b>Gael Marroquín</b></td>
  </tr>
</table>

<p align="center">
  <img src="assets/img/evidencia.jpg" alt="Foto Evidencia" width="300" height="300">
</p>

## 🔚 Conclusiones y Agradecimientos

El desarrollo del Sistema de Gestión de Tareas de TechNova ha permitido aplicar de manera práctica los conocimientos adquiridos en estructuras de datos y programación orientada a objetos. Los principales logros incluyen:

- **Implementación efectiva de pilas, colas y listas**, adaptadas a distintos tipos de tareas: urgentes, administrativas y departamentales.  
- **Optimización del flujo de trabajo**, priorizando incidencias críticas y garantizando que las tareas regulares se procesen en orden de llegada.  
- **Desarrollo de una interfaz gráfica intuitiva**, que permite a los usuarios interactuar con el sistema de forma eficiente y sencilla.  
- **Documentación completa y profesional**, incluyendo diagramas UML, explicación de estructuras de datos aplicadas y casos de uso.  
- **Preparación para futuras mejoras**, como persistencia de datos, reportes automáticos y ampliación de funcionalidades.  

### Impacto Académico y Práctico
Este proyecto ha permitido integrar conocimientos de programación, estructuras de datos, diseño de software y gestión de procesos internos. Además, ha demostrado cómo los conceptos teóricos pueden aplicarse a un escenario práctico, mejorando la organización y eficiencia de tareas dentro de una empresa.

### Agradecimientos
- A **la profesora Blanca Aracely Aranda Machorro**, por su guía y apoyo en el desarrollo académico del proyecto.  
- A **compañeros y colaboradores**, por la revisión, sugerencias y apoyo durante la implementación del sistema.  
- A **la Universidad TecMilenio**, por proporcionar el entorno académico y los recursos tecnológicos necesarios.  
