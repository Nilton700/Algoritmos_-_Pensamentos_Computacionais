# 🌡️ Monitor de Temperatura

Um programa desenvolvido em **linguagem C** para realizar o monitoramento de temperaturas informadas pelo usuário, emitindo alertas quando a temperatura ultrapassa um limite definido.

---

## 👨‍💻 Autor

**Nilton Alves dos Santos**
🎓 Aluno do curso de **Engenharia de Software**

### 📚 Informações acadêmicas

* **Disciplina:** Algoritmos e Pensamentos Computacionais
* **Professora:** Karla Sartin
* **Linguagem:** C
* **Ambiente de execução:** GDB Online / GCC

---

## 🎯 Objetivo do Projeto

O **Monitor de Temperatura** foi desenvolvido com o objetivo de auxiliar no acompanhamento de temperaturas informadas pelo usuário.

O programa realiza leituras contínuas de temperatura e verifica se o valor informado ultrapassa o limite estabelecido de **80°C**. Quando isso acontece, o sistema apresenta uma mensagem de alerta ao usuário.

Além disso, o programa possui um mecanismo de segurança que encerra automaticamente o monitoramento caso sejam registradas **três temperaturas acima de 80°C consecutivamente**.

Ao finalizar o programa, é apresentado um relatório contendo informações sobre as temperaturas registradas durante o monitoramento.

---

## ⚙️ Funcionalidades

O programa possui as seguintes funcionalidades:

* 🌡️ Leitura de temperaturas em °C;
* ⚠️ Alerta para temperaturas acima de **80°C**;
* 🔢 Contagem de temperaturas acima do limite de forma consecutiva;
* 🛑 Encerramento automático após três alertas consecutivos;
* ❌ Identificação e rejeição de temperaturas abaixo do zero absoluto;
* 🔄 Continuidade do monitoramento após valores inválidos;
* ⌨️ Opção de encerramento manual utilizando a letra `x`;
* 📊 Cálculo da média das temperaturas válidas;
* 🔺 Identificação da maior temperatura registrada;
* 🔻 Identificação da menor temperatura registrada;
* 🔢 Contagem da quantidade de temperaturas válidas informadas;
* 📋 Geração de um relatório final.

---

## 🌡️ Limite de Temperatura

O limite de temperatura utilizado pelo programa é de:

```text
80°C
```

Sempre que o usuário informa uma temperatura **maior que 80°C**, o programa apresenta uma mensagem de alerta:

```text
ALERTA! Temperatura acima de 80°C!
```

É importante destacar que uma temperatura exatamente igual a **80°C** não gera alerta, pois a condição utilizada no programa verifica se:

```c
temperatura > 80
```

Portanto:

| Temperatura | Resultado          |
| ----------: | ------------------ |
|        75°C | Temperatura normal |
|        80°C | Temperatura normal |
|        81°C | ⚠️ Alerta          |
|       100°C | ⚠️ Alerta          |

---

## 📥 Leitura das Temperaturas

O programa realiza leituras continuamente utilizando um laço de repetição.

A cada repetição, o usuário pode informar:

* Uma temperatura numérica;
* A letra `x` para encerrar o programa.

A entrada é inicialmente armazenada como texto para permitir que o programa diferencie uma temperatura numérica da opção de encerramento.

Depois, o valor é convertido para uma temperatura numérica e passa pelas validações necessárias.

---

## 🔎 Identificação de Temperaturas Acima do Limite

Após receber uma temperatura válida, o programa verifica se ela ultrapassa os **80°C**.

Essa verificação é realizada através de uma estrutura condicional:

```c
if (temperatura > 80)
```

Quando a condição é verdadeira, o programa:

1. Exibe uma mensagem de alerta;
2. Aumenta o contador de alertas consecutivos;
3. Continua permitindo que o usuário informe novas temperaturas.

Exemplo:

```text
Digite a temperatura: 85

ALERTA! Temperatura acima de 80°C!
Alertas consecutivos: 1
```

---

## 🔢 Contagem de Temperaturas Consecutivas

O programa utiliza uma variável chamada:

```c
int alertas = 0;
```

Essa variável controla quantas temperaturas acima de 80°C foram registradas **em sequência**.

Sempre que uma temperatura ultrapassa 80°C:

```c
alertas++;
```

Caso o usuário informe uma temperatura igual ou inferior a 80°C, a sequência é interrompida e o contador volta para zero:

```c
alertas = 0;
```

### Exemplo

```text
85°C → Alerta 1
90°C → Alerta 2
70°C → contador volta para 0
95°C → Alerta 1
```

Nesse exemplo, o programa não é encerrado porque nunca ocorreram três temperaturas acima de 80°C consecutivamente.

Caso aconteça:

```text
85°C → Alerta 1
90°C → Alerta 2
95°C → Alerta 3
```

o programa encerra automaticamente o monitoramento.

---

## ❌ Tratamento de Valores Inválidos

O programa também possui tratamento para temperaturas fisicamente inválidas.

O limite inferior utilizado é o **zero absoluto**:

```text
-273,15°C
```

Caso o usuário informe uma temperatura abaixo desse valor, o programa apresenta:

