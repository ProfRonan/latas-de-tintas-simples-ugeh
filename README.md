# Latas de Tintas

O script principal de vocês deve estar no arquivo `main.py`.

## 📝 Instruções 📝

No arquivo `main.py`, escreva instruções para resolver um problema de uma loja de tintas.

Não altere o código já criado adicione suas instruções **APENAS** no(s) local(is) indicado(s).

O programa deverá pedir o tamanho em metros quadrados da área a ser pintada.

Considere que a cobertura da tinta é de 1 litro para cada 3 metros quadrados e que a tinta é vendida em latas de 18 litros, que custam R$ 80,00.

Informe ao usuário a quantidades de latas de tinta a serem compradas e o preço total.

## 🧑‍💻 Exemplo de Execução 🧑‍💻

- Valor digitado pelo usuário: `0`
- Resposta do programa `Serão necessárias 0 latas totalizando R$ 0`

- Valor digitado pelo usuário: `1`
- Resposta do programa `Serão necessárias 1 latas totalizando R$ 80`

- Valor digitado pelo usuário: `2`
- Resposta do programa `Serão necessárias 1 latas totalizando R$ 80`

- Valor digitado pelo usuário: `54`
- Resposta do programa `Serão necessárias 1 latas totalizando R$ 80`

- Valor digitado pelo usuário: `55`
- Resposta do programa `Serão necessárias 2 latas totalizando R$ 160`

- Valor digitado pelo usuário: `215`
- Resposta do programa `Serão necessárias 4 latas totalizando R$ 320`

## Créditos

Exercício 18 do [Mundo Python](https://wiki.python.org.br/EstruturaSequencial) texto sob a licença [Creative Commons](https://creativecommons.org/licenses/by/2.5/br/).

## 🧪 Testes Automáticos 🧪

Para testar automaticamente o programa **antes** de fazer um commit e enviar o seu trabalho existem algumas formas de fazer isso.

1. executar o módulo `unittest` direto no terminal.
   Para isso, basta executar o seguinte comando:

```bash
python -m unittest discover -s test
```

2. executar o arquivo `test_main.py` no terminal.
   Para isso, basta executar o seguinte comando:

```bash
python test/test_main.py
```

3. caso você esteja usando o [VSCode](https://code.visualstudio.com/), você pode abrir a paleta de comandos `CTRL+SHIFT+P` e digitar `Run All Tests`.

4. no seu editor de código, você pode executar o arquivo `test_main.py` e verificar o resultado dos testes no terminal.

## 🤖 Observações Importantes 🤖

- **Não altere o nome dos arquivos**. Os arquivos `test_main.py` e `main.py` precisam ter esses nomes para que os testes funcionem.
- **Não altere o nome das funções**. Os testes dependem que as funções tenham os nomes especificados no enunciado ou já escritos nos arquivos.
- **Não altere o nome dos parâmetros**. Os testes dependem que as funções tenham os parâmetros especificados no enunciado ou já escritos nos arquivos.
- **Antes de fazer um commit**, execute os testes usando um dos métodos acima para verificar se o seu programa está funcionando corretamente.
- **Caso não consiga corrigir os erros**, entre em contato com o professor ou monitores para que eles possam te ajudar.
  Para isso você deve fazer um commit com o seu trabalho incompleto e abrir uma **issue** no repositório do exercício explicando o seu problema.

## 👀 Curiosidades 👀

O arquivo `requirements.txt` contém uma lista de dependências que o seu programa precisa para funcionar.

No caso desse exercício, a única dependência é o módulo `unittest` que é usado para fazer os testes automáticos.
E como o módulo `unittest` já vem instalado com o python, não é necessário instalar nada.

> Quando precisarmos instalar dependências, o comando `pip` é usado para instalar pacotes do python.
> Caso você precise instalar as dependências do seu programa, basta executar o seguinte comando:
>
> ```bash
> pip install -r requirements.txt
> ```

Os arquivos `Dockerfile` contém as instruções para criar uma imagem do docker com o seu programa.
Isso é útil para que eu possa executar o seu programa em um ambiente controlado e não ter problemas com dependências nem com possível códigos maliciosos na hora de rodar o programa.
São usados dois arquivos `Dockerfile`, um para rodar o seu programa e outro para rodar os testes.

Os arquivos dentro `.vscode` servem para configurar o ambiente de desenvolvimento no [VSCode](https://code.visualstudio.com/).
E facilitar a execução dos testes e do programa.

Os arquivos dentro da pasta `test` são usados para testar o seu programa.

O arquivo `.gitignore` serve para dizer ao git quais arquivos ele deve ignorar.

### :whale: Rodando o programa dentro do docker :whale:

Para aqueles que gostariam de aprender mais sobre o [docker](https://www.docker.com/), aqui vai uma breve explicação de como usar o docker para rodar o seu programa e os testes.

Primeiro, você precisa instalar o docker na sua máquina.
Para isso, basta seguir as instruções do site do [docker](https://docs.docker.com/get-docker/).

Depois de instalar o docker, você precisa criar uma imagem do docker com o seu programa.
Para isso, você precisa criar um arquivo `Dockerfile` com as instruções para criar a imagem do docker.
No caso desse exercício, o arquivo `Dockerfile` já está pronto.

Para criar a imagem do docker com o seu programa, basta executar o seguinte comando:

```bash
docker build -t python-app .
```

Para rodar o seu programa dentro do docker, basta executar o seguinte comando:

```bash
docker run -it --rm python-app
```

Para criar a imagem do docker com os testes, basta executar o seguinte comando:

```bash
docker build -t python-app-test -f test/Dockerfile .
```

Para rodar os testes dentro do docker, basta executar o seguinte comando:

```bash
docker run -it --rm python-app-test
```
