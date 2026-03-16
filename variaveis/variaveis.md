# GLOBAL:
- É aquela variavel que é declarda fora de qualquer função ou bloco
- Ela fica disponivel em qualquer lugar do codigo 
- ela e acessivel por todo o script 
- no navegador, variaveis globais costumam ser anexadas ao objeto Window. 
---
# ESCOPO:
- No JS antigo, apenas functions isolavam variaveis 
- Com o ES6, qualquer par de chaves {} cria um "muro" para as variaveis declaradas com "let" ou "const"
- Imagine o escopo como uma via de mao unica: quem está dentro do bloco consegue ver o que está fora, mas quem está fora não consegue enxergar o que está lá dentro.
---
# TIPOS:
var (A "antiga")
```js
const cpf = "123.456.789-00";

// Se você tentar fazer isso:
// cpf = "000.000.000-00"; 
// Erro: Assignment to constant variable.
```
- Evite usar hoje em dia. Ela é perigosa porque não respeita blocos (como if ou for), apenas funções.
---
let (A "Moderna e Flexível")
```js
let pontosDeVida = 100;

if (tomouDano) {
    pontosDeVida = 80; // Funciona perfeitamente!
}
```
- É a substituta ideal para o var quando você sabe que o valor vai mudar.
---
const (A "Fixa")
```js
    const cpf = "123.456.789-00";
    
    // Se você tentar fazer isso:
    // cpf = "000.000.000-00"; 
    // Erro: Assignment to constant variable.
```
- É a sua primeira opção sempre. Use para tudo, a menos que você tenha certeza que o valor vai ser sobrescrito.
- Atenção: Como vimos no Object.freeze, se a const for um objeto ou array, você ainda consegue remover, adicionar ou alterara as propriedades dele, mas não pode trocar o objeto inteiro por outro.