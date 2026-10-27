# Saludos en Go

Este paquete proporciona una forma simple de obterner saludos personalizados en Go.

## Instalacion
Ejecuta el siguiente comando para instalar el paquete: 

```bash
go get -u github.com/jespinale/greetings
```
## Uso
A qui tienes un ejemplo de como utilizar el paquete en tu codigo:

```go
package main

import (
	"fmt"
	"log"

	"github.com/jespinale/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{"Jose", "Juan", "Pablo"}
	messages, err := greetings.Hellos(names)
	if err != nil {
		log.Fatal(err)
	}

	//message, err := greetings.Hello("Jose Espinal")
	//if err != nil {
	//	log.Fatal(err)
	//}

	fmt.Println(messages)
}

```
Este ejemplo importa el paquete github.com/jespinale/greetings y llama la funcion Hello
saludo personalizado. Si ocurre un error, se imprime un mensaje de error.
