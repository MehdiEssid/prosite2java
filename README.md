# prosite2java

class Animal {
    String family;
    String name;
    int age;
    boolean isMammal;

    
    public Animal(String family, String name, int age, boolean isMammal) {
        this.family = family;
        this.name = name;
        this.age = age;
        this.isMammal = isMammal;
    }

    
    public String toString() {
        return "Animal [family=" + family + ", name=" + name + ", age=" + age + ", isMammal=" + isMammal + "]";
    }
}


class Zoo {
    Animal[] animals; // tableau d’animaux
    String name;
    String city;
    int nbrCages;

  
    public Zoo(String name, String city, int nbrCages) {
        this.name = name;
        this.city = city;
        this.nbrCages = nbrCages;
        this.animals = new Animal[25]; // max 25 animaux
    }

   
    public void displayZoo() {
        System.out.println("Zoo name: " + name);
        System.out.println("City: " + city);
        System.out.println("Number of cages: " + nbrCages);
    }


    public String toString() {
        return "Zoo [name=" + name + ", city=" + city + ", nbrCages=" + nbrCages + "]";
    }
}

public class Main {
    public static void main(String[] args) {
      
        Animal lion = new Animal("Felidae", "Lion", 5, true);
        Animal elephant = new Animal("Elephantidae", "Elephant", 10, true);
        Animal snake = new Animal("Serpentes", "Cobra", 2, false);

        System.out.println(lion);
        System.out.println(elephant);
        System.out.println(snake);

        Zoo myZoo = new Zoo("MyZoo", "Tunis", 20);

      
        myZoo.displayZoo();

      
        System.out.println(myZoo);
    }
}