```text
Temperatura inválida!
Temperaturas abaixo do zero absoluto(-273.15 °C) não são válidas...
```

O valor inválido **não é contabilizado** no relatório e não participa do cálculo da média, da maior ou da menor temperatura.

O programa continua executando normalmente e solicita uma nova temperatura.

Também existe uma validação para entradas que não sejam números nem `x`. Nesse caso, o programa informa que o valor é inválido e solicita uma nova entrada.

---

## 🛑 Como Encerrar o Programa

Existem duas formas de encerramento.

### 1. Encerramento manual

O usuário pode digitar:

```text
x
```

ou:

```text
X
```

Nesse caso, o programa encerra o monitoramento e apresenta o relatório final.

### 2. Encerramento automático

O programa também pode ser encerrado automaticamente quando forem registradas:

```text
3 temperaturas consecutivas acima de 80°C 
```

Essa funcionalidade funciona como um mecanismo de alerta para situações em que a temperatura permanece acima do limite durante várias leituras consecutivas.

---

## 🔄 Por que utilizar `do...while`?

O programa utiliza preferencialmente a estrutura:

```c
do {
    // comandos
} while (condicao);
```

O `do...while` é adequado para este projeto porque o programa precisa **realizar pelo menos uma leitura antes de verificar se deve continuar executando**.

A estrutura funciona da seguinte maneira:

```text
        ↓
Executa o código
        ↓
Lê a temperatura
        ↓
Realiza as validações
        ↓
Verifica os alertas
        ↓
Verifica a condição
        ↓
   Continua?
    ↙      ↘
  Sim       Não
   ↓         ↓
Repete     Encerra
```

No programa, a condição principal é relacionada à quantidade de alertas consecutivos:

```c
} while (alertas < 3);
```

Enquanto o número de alertas consecutivos for menor que três, o monitoramento continua.

Quando o contador chegar a três, a condição se torna falsa e o programa encerra o laço.

O `do...while` também torna a lógica do monitoramento mais intuitiva, pois primeiro ocorre a leitura e o processamento da temperatura e somente depois é decidido se o programa deve realizar uma nova leitura.

---

## 📊 Relatório Final

Quando o programa é encerrado, ele apresenta um relatório com os dados obtidos durante o monitoramento.

O relatório informa:

* Quantidade de temperaturas válidas;
* Média das temperaturas;
* Maior temperatura registrada;
* Menor temperatura registrada;
* Motivo do encerramento.

Exemplo:

```text
====================================
          RELATORIO FINAL
====================================
Quantidade de temperaturas: 5
Media das temperaturas: 68.40 °C
Maior temperatura: 95.00 °C
Menor temperatura: 40.00 °C

O programa foi encerrado pelo usuario.
====================================
```

Temperaturas inválidas não são consideradas nesses cálculos.

---

## 🧮 Cálculo da Média

A média é calculada utilizando a soma das temperaturas válidas dividida pela quantidade de temperaturas válidas:

```c
media = soma / quantidade;
```

Por exemplo, considerando:

```text
25°C
40°C
78.9°C
```

Temos:

```text
Soma = 143.9
Quantidade = 3

Média = 143.9 / 3
Média = 47.96°C
```

---

## 💻 Compilação e Execução

### GDB Online

O programa pode ser executado diretamente no **GDB Online**, selecionando a linguagem **C** e inserindo o código no editor.

Depois, basta executar o programa e informar as temperaturas no terminal disponibilizado pela plataforma.

---

### GCC pelo terminal

Caso esteja utilizando o GCC instalado no computador, salve o código em um arquivo, por exemplo:

```text
monitor_temperatura.c
```

Depois, abra o terminal na pasta onde o arquivo está localizado e execute:

```bash
gcc monitor_temperatura.c -o monitor_temperatura
```

Após a compilação, execute o programa com:

### Windows

```bash
monitor_temperatura.exe
```

### Linux/macOS

```bash
./monitor_temperatura
```

---

## 🛠️ Conceitos de Programação Utilizados

Este projeto foi desenvolvido utilizando conceitos fundamentais da linguagem C, incluindo:

* Variáveis;
* Tipos de dados;
* Entrada e saída de dados;
* `if` e `else`;
* `do...while`;
* Operadores relacionais;
* Operadores lógicos;
* Contadores;
* Acumuladores;
* Conversão de dados;
* Validação de entrada;
* Cálculos matemáticos;
* Manipulação de caracteres;
* Controle de fluxo.

---

## 📌 Considerações Finais

O projeto **Monitor de Temperatura** foi desenvolvido como uma aplicação prática dos conceitos de **Algoritmos e Pensamentos Computacionais**, utilizando a linguagem C.

Através do uso de estruturas condicionais, laços de repetição, contadores, acumuladores e tratamento de entradas, o programa consegue realizar um monitoramento contínuo das temperaturas informadas pelo usuário, emitir alertas e produzir um relatório ao final da execução.

O projeto também demonstra a utilização do `do...while` em uma situação prática, permitindo que o sistema realize leituras sucessivas enquanto as condições de funcionamento forem atendidas.

Sinta-se livre para usar o código a vontade!

```
