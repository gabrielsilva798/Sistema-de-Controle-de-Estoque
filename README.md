
# 📦 Sistema de Controle de Estoque de Peças

Este projeto consiste na implementação de um sistema simples de **controle de estoque**, desenvolvido com **HTML e JavaScript**, que simula o **cadastro de entradas e saídas de peças**, com base em um fluxograma proposto na atividade prática do SENAI.

## 🚀 Funcionalidades

- ✅ Cadastro do **saldo inicial** do estoque.
- ➕ Lançamento de **entradas** de peças (tipo 1).
- ➖ Lançamento de **saídas** de peças (tipo 2).
- 🚫 Validação de saldo antes de saída (mensagem de **"Saldo insuficiente"**).
- 🔁 Estrutura de repetição para continuar ou encerrar o sistema.
- 📊 Exibição do histórico das operações realizadas.
- 🧾 Exibição do **saldo final** e da mensagem de encerramento.

## 📂 Estrutura

O sistema é todo implementado em um único arquivo `.html`, podendo ser executado diretamente em qualquer navegador moderno.

```html
<script>
  saldo = parseInt(prompt("Informar saldo inicial"));
  document.write("Saldo inicial: " + saldo + "<br>");
  encerrar = "n";
  while(encerrar == "n") {
    tipo = parseInt(prompt("Informar tipo de entrada"));
    quantidade = parseInt(prompt("Informar quantidade"));
    if(tipo == 1) {
      saldo += quantidade;
      document.write("Entrada: " + quantidade + "<br>");
    }
    if(tipo == 2) {
      if(saldo >= quantidade) {
        saldo -= quantidade;
        document.write("Saída: " + quantidade + "<br>");
      } else {
        document.write("Saldo insuficiente<br>");
        alert("Saldo insuficiente");
      }
    }
    document.write("Saldo: " + saldo + "<br>");
    encerrar = prompt("Deseja encerrar ? (s/n)");
  }
  document.write("Sistema encerrado<br>");
</script>
```

## 🧠 Conceitos aplicados

- Variáveis e tipos de dados (`parseInt`, `prompt`)
- Condicionais (`if/else`)
- Laços de repetição (`while`)
- Escrita dinâmica na página (`document.write`)
- Alertas ao usuário (`alert`)
- Fluxogramas para estruturação lógica

## 🖼️ Fluxograma

O sistema foi desenvolvido com base em um **fluxograma** contendo:
- Terminal (início/fim)
- Entrada/saída
- Processo
- Decisão
- Repetição com retorno condicional

## 🧪 Como testar

1. Salve o código como `estoque.html`
2. Clique duas vezes no arquivo ou abra com um navegador
3. Siga os prompts para inserir saldo, tipo de operação e quantidade
4. Observe o resultado direto na tela

## 📸 Print mostrando um teste.
![Caso de uso no navegador](imagens/Capturar.png)

## 📚 Fonte
Este projeto faz parte da **Unidade Curricular de Lógica de Programação – SENAI**, com base no material fornecido na atividade prática.
