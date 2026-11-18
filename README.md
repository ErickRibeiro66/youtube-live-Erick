# YouTube Live

Protótipo acadêmico de uma plataforma fictícia de transmissões ao vivo. A interface usa React, JavaScript, Vite, React Router, CSS com Grid e Flexbox e ícones do Lucide. As imagens ilustrativas ficam no projeto e foram geradas com ImageGen.

## Execução local

Use Node.js 22.12 ou superior e npm em Windows, macOS ou Linux.

```sh
npm ci
npm run dev
```

Acesse a URL que o Vite mostrar no terminal. Também é possível instalar as dependências com `npm install`.

```sh
npm run lint
npm run build
npm run preview
```

O build fica em `dist/`. Na hospedagem estática, configure o servidor para encaminhar rotas como `/login` e `/live/1` para `index.html`.

## Telas

- **Login** valida o formato do e-mail e os campos obrigatórios, permite alternar a visibilidade da senha e abre a Home. Qualquer e-mail de formato válido e uma senha preenchida servem para a demonstração.
- **Home** reúne o Festival Aurora, canais ao vivo, pesquisa por título, canal, categoria ou jogo, filtros, histórico, canais seguidos e lives com recompensas. O perfil oferece a opção de sair.
- **Live** carrega a transmissão pelo ID e apresenta player demonstrativo, descrição, inscrição, curtida, compartilhamento, Pix ilustrativo, recomendações e chat local com mensagem fixada e enquete na transmissão de Erick Gameplays.

## Dados locais e limitações

A proteção de rotas serve para demonstrar o fluxo. Não há autenticação real, servidor ou validação de credenciais. Use dados fictícios. O armazenamento guarda o nome de exibição derivado do e-mail, a categoria selecionada, IDs de lives curtidas e assistidas e nomes de canais seguidos. A senha e o endereço completo de e-mail ficam fora do armazenamento. Se o navegador bloquear o `localStorage`, o protótipo mantém as alterações em memória durante a sessão da página.

A imagem do player é estática. Os controles de reprodução e som simulam estados, e a tela cheia usa o recurso do navegador. O compartilhamento usa o menu nativo ou a área de transferência, com opção de copiar manualmente. As mensagens do chat aparecem localmente e são descartadas ao sair da transmissão. Pix e recompensas são ilustrativos. As opções de voz, transmissão a outros dispositivos, Mapa IRL, Multiview e criação de canais exibem mensagens de indisponibilidade.

## Qualidade da interface

- **Usabilidade** — estados de seleção, mensagens de validação, feedback de compartilhamento e chat, estados vazios e ações reversíveis.
- **Acessibilidade** — referências à WCAG 2.2 AA, navegação semântica, link para pular ao conteúdo, foco visível, controles de teclado, rótulos associados e preferência por movimento reduzido. O chat anuncia o envio de uma mensagem por vez.
- **Responsividade** — grids fluidos, menu recolhível, player 16:9 e chat abaixo do player em telas menores.
- **Portabilidade** — dependências declaradas com lockfile, imagens locais, caminhos gerenciados pelo Vite e tratamento de indisponibilidade do armazenamento e de APIs opcionais do navegador.
