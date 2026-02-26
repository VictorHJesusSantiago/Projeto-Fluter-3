<div align="center">

<img src="https://storage.googleapis.com/cms-storage-bucket/0dbfcc7a59cd1cf16282.png" alt="Flutter Logo" width="110" />

# 📱 Projeto Flutter 3 — Contador Stateful

**Um projeto de demonstração fundamental que explora os conceitos centrais de**
**`StatefulWidget` e gestão de estado com `setState()` no Flutter.**

<br>

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Material Design](https://img.shields.io/badge/Material%20Design-757575?style=for-the-badge&logo=materialdesign&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completo_(Demo)-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/Licença-MIT-blue?style=for-the-badge)
![PRs](https://img.shields.io/badge/PRs-Welcome-ff69b4?style=for-the-badge)

</div>

---

## 📚 Tabela de Conteúdos

> Navegue rapidamente pelas seções do projeto.

| # | Seção |
|:-:|:------|
| 1 | [📖 Sobre o Projeto](#-sobre-o-projeto) |
| 2 | [✨ Conceitos Principais](#-conceitos-principais) |
| 3 | [🛠️ Pilha de Tecnologias](#️-pilha-de-tecnologias) |
| 4 | [🔑 O Coração do Estado](#-o-coração-do-estado--análise-do-código) |
| 5 | [🚀 Começando (Getting Started)](#-começando-getting-started) |
| 6 | [📂 Estrutura de Arquivos](#-estrutura-de-arquivos) |
| 7 | [🤝 Como Contribuir](#-como-contribuir) |
| 8 | [👨‍💻 Autor](#-autor) |
| 9 | [📄 Licença](#-licença) |

---

## 📖 Sobre o Projeto

> Este repositório contém o aplicativo **"Contador"** — o ponto de partida padrão do Flutter, reimaginado como uma **lição fundamental** sobre a diferença entre Widgets Estáticos e Widgets com Estado.

O objetivo central é demonstrar como a **UI (Interface do Usuário)** pode reagir e ser reconstruída dinamicamente em resposta a uma interação do usuário, alterando um dado interno — o **estado** da aplicação.

Simples na aparência, poderoso nos conceitos que ensina.

---

## ✨ Conceitos Principais

> Este projeto demonstra os pilares da arquitetura reativa do Flutter de forma clara e progressiva.

| Conceito | Classe / Método | Descrição |
|:---------|:---------------:|:----------|
| 🧱 **StatelessWidget** | `MyApp` | Widget imutável — suas propriedades não mudam após a criação. Ideal para estrutura estática da aplicação. |
| 🔄 **StatefulWidget** | `MyHomePage` | Widget que mantém um **estado mutável** ao longo do tempo (ex: o número do contador). |
| 📦 **State Object** | `_MyHomePageState` | Objeto que armazena a informação mutável — a variável `_counter`. |
| ⚡ **setState()** | `setState()` | Função vital que **notifica o Flutter** sobre mudanças de estado, acionando o método `build()` para redesenhar a UI. |
| 🌳 **Árvore de Widgets** | `Scaffold → AppBar → Center → Column → Text` | Estrutura hierárquica que define o layout visual da tela. |
| 👆 **Interatividade** | `onPressed` | Captura eventos do usuário no `FloatingActionButton` para acionar a lógica de negócio. |

---

## 🛠️ Pilha de Tecnologias

> Tecnologias minimalistas, mas fundamentais — escolhidas para manter o foco total nos conceitos de estado.

| Tecnologia | Função no Projeto |
|:-----------|:------------------|
| **Flutter 3** | UI Toolkit da Google para construção de apps nativas multiplataforma (Android, iOS, Web, Desktop). |
| **Dart** | Linguagem de programação moderna, otimizada para desenvolvimento de UI reativa. |
| **setState()** | Método nativo do Flutter para gerenciamento de **estado local** do widget. |
| **Material Design** | Biblioteca de componentes visuais: `Scaffold`, `AppBar`, `FloatingActionButton`. |
| **Flutter SDK** | Ferramentas de compilação para Android, iOS, Web, Linux, macOS e Windows. |

---

## 🔑 O Coração do Estado — Análise do Código

> Toda a lógica interativa reside em `lib/main.dart`. O fluxo de dados é simples, direto e poderoso.

```dart
// 1. O StatefulWidget declara que possui estado mutável
class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});
  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

// 2. O State Object armazena e gerencia o dado mutável
class _MyHomePageState extends State<MyHomePage> {
  int _counter = 0; // ← O ESTADO: o dado que pode mudar

  void _incrementCounter() {
    setState(() {
      // 3. setState() notifica o Flutter e dispara o rebuild da UI
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    // 4. build() é chamado novamente, exibindo o novo valor de _counter
    return Scaffold(
      appBar: AppBar(title: Text(widget.title)),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            const Text('Você pressionou o botão este número de vezes:'),
            Text(
              '$_counter', // ← O estado é refletido aqui
              style: Theme.of(context).textTheme.headlineMedium,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter, // ← Evento do usuário
        tooltip: 'Incrementar',
        child: const Icon(Icons.add),
      ),
    );
  }
}
```

**Fluxo resumido:**

```
👆 Usuário pressiona o botão
        ↓
⚡ _incrementCounter() é chamado
        ↓
📦 setState() incrementa _counter
        ↓
🔄 Flutter chama build() novamente
        ↓
🖥️ UI é redesenhada com o novo valor
```

---

## 🚀 Começando (Getting Started)

### 📋 Pré-requisitos

| Requisito | Detalhe |
|:----------|:--------|
| **Flutter SDK** | Versão **3.x.x ou superior** instalada e configurada no `PATH`. |
| **Editor de Código** | Recomenda-se **VS Code** (com extensão Flutter) ou **Android Studio**. |
| **Dispositivo/Emulador** | Android, iOS, Chrome (web) ou Desktop configurado e em execução. |

---

### 🔧 Passo a Passo

**1. Clone o repositório:**

```bash
git clone https://github.com/VictorHJesusSantiago/projeto-flutter-1.git
cd projeto-flutter-1
```

**2. Instale as dependências:**

```bash
# Este projeto não possui dependências externas,
# mas este é o comando padrão do Flutter:
flutter pub get
```

**3. Verifique o ambiente Flutter:**

```bash
flutter doctor
```

**4. Execute a aplicação:**

```bash
# Em dispositivo padrão (emulador ou físico)
flutter run

# Especificamente no Chrome (Web)
flutter run -d chrome

# Listar todos os dispositivos disponíveis
flutter devices
```

---

### 🛰️ Plataformas Suportadas

| Plataforma | Comando | Status |
|:-----------|:--------|:------:|
| 🤖 **Android** | `flutter run -d android` | ✅ Suportado |
| 🍎 **iOS** | `flutter run -d ios` | ✅ Suportado |
| 🌐 **Web (Chrome)** | `flutter run -d chrome` | ✅ Suportado |
| 🪟 **Windows** | `flutter run -d windows` | ✅ Suportado |
| 🐧 **Linux** | `flutter run -d linux` | ✅ Suportado |
| 🍏 **macOS** | `flutter run -d macos` | ✅ Suportado |

---

## 📂 Estrutura de Arquivos

```plaintext
projeto-flutter-1/
│
├── 📁 android/                    # ⚙️  Configuração e código nativo Android
├── 📁 ios/                        # ⚙️  Configuração e código nativo iOS
├── 📁 linux/                      # ⚙️  Configuração nativa Linux
├── 📁 macos/                      # ⚙️  Configuração nativa macOS
├── 📁 windows/                    # ⚙️  Configuração nativa Windows
├── 📁 web/                        # ⚙️  Configuração nativa Web
│
├── 📁 lib/
│   └── 📄 main.dart               # ✨ PONTO DE ENTRADA — Toda a lógica do app
│
├── 📁 test/
│   └── 📄 widget_test.dart        # 🧪 Teste de widget padrão do Flutter
│
├── 📄 pubspec.yaml                # 📦 Metadados, dependências e assets do projeto
├── 📄 analysis_options.yaml       # 🔍 Regras de linter do Dart
└── 📄 .gitignore                  # 🚫 Arquivos ignorados pelo Git
```

---

## 🤝 Como Contribuir

> Contribuições tornam a comunidade open-source um lugar incrível para aprender e crescer. Qualquer melhoria é muito apreciada!

| Passo | Ação | Comando |
|:-----:|:-----|:--------|
| 1️⃣ | **Fork** | Crie um fork do repositório para a sua conta. |
| 2️⃣ | **Branch** | Crie sua feature branch. | `git checkout -b feature/NovaFeature` |
| 3️⃣ | **Commit** | Salve suas alterações com mensagem clara. | `git commit -m 'feat: Adiciona NovaFeature'` |
| 4️⃣ | **Push** | Envie a branch para o repositório remoto. | `git push origin feature/NovaFeature` |
| 5️⃣ | **Pull Request** | Abra um PR detalhando as mudanças realizadas. | — |

<div align="center">

<br>

**Se este projeto foi útil para os seus estudos, deixe uma estrela ⭐️ no repositório!**

</div>

---

## 👨‍💻 Autor

<div align="center">

<br>

**Victor H. J. Santiago**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/VictorHJesusSantiago)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victor-henrique-de-jesus-santiago/)

</div>

---

## 📄 Licença

<div align="center">

Este projeto está distribuído sob a **Licença MIT**.
Consulte o arquivo [`LICENSE`](./LICENSE) no repositório para mais informações.

![License](https://img.shields.io/badge/Licença-MIT-blue?style=for-the-badge)

</div>

---

<div align="center">

*Feito com 💙 e Flutter por **Victor H. J. Santiago***

</div>
