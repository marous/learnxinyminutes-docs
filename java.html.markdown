---
jazyk: java
přispěvatelé:
    - ["Jake Prather", "http://github.com/JakeHP"]
    - ["Jakukyo Friel", "http://weakish.github.io"]
    - ["Madison Dickson", "http://github.com/mix3d"]
    - ["Simon Morgan", "http://sjm.io/"]
    - ["Zachary Ferguson", "http://github.com/zfergus2"]
    - ["Cameron Schermerhorn", "http://github.com/cschermerhorn"]
    - ["Rachel Stiyer", "https://github.com/rstiyer"]
název souboru: LearnJava.java
---

Java je univerzální, souběžně, třída na bázi, objektově orientované počítačového
programovacího jazyka.
[Více informací zde.](http://docs.oracle.com/javase/tutorial/java/)

```java
// Jednořádkové komentáře začínají  //

/*
Víceřádkové komentáře vypadají takto.
*/

/**
Javadoc komentáře vypadají následovně. Používá se k popisu třídy nebo různých
atributů třídy.
*/

// 
třída import ArrayList uvnitř java.util balíčku
import java.util.ArrayList;
// Import všech tříd uvnitř java.security balíčku
import java.security.*;

// Každý soubor .java obsahuje jeden vnější úrovně veřejné třídy, se stejným názvem
// jako soubor .
public class LearnJava {

    // Aby bylo možné spustit java program, musí mít hlavní metodu jako vstup
     // bod.
    public static void main (String[] args) {

        // Použijte System.out.println() pro tisk řádků.
        System.out.println("Hello World!");
        System.out.println(
            "Integer: " + 10 +
            " Double: " + 3.14 +
            " Boolean: " + true);

        // Chcete-li tisknout bez nového řádku, použijte System.out.print().
        System.out.print("Hello ");
        System.out.print("World");

        // Použijte System.out.printf () pro jednoduchý formátovaný tisk.
        System.out.printf("pi = %.5f", Math.PI); // => pi = 3.14159

        ///////////////////////////////////////
        // proměnné
        ///////////////////////////////////////

        /*
        * Deklerace promenných 
        */
        //Deklerace proměnných užitím  <type> <name>
        int fooInt;
        // Deklerace mnohonásobných proměnných stejného 
        //  typu <type> <name1>, <name2>, <name3>
        int fooInt1, fooInt2, fooInt3;

        /*
        *  Inicializace proměnných
        */

        // Inicializace proměnných použitím<type> <name> = <val>
        int fooInt = 1;
        // Inicializace více proměnných stejného typu s stejnou
        // hodnotou <type> <name1>, <name2>, <name3> = <val>
        int fooInt1, fooInt2, fooInt3;
        fooInt1 = fooInt2 = fooInt3 = 1;

        /*
        * typy proměnných
        */
        // Byte - 8-bitové celé číslo dvojkového typu 
        // (-128 <= byte <= 127)
        byte fooByte = 100;

        // Short - 16-bitové celé číslo dvojkového typu
        
        // (-32,768 <= short <= 32,767)
        short fooShort = 10000;

        // Integer - celé číslo 32-bitové dvojkového doplňku
        // (-2,147,483,648 <= int <= 2,147,483,647)
        int fooInt = 1;

        // Long - 64-bitové celé číslo dvojkového doplňku
        // (-9,223,372,036,854,775,808 <= long <= 9,223,372,036,854,775,807)
        long fooLong = 100000L;
        // L se používá k označení, že tato proměnná hodnota je typu Long;
        // cokoli bez je považováno za celé číslo jako výchozí.

        // Note: Java nemá typy bez znaménka.

        // Float - Jednoduchou přesností 32-bitový IEEE 754 pohyblivou řadovou čarkou Point 
        // 2^-149 <= float <= (2-2^-23) * 2^127
        float fooFloat = 234.5f;
        // f or F se používá k označení, že tato proměnná hodnota je typu float;
        // otherwise it is treated as double.

        // Double - S dvojitou přesností 64-bitový IEEE 754 pohyblivou řadovou čarkou Point
        // 2^-1074 <= x <= (2-2^-52) * 2^1023
        double fooDouble = 123.4;

        // boolean - true & false
        boolean fooBoolean = true;
        boolean barBoolean = false;

        // Char - Jeden 16-bitový Unicode znak
        char fooChar = 'A';

        // finální proměnné nemůžou být přeřazeny do jiného objektu,
        final int HOURS_I_WORK_PER_WEEK = 9001;
        // ale mohou být inicializovány později.
        final double E;
        E = 2.71828;

        // BigInteger -Nezměnitelně libovolná-přesná celá čísla
        //
        // BigInteger je datový typ, který umožňuje programátorům manipulovat
        // celá čísla větší než 64 bitů. Celá čísla jsou uloženy jako soubor
        // bajtů a jsou manipulovány pomocí funkcí zabudovaných do BigInteger
        //
        // BigInteger mohou být inicializovány pomocí pole bajtů nebo řetězeců.      
        BigInteger fooBigInteger = new BigInteger(fooByteArray);

        // BigDecimal - Immutable, arbitrary-precision signed decimal number???????????nechapu výzanm??????????
        //
        // A BigDecimal takes two parts: an arbitrary precision integer 
        // unscaled value and a 32-bit integer scale??????????
        //
        // BigDecimal dovolí programátorovi úplnou kontrolu nad desetinná
        // zaokrouhlování. Doporučuje se používat BigDecimal s hodnotami měn
        // a kde se vyžaduje přesný počet desetinných míst.
        //
        // BigDecimal can be initialized with an int, long, double or String
        // or by initializing the unscaled value (BigInteger) and scale (int).
        BigDecimal fooBigDecimal = new BigDecimal(fooBigInteger, fooInt);
        
        // Dávejte si pozor na konstruktor, který bere float nebo double jako
        // nepřesnost float / double bude zkopírována do BigDecimal.
        //Preferujte řetězec konstruktoru, kdy budete potřebovat přesné hodnoty.
        BigDecimal tenCents = new BigDecimal("0.1");

        // Řetězce
        String fooString = "My String Is Here!";

        // \n je uniklý znak, který začíná nový řádek
        String barString = "Printing on a new line?\nNo Problem!";
        // \t je uniklý znak, který přidává znak tabulátoru
        String bazString = "Do you want to add a tab?\tNo Problem!";
        System.out.println(fooString);
        System.out.println(barString);
        System.out.println(bazString);

        // pole
        // Velikost pole musí být rozhodnuta vytvořením instance
        // Následující formáty pracují pro deklarování pole
        // <datatype>[] <var name> = new <datatype>[<array size>];
        // <datatype> <var name>[] = new <datatype>[<array size>];
        int[] intArray = new int[10];
        String[] stringArray = new String[1];
        boolean boolArray[] = new boolean[100];

        // Další způsob, jak deklarovat a inicializovat pole
        int[] y = {9000, 1000, 1337};
        String names[] = {"Bob", "John", "Fred", "Juan Pedro"};
        boolean bools[] = {true, false, false};

        // Indexování pole - přístupový prvek
        System.out.println("intArray @ 0: " + intArray[0]);

        // Pole jsou nulově indexované a proměnlivé.
        intArray[1] = 1;
        System.out.println("intArray @ 1: " + intArray[1]); // => 1

        // Jiné typy dat stojí za prozkoumání
        // ArrayLists - jsou jako pole s výjimkou více funkcí je k dispozici, a
        //             a velikost je proměnlivá.
        // LinkedLists - Realizace dvojitě propojenýho seznamu. Všechny
        //               operace fungoují tak, jak by mohlo být očekávano pro
        //                dvojitě propojený seznam.
        // Maps - Sada objektů, které mapují klíče k hodnotám. mapa je
        //        an interface and therefore cannot be instantiated.????????????????????????
        //        Typ klíče a hodnoty obsažené v mapě musí
        //        být určen při vytvoření instance prováděcí
        //        třídy. Každý klíč může mapovat pouze na jednu odpovídající hodnotu,
        //        a každý klíč se může objevit pouze jednou (bez duplikátů).
        // HashMaps - Tato třída používá hash tabulky pro realizaci rozhrání
        //            map. To umožňuje dobu zpracování základních
        //            operací, jako je získat a vložit prvek, zůstane
        //            konstantní i pro rozsáhlé sady.

        ///////////////////////////////////////
        // operátory
        ///////////////////////////////////////
        System.out.println("\n->Operators");

        int i1 = 1, i2 = 2; // Zkrácený zápis pro více deklarací

        // Aritmetika je přímočará
        System.out.println("1+2 = " + (i1 + i2)); // => 3
        System.out.println("2-1 = " + (i2 - i1)); // => 1
        System.out.println("2*1 = " + (i2 * i1)); // => 2
        System.out.println("1/2 = " + (i1 / i2)); // => 0 (int/int returns int)
        System.out.println("1/2 = " + (i1 / (double)i2)); // => 0.5

        // Modulo
        System.out.println("11%3 = "+(11 % 3)); // => 2

        // operátory porovnání
        System.out.println("3 == 2? " + (3 == 2)); // => false
        System.out.println("3 != 2? " + (3 != 2)); // => true
        System.out.println("3 > 2? " + (3 > 2)); // => true
        System.out.println("3 < 2? " + (3 < 2)); // => false
        System.out.println("2 <= 2? " + (2 <= 2)); // => true
        System.out.println("2 >= 2? " + (2 >= 2)); // => true

        // logické operátory
        System.out.println("3 > 2 && 2 > 3? " + ((3 > 2) && (2 > 3))); // => false
        System.out.println("3 > 2 || 2 > 3? " + ((3 > 2) || (2 > 3))); // => true
        System.out.println("!(3 == 2)? " + (!(3 == 2))); // => true

        // Bitové operátory!
        /*
        ~      Unární bitový doplněk
        <<     Podepsáný levý shift????????????????????????????????????????????Signed left shift
        >>     Podepsáný / Aritmeticky pravý shift????????????Signed/Arithmetic right shift
        >>>    Nepodepsané / Logický posun vpravo
        &      bitový operátor AND
        ^      exkluzivní bitový operátor exkluzivní OR
        |     inkluzivní bitový operátor OR
        */

        // operátory Inkrementace
        int i = 0;
        System.out.println("\n->Inc/Dec-rementation");
        // ++ a -- operátory přírůstku a úbytku o 1.
        // Pokud jsou umístěny před proměnné, oni zvýši pak vratí;
        // Po návratu proměnné následně zvýší.
        System.out.println(i++); // i = 1, prints 0 (post-increment)
        System.out.println(++i); // i = 2, prints 2 (pre-increment)
        System.out.println(i--); // i = 1, prints 2 (post-decrement)
        System.out.println(--i); // i = 0, prints 0 (pre-decrement)

        ///////////////////////////////////////
        // řídicí struktury
        ///////////////////////////////////////
        System.out.println("\n->Control Structures");

        // pokud jsou výroky c-like
        int j = 10;
        if (j == 10) {
            System.out.println("I get printed");
        } else if (j > 10) {
            System.out.println("I don't");
        } else {
            System.out.println("I also don't");
        }

        // while loop
        int fooWhile = 0;
        while(fooWhile < 100) {
            System.out.println(fooWhile);
            // Increment the counter
            // Iterated 100 times, fooWhile 0,1,2...99
            fooWhile++;
        }
        System.out.println("fooWhile Value: " + fooWhile);

        // Do While Loop
        int fooDoWhile = 0;
        do {
            System.out.println(fooDoWhile);
            // Increment the counter
            // Iterated 99 times, fooDoWhile 0->99
            fooDoWhile++;
        } while(fooDoWhile < 100);
        System.out.println("fooDoWhile Value: " + fooDoWhile);

        // For Loop
        // for loop structure => for(<start_statement>; <conditional>; <step>)
        for (int fooFor = 0; fooFor < 10; fooFor++) {
            System.out.println(fooFor);
            // Iterated 10 times, fooFor 0->9
        }
        System.out.println("fooFor Value: " + fooFor);
        
        // Nested For Loop Exit with Label?????????????
        outer:
        for (int i = 0; i < 10; i++) {
          for (int j = 0; j < 10; j++) {
            if (i == 5 && j ==5) {
              break outer;
              // breaks out of outer loop instead of only the inner one
            }
          }
        }
        
        // pro každý cyklus
        // Cyklus for je také schopen projit pole, stejně jako objekty
        // které realizuje rozhraní Iterable.
        int[] fooList = {1, 2, 3, 4, 5, 6, 7, 8, 9};
        // pro každou strukturu cyklu => for (<object> : <iterable>)
        // čte jako:  pro každý prvek v iterable
        // Poznámka: typ objektu musí odpovídat typu prvku v iterable.
        for (int bar : fooList) {
            System.out.println(bar);
            //Iterates 9 times and prints 1-9 on new lines
        }

        // Switch Case
        // Spínač pracuje s byty, short, char a datovými typy int.
        // Spolupracuje také s vyjmenovanými typy (popsáno v ENUM), 
        // třída String a pár speciálních tříd které obalují primitivní typy:
        // Character, Byte, Short, a Integer.
        int month = 3;
        String monthString;
        switch (month) {
            case 1: monthString = "January";
                    break;
            case 2: monthString = "February";
                    break;
            case 3: monthString = "March";
                    break;
            default: monthString = "Some other month";
                     break;
        }
        System.out.println("Switch Case Result: " + monthString);
        
        // Spouštění v Javě 7 a výše, přepínání Stringů funguje takhle:
        String myAnswer = "maybe";
        switch(myAnswer) {
            case "yes":
                System.out.println("You answered yes.");
                break;
            case "no":
                System.out.println("You answered no.");
                break;
            case "maybe":
                System.out.println("You answered maybe.");
                break;
            default:
                System.out.println("You answered " + myAnswer);
                break;
        }

        // podmínečný zkrácený zápis
        // Můžete použít '?' Operátor pro rychlé zadání nebo logický vidlice.
        // Čte jako "If (tvrzení) je pravdivé, použijte <první hodnoty>, jinak využijte
        // <druhou hodnotou>"
        int foo = 5;
        String bar = (foo < 10) ? "A" : "B";
        System.out.println(bar); // Vypíše A, protože tvrzení je pravdivé

        ////////////////////////////////////////
        // Převedení Datových typů a přetypování
        ////////////////////////////////////////

        // Převedení dat

        // Převdení řetězece na celé číslo
        Integer.parseInt("123");// Vrátí celé číslo verze"123"

        // Převdení celého čísla na řetězec
        Integer.toString(123);//returns a string version of 123

        // U ostatních konverzí vyzkoušejte následující třídy:
        // Double
        // Long
        // String

        // Typecasting
        // Můžete také obsadit Java objekty, je tu spousta detailů a nabídek
        // s některými více zprostředkujícími koncepty. Neváhejte a zkontrolujte si to tady:
        // http://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html

        ///////////////////////////////////////
        // Třídy a funkce
        ///////////////////////////////////////

        System.out.println("\n->Classes & Functions");

        // (Definice třídy Bicycle následovně)

        // Použijte new pro inicializaci třídy
        Bicycle trek = new Bicycle();

        // Volání metody objektů
        trek.speedUp(3); // You should always use setter and getter methods
        trek.setCadence(100);

        // toString vrací řetězcové vyjádření tohoto objektu.
        System.out.println("trek info: " + trek.toString());

        // Double Brace Inicializace
        // jazyk Java nemá synatxi pro jak vytvořit statické kolekce 
        // jednoduchým způsobem. Obvykle skončí následovně:
        private static final Set<String> COUNTRIES = new HashSet<String>();
        static {
           COUNTRIES.add("DENMARK");
           COUNTRIES.add("SWEDEN");
           COUNTRIES.add("FINLAND");
        }

        // Ale je tu fajnový způsob dosažení stejně věci s
        // snáze, pomocí něčeho co se jmenuje Double Brace
        // inicializace.
        private static final Set<String> COUNTRIES = new HashSet<String>() {{
            add("DENMARK");
            add("SWEDEN");
            add("FINLAND");
        }}

        // První závorka je vytvoření nového AnonymousInnerClass a
        // druhá deklaruje instance Inicializátor blok. Tento blok second one declares an instance initializer block. This block???????????????????????????????????????????????????????????????????????????????????????
        // je volán, když je vytvořena anonymní vnitřní třída.
        // To funguje nejen pro sbírky, funguje to pro všechny
        // ne finální třídy.

    } // Konec hlavní metody
} // Konec LearnJava třídy

// Můžete zahrnovat jiné, neveřejné třídy vnější úrovně v souboru .java,
// ale není to dobrým zvykem. Místo toho rozdělit třídy do samostatných souborů.

// Třída Deklarace Syntaxe:
// <public/private/protected> class <class name> {
//    // datová pole, konstruktory, funkce vše uvnitř.
//    // Funkce jsou nazývány jako metody v Javě.
// }

class Bicycle {

    // cyklistovo pole / proměnné
    public int cadence; // Public: Lze přistupovat odkudkoliv
    private int speed;  // Private: přístupné pouze zevnitř třídy
    protected int gear; // Protected: Přístupné ze třídy a podtřídy
    String name; // default: přístupné pouze z tohoto balíčku
    static String className; // Static proměná třídy

    // Static block 
    // Java nemá žádnou implementaci statických konstruktorů, ale
    // má statický blok, který může být použit pro inicializaci proměnné třídy
    // (staticlé proměné). 
    // Tento blok bude volán při načtení třídy.
    static {
        className = "Bicycle";
    }

    // Konstruktory jsou způsoby vytváření tříd
    // Tohle je konstruktor
    public Bicycle() {
        // Můžete také volat jiný konstruktor:
        // this(1, 50, 5, "Bontrager");
        gear = 1;
        cadence = 50;
        speed = 5;
        name = "Bontrager";
    }
    // This is a constructor that takes arguments
    public Bicycle(int startCadence, int startSpeed, int startGear,
        String name) {
        this.gear = startGear;
        this.cadence = startCadence;
        this.speed = startSpeed;
        this.name = name;
    }

    // Method Syntax:
    // <public/private/protected> <return type> <function name>(<args>)

    // Java classes often implement getters and setters for their fields

    // Method declaration syntax:
    // <access modifier> <return type> <method name>(<args>)
    public int getCadence() {
        return cadence;
    }

    // void methods require no return statement
    public void setCadence(int newValue) {
        cadence = newValue;
    }
    public void setGear(int newValue) {
        gear = newValue;
    }
    public void speedUp(int increment) {
        speed += increment;
    }
    public void slowDown(int decrement) {
        speed -= decrement;
    }
    public void setName(String newName) {
        name = newName;
    }
    public String getName() {
        return name;
    }

    //Method to display the attribute values of this Object.
    @Override // Inherited from the Object class.
    public String toString() {
        return "gear: " + gear + " cadence: " + cadence + " speed: " + speed +
            " name: " + name;
    }
} // end class Bicycle

// PennyFarthing is a subclass of Bicycle
class PennyFarthing extends Bicycle {
    // (Penny Farthings are those bicycles with the big front wheel.
    // They have no gears.)

    public PennyFarthing(int startCadence, int startSpeed) {
        // Call the parent constructor with super
        super(startCadence, startSpeed, 0, "PennyFarthing");
    }

    // You should mark a method you're overriding with an @annotation.
    // To learn more about what annotations are and their purpose check this
    // out: http://docs.oracle.com/javase/tutorial/java/annotations/
    @Override
    public void setGear(int gear) {
        gear = 0;
    }
}

// Interfaces
// Interface declaration syntax
// <access-level> interface <interface-name> extends <super-interfaces> {
//     // Constants
//     // Method declarations
// }

// Example - Food:
public interface Edible {
    public void eat(); // Any class that implements this interface, must
                       // implement this method.
}

public interface Digestible {
    public void digest();
}

// We can now create a class that implements both of these interfaces.
public class Fruit implements Edible, Digestible {  
    @Override
    public void eat() {
        // ...
    }

    @Override
    public void digest() {
        // ...
    }
}

// In Java, you can extend only one class, but you can implement many
// interfaces. For example:
public class ExampleClass extends ExampleClassParent implements InterfaceOne,
    InterfaceTwo {
    @Override
    public void InterfaceOneMethod() {
    }

    @Override
    public void InterfaceTwoMethod() {
    }

}

// Abstract Classes

// Abstract Class declaration syntax
// <access-level> abstract <abstract-class-name> extends <super-abstract-classes> {
//     // Constants and variables
//     // Method declarations
// }

// Marking a class as abstract means that it contains abstract methods that
// must be defined in a child class. Similar to interfaces, abstract classes
// cannot be instantiated, but instead must be extended and the abstract
// methods defined. Different from interfaces, abstract classes can contain a
// concrete and abstract methods. Methods in an interface cannot have a body,
// mixture of unless the method is static, and variables are final by default,
// unlike an abstract class. Also abstract classes CAN have the "main" method.
public abstract class Animal
{
    public abstract void makeSound();

    // Method can have a body
    public void eat()
    {
        System.out.println("I am an animal and I am Eating.");  
        // Note: We can access private variable here.
        age = 30;
    }

    // No need to initialize, however in an interface
    // a variable is implicitly final and hence has
    // to be initialized.
    protected int age;

    public void printAge()
    {
        System.out.println(age);  
    }

    // Abstract classes can have main function.
    public static void main(String[] args)
    {
        System.out.println("I am abstract");
    }
}

class Dog extends Animal
{
    // Note still have to override the abstract methods in the
    // abstract class.
    @Override
    public void makeSound()
    {
        System.out.println("Bark");
        // age = 30;	==> ERROR!	age is private to Animal
    }

    // NOTE: You will get an error if you used the
    // @Override annotation here, since java doesn't allow
    // overriding of static methods.
    // What is happening here is called METHOD HIDING.
    // Check out this SO post: http://stackoverflow.com/questions/16313649/
    public static void main(String[] args)
    {
        Dog pluto = new Dog();
        pluto.makeSound();
        pluto.eat();
        pluto.printAge();
    }
}

// Final Classes

// Final Class declaration syntax
// <access-level> final <final-class-name> {
//     // Constants and variables
//     // Method declarations
// }

// Final classes are classes that cannot be inherited from and are therefore a
// final child. In a way, final classes are the opposite of abstract classes
// because abstract classes must be extended, but final classes cannot be
// extended.
public final class SaberToothedCat extends Animal
{
    // Note still have to override the abstract methods in the
    // abstract class.
    @Override
    public void makeSound()
    {
        System.out.println("Roar");
    }
}

// Final Methods
public abstract class Mammal()
{
    // Final Method Syntax:
    // <access modifier> final <return type> <function name>(<args>)

    // Final methods, like, final classes cannot be overridden by a child
    // class, and are therefore the final implementation of the method.
    public final boolean isWarmBlooded()
    {
        return true;
    }
}

// Enum Type
//
// An enum type is a special data type that enables for a variable to be a set
// of predefined constants. The variable must be equal to one of the values
// that have been predefined for it. Because they are constants, the names of
// an enum type's fields are in uppercase letters. In the Java programming
// language, you define an enum type by using the enum keyword. For example,
// you would specify a days-of-the-week enum type as:
public enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY,
    THURSDAY, FRIDAY, SATURDAY 
}

// We can use our enum Day like that:
public class EnumTest {
    // Variable Enum
    Day day;
    
    public EnumTest(Day day) {
        this.day = day;
    }
    
    public void tellItLikeItIs() {
        switch (day) {
            case MONDAY:
                System.out.println("Mondays are bad.");
                break;
            case FRIDAY:
                System.out.println("Fridays are better.");
                break;   
            case SATURDAY: 
            case SUNDAY:
                System.out.println("Weekends are best.");
                break;     
            default:
                System.out.println("Midweek days are so-so.");
                break;
        }
    }
    
    public static void main(String[] args) {
        EnumTest firstDay = new EnumTest(Day.MONDAY);
        firstDay.tellItLikeItIs(); // => Mondays are bad.
        EnumTest thirdDay = new EnumTest(Day.WEDNESDAY);
        thirdDay.tellItLikeItIs(); // => Midweek days are so-so.
    }
}

// Enum types are much more powerful than we show above. 
// The enum body can include methods and other fields.
// You can see more at https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html

```

## Further Reading

The links provided here below are just to get an understanding of the topic, feel free to Google and find specific examples.

**Official Oracle Guides**:

* [Java Tutorial Trail from Sun / Oracle](http://docs.oracle.com/javase/tutorial/index.html)

* [Java Access level modifiers](http://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)

* [Object-Oriented Programming Concepts](http://docs.oracle.com/javase/tutorial/java/concepts/index.html):
    * [Inheritance](http://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html)
    * [Polymorphism](http://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html)
    * [Abstraction](http://docs.oracle.com/javase/tutorial/java/IandI/abstract.html)

* [Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)

* [Interfaces](http://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html)

* [Generics](http://docs.oracle.com/javase/tutorial/java/generics/index.html)

* [Java Code Conventions](http://www.oracle.com/technetwork/java/codeconvtoc-136057.html)

**Online Practice and Tutorials**

* [Learneroo.com - Learn Java](http://www.learneroo.com)

* [Codingbat.com](http://codingbat.com/java)

**Books**:

* [Head First Java](http://www.headfirstlabs.com/books/hfjava/)

* [Thinking in Java](http://www.mindview.net/Books/TIJ/)

* [Objects First with Java](http://www.amazon.com/Objects-First-Java-Practical-Introduction/dp/0132492660)

* [Java The Complete Reference](http://www.amazon.com/gp/product/0071606300)
