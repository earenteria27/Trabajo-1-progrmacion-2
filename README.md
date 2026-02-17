## 📖 ¿Qué es Markdown?
**Markdown** es un lenguaje de marcado ligero que permite aplicar formato a un texto simple mediante el uso de caracteres especiales (como asteriscos, almohadillas y guiones). Fue diseñado para ser fácil de escribir y, sobre todo, fácil de leer en su forma pura, antes de ser convertido a HTML.

### 1. ¿Qué es un repositorio en Git y cómo se diferencia de un proyecto "normal"?
Un repositorio es un contenedor que almacena no solo los archivos del proyecto, sino también todo el **historial de cambios** y metadatos. La diferencia es la carpeta oculta `.git`: un proyecto normal es solo el estado actual de los archivos; un repositorio permite "viajar en el tiempo" a versiones anteriores.

### 2. Áreas principales de Git
* **Working Directory:** Es la carpeta en tu computadora donde modificas los archivos actualmente.
* **Staging Area (Index):** Un área intermedia donde preparas los cambios que quieres incluir en el próximo commit.
* **Repository:** Donde Git guarda permanentemente los cambios en la base de datos local.

### 3. Representación interna de cambios
Git no guarda "diferencias", sino "instantáneas" (snapshots) mediante:
* **Blob:** Contenido de un archivo.
* **Tree:** Estructura de directorios (vincula nombres de archivos con blobs).
* **Commit:** Snapshot del proyecto con autor, fecha y mensaje.
* **Tag:** Un nombre legible asignado a un commit específico (como una etiqueta de versión v1.0).

### 4. Creación de un commit
Se crea con `git commit -m "mensaje"`. Almacena: la referencia al **tree** (estado de archivos), el autor, el mensaje descriptivo y un puntero al **commit padre** (excepto el primero).

### 5. ¿Git pull vs. Git fetch?
* **`git fetch`:** Descarga los cambios del servidor remoto pero **no los mezcla** con tu trabajo actual. Es solo para "mirar".
* **`git pull`:** Es la combinación de `fetch` + `merge`. Descarga los cambios y los intenta fusionar inmediatamente en tu rama actual.

### 6. ¿Qué es un branch (rama)?
Una rama es simplemente un **puntero móvil** que apunta a un commit específico. Git sabe en qué rama estás gracias a un puntero especial llamado `HEAD`.

### 7. Merge y conflictos
El **merge** une dos ramas. Los conflictos surgen cuando se cambia la misma línea de un archivo en ambas ramas. Se resuelven editando manualmente el archivo, eligiendo qué cambios conservar y haciendo un nuevo commit.

### 8. Área de staging (git add)
Funciona como un filtro. Si omites `git add`, los cambios en tu carpeta no serán registrados en el commit, permitiéndote seleccionar qué archivos están "listos" y cuáles no.

### 9. El archivo .gitignore
Es un archivo de texto donde listas carpetas y archivos que Git debe **ignorar** (como contraseñas, carpetas `node_modules` o archivos temporales). Influye evitando que archivos basura se suban al repositorio.

### 10. Commit amend vs. Nuevo commit
* **`--amend`:** Modifica el último commit realizado (útil para corregir un typo o añadir un archivo olvidado). **Reemplaza** el commit anterior.
* **Nuevo commit:** Crea un nuevo punto en la historia, manteniendo el anterior intacto.

### 11. Git stash
Se usa para **guardar temporalmente** cambios que no están listos para un commit, permitiéndote limpiar tu área de trabajo para cambiar de rama rápidamente. Es útil en emergencias (hotfixes).

### 12. Mecanismos para deshacer cambios
* **`git reset`:** Mueve el puntero de la rama a un estado anterior (puede borrar cambios).
* **`git revert`:** Crea un **nuevo commit** que hace lo opuesto a un commit anterior (es el método más seguro).
* **`git checkout`:** Se usa para cambiar de rama o restaurar archivos específicos a su estado anterior.

### 13. Remotos y Forks
* **Origin:** Nombre por defecto del servidor de donde clonaste el código.
* **Upstream:** Nombre común para el repositorio original de donde hiciste un "fork".
* **Gestión de forks:** Se usa `git remote add upstream [URL]` para mantener tu fork sincronizado con el proyecto original.

### 14. Inspección del historial
* **`git log`:** Muestra la lista de commits realizados.
* **`git diff`:** Muestra las diferencias exactas línea por línea entre archivos.
* **`git show`:** Muestra el contenido detallado de un commit específico.

