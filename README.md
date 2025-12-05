# Desarrollo de software utilizando Rust
![Rust](https://img.shields.io/badge/Rust-1.x-orange?logo=rust)
![Status](https://img.shields.io/badge/status-en%20desarrollo-yellow)

Este repositorio reune una serie de implementaciones en Rust orientadas al estudio práctico de algoritmos fundamentales, técnicas numéricas y modelos de concurrencia. El objetivo principal es construir un entorno claro y modular donde sea posible analizar cómo Rust resuelve problemas clásicos con un enfoque centrado en seguridad de la memoria, control explícito de recursos y rendimiento nativo.

## 🔒 Antes de comenzar: *¿Por que elegir Rust?*
Rust se destaca por su sistema de **ownership y borrowing**, que elimina problemas comunes como accesos inválidos, data races y fugas de memoria sin depender de un recolector de basura. Este proyecto utiliza estos principios para explorar la ejecución de algoritmos desde cero, analizar su comportamiento y comparar estrategias bajo un entorno seguro y predecible. 

Además, la ausencia de *runtime y el compilador optimizado* permiten medir y estudiar implementaciones con una precisión cercana a lenguajes de bajo nivel.

<br>

# 🗂️ Arquitectura del proyecto
La estructura del repositorio está diseñada para favorecer la extensibilidad. Cada área temática **—ordenamientos, métodos numéricos, concurrencia y utilidades—** se encuentra encapsulada en módulos independientes, permitiendo desarrollar nuevas técnicas, reemplazar algoritmos, agregar pruebas o evolucionar la arquitectura sin generar conflictos entre los componentes existentes. Esta organización también refleja la forma idiomática en que se estructuran proyectos de Rust de mediana a gran escala.

```bash
src/
├── main.rs
├── utils/                          
│   ├── format_arrays.rs
│   ├── format_input.rs
│   ├── format_space.rs
│   └── mod.rs
├── sorting_algorithms/             
│   ├── menu.rs
│   ├── sort_bubble.rs
│   ├── sort_heap.rs
│   ├── sort_insertion.rs
│   ├── sort_merge.rs
│   ├── sort_quick.rs
│   ├── sort_selection.rs
│   ├── strategy.rs
│   └── mod.rs
├── numerical_methods/              
│   ├── interpolation_and_regression/
│   ├── linear_systems/
│   ├── root_finding/
│   ├── menu.rs
│   └── mod.rs
├── concurrence/                    
│   ├── example_semaphore_crossing.rs
│   ├── example_shared_counter.rs
│   ├── example_task_scheduler.rs
│   ├── menu.rs
│   └── mod.rs
└── README.md                    
```


## 🦀 Propósito Técnico del Proyecto

El proyecto busca ofrecer un entorno de experimentación donde se pueda:
- Estudiar cómo Rust maneja memoria en algoritmos iterativos y recursivos.

- Explorar la relación entre estructuras de datos y el sistema de tipos.

- Comprender técnicas numéricas implementadas desde cero sin dependencias externas.

- Practicar modelos de concurrencia seguros mediante `Arc`, `Mutex`, `Threads` y comunicación entre tareas.

- Analizar rendimiento y estabilidad en implementaciones nativas.

Este repositorio no persigue únicamente implementar soluciones conocidas, sino también mostrar cómo Rust permite construirlas de forma robusta, clara y sin ambigüedades técnicas.

<br>

# ⚙️ Configuración del Entorno de Desarrollo

Rust debe instalarse mediante rustup, disponible para Linux, macOS y Windows. Puede descargarse desde la página oficial del lenguaje. Para ejecutar el proyecto es necesario contar con el toolchain oficial del lenguaje, que incluye:

- **rustc:** compilador de Rust

- **cargo:** herramienta de construcción, pruebas y manejo de dependencias

- **rustup:** instalador y gestor de versiones de Rust

Una vez instalado, el entorno dispondrá automáticamente de todo lo necesario para compilar, ejecutar y testear este proyecto. Con Rust instalado, los comandos principales son:

| Comandos        | Descripcion                     |
|-----------------|---------------------------------|
| cargo build     | Compilar el proyecto            |
| cargo run       | Ejecutar el programa principal  |
| cargo test      | Ejecutar las pruebas integradas |

**Nota:** Rust incorpora de forma nativa un sistema de testing, por lo que no se requieren librerías adicionales para validar el comportamiento del código.

<br>

# 💡  Descripción General de los Componentes
Este repositorio sirve como un banco de pruebas y exploración de varios conceptos fundamentales de la informática, implementados con la filosofía de Rust: seguridad, concurrencia y rendimiento.

### Algoritmos de ordenamiento:
Incluyen versiones desde cero de quicksort, mergesort, heapsort, bubble sort y otros métodos fundamentales. Se prioriza la claridad, el análisis de complejidad y el uso de traits para estrategias de ordenamiento flexibles.

### Métodos numéricos:
Contiene rutinas para resolver sistemas lineales, calcular raíces, interpolar y realizar regresiones. Estas implementaciones exploran estabilidad numérica y manejo explícito de valores mediante el sistema de tipos de Rust.

### Concurrencia:
Ejemplos de sincronización, contadores compartidos, simulaciones y planificación simple de tareas. Se utilizan std::thread, Arc, Mutex y otros componentes para explorar el modelo de concurrencia sin data races.

### Utilidades:
Funciones auxiliares para formateo, entrada y manipulación de datos que permiten mantener la lógica principal limpia y enfocada.

<br>

# 🔜 Expansión y Líneas Futuras
El proyecto está pensado para crecer. Las próximas ampliaciones incluyen:

- Nuevas estructuras de datos (árboles, colas, grafos).

- Benchmarks integrados mediante herramientas especializadas.

- Implementaciones asincrónicas con async/await y tokio.

- Más métodos numéricos y algoritmos avanzados.

<br>

# 🤝 Contribuciones
El repositorio está abierto a mejoras, sugerencias o análisis de implementación. Se aceptan issues y pull requests orientados a extender, mejorar o refactorizar los módulos existentes.