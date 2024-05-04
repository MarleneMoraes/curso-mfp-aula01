# Curso de Iniciação em Programação Esportiva

## Aula 01 | Introdução ao Curso (04/05)

### Duração e Horários

- Segunda fase da MFP: 14 e 15 de Junho.
  6 semanas – 11 aulas.
- Cada aula terá 1 hora de duração (teoria + prática).
- Quinta-feira – 19:00, e sábados – 14:00.
- Canal da SBC no Youtube, as gravações ficarão disponíveis.

### Introdução

- **Introdução à Programação Esportiva:** A programação competitiva é uma atividade em que os participantes resolvem problemas algorítmicos em um tempo limitado. É uma forma de aprimorar habilidades de resolução de problemas, pensamento lógico e eficiência de algoritmos.
- **Por que C++ é Importante:** C++ é uma linguagem de programação amplamente utilizada na programação competitiva devido à sua eficiência e flexibilidade. Ela permite que os programadores escrevam códigos mais rápidos e eficientes em termos de tempo e memória, o que é crucial em competições onde a velocidade e a precisão são essenciais.
- **Eficiência de Tempo:** C++ é uma linguagem compilada, o que significa que o código é traduzido para linguagem de máquina antes da execução. Isso resulta em um tempo de execução mais rápido em comparação com linguagens interpretadas, como Python ou Java, que são mais lentas em competições onde o tempo de execução é crítico.
- **Eficiência de Memória:** C++ oferece mais controle sobre a alocação de memória, permitindo que os programadores otimizem o uso de memória. Isso é importante em competições onde a limitação de memória pode ser um problema.
- **Uso Generalizado: **C++ é amplamente utilizado em competições de programação, e a maioria dos materiais e recursos disponíveis online são voltados para esta linguagem. Portanto, é uma escolha natural para quem deseja se destacar nesse campo.

### Estrutura básica em C++ - Formato Básico

```cpp
#include <iostream>
using namespace std;

int main() {
    	// código
    return 0;
}

```

ou...

```cpp
#include <iostream>

namespace std {
    int main() {
        	// código
        return 0;
    }
} // namespace std;

```
### Estrutura básica em C++ - Tipos de Dados 

| Tipo de Dado | Descrição                                             | Notas Adicionais                                                                                                    |
|--------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| int          | Números inteiros (positivos, negativos ou zero) | Pode ter tamanhos diferentes (short, int, long) dependendo da implementação e requisitos de alcance.             |
| float        | Números de ponto flutuante de precisão simples (decimais) | Tem menos precisão (tipicamente 6-7 dígitos decimais) em comparação com double.                              |
| double       | Números de ponto flutuante de dupla precisão (decimais) | Oferece maior precisão (tipicamente 15-17 dígitos decimais) em comparação com float.                          |
| char         | Único caractere (letra, número, símbolo)   | Representado usando codificação de caractere ASCII ou Unicode.                                                     |
| bool         | Valor booleano (verdadeiro ou falso)    | Usado para operações lógicas e instruções condicionais.                                                             |
| string       | Sequência de caracteres (palavra, frase, texto) | Requer a inclusão do arquivo de cabeçalho `<string>`.                                                                |

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    // Inteiro
    short numeroShort;
    long numeroLong;
    int numeroInteiro;
        
    // Ponto Flutuante
    float numeroFlutuante;
    double numeroDouble;
    
    // Caractere
    char caractere;

    // Seq. de Caracteres
    string string;
    return 0;
}
```
### Operações Lógicas

| Operador | Significado           |
|----------|-----------------------|
| >        | Maior que             |
| <        | Menor que             |
| >=       | Maior ou igual a      |
| <=       | Menor ou igual a      |
| ==       | Igual                 |
| !=       | Diferente             |


```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 3;
    
    cout << "a > b: " << (a > b) << endl; // true (1)
    cout << "a < b: " << (a < b) << endl; // false (0)
    cout << "a == b: " << (a == b) << endl; // false (0)
    cout << "a != b: " << (a != b) << endl; // true (1)
    cout << "a >= b: " << (a >= b) << endl; // true (1)
    cout << "a <= b: " << (a <= b) << endl; // false (0)
}
```

| Operador | Significado |
|----------|-------------|
| &&       | E (AND)     |
| \|\|     | OU (OR)     |
| !        | Negação (NOT) |

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 3;
    int c = 8;
    
    cout << "(a > b) && (a + b > c): " << (((a > b) && (a + b > c)) << endl; // true (1)
    cout << "(a < b) || (a == b): " << ((a < b) || (a == b)) << endl; // false (0)
    cout << "a != b: " << (a != b) << endl; // / true (1)
}
```
### Operações condicionais

