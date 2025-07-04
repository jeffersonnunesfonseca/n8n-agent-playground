# 🚀 n8n Local Playground

## 📋 Sobre o Projeto

Este playground é um ambiente pré-configurado para testes e estudos do [n8n](https://n8n.io/), uma ferramenta de automação de fluxos de trabalho. Este ambiente local facilita a integração e experimentação com várias ferramentas e serviços, incluindo:

- WhatsApp API
- Large Language Models (LLMs)
- Bancos de dados vetoriais
- E outros serviços para automação de processos

## 🧰 Pré-requisitos

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- Pelo menos 2GB de RAM disponível
- Portas 5678 e 8080 liberadas no seu computador

## 🚀 Como Executar o Projeto

### Passo 1: Clone o repositório

```bash
git clone https://github.com/jeffersonnunesfonseca/n8n-agent-playgroung.git n8n
cd n8n
```

### Passo 2: I nicie o ambiente Docker

Para iniciar todos os serviços do ambiente, execute:

```bash
docker compose up -d --build --force-recreate --remove-orphans
```

Explicação dos parâmetros:

- `-d`: Executa os containers em segundo plano
- `--build`: Constrói as imagens antes de iniciar os containers
- `--force-recreate`: Recria os containers mesmo se a configuração e a imagem não mudaram
- `--remove-orphans`: Remove containers para serviços não definidos no arquivo docker-compose atual

### Passo 3: Verificação

Aguarde alguns segundos para que todos os serviços inicializem completamente. Em seguida, acesse as interfaces web disponíveis nos links abaixo.

## 🔗 Acessos Disponíveis

- **n8n Interface**: [http://localhost:5678](http://localhost:5678)
  - Workflow de exemplo: [http://localhost:5678/workflow/kAU8oQL7TDqGTF5s](http://localhost:5678/workflow/kAU8oQL7TDqGTF5s)
- **Manager Evolution**: [http://localhost:8080/manager](http://localhost:8080/manager)
- **OpenAI (para configuração de API Keys)**: [https://platform.openai.com/settings/organization/api-keys](https://platform.openai.com/settings/organization/api-keys)

## 🛑 Como Parar o Ambiente

Para parar todos os serviços:

```bash
docker compose down
```

Para remover todos os dados e volumes:

```bash
docker compose down -v
```

## 📚 Recursos Adicionais

- [Documentação oficial do n8n](https://docs.n8n.io/)
- [Tutoriais do n8n](https://n8n.io/tutorials/)
- [Comunidade do n8n](https://community.n8n.io/)

## ❓ Solução de Problemas

Se encontrar algum problema ao iniciar o ambiente, verifique:

1. Se as portas 5678 e 8080 não estão sendo usadas por outros serviços
2. Se o Docker tem permissões suficientes para criar e gerenciar containers
3. Se há espaço em disco suficiente para as imagens Docker

Para visualizar os logs dos containers:

```bash
docker compose logs
```

Para um serviço específico:

```bash
docker compose logs n8n
```
