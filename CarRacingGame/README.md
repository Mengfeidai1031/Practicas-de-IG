# JUEGO DE CARRERAS 3D - UNITY

## Introducción

Este es un juego de carreras 3D desarrollado en Unity que ofrece una experiencia completa de selección y conducción de vehículos. El proyecto cuenta con 8 coches diferentes con características únicas, dos modos de juego distintos, y un sistema de generación automática de entornos que hace que la configuración sea mínima.

El juego está diseñado para ser fácil de configurar gracias a scripts automatizados que generan escenas, UI y mecánicas de juego con intervención manual mínima.

---

## Enlace a vídeo demo

Vídeo en Youtube: https://youtu.be/rsmmkvgkd2c

---

## Características y Funcionalidades Principales

### Selección de Coches
- **8 coches disponibles** para elegir antes de cada partida cada una con carácterísticas únicas (velocidad máxima, aceleración, movimiento, etc)
- Navegación intuitiva con botones de izquierda/derecha
- Vista previa 3D de cada vehículo
- Sistema de guardado que recuerda tu elección

<img width="1484" height="835" alt="image" src="https://github.com/user-attachments/assets/a43b0e44-56a7-420d-aa52-75cd443f3f09" />

### Dos Modos de Juego

<img width="1496" height="839" alt="image" src="https://github.com/user-attachments/assets/a1460a8b-681e-4727-8a96-1de829dde7e4" />

#### 1. **Atrapa las Monedas**
- Entorno procedural tipo **bosque** con árboles y rocas
- **5 monedas de oro** distribuidas aleatoriamente
- **Minimapa** que muestra tu posición y la ubicación de las monedas
- **Contador de monedas** recogidas (X/5)
- **Cronómetro** para medir tu tiempo
- Panel de victoria al completar el desafío

<img width="1492" height="838" alt="image" src="https://github.com/user-attachments/assets/260aff8a-eb80-492b-b3c3-b8c78939722a" />

#### 2. **Prueba tu Coche**
- Pista estilo **carretera** con asfalto gris y líneas blancas
- Circuito con **8 checkpoints invisibles**
- Sistema de **2 vueltas** para completar la prueba
- **Cronómetro** con precisión de milisegundos
- Registro de **mejor tiempo**
- Ideal para comparar el rendimiento de diferentes coches

<img width="1496" height="830" alt="image" src="https://github.com/user-attachments/assets/03eb881a-52ff-4e6e-b116-3a7c3da4cdbf" />

### Interfaz de Usuario
- **UI limpia y moderna** con textos blancos sobre fondos semi-transparentes
- **Botón "← SALIR"** en ambos modos de juego para regresar a la selección
- **Contadores en tiempo real** visibles durante el juego
- **Paneles de victoria/finalización** con opciones de reiniciar o volver al menú

### Generación Automática de Entornos
- **Terreno procedural** con césped verde
- **Árboles y rocas** colocados aleatoriamente en el modo monedas
- **Carretera realista** con líneas blancas en el modo prueba
- **Iluminación direccional** automática

---

## Controles de Teclado para los Coches

### Movimiento Básico
| Tecla | Acción |
|-------|--------|
| **W** o **↑** | Acelerar hacia adelante |
| **S** o **↓** | Reversa |
| **A** o **←** | Girar a la izquierda |
| **D** o **→** | Girar a la derecha |
| **ESPACIO** | Freno de mano |

### Navegación de Menús
| Tecla | Acción |
|-------|--------|
| **Click Izquierdo** | Seleccionar botones |
| **Botón "<"** | Coche anterior |
| **Botón ">"** | Coche siguiente |
| **SELECCIONAR** | Confirmar elección |
| **← SALIR** | Volver a selección de coches |

---

### Sistema de Setup Automático

#### **AutoSetup.cs**
Script principal que genera todas las escenas y componentes de UI automáticamente.

**Funcionalidades**:
- Crea las 4 escenas del proyecto
- Genera toda la interfaz de usuario (botones, textos, paneles)
- Configura cámaras e iluminación
- Añade escenas al Build Settings automáticamente
- Detecta automáticamente los coches importados del Asset Store

**Menú de Unity**: `Game Setup`

