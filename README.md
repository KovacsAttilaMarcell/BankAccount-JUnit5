
# BankAccount – JUnit 5

## A projekt bemutatása

A projekt célja egy egyszerű bankszámlát modellező `BankAccount` osztály megvalósítása Java nyelven, valamint működésének ellenőrzése JUnit 5 egységtesztekkel.

A számla induló egyenlege 0.

## Alkalmazott technológiák

- Java 27
- JUnit 5
- Maven
- IntelliJ IDEA
- Git és GitHub

## Megvalósított funkciók

A `BankAccount` osztály három publikus metódust tartalmaz:

- `deposit(double amount)` – növeli az egyenleget a megadott összeggel.
- `withdraw(double amount)` – csökkenti az egyenleget a megadott összeggel.
- `getBalance()` – visszaadja az aktuális egyenleget.

A program nem engedélyezi a negatív vagy nulla összegű befizetést és pénzfelvételt, valamint megakadályozza az aktuális egyenlegnél nagyobb összeg felvételét.

Érvénytelen művelet esetén `IllegalArgumentException` kivételt dob, és az egyenleg változatlan marad.

A megvalósítás a `NaN`, a végtelen és a túlcsordulást okozó befizetési értékeket is elutasítja.

## A projekt felépítése

```text
BankAccount-JUnit5/
├── src/
│   ├── main/java/BankAccount.java
│   └── test/java/BankAccountTest.java
├── pom.xml
├── .gitignore
└── README.md
```

## A projekt futtatása

A projekt Java 27 JDK-val és Mavennel használható.

1. Klónozd vagy töltsd le a GitHub-repositoryt.
2. Nyisd meg a projektet IntelliJ IDEA-ban.
3. Várd meg a Maven-függőségek betöltését.
4. A `BankAccount` osztályt más Java-kódból lehet példányosítani és használni.

A projekt nem tartalmaz külön konzolos felhasználói felületet, mivel a feladat az osztály implementálására és egységtesztelésére irányul.

## Egységtesztek futtatása

A tesztek futtathatók IntelliJ IDEA-ban a `BankAccountTest` osztály melletti futtatás ikonnal, vagy terminálból:

```bash
mvn test
```

## Tesztesetek

A projekt 10 JUnit 5 egységtesztet tartalmaz:

1. Új bankszámla egyenlege 0.
2. Befizetés növeli az egyenleget.
3. Több befizetés összeadódik.
4. Pénzfelvétel csökkenti az egyenleget.
5. A teljes egyenleg felvehető.
6. Túlköltés kivételt dob.
7. Negatív befizetés kivételt dob.
8. Nulla összegű befizetés kivételt dob.
9. Negatív pénzfelvétel kivételt dob.
10. Nulla összegű pénzfelvétel kivételt dob.

A hibás műveleteket ellenőrző tesztek azt is vizsgálják, hogy a sikertelen műveletek után az egyenleg változatlan marad.

A tesztek a JUnit 5 `@Test`, `@BeforeEach`, `assertEquals()` és `assertThrows()` lehetőségeit használják.

## Eredmény

A projekt 10 egységtesztje sikeresen lefutott, hiba nélkül.
