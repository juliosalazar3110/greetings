# Saludos en Go

Este paquete proporciona una forma simple de obtener saludos personalizados

# Instalación
Ejecuta el siguiente comando para instalar el paquete
```bash
go get -u github.com/juliosalazar3110/greetings
```

## Uso
Ejemplo de como utilizarlo
```
package main

import (
	"fmt"
	"log"

	"github.com/juliosalazar3110/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)
	names := []string{
		"julio", "cesar", "andrea",
	}

	messages, err := greetings.Hellos(names)

	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)
}
```