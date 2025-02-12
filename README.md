<h1 align=center> YAML-Templates</h1>
<p align=center>Templates para Fluxos de Trabalho diversos (Workflows)</p>

## O que é um _Workflow_?
Um fluxo de trabalho é uma ação executada em seu repositório do Git-Hub que facilita o desenvolvimento de seu projeto. 
Esses fluxos de trabalho são chamados de **Git-Hub Actions** e podem fazer as mais diversas tarefas, como executar comandos de PowerShell e Shell do Linux. Também podem ser executados em horários agendados como uma _Cron Job_. Praticamente você pode fazer o que quiser.

Os workflows podem ser usados para testar se aplicações não tem nenhum erro de compilação antes de mesclar um Pull-Request. Isso é muito útil no desenvolvimento de projetos em equipe.
<h2 align=center>Tem algum template de Workflow que não citei aqui? Crie um Pull-Request</h2>

<details><summary>

Clique para ver Templates de _Workflow_ 

</summary>

- ### [Build de aplicação Flutter para Android](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/android%20Flutter%20project.yml)
- ### [Build de aplicação Flutter para IOS](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/ios%20Flutter%20project.yml)
- ### [Build de aplicação Ionic para Android](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/android%20Ionic%20project.yml)
- ### [Build de aplicação Ionic para IOS](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/ios%20Ionic%20project.yml)
- ### [Deploy de arquivos por FTP](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/deploy%20FTP.yml)
- ### [Build de Aplicações .NET C#](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/desktop%20.NET%20Core.yml)
- ### [Build de Aplicações C com GCC](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/desktop%20GCC.yml)
- ### [Build de Projetos do Raspberry Pi Pico com Pico SDK](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/RaspberryPi%20Pico%20W%20Pico%20SDK.yml) 
- ### [Personalizar um botão de arrecadação de fundos no seu repositório ](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/FUNDING.yml)
- ### [Gerar binário executável de script Shell](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/desktop%20sh%20to%20BIN.yml)
- ### [Gerar executável de script do PowerShell](https://github.com/ThiagoSousa81/YAML-Templates/blob/main/desktop%20ps1%20to%20exe.yml)

</details>

> É importante mencionar que o uso de workflows consome uma cota em minutos de uso na sua conta do Git-Hub. Verifique sua cota constantemente, ou tente hospedar seu workflow em outra plataforma se necessário. 
>
> As cotas são reiniciadas em um ciclo a cada 30 dias
>
> Planos gratuitos do Git-Hub tem uma cota de 2000 minutos de wokflow mensais

## Estrutura de um _Workflow_

    # Nome do workflow. Este nome será exibido na interface do GitHub.
    name: Simple Workflow

    # Define os eventos que acionam o workflow.
    on:

    # O cronograma abaixo define que o workflow será executado todos os dias à meia-noite (UTC).
    schedule:
    - cron: '0 0 * * *'

    # Poderá ser acionado também em um push para a branch 'main'.
    push:
        branches:
        - main

    # Define os jobs que serão executados como parte do workflow.
    jobs:
    
    # Nome do job. Você pode nomear como quiser.
    print_message:
        # Define o ambiente em que o job será executado. Aqui estamos usando a última versão do Ubuntu.
        runs-on: ubuntu-latest

        # Define as etapas (steps) que serão executadas neste job.
        steps:
        # A primeira etapa é imprimir uma mensagem no console.
        - name: Print a message
            # Executa um comando de shell que imprime uma mensagem.
            run: echo "Hello, World! Este é meu primeiro Workflow do Git-Hub Actions!"

## 🐞 Encontrei um bug...
### Abra uma [Issue](https://github.com/ThiagoSousa81/YAML-Templates/issues/new) e vamos conversar 🧑‍💻