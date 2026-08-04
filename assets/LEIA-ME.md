# Assets da advertorial Pelaria

Coloque cada arquivo na pasta certa **com o nome exato da tabela**. O HTML já
aponta para esses caminhos: não precisa editar código, é só soltar o arquivo.

Enquanto um arquivo não existir, a página mostra a caixa cinza descritiva no
lugar dele. Nada quebra, nada fica em branco. Assim que o arquivo aparece com o
nome certo, a mídia entra sozinha e a caixa cinza some.

> Nomes de arquivo: tudo minúsculo, sem acento e sem espaço. A Vercel diferencia
> maiúscula de minúscula, então `Hero-Vertical.MP4` não é a mesma coisa que
> `hero-vertical.mp4` e a mídia não vai carregar.

---

## 1. Vídeos · `assets/videos/`

| Arquivo | Onde aparece | Proporção | Peso alvo |
|---|---|---|---|
| `hero-vertical.mp4` | Seção 1, hero | 9:16 vertical | até 3 MB |
| `click-clean.mp4` | Seção 4, mecanismo | 16:10 horizontal | até 4 MB |

**Conteúdo esperado**

- `hero-vertical.mp4`: mão escovando o pet, corte para o botão sendo apertado e
  a manta de pelo saindo da escova.
- `click-clean.mp4`: close do botão sendo apertado e a placa ejetando a manta de
  pelo compacta. É o vídeo mais importante da página, vale o melhor take.

**Especificação técnica**

- Formato MP4, codec H.264, áudio removido (a página roda tudo mudo).
- 1080p no vertical (1080x1920), 1280x800 no horizontal. Não adianta 4K.
- 6 a 12 segundos, em loop que não tenha corte visível ao repetir.
- Peso é o que mais importa aqui: tráfego pago no 4G abandona página pesada.
  Se passar do alvo, comprima antes de subir (HandBrake, CloudConvert, ou
  `ffmpeg -i entrada.mp4 -an -vcodec libx264 -crf 28 -preset slow saida.mp4`).

## 2. Capas dos vídeos · `assets/posters/`

| Arquivo | Vídeo correspondente | Peso alvo |
|---|---|---|
| `hero-vertical.jpg` | `hero-vertical.mp4` | até 150 KB |
| `click-clean.jpg` | `click-clean.mp4` | até 150 KB |

A capa é o primeiro quadro que o visitante vê antes do vídeo carregar. Use um
frame do próprio vídeo, na mesma proporção. JPG com qualidade 75 a 80 basta.

## 3. Imagens de conteúdo · `assets/imagens/`

| Arquivo | Onde aparece | Proporção | Peso alvo |
|---|---|---|---|
| `cerdas-macro.jpg` | Seção 5, segurança | 16:10 horizontal | até 250 KB |

Macro das pontas de resina das cerdas, em zoom. Precisa dar para ver a esfera
arredondada na ponta: é essa foto que sustenta o argumento de "não arranha".

## 4. Fotos dos depoimentos · `assets/depoimentos/`

| Arquivo | Card | Proporção | Peso alvo |
|---|---|---|---|
| `depoimento-1.jpg` | 1 | 1:1 quadrada | até 200 KB |
| `depoimento-2.jpg` | 2 | 1:1 quadrada | até 200 KB |
| `depoimento-3.jpg` | 3 | 1:1 quadrada | até 200 KB |
| `depoimento-4.jpg` | 4 | 1:1 quadrada | até 200 KB |
| `depoimento-5.jpg` | 5 | 1:1 quadrada | até 200 KB |

São opcionais e independentes: se você só tiver foto real dos cards 1 e 3, suba
só esses dois. Os outros cards ficam sem foto, com o depoimento em texto, e o
layout continua correto.

Use apenas foto real de cliente, do próprio anúncio de origem. Foto de banco de
imagem em card rotulado "Avaliação verificada do produto" é propaganda enganosa.

## 5. Marca · `assets/marca/`

| Arquivo | Uso | Tamanho |
|---|---|---|
| `favicon.png` | Ícone da aba do navegador | 512x512 px |
| `compartilhamento.jpg` | Prévia ao compartilhar o link | 1200x630 px |

O `compartilhamento.jpg` é o que aparece quando alguém manda o link no WhatsApp
ou quando o anúncio é compartilhado. Vale colocar o produto e o nome Pelaria,
legível em miniatura.

---

## Depois de subir os arquivos

1. Abra a página e confira se todas as caixas cinza sumiram. Caixa cinza que
   sobrou significa nome de arquivo errado.
2. Teste no celular, em rede móvel, não só no Wi-Fi.
3. Confirme que os vídeos rodam mudos e em loop.
