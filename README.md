# README.md
# Proyecto Estudiante

## Instalación y Configuración

### Requisitos
- JDK 11
- IntelliJ IDEA
- Git

### Instalación del JDK
1. Visita [Java SE Development Kit 11 Downloads](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Descarga e instala el JDK 11 según tu sistema operativo.

### Instalación de IntelliJ IDEA
1. Visita [JetBrains IntelliJ IDEA](https://www.jetbrains.com/idea/download/).
2. Descarga e instala IntelliJ IDEA Community o Ultimate.

### Instalación de Git
1. Visita [Git SCM Downloads](https://git-scm.com/).
2. Descarga e instala Git según tu sistema operativo.

## Uso del Programa

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/ProyectoEstudiante.git
   cd ProyectoEstudiante


### 2. Archivo `.gitignore`

```plaintext
# Archivos compilados de Java
*.class

# Archivos de proyecto de IntelliJ IDEA
.idea
*.iml
out/

# Archivos temporales del sistema
*.swp

public class Estudiante {
    private String nombre;
    private int[] calificaciones;

    public Estudiante(String nombre, int[] calificaciones) {
        this.nombre = nombre;
        this.calificaciones = calificaciones;
    }

    public double calcularPromedio() {
        int suma = 0;
        for (int calificacion : calificaciones) {
            suma += calificacion;
        }
        return (double) suma / calificaciones.length;
    }

    public char obtenerCalificacion(double promedio) {
        if (promedio <= 50) {
            return 'F';
        } else if (promedio <= 60) {
            return 'E';
        } else if (promedio <= 70) {
            return 'D';
        } else if (promedio <= 80) {
            return 'C';
        } else if (promedio <= 90) {
            return 'B';
        } else {
            return 'A';
        }
    }

    public void imprimirResultados() {
        double promedio = calcularPromedio();
        char calificacion = obtenerCalificacion(promedio);
        System.out.println("Nombre del estudiante: " + nombre);
        for (int i = 0; i < calificaciones.length; i++) {
            System.out.println("Calificación " + (i + 1) + ": " + calificaciones[i]);
        }
        System.out.println("Promedio: " + promedio);
        System.out.println("Calificación: " + calificacion);
    }
}


public class Main {
    public static void main(String[] args) {
        int[] calificaciones = {85, 90, 78, 88, 92};
        Estudiante estudiante = new Estudiante("Juan Perez", calificaciones);
        estudiante.imprimirResultados();
    }
}


mkdir src


git add README.md .gitignore src/Estudiante.java src/Main.java


git commit -m "Inicializar proyecto con archivos de configuración y código"
git push origin develop

git add diagrama_flujo.png diagrama_clases.png
git commit -m "Añadir diagrama de flujo y diagrama de clases"
git push origin develop

