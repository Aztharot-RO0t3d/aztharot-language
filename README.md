# Documentación del Proyecto Aztharot
---

Aztharot es un lenguaje de programación híbrido diseñado para abordar necesidades tanto de alto nivel (desarrollo rápido de aplicaciones y herramientas) como de bajo nivel (control detallado del hardware y sistemas operativos). Es especialmente útil para:

- Ciberseguridad: Simplificar la creación de herramientas avanzadas como analizadores de redes, pruebas de penetración, y manipulación de datos binarios.
  
- Desarrollo de Interfaces Modernas: Proveer una sintaxis que permita construir aplicaciones visualmente atractivas sin depender de tecnologías externas como CSS o JavaScript.

- Sistemas de Bajo Nivel: Ofrecer herramientas para la creación de sistemas operativos, kernels y bootloaders desde cero.

### Características Principales:

- Sintaxis Minimalista y Híbrida: Diseñada para ser intuitiva, permitiendo tipado dinámico o estático según las necesidades del proyecto.

- Fases Dual (Alto y Bajo Nivel): Perfecto para desarrolladores que necesitan flexibilidad.

- Opciones de Compilación e Interpretación: Ofrece lo mejor de ambos mundos, permitiendo prototipado rápido o generación de binarios eficientes.

---

## Propósito del Proyecto

Aztharot no es solo otro lenguaje de programación. Busca solucionar problemas específicos que enfrentan los desarrolladores:

1. Falta de Lenguajes Híbridos para Ciberseguridad y Sistemas Operativos:
  - La mayoría de los lenguajes están orientados a un ámbito específico (Python para scripts, C para bajo nivel). Aztharot combina ambos mundos.

2. Interfaces Visuales Atractivas sin Complejidad:
  - Reduce la necesidad de depender de múltiples tecnologías para el diseño de UI.

3. Control Total del Hardware:
  - Con herramientas integradas para acceder directamente a registros, memoria, y otros recursos de hardware.
---
## Estructura del Proyecto

La estructura del proyecto está diseñada para maximizar la claridad y la modularidad. Cada carpeta y archivo tiene un propósito definido:
```bash
Aztharot/
├── docs/                      # Documentación completa del proyecto
│   ├── guía-desarrolladores.txt
│   ├── guía-usuarios.txt
│   ├── sintaxis.txt
│   ├── plan_futuro.txt
│   └── cambios_versiones.txt
├── lenguaje/                  # Implementación del lenguaje
│   ├── src/                   # Código fuente del lenguaje
│   │   ├── lexer.asm          # Lexer en Assembly
│   │   ├── parser.asm         # Parser en Assembly
│   │   ├── ast.c              # Generador del AST en C
│   │   ├── codegen.c          # Generador de código intermedio en C
│   │   ├── runtime.c          # Implementación del tiempo de ejecución
│   │   ├── main.c             # Punto de entrada del lenguaje
│   │   └── Makefile           # Script para construir el lenguaje
│   ├── include/               # Archivos de cabecera
│   │   ├── ast.h              # Definición de estructuras del AST
│   │   ├── codegen.h          # Declaraciones del generador de código
│   │   ├── runtime.h          # Funciones auxiliares del tiempo de ejecución
│   │   └── common.h           # Utilidades y constantes comunes
│   ├── pruebas/               # Casos de prueba del lenguaje
│   │   ├── prueba_lexer.asm
│   │   ├── prueba_parser.asm
│   │   ├── prueba_ast.c
│   │   └── prueba_runtime.c
│   ├── ejemplos/              # Ejemplos prácticos en Aztharot
│   │   ├── hola_mundo.azth
│   │   ├── escaneo_puertos.azth
│   │   └── ejemplo_ui.azth
│   └── LEEME.txt              # Información básica
├── compilador/                # Implementación del compilador
│   ├── src/                   # Código fuente del compilador
│   │   ├── lexer.asm          # Lexer en Assembly para el compilador
│   │   ├── parser.asm         # Parser en Assembly para el compilador
│   │   ├── ast.c              # AST específico del compilador
│   │   ├── bytecode.c         # Generador de bytecode
│   │   ├── backend.c          # Backend para código nativo
│   │   ├── main.c             # Punto de entrada del compilador
│   │   └── Makefile           # Script para construir el compilador
│   ├── include/               # Archivos de cabecera del compilador
│   │   ├── bytecode.h
│   │   ├── backend.h
│   │   └── common.h
│   ├── pruebas/               # Pruebas unitarias y de integración
│   │   ├── prueba_lexer.asm
│   │   ├── prueba_parser.asm
│   │   ├── prueba_bytecode.c
│   │   └── prueba_backend.c
│   └── LEEME.txt              # Información básica sobre el compilador
├── LICENCIA                   # Licencia del proyecto
├── CONTRIBUIR.txt             # Guía para contribuciones
└── LEEME.txt                  # Descripción del proyecto
```
---
## Explicación de Jerarquia de Archivos

### docs/

Contiene toda la documentación necesaria para desarrolladores y usuarios:

- `guía-desarrolladores.txt`: Explica cómo contribuir al desarrollo del lenguaje.
- `guía-usuarios.txt`: Manual detallado para programadores.
- `sintaxis.txt`: Descripción completa de la sintaxis del lenguaje.
- `plan_futuro.txt`: Ideas y mejoras planificadas para futuras versiones.
-  `cambios_versiones.txt`: Registro de cambios realizados en cada versión.

### lenguaje/src/
- `lexer.asm` y `parser.asm`: Implementan el análisis léxico y sintáctico usando Assembly para control máximo.
- `ast.c`: Crea una representación jerárquica del programa.
- `codegen.c`: Convierte el AST en código intermedio o nativo.
- `runtime.c`: Implementa funciones estándar para el tiempo de ejecución.
- `main.c`: Punto de entrada que coordina todas las etapas del lenguaje.

### compilador/src/
Similar a `lenguaje/src`, pero enfocado en convertir código fuente a bianrios ejecutables.

---
