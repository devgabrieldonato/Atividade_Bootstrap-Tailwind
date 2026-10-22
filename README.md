# Atividade Bootstrap e Tailwind CSS

Reprodução do protótipo **Empresa** em duas implementações independentes, com os mesmos textos, imagens, cores e organização visual. O objetivo é comparar uma abordagem baseada em componentes e grade (Bootstrap) com uma abordagem de classes utilitárias (Tailwind CSS).

## Executar

Abra `bootstrap/index.html` ou `tailwind/index.html` no navegador. Os frameworks e a imagem estão salvos em cada pasta; não é necessário instalar Node, npm ou baixar dependências. A versão Tailwind requer JavaScript habilitado e um navegador moderno.

Opcionalmente, na raiz do repositório, execute:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Acesse:

- Bootstrap: http://localhost:8000/bootstrap/
- Tailwind: http://localhost:8000/tailwind/

Encerre o servidor com `Ctrl+C`. Os links CLICRBS, SENAC e TERRA levam aos sites externos e precisam de internet.

## Estrutura

```text
bootstrap/
  index.html
  style.css
  assets/bootstrap.min.css
  assets/prototipo.png
tailwind/
  index.html
  assets/tailwind-browser.js
  assets/prototipo.png
docs/
  analise-critica.docx
  analise-critica.md
README.md
```

As pastas são autossuficientes; a imagem é repetida intencionalmente para permitir abrir cada versão separadamente.

## Construção com Bootstrap

Usa Bootstrap 5.3.3. A grade `row` com `col-12 col-md-4` forma uma coluna em telas pequenas e três a partir de 768px. Utilitários de flexbox alinham os botões. O arquivo `style.css`, carregado depois do framework, personaliza tipografia, espaçamentos, cores e largura do conteúdo.

## Construção com Tailwind CSS

Usa `@tailwindcss/browser` 4.1.18, com uma cópia local do compilador de navegador. Classes como `grid-cols-1 md:grid-cols-3`, `max-w-[1200px]` e `bg-[#f2f2f2]` definem o layout diretamente no HTML. Não há CSS do Bootstrap nessa versão.

A distribuição para navegador foi escolhida para facilitar a execução da atividade sem ferramentas de build. É destinada ao desenvolvimento: para publicar em produção, substitua-a pelo CSS estático gerado pela CLI do Tailwind.

## Fidelidade ao protótipo e imagens

As duas versões preservam banner, título, subtítulo, foto principal, dois parágrafos e três cartões na mesma ordem. Em telas pequenas, o conteúdo ganha margens de 20px e os cartões ficam empilhados; em telas maiores, o conteúdo tem 88% de largura, limitado a 1200px.

A imagem fornecida foi mantida sem alteração. Contêineres com `aspect-ratio`, `overflow-hidden` e posicionamento percentual exibem suas regiões fotográficas. Os textos do corpo e cartões são HTML real e selecionável. O título EMPRESA está incorporado à foto do banner original, acompanhado de um `h1` visualmente oculto para leitores de tela. Para trocar esse título visualmente, substitua o banner por uma foto sem texto e apresente o `h1` sobre ela. Usar fotos individuais também reduziria o tamanho dos arquivos e eliminaria a dependência das coordenadas do protótipo.

O protótipo foi fornecido para esta atividade; nenhuma licença de redistribuição das fotografias foi informada.

## Branches

- `bootstrap`: implementação Bootstrap.
- `tailwind`: implementação Tailwind CSS.
- `main`: integração das duas versões e documentação.

O repositório está preparado localmente. Para enviar a um repositório vazio no GitHub, depois de criar o destino na sua conta:

```sh
git remote add origin URL_DO_SEU_REPOSITORIO
git push -u origin main bootstrap tailwind
```

## Análise crítica

`docs/analise-critica.docx` apresenta a comparação com exemplos do próprio código. A fonte editável em Markdown está ao lado. Complete a seção de avaliação pessoal após experimentar as duas versões: ela não deve atribuir a você uma experiência que ainda não relatou.

## Verificação

Confira em larguras de 375px, 768px e 1366px: ordem do conteúdo, ausência de rolagem horizontal, transição de uma para três colunas e funcionamento dos links. Navegue com Tab para verificar o foco dos botões.

A verificação automatizada local confere a existência dos arquivos referenciados, igualdade dos textos e destinos dos links entre as versões e integridade do DOCX. A revisão visual em navegador e a renderização paginada do Word não foram concluídas neste ambiente.

## Referências e dependências

- [Bootstrap — grade](https://getbootstrap.com/docs/5.3/layout/grid/)
- [Tailwind CSS — compilador de navegador](https://tailwindcss.com/docs/installation/play-cdn)
- Bootstrap 5.3.3: https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css
- Tailwind browser 4.1.18: https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4.1.18/dist/index.global.js

Bootstrap e Tailwind CSS são distribuídos sob licença MIT; os arquivos de terceiros preservam seus avisos de licença.
