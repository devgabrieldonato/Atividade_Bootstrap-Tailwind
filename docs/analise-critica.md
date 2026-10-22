# Comparação entre Bootstrap e Tailwind CSS

A atividade reproduz o protótipo Empresa com as mesmas imagens, textos e organização em duas páginas. O Bootstrap concentra a estrutura em classes de grade e componentes, enquanto o Tailwind permite especificar os valores visuais diretamente no HTML. Neste projeto, Bootstrap torna a estrutura dos três cartões mais curta; Tailwind torna as medidas do protótipo mais explícitas. A preferência pessoal deve ser registrada pelo estudante após executar e alterar as duas versões.

## Facilidade de uso e compreensão das classes

Na versão Bootstrap, `row` e `col-12 col-md-4` distribuem os cartões. Cada cartão ocupa a largura completa no celular e quatro das doze colunas a partir de 768 pixels, formando três colunas. Classes como `d-flex`, `flex-column` e `mt-auto` alinham os botões na base dos cartões.

Na versão Tailwind, `grid grid-cols-1 md:grid-cols-3 gap-[50px]` declara a mesma intenção em uma única grade. A leitura exige conhecer os prefixos responsivos e a notação entre colchetes. Depois disso, valores como `text-[22px]` e `bg-[#f2f2f2]` tornam tamanho e cor identificáveis sem consultar outro arquivo.

## Organização e personalização

O Bootstrap utiliza `bootstrap/index.html` para a estrutura e `bootstrap/style.css` para a identidade visual. A classe `related-button` reúne cor, tamanho e estados do botão; uma alteração nessa regra alcança os três links. A personalização exige acompanhar a cascata do CSS, pois o arquivo local complementa as regras do framework.

O Tailwind concentra a apresentação nas classes do HTML. O botão usa, entre outras, `rounded-full`, `px-[26px]`, `py-[14px]` e `hover:bg-[#d44525]`. Isso facilita associar aparência e elemento, mas repete listas longas nos três cartões. Em uma aplicação maior, um componente reutilizável reduziria essa repetição; aqui o HTML estático facilita a comparação didática.

## Dificuldades e soluções adotadas

A grade padrão do Bootstrap inclui gutters e limites de largura que não coincidem automaticamente com o protótipo. A solução foi definir um container com largura de 88%, limite de 1200 pixels e gutter horizontal de 50 pixels. No Tailwind, os mesmos valores aparecem como `md:w-[88%]`, `max-w-[1200px]` e `gap-[50px]`.

As fotos foram fornecidas dentro de uma captura única, sem arquivos individuais. As duas versões exibem somente as regiões fotográficas por meio de contêineres com proporção fixa, `overflow-hidden` e posicionamento percentual da imagem. Isso preserva a referência, porém acopla as coordenadas ao arquivo original e mantém uma imagem maior do que seria necessário com fotos separadas. O texto EMPRESA já está gravado no banner; um h1 visualmente oculto fornece o título a leitores de tela. Com a foto original sem texto, seria preferível tornar o título visível em HTML.

A adaptação ao celular usa uma coluna abaixo de 768 pixels, margens laterais de 20 pixels e títulos menores. Em telas maiores, as duas versões retomam três colunas. Os parágrafos permanecem como texto HTML selecionável e os botões são links reais, com estados de foco para navegação pelo teclado.

## Vantagens e limitações

Bootstrap oferece uma estrutura compacta para a grade e estilos de componentes que servem como ponto de partida. Neste layout, a fidelidade visual ainda depende de CSS próprio para medidas, cores e espaçamentos. O CSS completo do framework também inclui recursos não usados nesta página.

Tailwind permite ajustar medidas específicas com utilitários, sem criar uma classe semântica para cada elemento. Neste projeto, a contrapartida é o HTML mais extenso e a repetição das classes dos cartões. Foi incluída uma cópia local do compilador de navegador para uso didático sem instalação. Essa modalidade depende de JavaScript e é indicada para desenvolvimento; para produção, deve-se gerar um arquivo CSS estático com a CLI.

## Avaliação pessoal a completar

Após abrir as duas páginas, altere a cor dos três botões e o espaçamento dos cartões. Registre qual versão permitiu localizar e aplicar essas mudanças com mais segurança, quais classes exigiram consulta e se houve alterações involuntárias em outros elementos.

Tecnologia com que me senti mais confortável: ____________________

Exemplo concreto do projeto que justifica minha escolha: ____________________

Dificuldade que encontrei e como resolvi: ____________________

A comparação técnica sugere Bootstrap quando se valoriza uma estrutura curta com estilos centralizados e Tailwind quando se deseja ajustar a aparência diretamente no elemento. Essa observação não substitui a experiência pessoal solicitada na atividade.

## Referências

Bootstrap — Grid system: https://getbootstrap.com/docs/5.3/layout/grid/

Tailwind CSS — Play CDN: https://tailwindcss.com/docs/installation/play-cdn

Arquivos analisados: bootstrap/index.html, bootstrap/style.css e tailwind/index.html.
