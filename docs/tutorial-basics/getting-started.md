---
sidebar_position: 1
---

# Getting Started

## Configurando workspace thingML para o Visual Studio Code (VsCode)

**Passo 1**  - Faça o download da extensão thingML para vscode em: [download automático](https://github.com/TelluIoT/ThingML/releases/download/21.7.1/thingml-vscode-21.7.1.vsix )

**Passo 2** - Vá até a pasta **(C:\Users\SeuUsuario\.vscode\extensions\)** e dentro dela crie uma pasta para a nova extensão. **Evite usar espaços no nome da pasta.**
Dentro da pasta criada, coloque o arquivo .vsix baixado, mantenha copiado o caminho para o arquivo baixado dentro da pasta.

**Passo 3** - Acesse um terminal(prompt de comando). Pode ser o PowerShell ou o terminal do VsCode por exemplo.

**Modo 1:**
    No terminal, digite o comando:

    code --install-extension <caminho para seu arquivo .vsix>

    O comando completo deve se parecer com:
    code --install-extension C:\Users\SeuUsuario\.vscode\extensions\ThingML\thingml-vscode-21.7.1.vsix

**Modo 2:**
    No Vscode, navegue até o local onde você salvou o arquivo .vsix e em seguida digite o comando abaixo<br></br>
    **Obs:**  o ideal é que o arquivo esteja salvo no caminho mostrado no passo 2
  

    code --install-extension thingml-vscode-21.7.1.vsix

**Passo 4** - Para testar a instalação, execute um arquivo ThingML, siga o tutorial "hello world" disponível na seção "Syntax" desta documentação
