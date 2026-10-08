# 🦫 Bivvo

**Transformando voz em ordens de serviço inteligentes.**

O **Bivvo** é uma plataforma de gerenciamento de ordens de serviço que utiliza inteligência artificial para transformar gravações de áudio em registros estruturados, simplificando o trabalho de profissionais e empresas prestadoras de serviços.

Com uma experiência intuitiva, o Bivvo permite registrar solicitações por voz, organizar atendimentos e acompanhar a execução dos serviços em um único ambiente.

> **Falou. Registrou. Resolveu.**

---

## 🚀 Sobre o projeto

O Bivvo nasceu para simplificar o processo de criação e gerenciamento de ordens de serviço.

Em vez de preencher formulários extensos, o usuário pode simplesmente descrever um serviço por áudio. A inteligência artificial interpreta as informações e gera uma ordem de serviço estruturada, que pode ser revisada antes de ser salva.

### Funcionalidades planejadas

- 🎙️ **Ordens de serviço por voz:** criação de registros a partir de áudios.
- 🤖 **Inteligência artificial:** transcrição e extração de informações relevantes.
- 📋 **Gestão de ordens:** criação, edição, consulta e acompanhamento.
- 👥 **Gestão de clientes:** organização das informações dos clientes.
- 📊 **Dashboard:** indicadores e visão geral dos atendimentos.
- 🔔 **Notificações:** acompanhamento de atualizações importantes.
- 🔐 **Autenticação:** acesso seguro às funcionalidades.

As funcionalidades estão sujeitas à evolução do desenvolvimento.

## 🏗️ Arquitetura

O projeto utiliza uma arquitetura **monorepo**, mantendo as aplicações no mesmo repositório, mas com dependências e ciclos de execução independentes.

```text
bivvo/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
│
├── apps/
│   ├── api/           # API REST - NestJS
│   ├── mobile/        # Aplicativo - React Native
│   └── web/           # Dashboard - React
│
├── docs/
│   └── DESIGN_SYSTEM.md
│
├── .editorconfig
├── .gitignore
├── README.md
└── LICENSE
```

### Aplicações

| Aplicação | Descrição | Tecnologia |
|---|---|---|
| **Mobile** | Aplicativo para criação e acompanhamento de ordens de serviço | React Native + Expo |
| **Web** | Dashboard administrativo e gerenciamento de serviços | React + Vite |
| **API** | Autenticação, regras de negócio, persistência e integração com IA | NestJS |

A comunicação entre as aplicações ocorre por meio de uma API REST.

## 🛠️ Tecnologias

### Mobile

- React Native
- Expo
- TypeScript
- Expo Router

### Web

- React
- TypeScript
- Vite
- Tailwind CSS

### Backend

- Node.js
- NestJS
- TypeScript
- API REST

### Infraestrutura

As tecnologias de banco de dados, armazenamento de arquivos, processamento de IA e hospedagem serão definidas conforme os requisitos do projeto.

## 🎙️ Fluxo de funcionamento

O principal fluxo do Bivvo consiste em transformar uma descrição em áudio em uma ordem de serviço.

1. **Gravação:** o usuário descreve o serviço pelo aplicativo.
2. **Envio:** o áudio é enviado à API.
3. **Transcrição:** o conteúdo falado é convertido em texto.
4. **Interpretação:** a IA identifica informações relevantes, como descrição, cliente e localização, quando mencionadas.
5. **Estruturação:** o sistema monta uma proposta de ordem de serviço.
6. **Revisão:** o usuário valida ou modifica os dados extraídos.
7. **Registro:** a ordem de serviço é salva e disponibilizada para acompanhamento.

A confirmação do usuário faz parte do fluxo para reduzir erros de interpretação e garantir a qualidade das informações registradas.

## ⚙️ Ambiente de desenvolvimento

### Pré-requisitos

- Node.js em versão LTS compatível com as aplicações
- npm
- Git
- Ambiente de desenvolvimento React Native/Expo

### Clonando o repositório

```bash
git clone https://github.com/SEU-USUARIO/bivvo.git
cd bivvo
```

Substitua `SEU-USUARIO` pelo proprietário real do repositório.

### Executando a API

```bash
cd apps/api
npm install
npm run start:dev
```

### Executando o aplicativo mobile

```bash
cd apps/mobile
npm install
npm run start
```

### Executando o website

```bash
cd apps/web
npm install
npm run dev
```

Cada aplicação possui seu próprio `package.json` e deve ser configurada de acordo com suas necessidades.

As variáveis de ambiente e integrações externas devem ser configuradas antes da execução das funcionalidades que dependem delas.

## 🎨 Design System

O Bivvo utiliza uma identidade visual minimalista, inspirada no castor, símbolo de construção, organização e produtividade.

### Paleta de cores

| Cor | Hexadecimal | Aplicação |
|---|---|---|
| Laranja queimado | `#EA580C` | Ações principais e destaques |
| Marrom escuro | `#431407` | Marca, títulos e elementos visuais |
| Creme | `#FFF7ED` | Fundos das interfaces |
| Branco | `#FFFFFF` | Cards e superfícies |
| Cinza quente | `#57534E` | Textos secundários |
| Verde | `#15803D` | Confirmações e estados de sucesso |

As diretrizes de tipografia, componentes, espaçamento e acessibilidade estão documentadas em [Design System](docs/DESIGN_SYSTEM.md).

## 📚 Documentação

A documentação técnica e visual do projeto está organizada no diretório `docs/`.

| Documento | Descrição |
|---|---|
| [Design System](docs/DESIGN_SYSTEM.md) | Identidade visual e padrões de interface |

Novos documentos serão adicionados conforme a evolução da arquitetura e das funcionalidades.

## 🤝 Contribuição

As atividades e melhorias do projeto são organizadas por meio das **GitHub Issues**.

Para contribuir:

1. Consulte as issues existentes.
2. Crie uma issue utilizando o template apropriado.
3. Crie uma branch para sua alteração.
4. Realize as modificações necessárias.
5. Abra um Pull Request descrevendo as alterações.

Os padrões de implementação devem respeitar as diretrizes estabelecidas no repositório.

## 📌 Status do projeto

**Em desenvolvimento.**

O Bivvo está em fase de definição e implementação das funcionalidades do MVP.

## 📄 Licença

A licença do projeto ainda será definida.

---

**Bivvo — Falou. Registrou. Resolveu.**