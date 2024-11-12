# README - Programa de Saudação Multilíngue

## Descrição

Este programa solicita ao usuário a entrada de um código de idioma (como "pt", "en", "de", "jp" ou "es") e, com base nesse código, imprime uma mensagem de saudação na língua correspondente. Caso o código fornecido não seja reconhecido, o programa informa que o idioma não é válido.

## Funcionalidades

- Solicita ao usuário um código de idioma.
- Compara o código inserido com uma lista de idiomas predefinidos: português (pt), inglês (en), alemão (de), japonês (jp) e espanhol (es).
- Exibe uma saudação correspondente ao idioma informado:
  - **pt**: "Olá mundo"
  - **en**: "Hello world"
  - **de**: "Hallo Welt"
  - **jp**: "こんにちは世界!" ("Konnichiwa Sekai!")
  - **es**: "Hola mundo"
- Se o código inserido não corresponder a nenhum idioma reconhecido, o programa informa que o código é inválido.

## Como Usar

1. Compile o programa com um compilador C. Por exemplo, com o GCC:
   ```bash
   gcc saudacao.c -o saudacao
   ```

2. Execute o programa gerado:
   ```bash
   ./saudacao
   ```

3. Quando solicitado, insira um código de idioma (um dos seguintes: `pt`, `en`, `de`, `jp`, `es`).

4. O programa exibirá a saudação correspondente ou uma mensagem de erro, se o código inserido não for reconhecido.

## Exemplo de Execução

### Exemplo 1: Saudação em português
```bash
Digite um código de idioma (pt, en, de, jp, es): pt
olá mundo
```

### Exemplo 2: Saudação em inglês
```bash
Digite um código de idioma (pt, en, de, jp, es): en
hello world
```

### Exemplo 3: Código de idioma inválido
```bash
Digite um código de idioma (pt, en, de, jp, es): fr
código de idioma não reconhecido
```

## Explicação do Código

1. **Entrada do usuário**: O código utiliza `fgets` para ler a entrada do usuário. A função `fgets` é preferida ao `scanf` para evitar problemas de estouro de buffer.
   
2. **Remoção do caractere de nova linha**: Após a entrada, a função `strcspn` é usada para remover o caractere de nova linha (`\n`) que pode ser inserido ao pressionar "Enter".
   
3. **Comparação de códigos de idioma**: O programa compara o código inserido pelo usuário com os idiomas predefinidos usando a função `strcspn` para verificar se o código corresponde exatamente ao esperado.

4. **Saudação**: Se o código corresponder a um idioma conhecido, o programa imprime a saudação correspondente. Caso contrário, uma mensagem de erro é exibida.

## Considerações Finais

Este é um programa simples e didático para demonstrar o uso de entradas de usuário, comparação de strings e controle de fluxo em C. Para expandir o programa, você poderia adicionar mais idiomas, melhorar a gestão de erros ou permitir que o usuário insira a saudação diretamente.

## Licença

Este código está disponível para uso livre.
