# 🎲 Juego de Dados - Estructuras de Datos

Un juego de dados interactivo desarrollado en Java que implementa diversas estructuras de datos para gestionar jugadores, premios, castigos y el historial del juego.

## 📋 Descripción

Este proyecto es un juego de dados donde los jugadores compiten para llegar primero a la meta. El juego utiliza múltiples estructuras de datos para gestionar el flujo del juego, incluyendo colas para los jugadores, pilas para premios y castigos, listas circulares y dobles para el historial, y un árbol binario para el sistema de ayuda.

## ✨ Características

- **Hasta 4 jugadores**: Soporta de 1 a 4 jugadores simultáneos
- **Sistema de premios y castigos**: Los jugadores reciben premios si obtienen números pares y castigos si obtienen números impares
- **Meta configurable**: La posición máxima del tablero es configurable (20, 30, 40, 50, 60, 70, 80, 90, 100)
- **Sistema de rebote**: Si un jugador se pasa de la meta, rebota hacia atrás
- **Historial de movimientos**: Registro completo de todos los movimientos de cada jugador
- **Estado del juego**: Visualización del estado actual de todos los jugadores
- **Chatbot de ayuda**: Sistema interactivo de preguntas y respuestas sobre el juego
- **Interfaz gráfica**: Utiliza JOptionPane para una experiencia de usuario amigable

## 🏗️ Estructuras de Datos Implementadas

El proyecto implementa las siguientes estructuras de datos:

### Colas (Queue)
- **ColaJugadores**: Gestiona el orden de turnos de los jugadores
- **ColaPremios**: Cola para premios (aunque también se usa como pila)

### Pilas (Stack)
- **PilaPremios**: Almacena los premios disponibles (+2, +8, +0)
- **PilaCastigos**: Almacena los castigos disponibles (-3, -1, -5)

### Listas
- **ListaCircular**: Para mostrar el estado actual del juego
- **ListaDobleCircular**: Para el historial de jugadores (bitácora)
- **ListaDobleMovimientos**: Para el historial individual de cada jugador
- **ListaEnlazada**: Lista enlazada simple

### Árboles
- **Arbolbinario**: Árbol binario de búsqueda para el sistema de ayuda y preguntas

### Nodos
- **Nodo**: Nodo básico para listas enlazadas
- **NodoCircular**: Nodo para listas circulares
- **NodoDoble**: Nodo para listas dobles
- **NodoJugador**: Nodo específico para la cola de jugadores
- **NodoPremio**: Nodo para premios
- **NodoCastigo**: Nodo para castigos
- **NodoArbol**: Nodo para el árbol binario
- **NodoPregunta**: Nodo para preguntas del chatbot

## 🎮 Reglas del Juego

1. Cada jugador lanza **dos dados** en su turno
2. Se suma el resultado de ambos dados para avanzar en el tablero
3. **Si el número es par**: El jugador recibe un premio (avanza posiciones adicionales)
4. **Si el número es impar**: El jugador recibe un castigo (retrocede posiciones)
5. **Castigo especial (-1)**: Si un jugador recibe el castigo -1, regresa a la posición 1
6. **Meta**: El primer jugador en llegar exactamente a la meta gana
7. **Rebote**: Si un jugador se pasa de la meta, rebota hacia atrás

## 📦 Requisitos

- **Java**: Versión 17 o superior
- **Maven**: Para la gestión de dependencias y compilación
- **Sistema Operativo**: Windows, Linux o macOS

## 🚀 Instalación

1. Clona o descarga el repositorio:
```bash
git clone <url-del-repositorio>
cd JUEGO-DE-DADOS
```

2. Navega al directorio del proyecto:
```bash
cd GAME-ESTRUCTURA-DE-DATOS/GAME
```

3. Compila el proyecto con Maven:
```bash
mvn clean compile
```

4. Ejecuta el juego:
```bash
mvn exec:java
```

O ejecuta directamente el JAR compilado:
```bash
java -jar target/GAME-1.0-SNAPSHOT.jar
```

## 💻 Uso

1. Al iniciar el juego, selecciona **"Jugar"** en el diálogo de bienvenida
2. Selecciona la cantidad de jugadores (1-4)
3. Ingresa el nombre de cada jugador
4. En el menú principal, puedes:
   - **Iniciar Juego**: Comenzar a jugar turnos
   - **Editar Partida**: Configurar la posición máxima y permitir más jugadores
   - **Editar/Añadir Jugadores**: Agregar o eliminar jugadores
   - **Listar Premios/Castigos**: Ver los premios y castigos disponibles
   - **Mantener Pilas**: Ver el estado de las pilas de premios y castigos
   - **Estado Actual Del Juego**: Ver las posiciones actuales de todos los jugadores
   - **Ver Historial**: Consultar el historial completo de movimientos
   - **Ayuda**: Acceder al FAQ y al chatbot de ayuda
   - **Salir**: Terminar el juego

## 📁 Estructura del Proyecto

```
JUEGO-DE-DADOS/
├── GAME-ESTRUCTURA-DE-DATOS/
│   └── GAME/
│       ├── pom.xml
│       ├── src/
│       │   └── main/
│       │       └── java/
│       │           └── gamepack/
│       │               ├── GAME.java              # Clase principal
│       │               ├── Jugador.java           # Clase del jugador
│       │               ├── ColaJugadores.java     # Cola de jugadores
│       │               ├── ColaPremios.java      # Cola de premios
│       │               ├── PilaPremios.java      # Pila de premios
│       │               ├── PilaCastigos.java     # Pila de castigos
│       │               ├── ListaCircular.java     # Lista circular
│       │               ├── ListaDobleCircular.java # Lista doble circular
│       │               ├── ListaDobleMovimientos.java # Lista doble para movimientos
│       │               ├── ListaEnlazada.java    # Lista enlazada simple
│       │               ├── Arbolbinario.java      # Árbol binario
│       │               ├── Chatbot.java           # Sistema de ayuda
│       │               └── Nodos/                 # Varios tipos de nodos
│       └── target/                                # Archivos compilados
└── README.md
```

## 👥 Autores

- **Bryan**
- **Bustax**
- **Chelo**
- **Fabia** (Chatbot y Árbol Binario)

## 📝 Versión

**Versión actual**: 2.1.8

## 🎯 Funcionalidades Adicionales

### Chatbot de Ayuda
El juego incluye un chatbot interactivo que puede responder preguntas sobre:
- Número de jugadores permitidos
- Sistema de premios (números pares)
- Sistema de castigos (números impares)
- Cómo ganar el juego

### Historial de Movimientos
Cada jugador tiene un historial completo de sus movimientos, almacenado en una lista doble enlazada que permite navegar hacia adelante y hacia atrás.

### Estado del Juego
El estado actual de todos los jugadores se muestra utilizando una lista circular, permitiendo una visualización ordenada de las posiciones.

## 📄 Licencia

Este proyecto es un trabajo académico desarrollado para demostrar la implementación de estructuras de datos en Java.

## 🤝 Contribuciones

Este es un proyecto académico. Si deseas contribuir o hacer sugerencias, por favor abre un issue o contacta a los autores.

---

¡Disfruta del juego! 🎲🎉

