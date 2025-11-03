<div align="center"><h1>📱 Projeto Flutter 3 - Contador Stateful 🔢 </h1><p><strong>Um projeto de demonstração fundamental que explora os conceitos centrais de <code>StatefulWidget</code> e gestão de estado com <code>setState()</code> no Flutter.</strong></p><p><img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter"><img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart"><a href="#"><img src="https://img.shields.io/badge/Status-Completo_(Demo)-brightgreen?style=for-the-badge" alt="Status do Projeto"></a><a href="#"><img src="https://img.shields.io/badge/Licen%C3%A7a-MIT-blue?style=for-the-badge" alt="Licença"></a><a href="#">
<img src="https://img.shields.io/badge/PRs-Welcome-ff69b4?style=for-the-badge" alt="PRs Welcome"></a>
  
-----------------------------------------------------------------------------------------------------------------------------
<details><summary><strong>📚 Tabela de Conteúdos</strong></summary><ol><li><a href="#-sobre-o-projeto">


 📖 Sobre o Projeto</a></li><li><a href="#-demonstração-em-vídeo">🎥 Demonstração em Vídeo</a></li><li><a href="#-conceitos-principais">✨ Conceitos Principais</a></li><li><a href="#-pilha-de-tecnologias-tech-stack">🛠️ Pilha de Tecnologias (Tech Stack)</a></li><li><a href="#-o-coração-do-estado-análise-do-código">🔑 O Coração do Estado (Análise do Código)</a></li><li><a href="#-começando-getting-started">🚀 Começando (Getting Started)</a></li><li><a href="#-estrutura-de-ficheiros">📂 Estrutura de Ficheiros</a></li><li><a href="#-como-contribuir">🤝 Como Contribuir</a></li><li><a href="#-autor">👨‍💻 Autor</a></li><li><a href="#-licença">📄 Licença</a></li></ol></details>

 ----------------------------------------------------------------------------------------------------------------------------
 📖 Sobre o Projeto
 
Este repositório contém o aplicativo "Contador". Embora seja o ponto de partida padrão (flutter create), ele foi concebido para ser uma lição fundamental sobre a diferença entre Widgets Estáticos e Widgets com Estado.O objetivo é demonstrar como a UI (Interface do Utilizador) pode reagir e ser reconstruída em resposta a uma interação do utilizador, alterando um dado interno (o estado).

-----------------------------------------------------------------------------------------------------------------------------
✨ Conceitos Principais

Este projeto simples é uma demonstração poderosa de 

1. StatelessWidget: (MyApp) Widgets que são imutáveis; as suas propriedades não podem mudar. São perfeitos para a estrutura estática da aplicação.

2. StatefulWidget: (MyHomePage) Widgets que mantêm um estado que pode mudar ao longo do tempo (ex: o número do contador).

3. State Object: O objeto (_MyHomePageState) que armazena a informação mutável (a variável _counter).

4. setState(): A função vital que notifica o Flutter que o estado mudou. Esta chamada aciona o método build para ser executado novamente, "redesenhando" a UI com os novos dados.

5. Árvore de Widgets: A estrutura hierárquica (Scaffold -> AppBar -> Center -> Column -> Text) que define o layout.

6. Interatividade: Capturar eventos de utilizador (onPressed) num FloatingActionButton para acionar a lógica de negócio.

----------------------------------------------------------------------------------------------------------------------------
🛠️ Pilha de Tecnologias (Tech Stack)

A tecnologia utilizada neste projeto é minimalista, mas fundamental:

  Framework (Flutter): UI Toolkit da Google para apps nativas multiplataforma.

  Linguagem (Dart): A linguagem de programação moderna e otimizada para UI.
  
  Gestão de Estado (setState()): O método nativo do Flutter para gerir o estado local do widget.
  
  Design System (Material Design): Biblioteca de componentes visuais (Scaffold, AppBar, FAB).
  
  Build (Flutter SDK): Ferramentas de compilação para Android, iOS, Web, etc.
  
--------------------------------------------------------------------------------------------------------------------------- 
🔑 O Coração do Estado (Análise do Código)

Toda a lógica interativa do aplicativo reside no ficheiro lib/main.dart. O fluxo de dados é simples e poderoso:

-----------------------------------------------------------------------------------------------------------------------------
🚀 Começando (Getting Started)

  Para executar este projeto localmente, siga estes passos.
  
  1. Pré-requisitos:

     Ter o Flutter SDK (v3.x.x ou superior) instalado.

     Um editor de código (como VS Code ou Android Studio).

  2. Guia de Instalação
     Clone o repositório:

         git clone https://github.com/victorhjsantiago/projeto-flutter-1.git

         cd projeto-flutter-1

  3. Instale as dependências:(Este projeto não tem dependências externas, mas este é o comando padrão.)

          flutter pub get

  4. Execute a Aplicação: Certifique-se de que tem um dispositivo (emulador ou físico) em execução.
  
          flutter run

      (Para executar na web, utilize: flutter run -d chrome)

----------------------------------------------------------------------------------------------------------------------------
📂 Estrutura de Ficheiros

projeto-flutter-1/

├── android/            # Configuração e código nativo do Android

├── ios/                # Configuração e código nativo do iOS

├── lib/

│   └── main.dart       # <--- ✨ O PONTO DE ENTRADA E O CORAÇÃO DA APP ✨

├── linux/              # Configuração nativa do Linux

├── macos/              # Configuração nativa do macOS

├── test/

│   └── widget_test.dart # Teste de widget padrão

├── web/                # Configuração nativa da Web

├── .gitignore

├── analysis_options.yaml # Regras de Linter do Dart

└── pubspec.yaml        # Metadados e dependências do projeto

----------------------------------------------------------------------------------------------------------------------------
🤝 Como Contribuir

  Contribuições são o que tornam a comunidade open-source um lugar incrível para aprender, inspirar e criar. Qualquer contribuição que fizer será imensamente apreciada. 
  
  Se tiver uma sugestão para melhorar este projeto (mesmo sendo um demo!), por favor, faça um fork do repositório e crie um pull request.
  
  1. Faça um Fork do Projeto
  
  2. Crie a sua Feature Branch (git checkout -b feature/NovaFeatureIncrivel)
  
  3. Faça Commit das suas mudanças (git commit -m 'Adiciona NovaFeatureIncrivel')
  
  4. Faça Push para a Branch (git push origin feature/NovaFeatureIncrivel)
  
  5. Abra um Pull Request

  Não se esqueça de dar uma estrela ⭐️ ao projeto!
  
-----------------------------------------------------------------------------------------------------------------------------  
  👨‍💻 Autor
  <div align="center"><strong>Victor H. J. Santiago</strong>
    
  <a href="https://github.com/victorhjsantiago"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a><a href="URL_DO_SEU_LINKEDIN_AQUI"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>

-----------------------------------------------------------------------------------------------------------------------------
📄 Licença

Distribuído sob a Licença MIT. Veja LICENSE para mais informações.