**Opciones del Menú**:
1. **Create All Scenes** - Crea las 4 escenas vacías
2. **Find Car Prefabs Automatically** - Busca los modelos de coches en el proyecto
3. **Setup Car Selection Scene** - Configura la escena de selección completa
4. **Setup Main Menu Scene** - Configura el menú principal
5. **Setup Game Scenes (Coin & Test)** - Configura ambos modos de juego
6. **Add Scenes to Build Settings** - Añade todas las escenas al build

<img width="797" height="216" alt="image" src="https://github.com/user-attachments/assets/8f4ea206-af05-4707-9fbb-b00457f7473b" />

**Uso**:
```
1. Importar asset pack de coches
2. Ejecutar "Game Setup > 1. Create All Scenes"
3. Ejecutar "Game Setup > 2. Find Car Prefabs Automatically"
4. Ejecutar "Game Setup > 3. Setup Car Selection Scene"
5. Ejecutar "Game Setup > 4. Setup Main Menu Scene"
6. Ejecutar "Game Setup > 5. Setup Game Scenes (Coin & Test)"
7. Ejecutar "Game Setup > 6. Add Scenes to Build Settings"
8. Asignar manualmente los 8 coches en los CarSpawner
9. ¡Jugar!
```

---

## 🚀 Inicio Rápido

### Requisitos
- Unity 2022.3 LTS o superior
- Asset Pack: "Low Poly Car Vehicle Pack" (o similar con 8 coches)

### Configuración en 5 Minutos

1. **Importar Asset de Coches**
   ```
   Window > Asset Store > Buscar "Low Poly Car Vehicle Pack" > Import
   ```

2. **Copiar Scripts**
   - Crear carpeta `Assets/Scripts`
   - Copiar los 12 scripts principales

3. **Ejecutar Setup Automático**
   ```
   Game Setup > 1. Create All Scenes
   Game Setup > 2. Find Car Prefabs Automatically
   Game Setup > 3. Setup Car Selection Scene
   Game Setup > 4. Setup Main Menu Scene
   Game Setup > 5. Setup Game Scenes (Coin & Test)
   Game Setup > 6. Add Scenes to Build Settings
   ```

4. **Asignar Coches Manualmente**
   - Abrir escena CarSelection
   - Seleccionar GameManager
   - Arrastrar 8 coches al array "Car Prefabs"
   - Repetir en CoinCollection > CarSpawner
   - Repetir en TestTrack > CarSpawner
  
<img width="486" height="680" alt="image" src="https://github.com/user-attachments/assets/9d174f24-fad8-40e6-a2bf-69954dab7e4a" />

5. **Configurar Input**
   ```
   Edit > Project Settings > Player > Active Input Handling
   → Cambiar a "Input Manager (Old)" o "Both"
   → Reiniciar Unity
   ```

6. **¡Jugar!**
   - Abrir CarSelection
   - Presionar Play ▶
   - Disfrutar

---

## Notas Técnicas

### Sistema de Física
- Utiliza WheelColliders de Unity para física realista de ruedas
- Rigidbody con interpolación para movimiento suave
- Centro de masa ajustado para estabilidad
- Fricción y suspensión configuradas por script

### Sistema de Guardado
- Usa PlayerPrefs para guardar el coche seleccionado
- Persiste entre sesiones del juego
- Guarda índice y nombre del coche

### Optimización
- Materiales creados una sola vez y reutilizados
- Destrucción de colliders innecesarios (líneas de carretera)
- Generación procedural eficiente
- Checkpoints invisibles para mejor rendimiento

---

## Créditos

**Desarrollado con**:
- Unity 2022.3 LTS
- C# 
- Sistema de generación procedural personalizado
- Scripts de automatización custom

<img width="3840" height="2160" alt="image" src="https://github.com/user-attachments/assets/8d46a22b-5380-4849-ab47-b88f9698f243" />

**Asset Pack de Coches**:
- Low Poly Car Vehicle Pack (Unity Asset Store)

<img width="1200" height="630" alt="image" src="https://github.com/user-attachments/assets/769af122-2cce-413a-8068-73c7d2837b84" />

**IA**
- Claude sonnet 4.5

<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/c337c662-f469-471d-95dd-d2b4c0af4b52" />

---

## Autor

**Meng Fei Dai**  
[GitHub: @Mengfeidai1031](https://github.com/Mengfeidai1031)
