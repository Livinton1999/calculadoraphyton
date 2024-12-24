// Sistema de Cálculo de Nutrientes
import java.util.*;

class CalculadoraDeNutrientes {
    static class Nutriente {
        String nombre;
        double calorias;
        double proteinas;
        double grasas;
        double carbohidratos;

        public Nutriente(String nombre, double calorias, double proteinas, double grasas, double carbohidratos) {
            this.nombre = nombre;
            this.calorias = calorias;
            this.proteinas = proteinas;
            this.grasas = grasas;
            this.carbohidratos = carbohidratos;
        }
    }

    static final double LIMITE_CALORIAS = 2000.0; // Umbral de aceptabilidad

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Nutriente> ingredientes = new ArrayList<>();

        System.out.println("Ingrese el número de ingredientes:");
        int n = scanner.nextInt();

        for (int i = 0; i < n; i++) {
            System.out.println("Ingrese el nombre del ingrediente:");
            String nombre = scanner.next();
            System.out.println("Ingrese las calorías por gramo:");
            double calorias = scanner.nextDouble();
            System.out.println("Ingrese las proteínas por gramo:");
            double proteinas = scanner.nextDouble();
            System.out.println("Ingrese las grasas por gramo:");
            double grasas = scanner.nextDouble();
            System.out.println("Ingrese los carbohidratos por gramo:");
            double carbohidratos = scanner.nextDouble();

            System.out.println("Ingrese la cantidad consumida en gramos:");
            double gramos = scanner.nextDouble();

            ingredientes.add(new Nutriente(nombre, 
                calorias * gramos, 
                proteinas * gramos, 
                grasas * gramos, 
                carbohidratos * gramos));
        }

        double totalCalorias = 0, totalProteinas = 0, totalGrasas = 0, totalCarbohidratos = 0;

        for (Nutriente ingrediente : ingredientes) {
            totalCalorias += ingrediente.calorias;
            totalProteinas += ingrediente.proteinas;
            totalGrasas += ingrediente.grasas;
            totalCarbohidratos += ingrediente.carbohidratos;
        }

        System.out.println("Valores Nutricionales Totales:");
        System.out.println("Calorías: " + totalCalorias);
        System.out.println("Proteínas: " + totalProteinas);
        System.out.println("Grasas: " + totalGrasas);
        System.out.println("Carbohidratos: " + totalCarbohidratos);

        System.out.println("El valor nutricional de la comida es " + 
            (totalCalorias <= LIMITE_CALORIAS ? "aceptable" : "no aceptable"));
    }
}

// Sistema de Ordenamiento de Películas
class SistemaDeOrdenamientoDePeliculas {
    static class Pelicula {
        String titulo;
        int anio;
        String genero;

        public Pelicula(String titulo, int anio, String genero) {
            this.titulo = titulo;
            this.anio = anio;
            this.genero = genero;
        }

        @Override
        public String toString() {
            return "Título: " + titulo + ", Año: " + anio + ", Género: " + genero;
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Pelicula> peliculas = new ArrayList<>();

        System.out.println("Ingrese el número de películas:");
        int n = scanner.nextInt();

        for (int i = 0; i < n; i++) {
            System.out.println("Ingrese el título de la película:");
            String titulo = scanner.next();
            System.out.println("Ingrese el año de lanzamiento:");
            int anio = scanner.nextInt();
            System.out.println("Ingrese el género:");
            String genero = scanner.next();

            peliculas.add(new Pelicula(titulo, anio, genero));
        }

        peliculas.sort(Comparator.comparingInt(pelicula -> pelicula.anio));

        System.out.println("Películas Ordenadas por Año:");
        for (Pelicula pelicula : peliculas) {
            System.out.println(pelicula);
        }
    }
}
