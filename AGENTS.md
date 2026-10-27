# Repository Guidelines

## Estrutura do projeto

Este repositório contém uma exportação estática de um site. `index.html` é a página principal e concentra a marcação, estilos e lógica interativa. `assets/` guarda imagens, favicon e cópias locais de bibliotecas usadas pela página. `assets/_wd3/` contém metadados da captura, como manifesto e índice dos recursos. Não há diretórios separados de aplicação ou testes.

## Desenvolvimento local

Não há `package.json`, sistema de build ou scripts de teste configurados. Para abrir o site por HTTP, na raiz execute:

```sh
python3 -m http.server 8000
```

Acesse `http://localhost:8000` no navegador e encerre o servidor com `Ctrl+C`. A página também foi preparada para abrir como arquivo local, mas HTTP facilita verificar o carregamento de recursos e o comportamento do navegador.

## Estilo e alterações

Preserve a estrutura da exportação: mantenha a página de entrada em `index.html` e os recursos locais em seus caminhos existentes sob `assets/`. O HTML é extenso e contém código embutido; faça alterações localizadas, mantenha a indentação e o estilo da seção editada e evite reformatar o arquivo inteiro. Use nomes descritivos para novos recursos e atualize referências no HTML quando mover ou adicionar arquivos. Não edite bibliotecas vendorizadas ou metadados da captura sem necessidade funcional clara.

## Verificação

Não existe framework de testes nem requisito de cobertura configurado. Após uma alteração, abra a página no navegador e verifique a seção afetada, a navegação, o console e o carregamento de imagens ou scripts relacionados. Para mudanças responsivas, confira também uma largura de tela móvel. Se alterar caminhos de recursos, confirme que eles respondem pelo servidor local.

## Commits e pull requests

Não há histórico Git disponível nesta cópia para inferir convenções existentes. Prefira mensagens curtas, no imperativo e com escopo claro, por exemplo: `Ajusta navegação mobile`. Em pull requests, descreva o que mudou e como foi verificado; inclua capturas de tela para mudanças visuais e liste recursos adicionados ou removidos.

## Segurança e configuração

Não inclua credenciais, tokens ou dados privados em `index.html` nem em `assets/`. Preserve as dependências locais e evite introduzir chamadas externas sem explicar sua finalidade e impacto no funcionamento offline.
