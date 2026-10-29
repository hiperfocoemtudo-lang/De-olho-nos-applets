# De Olho nos Applets

Uma gaveta flutuante para organizar os applets do Cinnamon e deixar o painel mais livre.

Um pequeno olho monocromático controla a gaveta: ao clicar, ele se abre com uma animação e revela os applets guardados. Ao clicar novamente, o olho se fecha e a gaveta desaparece. Os applets continuam dentro dela e funcionando em segundo plano.

## Recursos

- **Applets reais:** guarda os próprios applets do painel, preservando suas funções e menus.
- **Arrastar e soltar:** organize os applets usando o modo de edição nativo do Cinnamon.
- **Olho animado:** acompanha a abertura e o fechamento da gaveta.
- **Posição flutuante:** abre abaixo do olho e usa o espaço acima quando necessário na borda inferior da tela.
- **Largura dinâmica:** cresce para acomodar applets mais largos e diminui quando o conteúdo encolhe, respeitando o espaço da tela.
- **Botões compactos:** mantém as áreas dos itens próximas dos ícones, evitando que sejam esticadas na altura.
- **Personalização:** ajuste dimensões, espaçamentos, tamanho do olho, animações e aparência clara ou escura.
- **Organização salva:** recupera os applets guardados ao recarregar a gaveta ou iniciar uma nova sessão.
- **Devolução ao painel:** retorne um applet individualmente ou devolva todos de uma vez.

## Requisitos

- Ambiente de trabalho **Cinnamon**.
- Applets já instalados e adicionados ao painel.

Desenvolvido e testado no Linux Mint com Cinnamon 6.6, em sessão X11. A compatibilidade com outras versões do Cinnamon e com cada applet de terceiros pode variar.

## Instalação

Baixe e extraia os arquivos do projeto. A pasta deve manter esta estrutura:

```text
Gaveta-Olho/
├── instalar.sh
├── README.md
└── gaveta-olho@local/
    ├── applet.js
    ├── metadata.json
    ├── settings-schema.json
    └── stylesheet.css
```

Abra um terminal nessa pasta e execute, sem `sudo`:

```sh
sh instalar.sh
```

O instalador copia o applet para a pasta do seu usuário, preserva as preferências existentes e adiciona o olho ao painel. Quando disponível, dá preferência ao painel superior.

### Instalação manual

Copie a pasta `gaveta-olho@local` para:

```text
~/.local/share/cinnamon/applets/
```

Depois, abra **Configurações do Sistema → Applets**, procure **Gaveta do Olho** e adicione ao painel.

## Como usar

### Guardar applets

1. Clique com o botão direito no olho e escolha **Organizar applets**.
2. Arraste um applet do painel para a gaveta ou diretamente para o olho.
3. Clique em **Concluir** para sair do modo de edição.
4. Clique no olho para mostrar ou esconder a gaveta.

O modo de edição é necessário para arrastar os applets. Depois de concluir a organização, use-os normalmente dentro da gaveta.

**Fechar a gaveta não devolve os applets ao painel.** Eles permanecem guardados e continuam funcionando; para interagir com eles novamente, abra o olho.

### Devolver ao painel

- **Um applet:** entre em **Organizar applets** e clique no botão **↥** ao lado dele.
- **Todos os applets:** clique com o botão direito no olho e escolha **Devolver todos ao painel**.

## Personalização

Clique com o botão direito no olho e selecione **Configurar**.

| Opção | O que ajusta |
| --- | --- |
| Largura mínima da gaveta | Largura inicial; pode aumentar automaticamente conforme o conteúdo. |
| Altura da gaveta | Espaço vertical disponível para os applets. |
| Distância horizontal | Espaço entre os applets de uma linha. |
| Distância vertical | Espaço entre as linhas. |
| Aparência | Modo claro ou escuro da gaveta. |
| Tamanho do olho | Tamanho do ícone no painel. |
| Animações | Ativa ou desativa as animações. |

Os espaçamentos horizontal e vertical são independentes. Os itens passam para novas linhas quando necessário. A gaveta respeita o limite da tela; conteúdos maiores que esse limite ou que a altura configurada podem precisar de rolagem.

Se a janela de configuração estava aberta durante uma atualização, feche-a e abra novamente para visualizar as novas opções.

## Remoção

Remova a **Gaveta do Olho** pela ferramenta de applets do Cinnamon. Antes de ser descarregado, o applet devolve ao painel os itens que estavam guardados.

Para apagar também os arquivos instalados, remova a pasta `~/.local/share/cinnamon/applets/gaveta-olho@local` **depois** de retirar o applet do painel.

## Relatar um problema

Ao abrir uma issue, informe:

- Versão do Linux Mint e do Cinnamon.
- Nome e versão do applet que apresentou o problema.
- O que você fez e o que aconteceu.
- Uma captura de tela, se ajudar a mostrar o comportamento.

## Informações do projeto

- **Nome:** Gaveta do Olho
- **Identificador:** `gaveta-olho@local`
- **Versão documentada:** 1.2.1
