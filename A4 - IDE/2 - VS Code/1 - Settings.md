```java
{
  "explorer.compactFolders": false, // Define o theme do vscode
  "workbench.iconTheme": "material-icon-theme", // define o tipo de icones do vscode
  "workbench.startupEditor": "none", // definimos o que será feito quando o vscode inicializar, neste caso nada
  "editor.fontSize": 14, // tamanho da fonte
  "editor.lineHeight": 24, // altura da linha
  // "editor.rulers": [
  //   80,
  //   120
  // ], // tamanho das linhas de quebra
  // "editor.wordWrap": "on", // habilitar por padrão a quebra automática
  "editor.tabSize": 2, // tamanho do tab em espaços
  "editor.renderLineHighlight": "gutter", // tipo de destaque de linha
  // "editor.formatOnSave": true, // formata o arquivo ao salvar
  // "editor.formatOnPaste": false, // required
  // "editor.formatOnType": false, // required
  // "editor.formatOnSaveMode": "file", // required to format on save
  // "editor.suggestSelection": "first",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.addMissingImports": "explicit"
  },
  "files.trimTrailingWhitespace": true, // elimina espaços desnecessários no final da linha
  "files.insertFinalNewline": true, // insere uma nova linha no final do arquivo
  "files.trimFinalNewlines": true, // remove espaços nas novas linhas finais
  "files.exclude": { // esconde estas pastas do browser de arquivos
    "**/node_modules": true,
  },
  // "terminal.integrated.fontFamily": "Menlo for Powerline", // fonte do console
  "terminal.integrated.fontSize": 14, // tamanho da fonte do console
  "terminal.integrated.fontWeight": "300", // espessura da fonte no console
  "git.enableSmartCommit": true, // habilita commits inteligentes
  "git.autofetch": true, // realiza o auto fetch no plugin de git
  "breadcrumbs.enabled": true, // habilita o caminho de pão no cabeçalho do editor
  "liveServer.settings.donotShowInfoMsg": true, // Desativa mensagens de informação do Live Server, mantendo a interface do usuário mais limpa
  "liveServer.settings.CustomBrowser": "chrome", // Define o Chrome como o navegador padrão para o Live Server, garantindo que os projetos sejam abertos neste navegador
  "console-ninja.featureSet": "Community",
  "security.allowedUNCHosts": [
    "wsl.localhost"
  ],
  "remote.autoForwardPortsSource": "hybrid", // Define a política de encaminhamento automático de portas para "híbrido", otimizando a experiência de desenvolvimento remoto
  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue", // Configura o IntelliCode do VSCode para selecionar sugestões de código automaticamente baseado em usos anteriores
  "tabnine.experimentalAutoImports": true, // Ativa importações automáticas experimentais pelo TabNine, melhorando a eficiência ao escrever código
  // Habilita o suporte do Emmet para JSX dentro de arquivos JavaScript, aumentando a produtividade no desenvolvimento de interfaces
  "emmet.syntaxProfiles": {
    "javascript": "jsx"
  },
  // Amplia o suporte do Emmet para incluir React e CSS em arquivos JavaScript, facilitando a escrita de código mais rápido
  "emmet.includeLanguages": {
    "javascript": [
      "javascriptreact",
      "css"
    ]
  },
  // Personaliza as cores dos pares de colchetes para melhorar a legibilidade do código com cores distintas
  "RainbowBrackets.consecutivePairColors": [
    "()",
    "[]",
    "{}",
    [
      "Gold",
      "Orchid",
      "LightSkyBlue"
    ],
    "Revioletd"
  ],
  // Define o estilo da borda para o escopo ativo em Rainbow Brackets, melhorando a visualização do escopo do código
  "RainbowBrackets.activeScopeCSS": [
    "borderStyle : solid",
    "borderWidth : 1px",
    "borderColor : {color}; opacity: 0.5"
  ],
  // Associa ícones específicos a pastas no tema Material Icon, personalizando a visualização do explorador de arquivos
  "material-icon-theme.folders.associations": {
    "entities": "class",
    "repositories": "mappings",
    "usecases": "controller"
  },
"terminal.integrated.defaultProfile.windows": "PowerShell", // Define o PowerShell como o perfil padrão do terminal integrado no Windows, otimizando o fluxo de trabalho no terminal
  // Configura perfis de terminal específicos, permitindo fácil acesso a diferentes ambientes de terminal como PowerShell, Git Bash e WSL
  "terminal.integrated.profiles.windows": {
    "PowerShell": {
      "source": "PowerShell",
      "icon": "terminal-powershell"
    },
    "Git Bash": {
      "source": "Git Bash"
    },
    "Ubuntu-20.04 (WSL)": {
      "path": "C:\\Windows\\System32\\wsl.exe",
      "args": [
        "-d",
        "Ubuntu-20.04"
      ]
    }
  },
  "terminal.integrated.env.linux": {},
  "terminal.integrated.env.windows": {},
  "workbench.editorAssociations": {
    "*.class": "default"
  },
  "git.confirmSync": false,
  "[jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
"workbench.colorTheme": "Dracula",
"github.copilot.editor.enableAutoCompletions": true,
  "liveshare.accessibility.voice": "pt-BR-Antonio",
  "accessibility.voice.speechLanguage": "pt-BR",
  "liveshare.accessibility.voiceEnabled": false,
  "accessibility.signals.voiceRecordingStopped": {
    "sound": "on"
},
"window.zoomLevel": -1,
"accessibility.voice.keywordActivation": "chatInContext",
}

```
