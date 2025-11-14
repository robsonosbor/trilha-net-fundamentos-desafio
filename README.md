## 🅿️ Sistema de Estacionamento - Desafio DIO - Trilha .NET - Fundamentos

Este é um projeto simples de sistema de gerenciamento de estacionamento desenvolvido em **C#** como um desafio fundamental de programação. Ele simula as operações básicas de um estacionamento, permitindo cadastrar veículos, remover veículos e calcular o valor a ser pago com base no tempo de permanência.

[![Imagem de capa](https://github.com/robsonosbor/trilha-net-fundamentos-desafio/blob/main/diagrama_classe_estacionamento.png)](/)

---

### 🚀 Tecnologias

* **Linguagem:** C#
* **.NET Framework:** .NET 9.0

---

### ✨ Funcionalidades

O sistema oferece as seguintes funcionalidades principais através de um menu de console:

1.  **Cadastrar veículo:** Adiciona a placa de um veículo à lista de veículos estacionados.
2.  **Remover veículo:** Remove um veículo da lista, solicita a quantidade de horas que permaneceu estacionado e calcula o valor total a ser pago.
3.  **Listar veículos:** Exibe todas as placas dos veículos atualmente estacionados.
4.  **Encerrar:** Finaliza a execução do programa.

---

### ⚙️ Como Usar

Ao iniciar o programa, o usuário é solicitado a definir o **preço inicial** e o **preço por hora** do estacionamento.

```bash
Seja bem vindo ao sistema de estacionamento!
Digite o preço inicial:
# [Insira o valor, ex: 5.00]
Agora digite o preço por hora:
# [Insira o valor, ex: 2.00]

```

Após a configuração inicial, o menu de opções é exibido:

```bash
Digite a sua opção:
1 - Cadastrar veículo
2 - Remover veículo
3 - Listar veículos
4 - Encerrar

```

## 💻 Estrutura do Código

O projeto é composto por dois arquivos principais:

* **`Program.cs`:**
    * Contém o **ponto de entrada** da aplicação.
    * Define o *encoding* para **UTF8**.
    * Lê os valores de `precoInicial` e `precoPorHora`.
    * Instancia a classe `Estacionamento`.
    * Implementa o *loop* do menu principal e trata as opções do usuário (`switch`).

* **`Models/Estacionamento.cs` (Classe `Estacionamento`):**
    * Responsável por gerenciar a **lógica do estacionamento**.
    * **Propriedades Privadas:**
        * `precoInicial` (`decimal`): Valor fixo a ser cobrado.
        * `precoPorHora` (`decimal`): Valor cobrado por hora adicional.
        * `veiculos` (`List<string>`): Lista para armazenar as placas dos veículos estacionados.
    * **Construtor:**
        * Recebe e atribui os valores iniciais de `precoInicial` e `precoPorHora`.
    * **Métodos Públicos:**
        * `AdicionarVeiculo()`: Solicita a placa e a adiciona à lista.
        * `RemoverVeiculo()`:
            * Solicita a placa e verifica se está na lista.
            * Se encontrado, solicita as horas, calcula o `valorTotal` e remove o veículo.
        * `ListarVeiculos()`: Exibe todas as placas na lista ou uma mensagem se estiver vazia.

---

## 🤝 Contribuições

Este projeto faz parte de um desafio de fundamentos. Se você deseja aprimorá-lo (por exemplo, adicionando validações de entrada, formatação de placas, ou persistência de dados), sinta-se à vontade para fazer um **fork** e enviar um **pull request**.