##  Programación 

### 15. ¿Cuáles son los tipos de datos primitivos en Java?
Java tiene 8 tipos de datos primitivos:
* **Enteros:** `byte`, `short`, `int`, `long`.
* **Punto flotante (decimales):** `float`, `double`.
* **Carácter:** `char`.
* **Lógico:** `boolean` (true/false).

### 16. Estructuras de control de flujo en Java
* **if / else:** Permite ejecutar un bloque de código si se cumple una condición, y otro bloque si no se cumple.
* **switch:** Selecciona uno de muchos bloques de código para ser ejecutado basándose en el valor de una variable.
* **Bucles (for, while, do-while):** Repiten un bloque de código mientras se cumpla una condición específica.

### 17. Importancia de nombres significativos
Es vital para la **legibilidad y mantenimiento** del código. Un nombre como `calcularSalarioTotal()` es mucho más claro que `calc()`. Ayuda a que otros desarrolladores (o tú mismo en el futuro) entiendan qué hace el código sin necesidad de leer línea por línea.

### 18. ¿Qué es la Programación Orientada a Objetos (POO)?
Es un paradigma de programación basado en el concepto de **"objetos"**, los cuales pueden contener datos (atributos) y código (métodos). Busca replicar el funcionamiento de entidades del mundo real en el software.

### 19. Los cuatro pilares de la POO
1.  **Abstracción:** Manejar la complejidad ocultando detalles innecesarios y mostrando solo lo relevante.
2.  **Encapsulamiento:** Agrupar datos y métodos en una unidad (clase) y restringir el acceso directo a algunos componentes.
3.  **Herencia:** Proceso mediante el cual una clase adquiere las propiedades y métodos de otra.
4.  **Polimorfismo:** Capacidad de una entidad de presentar diferentes formas (por ejemplo, un mismo método que se comporta distinto en diferentes clases).

### 20. La Herencia en POO y Java
Permite crear una clase nueva (hija) basada en una clase existente (padre). En Java se utiliza la palabra reservada `extends`. Sirve para **reutilizar código** y crear jerarquías lógicas.

### 21. Modificadores de acceso en Java
Controlan la visibilidad de las clases, métodos y variables. Los más comunes son:
* **public:** Accesible desde cualquier clase.
* **private:** Solo accesible dentro de la propia clase.
* **protected:** Accesible dentro del mismo paquete y por subclases.
* **default (por defecto):** Accesible solo dentro del mismo paquete.

### 22. ¿Qué es una variable de entorno?
Es un valor dinámico cargado en el sistema operativo que puede ser utilizado por los procesos en ejecución.
* **Importancia:** Permiten configurar aspectos del sistema sin cambiar el código (por ejemplo, la ruta de instalación de Java en `JAVA_HOME` o el `PATH` para ejecutar comandos desde cualquier carpeta).

##  Programación Practica

### 1. Calculadora Básica

```java
public class Calculadora {
    public static void main(String[] args) {
        // Valores por defecto
        double num1 = 10;
        double num2 = 5;

        System.out.println("Número 1: " + num1);
        System.out.println("Número 2: " + num2);
        System.out.println("-------------------------");
        System.out.println("Suma: " + (num1 + num2));
        System.out.println("Resta: " + (num1 - num2));
        System.out.println("Multiplicación: " + (num1 * num2));
        System.out.println("División: " + (num1 / num2));
    }
}

public class ContadorLetras {
    public static void main(String[] args) {
        // Palabra Programacion
        String palabra = "programacion";
        int vocales = 0;
        int consonantes = 0;

        for (int i = 0; i < palabra.length(); i++) {
            char letra = palabra.charAt(i);

            if (letra == 'a' || letra == 'e' || letra == 'i' || letra == 'o' || letra == 'u') {
                vocales++;
            } else {
                consonantes++;
            }
        }

        System.out.println("Palabra: " + palabra);
        System.out.println("Vocales: " + vocales);
        System.out.println("Consonantes: " + consonantes);
    }
}

public class InvertirTexto {
    public static void main(String[] args) {
        // Texto por defecto
        String original = "java";
        String invertido = "";

        // Bucle que recorre de atrás hacia adelante
        for (int i = original.length() - 1; i >= 0; i--) {
            invertido = invertido + original.charAt(i);
        }

        System.out.println("Original: " + original);
        System.out.println("Invertido: " + invertido);
    }
}