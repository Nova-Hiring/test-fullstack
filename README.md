# Tablero Kanban con React & DnD-kit
Experimenta el poder de la organización y gestión de tareas con nuestro Tablero Kanban desarrollado usando React, TypeScript, Tailwind CSS y DnD-kit. Mantén el control de tus tareas y proyectos sin esfuerzo.

## ⚙️ Stack Tecnológico:

- React con Vite
- TypeScript
- Tailwind CSS
- DnD-kit

## Características :point_down:
- Crear, editar y eliminar columnas
- Añadir, eliminar y editar tareas
- Arrastrar tareas dentro de su propia columna
- Arrastrar tareas entre diferentes columnas

## Cómo ejecutar localmente :thinking:
- Asegúrate de tener Node.js y npm instalados.
- Clona el repositorio: `git clone https://github.com/Muhammad-Faizan-Tariq/kanban-board-react-dnd-kit.git`
- Instala las dependencias: `npm i tailwind @dnd-kit/core @dnd-kit/sortable @heroicons/react`
- Inicia el servidor de desarrollo: `npm run dev`
- Abre tu navegador y visita: `http://localhost:5173`

---

# Prueba Técnica - Kanban Board con Tasks Ejecutables

### Contexto del Proyecto

Este es un tablero Kanban interactivo construido con React, TypeScript y @dnd-kit para funcionalidad de drag & drop. Actualmente permite:
- Crear y eliminar columnas
- Crear y eliminar tasks dentro de cada columna
- Reorganizar columnas y tasks mediante drag & drop
- Editar el contenido de tasks y columnas inline

### Objetivo de la Tarea

Extender la funcionalidad del tablero Kanban para que las tasks no sean solo texto estático, sino acciones ejecutables. El sistema debe permitir crear diferentes tipos de tasks y ejecutarlas en orden mediante un botón "Play" en cada columna.

### Requisitos Funcionales

#### 1. Modal de Creación de Tasks

Al hacer clic en el botón "Add task" de una columna, debe abrirse un modal que permita al usuario:

- **Seleccionar el tipo de task** entre tres opciones:
  - Toast de Error
  - Toast de Éxito
  - ChatGPT Query

- **Introducir el contenido** de la task según su tipo:
  - Para **Toasts**: Un mensaje de texto que se mostrará en el toast
  - Para **ChatGPT Query**: Un prompt/pregunta que se enviará a la API de OpenAI

#### 2. Diferenciación Visual de Tasks

Cada tipo de task debe ser visualmente distinguible en el tablero:

- **Toast de Error**: Debe tener un estilo/color que indique error (rojo/naranja)
- **Toast de Éxito**: Debe tener un estilo/color que indique éxito (verde)
- **ChatGPT Query**: Debe tener un estilo/color diferente que lo identifique (azul/morado/otro)

El usuario debe poder identificar el tipo de task de un vistazo.

#### 3. Botón "Play" en Columnas

Cada columna debe tener un botón "Play" (puede ser un icono de play ▶️) que:

- Al hacer clic, ejecute todas las tasks de esa columna **en orden secuencial**
- Las tasks se ejecutan una tras otra automáticamente
- Las ejecuciones deben tener un delay apropiado entre ellas para que el usuario pueda observar los resultados

#### 4. Ejecución de Tasks

Cuando se ejecuta una task, debe comportarse según su tipo:

**Toast de Error**
- Mostrar un toast de error con el mensaje definido en la task
- Usar un color/estilo apropiado para errores
- El toast debe desaparecer automáticamente después de unos segundos

**Toast de Éxito**
- Mostrar un toast de éxito con el mensaje definido en la task
- Usar un color/estilo apropiado para mensajes exitosos
- El toast debe desaparecer automáticamente después de unos segundos

**ChatGPT Query**
- Enviar el prompt de la task a la API de ChatGPT
- Mostrar la respuesta de ChatGPT en un toast o modal
- Manejar estados de carga mientras se espera la respuesta
- Manejar posibles errores de la API

#### 5. Integración con ChatGPT API

Para las tasks de tipo ChatGPT, debes integrar la API de OpenAI:

**API Key de OpenAI:**
```
Enviada por email
```

Usa esta API key para hacer llamadas a la API de OpenAI (puedes incluirla directamente en el código para esta prueba).

### Criterios de Aceptación

**Funcionalidad**
- [ ] El modal de creación permite seleccionar entre los 3 tipos de task
- [ ] Cada tipo de task se visualiza de manera diferente en el tablero
- [ ] El botón "Play" ejecuta todas las tasks de la columna en orden
- [ ] Los toasts de error y éxito se muestran correctamente
- [ ] Las queries de ChatGPT se envían y las respuestas se muestran al usuario
- [ ] Las ejecuciones son secuenciales con delays apropiados

**Experiencia de Usuario**
- [ ] El modal es intuitivo y fácil de usar
- [ ] Los diferentes tipos de task son claramente distinguibles
- [ ] Los toasts son visibles y se comportan correctamente
- [ ] Hay feedback visual durante la ejecución de tasks (loading, estados, etc.)
- [ ] Los errores se manejan de manera apropiada

**Código**
- [ ] Se mantiene el uso de TypeScript
- [ ] El código es limpio y mantenible

### Recursos Técnicos

- **Documentación OpenAI API**: https://platform.openai.com/docs/api-reference
- **Modelo recomendado**: gpt-5-mini-2025-08-07

### Consideraciones

- Tienes libertad para elegir las librerías que consideres necesarias (para modales, toasts, etc.)
- Puedes modificar la estructura de datos existente (tipos Task y Column) según lo necesites
- El diseño visual debe ser consistente con el estilo actual del proyecto
- No es necesario persistir las tasks en una base de datos (el estado en memoria es suficiente)

### Tiempo Estimado

Esta tarea debería tomar aproximadamente **3-5 horas** para un desarrollador fullstack con experiencia en React.

---

**¡Buena suerte!** Si tienes dudas sobre los requisitos, no dudes en hacer suposiciones razonables y documentarlas en tu código o en un README.
