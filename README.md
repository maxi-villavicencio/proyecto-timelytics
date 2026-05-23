# Proyecto Timelytics
PROGRAMACION I / ALGORITMOS Y ESTRUCTURA DE DATOS I

# Timelytics
Sistema de gestión y análisis de fichadas para empleados. Genera automáticamente reportes en CSV y TXT con estadísticas de horas trabajadas, horas extras, rankings por empleado y por sector.

## Descripción
Timelytics simula y procesa datos de asistencia laboral. Al ejecutarse, genera datos aleatorios de empleados y jornadas, y produce un conjunto de reportes listos para analizar.

Parametros de negocio:
1- Cantidad maxima de empleados: 5
2- Horario de apertura: 10hs y horario de cierre: 22hs
3- Jornada laboral: 8hs
4- Cantidad maxima de horas extra por dia: 4hs
5- Definimos 28 dias laborales por mes

El sistema incluye:
- Autenticación de usuarios con CRUD (crear, modificar, eliminar)
- Generación de datos de empleados y jornadas laborales
- Cálculo de horas extras por empleado y por sector
- Rankings ordenados por horas extras
- Estadísticas globales
- Reportes gráficos en texto (barras ASCII)
- Log de auditoría con timestamps

## Estructura del proyecto

## 🗂️ Estructura del proyecto

    proyecto-tymelitics/
    │
    ├── codigo_timelytics/
    │   ├── main.py               # Punto de entrada del programa
    │   ├── empleados.py          # Generación de empleados aleatorios
    │   ├── jornada.py            # Generación de jornadas laborales
    │   ├── sector.py             # Definición de sectores
    │   ├── diccionario.py        # Estructura central de datos en memoria
    │   ├── ranking_empleado.py   # Ranking de horas extras por empleado
    │   ├── ranking_sector.py     # Ranking de horas extras por sector
    │   ├── horas_liquidadas.py   # Cálculo de horas totales liquidadas
    │   ├── estadisticas.py       # Estadísticas globales del período
    │   ├── reportes_texto.py     # Reportes gráficos con barras ASCII
    │   ├── user.py               # Gestión de usuarios (CRUD)
    │   └── log.py                # Sistema de logging con fecha/hora
    │
    ├── .gitignore
    └── README.md

## Cómo ejecutar

1. Clonar el repositorio:

       git clone https://github.com/maxi-villavicencio/proyecto-timelytics.git
       cd proyecto-timelytics

2. Ejecutar el programa:

       python src/main.py

3. Al iniciarse, el sistema crea automáticamente el usuario administrador:
   - **Usuario:** `ADMIN`
   - **Contraseña:** `1234`

> Este proyecto es de carácter académico/demostrativo. Las credenciales están en texto plano con fines didácticos.

## Archivos generados

Al ejecutar el programa y confirmar la generación de reportes, se crean los siguientes archivos:

| Archivo | Contenido |
|---|---|
| `empleados.csv` | Datos de los 5 empleados generados aleatoriamente |
| `sector.csv` | Sectores de la empresa (RR.HH., Desarrollo, Ventas) |
| `jornada.csv` | Registro de asistencia diaria por empleado |
| `ranking.csv` | Ranking de empleados por horas extras |
| `ranking_sector.csv` | Ranking de sectores por horas extras |
| `horas_liquidadas.csv` | Total de horas trabajadas y extras por empleado |
| `estadisticas_globales.csv` | Totales y promedios del período |
| `reporte_ranking_empleados.txt` | Gráfico de barras ASCII por empleado |
| `reporte_ranking_sector.txt` | Gráfico de barras ASCII por sector |
| `log.txt` | Registro de auditoría con timestamps |

## Módulos principales

### `main.py`
Orquesta el flujo completo: generación de datos → login → CRUD de usuarios → generación de reportes.

### `diccionario.py`
Construye una estructura de datos en memoria cruzando `empleados.csv` y `jornada.csv`. Es la base para los módulos de ranking y estadísticas.

### `reportes_texto.py`
Genera gráficos de barras ASCII escalados proporcionalmente al valor máximo de cada dataset.

### `log.py`
Registra cada acción del sistema con fecha y hora en `log.txt`, útil para auditoría.

## Tecnologías

- **Python 3** — sin dependencias externas, solo biblioteca estándar
- Manejo de archivos CSV y TXT
- Módulo `random` para simulación de datos
- Módulo `datetime` para logging

## 👥 Equipo

- [Maxi Villavicencio](https://github.com/maxi-villavicencio)
- [Anderson Brayner](https://github.com/adsn-brayner)
- [MAteo Fontana](https://github.com/usuario-compañero2)


## 👤 Autor del fork

**Maxi Villavicencio**  
[GitHub](https://github.com/maxi-villavicencio)
