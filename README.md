# Mega Arena Royale — Melhorias de IA dos Bots (TP02 — Inteligência Artificial / UFOP)

## Sobre este projeto

Este repositório contém **exclusivamente melhorias no jogo em si**, focadas no comportamento
(inteligência artificial) dos bots do jogo **Mega Arena Royale**.

> **Autoria da versão base do jogo: Tiago Linhares Medeiros.**
>
> Todo o jogo original (mecânicas, arte, interface, loja, passe de batalha, modos de jogo)
> é de autoria de Tiago Linhares Medeiros. O trabalho realizado aqui **não** cria um jogo novo:
> apenas evolui os comportamentos dos bots sobre essa base já existente.

As melhorias implementadas seguem o documento `propostaAtualizacao.pdf`, elaborado para o
Trabalho Prático 02 da disciplina de Inteligência Artificial (ICEA/UFOP).

## O que foi melhorado

Somente a IA dos bots, em quatro frentes:

1. **Modo Chefão — Bot Chefão**
   - Navegação em espaços estreitos (o corpo 2×2 do chefão desvia de passagens 1×1);
   - Fuga para se curar quando o HP cai abaixo de (10 × dificuldade)%;
   - Cura passiva de 1% do HP máximo por segundo;
   - Foco no adversário com menor vida dentro do campo de visão de (2 × dificuldade) tiles.

2. **Modo Chefão — Bots da Equipe**
   - Foco no chefão como alvo principal;
   - Fuga para se curar com pouca vida;
   - Busca por item de cura (sem item disponível, mantém distância e ataca de longe);
   - Acompanham o jogador humano pelo mapa.

3. **Modo Dupla**
   - O bot parceiro segue os mesmos comportamentos dos bots da equipe do modo Chefão
     (fuga para se curar, busca por item de cura e acompanhamento do jogador humano).

4. **Modo 1v9 — Bots Inimigos**
   - Percepção (raio de visão) escalada pela dificuldade;
   - Foco no adversário mais próximo dentro do campo de visão;
   - Fuga e busca por item de cura com pouca vida;
   - Esconder-se abaixo de 30% de vida;
   - Ataque corpo a corpo (faca) quando o adversário está perto;
   - Esquiva ao identificar um tiro próximo (com recarga que varia com a dificuldade);
   - Prioridade em coletar itens de ataque.

Todos os comportamentos escalam com o nível de dificuldade da partida.

## Como jogar

Abra `jogodetiro.html/jogodetiro.html` em qualquer navegador moderno. Não há dependências.

- **WASD**: mover | **Mouse**: mirar | **Clique**: atirar
- **1**: espada | **2**: granada | **3**: basuca | **Espaço**: esquiva

## Créditos

- **Versão base do jogo:** Tiago Linhares Medeiros
- **Melhorias de IA (TP02):** Pedro Henrique Amaral Estevão e Gustavo Tadeu Alves do Couto
