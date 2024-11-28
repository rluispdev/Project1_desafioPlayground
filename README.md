
## Santander Bootcamp 2023 -  Mobile iOS com Swift

# Fundamentos de Swift e iOS

Este projeto simples em Swift explora o conceito de opcionais e diferentes maneiras de lidar com eles na interpolação de strings. 

**O Desafio:**

O objetivo deste exercício é demonstrar o uso de opcionais em Swift, incluindo:

* Criar um projeto no playground usando o Xcode.
* Definir uma constante com o valor inicial "Steve".
* Definir uma variável do tipo String opcional com o valor inicial "Jobs".
* Escrever um `print` fazendo interpolação com a constante e a variável, definindo um valor default para a variável opcional como "Wozniak".
* Fazer um Optional Binding na variável e, dentro da condição, fazer outro `print` com interpolação entre a constante e a variável que foi desembrulhada.

**Solução:**

```swift
import UIKit

let name  = "Steve"
var lastName : String? = "Jobs"

// 1. Forced Unwrapping
var securityRead = (lastName != nil) ? lastName! : "Wozinick" 
print("This is \(name) \(securityRead)") // Saída: This is Steve Jobs

// 2. Optional Binding
securityRead = (lastName != nil) ? lastName : "Wozinick" 
if let lastName = lastName {
  print("This is \(name) \(lastName)") // Saída: This is Steve Jobs
} else {
  print("This is \(name) Wozinick") 
}

// 3. Nil-Coalescing Operator
securityRead = (lastName != nil) ? lastName : "Wozinick" 
print("This is \(name) \(securityRead ?? "Wozinick")") // Saída: This is Steve Jobs

// 4. String Interpolation com if let
securityRead = (lastName != nil) ? lastName : "Wozinick" 
print("This is \(name) \(if let lastName = lastName { lastName } else { "Wozinick" })") // Saída: This is Steve Jobs
