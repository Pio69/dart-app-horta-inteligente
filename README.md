# Horta Inteligente App🌱

Aplicativo desenvolvido em **Flutter e Dart** para consultar informações de uma horta conectada. O projeto utiliza requisições HTTP para acessar uma aplicação na plataforma **Losant** e apresentar leituras de sensores e eventos.

## Funcionalidades

- Tela de login integrada ao serviço configurado no projeto.
- Exibição de temperatura e umidade do ar, luminosidade e umidade do solo.
- Listagem de eventos e seus estados.
- Interface organizada em abas para dados e eventos.

## Tecnologias

- [Flutter](https://flutter.dev/) e Dart
- [Losant](https://www.losant.com/) para a integração com a horta conectada
- Requisições HTTP e respostas JSON
- `flutter_native_splash` para a tela inicial

## Como executar

### Pré-requisitos

- Flutter instalado, com uma versão do Dart compatível com a restrição do projeto: **>= 2.18.1 e < 3.0.0**.
- Um dispositivo, emulador ou outro ambiente configurado para executar Flutter.
- Acesso à aplicação Losant configurada no código e credenciais válidas para o login.

### Instalação

```bash
git clone https://github.com/Pio69/dart-app-horta-inteligente.git
cd dart-app-horta-inteligente
flutter pub get
flutter run
```

O Flutter mostra os dispositivos disponíveis caso seja necessário escolher um. Para conferir a configuração do ambiente, use `flutter doctor`.

## Integração com a Losant

As URLs da aplicação estão definidas diretamente nos arquivos das páginas:

- `lib/pages/login.page.dart` — login.
- `lib/pages/data.page.dart` — consulta das leituras dos sensores.
- `lib/pages/events.page.dart` — consulta dos eventos.

Para usar outra aplicação ou API, será necessário adaptar esses endereços e, se a estrutura das respostas for diferente, o código que interpreta os dados. A exibição depende da disponibilidade do serviço e do formato esperado das respostas.

## Estrutura do projeto

```text
lib/
├── main.dart                    # inicialização do aplicativo
└── pages/
    ├── login.page.dart          # tela de login
    ├── home.page.dart           # navegação entre abas
    ├── data.page.dart           # leituras dos sensores
    ├── events.page.dart         # eventos
    ├── reset-password.page.dart # tela de recuperação de senha
    ├── signup.page.dart         # tela de cadastro
    └── initial.page.dart        # tela inicial
assets/images/                   # imagens do aplicativo
```

O projeto também contém telas de cadastro e recuperação de senha; seus fluxos devem ser revisados antes de serem usados como funcionalidades completas.
