# Customizable Printer

A simple Java project for practicing the Decorator Design Pattern.

The program has a basic printer that prints a message to the console. Decorators can be added to change the message before it is printed.

## Classes

- `Printer` - interface with the `print()` method
- `BasicPrinter` - prints the message to the console
- `PrinterDecorator` - base class for the decorators
- `XMLPrinter` - changes the message to XML format
- `EncryptedPrinter` - encodes the message before printing
- `Main` - runs and tests the program

## Example

```java
Printer printer = new BasicPrinter();
printer.print("Hello World!");

Printer printer2 =
        new EncryptedPrinter(
                new XMLPrinter(
                        new BasicPrinter()
                )
        );

printer2.print("Hello World!");
```

## Output

```text
Hello World!
<message>SGVsbG8gV29ybGQh</message>
```

## Technologies

- Java
- Maven
- Decorator Design Pattern