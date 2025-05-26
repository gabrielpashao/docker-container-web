# 📦 Container da Aplicação Web – **Solifit**
### 💻 Desafio da DIO: *"Criando um Container de uma Aplicação Web"*

Este projeto é a solução do desafio da DIO, que consiste em **containerizar uma aplicação web simples utilizando Docker e Docker Compose**. A aplicação é um site estático chamado **Solifit**, empacotado como `.tar.gz` e entregue via Apache HTTP Server.

---

## ✅ Pré-requisitos

Antes de começar, você precisará ter os seguintes softwares instalados:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)

> 💡 **Observação**: Se você estiver utilizando Docker instalado via *Snap*, evite utilizar **bind mounts**. Este projeto utiliza **volumes nomeados**, compatíveis com Snap e outras distribuições.

---

## 🚀 Como Executar

1. **Clone o repositório ou copie a pasta `projeto-docker`:**

```bash
git clone https://github.com/paixao-dev/projeto-docker.git
```

2. **Acesse a pasta clonada:**

```bash
cd projeto-docker
```

3. **Execute o Docker Compose:**

```bash
$ docker compose up -d --build
```
3. **Abra o navegador e acesse:**

```bash
http://localhost:8080
```
---

## 📁 Estrutura do Projeto

```bash
projeto-docker/
│
├── docker-compose.yml       # Define o serviço e volume
├── Dockerfile               # Instruções de build da imagem
├── solifit.tar.gz           # Arquivos da aplicação web compactados
```
---

## 🔧 O que o Dockerfile faz?

* Usa a imagem httpd como base (Apache).
* Cria e monta um volume nomeado (appdata) persistente.
* Descompacta o arquivo `solifit.tar.gz` no diretório `/usr/local/apache2/htdocs` dentro do container.
* Ajusta permissões para evitar erros 403 e problemas com carregamento de imagens.

---

## 👤 Autor

### **Gabriel Paixão**
Estudante de TI e entusiasta de DevOps e containers 🐳
- [GitHub](https://github.com/gabrielpashao/)
- [Linkedin](https://linkedin.com/in/gabrielspaixao/)
