# LEANDRO TV HUB

Projeto inicial de launcher para Android TV / Google TV, com tema preto OLED.

## O que já está implementado
- Tela inicial com relógio, data e categorias.
- Atalhos para Flix Cine, YouTube, TCL Channel, Spotify e YouTube Music (se instalados).
- Atalho de orientação para Xbox Series S via HDMI.
- Tela de configurações com alternância de efeitos sonoros, sons de navegação, sons de abrir apps, animações e relógio/data.
- Volume dos efeitos em passos de 10%, iniciando em 50%.
- Tela Sobre com autoria e Instagram.
- Intent HOME para permitir selecionar o app como launcher padrão.

## Como gerar o APK
1. Instale o Android Studio em um computador.
2. Extraia este ZIP.
3. Abra a pasta `LeandroTVHub` no Android Studio.
4. Aguarde o Gradle Sync e aceite a instalação do Android SDK 35, se solicitado.
5. Selecione **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. O APK de debug costuma aparecer em `app/build/outputs/apk/debug/app-debug.apk`.

## Como escolher como launcher
Depois de instalar, pressione Home no controle remoto e escolha LEANDRO TV HUB. Em alguns modelos, a opção de launcher padrão pode ficar em Configurações > Apps > Apps padrão.

## Observações importantes
- O Android restringe a descoberta e abertura de apps de terceiros; a busca por nome é uma tentativa simples e pode exigir ajuste para pacotes específicos dos apps instalados.
- O botão Xbox não muda automaticamente a entrada HDMI: isso depende do suporte da TV a HDMI-CEC e das APIs do fabricante.
- Os efeitos usam tons simples do sistema, não arquivos de áudio personalizados.
- Este ZIP contém o código-fonte do projeto, não um APK compilado.


## Compilação automática pelo GitHub
O projeto inclui `.github/workflows/build-apk.yml`. Depois de enviar os arquivos ao repositório:
1. Abra a aba **Actions**.
2. Se solicitado, habilite GitHub Actions para o repositório.
3. Abra **Gerar APK Android** e clique em **Run workflow** (ou faça um push para `main`/`master`).
4. Quando terminar com status verde, abra a execução e baixe o artefato **Leandro-TV-HUB-APK**.
5. O arquivo baixado contém `app-debug.apk`, que pode ser transferido para a TV para teste.
