# IA
# Documentação para Configuração e Execução do Ollama

## 1. Baixando e Instalando o Ollama

Para começar, faça o download e instale o Ollama a partir do seguinte link:

- [Baixar o Ollama](https://ollama.com/download)

## 2. Criar um Diretório de Trabalho

Abra o terminal e crie um diretório para armazenar seus arquivos de configuração:

```bash
mkdir teste
```


## 3. Adicionar o Modelo Llama 3 (Opcional)

Se desejar, você pode baixar o modelo Llama 3 com o seguinte comando:

```bash
ollama pull llama3
```


## 4. Listar Todos os Modelos Disponíveis
Para visualizar todos os modelos disponíveis, use o comando:

```bash
ollama list
```


##  5. Criar um Novo Arquivo de Modelo
Para criar um arquivo de configuração para um modelo específico, execute:

```bash
ollama show llama3:latest --modelfile > teste.modelfile
```


##  6. Editar o Arquivo de Modelo
Abra o arquivo teste.modelfile para editação. Você pode usar o editor de texto de sua escolha, como o VS Code:

```bash
code .
```


Exemplo de Modificação do Arquivo de Modelo
Você pode definir o sistema no arquivo teste.modelfile conforme o exemplo abaixo. Para mais detalhes, consulte a documentação oficial do Modelfile.

# Exemplo de conteúdo:

```python
SYSTEM  """Hello, my name is Teste de Genival. I am a senior software developer with over 30 years of experience in the field. My expertise spans a wide range of technologies, including Java, JavaScript, React, React Native, Vue.js, Angular, Node.js, TypeScript, PHP, and Python. My practices and approaches focus on applying development best practices, with an emphasis on agility, clean architecture, and SOLID principles. I am here to serve as your assistant, providing support and clarifications in both Portuguese and English."""
```

## 7. Criar o Modelo no Ollama
Para criar um novo modelo com base no arquivo de configuração, execute:

```bash
ollama create teste --file teste.modelfile
```


## 8. Listar Todos os Modelos Novamente
Para confirmar que o modelo foi criado, liste todos os modelos novamente:

```bash
ollama list
```


## 9. Executar o Modelo
Execute o modelo recém-criado com o comando:

```bash
ollama run teste
```


##  10. Visualização Opcional (Utilizando Docker)
Se desejar usar a visualização via Docker, execute o seguinte comando:

```bash
```sudo docker run -d -p 3000:8080 --add-host=host.docker.interna
l:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main