# SE 237 — Week 2 Coding Practice Lab

Six Java exercises covering references, constructor validation, defensive copying, queries without side effects, class relationships, and separate responsibilities.

Each of the twelve variants includes `Main.java` and `output.txt`, which records its actual console output. Each example is self-contained and uses its own folder because class names such as `Main` are repeated.

## Exercises

| Exercise | Variants, source code, and recorded output |
| --- | --- |
| 1 — Object and Reference | [Same object](exercise-01-same-object/) · [code](exercise-01-same-object/Main.java) · [output](exercise-01-same-object/output.txt)<br>[Independent objects](exercise-01-independent/) · [code](exercise-01-independent/Main.java) · [output](exercise-01-independent/output.txt) |
| 2 — Protect an Object in the Constructor | [Valid object](exercise-02-valid/) · [code](exercise-02-valid/Main.java) · [output](exercise-02-valid/output.txt)<br>[Invalid quantity](exercise-02-invalid-quantity/) · [code](exercise-02-invalid-quantity/Main.java) · [output](exercise-02-invalid-quantity/output.txt)<br>[Invalid loss percentage](exercise-02-invalid-loss/) · [code](exercise-02-invalid-loss/Main.java) · [output](exercise-02-invalid-loss/output.txt) |
| 3 — Protect an Internal List | [Defensive copy](exercise-03-copy/) · [code](exercise-03-copy/Main.java) · [output](exercise-03-copy/output.txt)<br>[Attempt to clear the list](exercise-03-clear/) · [code](exercise-03-clear/Main.java) · [output](exercise-03-clear/output.txt) |
| 4 — A Query Method Without Side Effects | [Repeated queries](exercise-04-query/) · [code](exercise-04-query/Main.java) · [output](exercise-04-query/output.txt) |
| 5 — Dependency vs Association | [Dependency through a parameter](exercise-05-dependency/) · [code](exercise-05-dependency/Main.java) · [output](exercise-05-dependency/output.txt)<br>[Association through a field](exercise-05-association/) · [code](exercise-05-association/Main.java) · [output](exercise-05-association/output.txt) |
| 6 — Give Each Class One Clear Job | [Original message](exercise-06-original/) · [code](exercise-06-original/Main.java) · [output](exercise-06-original/output.txt)<br>[Updated planner message](exercise-06-updated/) · [code](exercise-06-updated/Main.java) · [output](exercise-06-updated/output.txt) |

## Run an example

Use JDK 10 or later; `List.copyOf` and `Map.copyOf` require Java 10+. Open a terminal in the chosen example folder, then run:

```sh
javac Main.java
java Main
```

Run each variant from its own folder. Compare the console result with that folder's `output.txt`.

## Expected exceptions

The two invalid constructor examples intentionally throw `IllegalArgumentException`: one rejects a nonpositive quantity, and the other rejects a loss percentage outside 0–99. The list-clear example intentionally throws `UnsupportedOperationException` because `List.copyOf` produces an unmodifiable list. These exceptions are required observations in the lab. Stack-trace details can vary between JDK versions.
