# Site Dra. Ana Cláudia Reis (em aprovação)

Site estático de uma página: `index.html`, `404.html`, `assets/`, `fonts/`. Sem build e sem scripts externos.
Abra com qualquer servidor estático (ex.: `python -m http.server`).

Demonstração: https://paparidisbrancher.github.io/dra-ana-claudia-reis/ (repo `paparidisbrancher/dra-ana-claudia-reis`, Pages na `main`).

Enquanto estiver em aprovação: `noindex` no `<head>` e `robots.txt` bloqueando buscadores. Remover os dois na publicação.

## Pendências com a cliente

Tudo o que aparece no site com a etiqueta **"a confirmar"** (classe `pend` no HTML). Ao confirmar, troque o texto e remova a classe.

- [ ] CRO-MG 62571 (aparece nas fotos do Instagram; conferir no CRO-MG)
- [ ] Formação, cursos e trajetória (seção Sobre)
- [ ] Rinomodelação: ainda oferece? (os demais tratamentos foram confirmados em 22/10)
- [ ] Título: o selo das fotos diz "Odontologia estética e endodontia". O site usa só "cirurgiã-dentista" até a especialidade registrada ser confirmada
- [ ] Endereços e horários em Carmo da Cachoeira e Varginha
- [ ] Número de WhatsApp (o link pronto, com a mensagem neutra, está num comentário na seção Contato). Hoje o botão principal abre o direct do Instagram
- [ ] Etapas reais do atendimento (Como funciona)
- [ ] Respostas das dúvidas frequentes revisadas por ela
- [ ] Logo oficial em SVG ou PNG transparente (hoje o nome está em texto, como wordmark provisório)
- [ ] Paleta oficial (as cores atuais são provisórias, ver `:root` no `index.html`)
- [ ] Domínio final (para `og:image` com URL completa, `canonical` e sitemap)

Fica de fora até haver material revisado por ela: **conteúdos educativos**.

## Imagens

Autorização: segundo o Erick (31/10/2026), as fotos publicadas no Instagram da doutora já têm autorização das pacientes. Os antes e depois mantêm o nome e o CRO gravados na própria foto, como no Instagram.

| Arquivo | Origem (pasta do Instagram) | Uso |
|---|---|---|
| `retrato-estudio-*.webp` | `03addf2f82ffd7e8.jpg` | Hero |
| `retrato-sofa-*.webp` | `a7d6e708c5347702.jpg` (recortada sem o texto "Posso ser sincera?") | Sobre |
| `retrato-perfil-*.webp` | `foto-perfil-instagram.jpg` | Contato |
| `og.jpg` | recorte do retrato de estúdio | Compartilhamento |
| `resultado-1..6-*.webp` | `b1018054`, `edd23edf`, `77448bde`, `f5277607`, `c902e045` (recortada sem a legenda), `da61737a` | Resultados |

São capturas comprimidas do Instagram. Pedir os originais em alta resolução à cliente.
Não usadas: close-ups de lábios, a foto no barco e a selfie com adesivo.

## SEO

Feito: título e descrição com tratamento e cidades, `canonical`, Open Graph e cartão do X/Twitter, dados estruturados (`Dentist` em JSON-LD, só com dados confirmados), `sitemap.xml`, ícones PNG e um único `h1`.

Para publicar de verdade:
1. Domínio próprio: trocar `https://paparidisbrancher.github.io/dra-ana-claudia-reis/` em `index.html` (canonical, og, JSON-LD) e no `sitemap.xml`.
2. Tirar o `noindex` do `<head>` e trocar `Disallow: /` por `Allow: /` no `robots.txt`. No GitHub Pages de projeto o robots.txt nem é lido (só vale o da raiz do domínio); quem segura o site fora do Google é o `noindex`.
3. Cadastrar o domínio no Google Search Console e enviar o sitemap.
4. Ao confirmar endereço, telefone, horários e CRO: acrescentar ao JSON-LD (`address`, `telephone`, `openingHoursSpecification`) e escrever exatamente igual no Perfil da Empresa no Google. Para busca local ("harmonização facial Varginha") é esse perfil que mais pesa, mais do que o site.

## Tipografia e cores

- Títulos: Bodoni Moda. Texto: Jost (geométrica, próxima da assinatura usada nas fotos). Ambas OFL, servidas de `fonts/`.
- Paleta provisória: marfim #F6F3EE, areia #E8DFD5, taupe #B9A99C, marrom #3B302C, grafite #282523, e #271E1B no hero (o mesmo fundo do retrato de estúdio).
