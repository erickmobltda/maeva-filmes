# Maeva Filmes

Um projeto simples com um propósito especial: toda semana, o Claude recomenda automaticamente 1 filme e 1 série para a Maeva — 5 anos, cheia de sensibilidade, amante de música, magia e dança.

## O que é este projeto

Este repositório é o "cérebro" de um Routine semanal automatizado. Ele guarda o perfil da Maeva, o histórico do que ela já assistiu e todas as recomendações geradas ao longo do tempo.

## Como o Routine funciona

Todo **sábado às 08h**, o Claude Code acorda e executa o seguinte:

1. Lê o arquivo `perfil.md` — entende quem é a Maeva, o que ela ama, o que deve evitar.
2. Lê o arquivo `historico.md` — verifica tudo que ela já assistiu para não repetir.
3. Pesquisa na internet o que está disponível hoje no Netflix, Disney+ e Prime Video no Brasil.
4. Escolhe 1 filme e 1 série que combinam com o perfil dela — priorizando trilha sonora, magia, arte e sensibilidade.
5. Registra as recomendações em `recomendacoes.md` e atualiza `historico.md`.
6. Faz commit direto na main com a data do dia.

Nenhuma ação manual é necessária para que as recomendações aconteçam.

## Como manter o histórico

Quando a Maeva assistir algo novo — seja uma das recomendações ou qualquer outro título —, basta abrir o arquivo `historico.md` e adicionar uma linha na seção **Assistidos**:

**Formato:**
```
- Título (tipo: filme ou série) — avaliação
```

**Exemplos:**
```
- Meu Amigo Totoro (filme) — amou
- Peppa Pig (série) — gostou
- Tal Filme (filme) — não terminou
```

Isso garante que o Routine nunca recomende algo que ela já viu.

## Arquivos do projeto

| Arquivo | Descrição |
|---|---|
| `perfil.md` | Perfil completo da Maeva: interesses, o que evitar, critérios de qualidade |
| `historico.md` | Tudo que ela já assistiu + recomendações geradas |
| `recomendacoes.md` | Arquivo acumulado com todas as recomendações semanais |
| `CLAUDE.md` | Instruções para o Routine — o que o Claude deve fazer toda semana |
