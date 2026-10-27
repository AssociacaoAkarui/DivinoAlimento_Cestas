# Plataforma do Divino Alimento - versão Cestas

A plataforma do Divino Alimento facilita o fluxo de informação de vendas alimentos produzido por diversos agricultores e agricultoras, para diversos compradores e compradoras, por meio do ciclos de entrega de alimentos para venda de **cestas**.

Uma plataforma criada em 2021 a luz iniciativa do Divino Alimento, que é contada com mais detalhes no site da [Akarui](https://www.akarui.org.br/divinoalimento) com apoio do grupo de consumidores de cestas de São Luiz do Paraitinga. 

Para conhecer um pouco mais da plataforma connheça o [site](https://site.multifarm.top/docs/proj/divino/apresentacao) de documentação.

---

## Passo a passo para instalar a plataforma versão 1 em seu computador

Clonar o repositório em um lugar do computador de seu conhecimento. 

No terminal, utilizar o código abaixo:

`git clone https://github.com/AssociacaoAkarui/DivinoAlimento_Cestas.git`

Entrar na pasta que foi criada, utilizando o comando cd 

`cd DivinoAlimento`

Copiar o arquivo com nome "env.example" para a pasta oculta com nome .env. Nesse documento "env.example" tem as configuração das portas e dos acessos incluíndo login e senha.

`cp env.example .env`

Nesse arquivo, a porta padrão é 13000 e pode ser alterada

Vamos ao *rake*, para poder ligar ou desligar o docker que contém o programa do Divino Alimento. Para conhecer os comandos, utilize:

`rake --tasks`

Para construir:

`rake vivo:constroi`

Para subir o docker

`rake vivo:liga`

*Obs: nesse momento precisa colocar o usuário que foi criado, como usuário administrativo para que possa ter acesso a todo o programa. 

Assim precisamos popular o banco de dados. Para tanto:

`rake vivo:popular`

*observação: na tela do sistema é possível acrescentar outras cestas ou editar as informações destas duas. Porém os relatórios não irão incluir as novas cestas cadastradas.*

Para acessar o programa usamos a porta 13000 (ou a porta que deixamos configurada no arquivo .env). Para tanto no buscador de internet colocar:

`localhost:13000`

Para parar o docker

`rake vivo:para`

## Dependências ou programas necessários em seu computador para utilizar o programa:

1. **docker-compose-v2**
2. **rake**
3. **git**
