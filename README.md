# Cartão da Copa do Mundo 2026 🏆

Um cartão interativo no estilo das tabelas de bolão dos anos 90, com cara moderna.
Marque o placar de cada jogo e a tabela de cada grupo se ajeita sozinha; o mata-mata
(16-avos → oitavas → quartas → semis → final) tem chaves onde o vencedor sobe sozinho.

Página única, sem dependências de build. Abre direto no navegador.

## Publicar no GitHub Pages

1. Coloque o `index.html` na raiz do repositório e suba para a branch `main`.
2. No GitHub: **Settings → Pages → Build and deployment → Source: _Deploy from a branch_**,
   selecione **`main`** e a pasta **`/ (root)`**, e salve.
3. Em ~1 min o site fica no ar em: `https://diogomes.github.io/2026FIFAWorldCup/`

## Atualizar os resultados

Edite **apenas** o objeto `RESULTS` no fim do `index.html`. O formato é:

```js
const RESULTS={
 A:{0:[2,0], 1:[2,1], 2:[1,1], 3:[1,0]},  // GRUPO: { índice do jogo : [gols casa, gols fora] }
 ...
};
```

O índice (0 a 5) é a posição do jogo na lista `m` daquele grupo (logo acima, no objeto `GROUPS`).
Jogos sem resultado em `RESULTS` ficam em branco para palpites; os que têm resultado ficam
travados e em caneta verde. Commit + push e o Pages atualiza sozinho.

## Estado em 22/06/2026

- 1ª rodada completa (24 jogos).
- 2ª rodada correu dos Grupos A ao I e abriu o J. Destaques: México 1×0 Coreia
  (1º classificado da Copa), Brasil 4×0 Haiti, Argentina 2×0 Áustria, França 3×0 Iraque
  e Espanha 3×0 Arábia Saudita.
- A 2ª rodada dos Grupos K e L (23/06) ainda não rolou.