| Operador | Significado        |
|----------|--------------------|
| if       | se                 |
| if/else  | se/senão           |
| switch   | escolha            |

```cpp
#include <iostream>
using namespace std;

int numerosInteirosIfElse() {
    int numero;

    cout << "Digite um número inteiro: ";
    cin >> numero;

    if (numero > 0) {
       cout << "O número é positivo." << endl;
    } else {
        cout << "O número é negativo ou zero." << endl;
    }
    return 0;
}

int numerosInteirosIfElseIf() {
    int numero;

    cout << "Digite um número inteiro: ";
    cin >> numero;

    if (numero > 0) {
        cout << "O número é positivo." << endl;
    } else if (numero < 0) {
        cout << "O número é negativo." << endl;
    } else {
        cout << "O número é zero." << endl;
    }

    return 0;
}

int diasDaSemanaSwitchCase(){
    int dia;

    cout << "Digite o número do dia da semana (1-7): ";
    cin >> dia;

    switch (dia) {
       case 1: 
            cout << "Domingo" << endl;
            break;
        case 2:
            cout << "Segunda" << endl;
            break;
       case 3:
            cout << "Terça" << endl;
            break;
       case 4:
            cout << "Quarta" << endl;
            break;
       case 5:
            cout << "Quinta" << endl;
            break;
       case 6:
            cout << "Sexta" << endl;
            break;
       case 7:
            cout << "Sábado" << endl;
            break;
       default:
            cout << "Inválido" << endl;
    }
    return 0;
}

```
#### Exercícios

- [DDD](https://judge.beecrowd.com/en/problems/view/1050)
- [Triangle Types](https://judge.beecrowd.com/en/problems/view/1045)

### Estruturas de Repetição (Loops)

| Operador   | Significado      |
|------------|------------------|
| while      | Enquanto         |
| do...while | Faça...Enquanto  |
| for        | Para cada        |

```cpp
#include <iostream>
using namespace std;

int main() {
    int c = 0;
    while (c < 5) {
        cout << "Contador: " << c << endl;
        c++;
    }

    do {
        cout << "Contador: " << c  << endl;
        c++;
    } while (c < 5);

    for (int i = 0; i <  5; i++) {
       cout << "Contador: " << i << endl;
    }

    return 0;
}
```
#### Exercícios

- [Even Numbers](https://judge.beecrowd.com/en/problems/view/1059)
- [Even Between five Numbers](https://judge.beecrowd.com/en/problems/view/1065)

### Overflow, TLE, RTE, MLE

- **Overflow:** Ocorre quando o resultado de uma operação excede o intervalo de valores que o tipo de dado pode armazenar. Por exemplo, ao tentar armazenar um número muito grande em um int, pode ocorrer overflow.
- **TLE (Time Limit Exceeded):** Indica que o programa excedeu o tempo limite de execução permitido. Isso pode acontecer se o algoritmo não for eficiente o suficiente para lidar com o tamanho da entrada.
- **RTE (Runtime Error):** Ocorre quando o programa falha durante a execução devido a um erro, como divisão por zero, acesso a memória não alocada ou estouro de pilha.
- **MLE (Memory Limit Exceeded):** Indica que o programa excedeu o limite de memória permitido. Isso pode ocorrer se o programa usar uma quantidade muito grande de memória, por exemplo, ao declarar arrays grandes ou usar recursão sem critério de parada adequado.

### Complexidade de Algoritmos

A complexidade de um algoritmo refere-se à quantidade de recursos computacionais, como tempo e espaço, que ele consome em função do tamanho da entrada.

A notação Big O (O) é usada para descrever a complexidade de um algoritmo.

Exemplos comuns de complexidade:
| Complexidade     | Descrição                              |
|------------------|----------------------------------------|
| O(1)             | Tempo ou espaço constante.             |
| O(log n)         | Tempo ou espaço logarítmico.           |
| O(n)             | Tempo ou espaço linear.                |
| O(n log n)       | Tempo ou espaço linearítmico.          |
| O(n^2)           | Tempo ou espaço quadrático.            |
| O(n^2n)           | Tempo ou espaço Exponencial.          |

- **Previsão do Tempo de Execução:** A complexidade do algoritmo ajuda a prever o tempo de execução em diferentes tamanhos de entrada.
Por exemplo, se um algoritmo tem complexidade O(n), podemos esperar que ele execute aproximadamente 10 vezes mais rápido para uma entrada 10 vezes menor.