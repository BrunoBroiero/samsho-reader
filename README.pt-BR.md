# SamSho Reader

[English](README.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Italiano](README.it.md) ·
**Português (Brasil)** · [日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

Um mod de leitor de tela para **SAMURAI SHODOWN** (2019; Steam, PC). Ele lê os menus, a história, as listas de comandos, as tabelas e o texto na tela com o leitor de tela que você já usa (NVDA, JAWS), no idioma em que o jogo está.

Por Bruno Broiero, com ajuda do Claude.

## O que ele faz

- Menu principal e todos os submenus, com a descrição de cada entrada.
- Opções: jogo, tela, som (volumes em %), idioma e legendas, configuração de botões (cada ação com sua tecla ou botão).
- Seleção de personagem, incluindo aleatório, trajes e cores; cenários; atribuição de lados no Versus.
- História: legendas e diálogos, desbloqueios, epílogo e créditos.
- Tutorial: instrução, tarefa e mensagem final, com as teclas em palavras.
- Lista de comandos: cada golpe com seu comando na notação escolhida; percorrida com o analógico ou F2 / F3.
- Pausa e ajustes do Treino.
- Banco de dados: perfil, rankings próprios, registros gerais.
- Galeria: filmes, ilustrações, vozes e músicas, com suas abas e páginas.
- Online: placares, telas de batalha ranqueada e casual, listas de fantasmas da Batalha fantasma.
- Resultados: a frase do vencedor é lida sozinha; a pontuação fica retida e é pedida com o analógico ou F1.
- Avisos de desbloqueio e notificações.

Não é lido:

- A tela de parabéns no fim da história é uma imagem sem texto.
- As salas e o chat online não foram testados com adversários.

## Instalação

É preciso a versão Steam para PC de SAMURAI SHODOWN, Windows x64 e um leitor de tela em execução (NVDA ou JAWS). O UE4SS, o carregador de mods para jogos Unreal, vem dentro do zip, na versão que funciona com este jogo.

Extraia todo o conteúdo do zip em `SamuraiShodown\Binaries\Win64` (na Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, a pasta `ue4ss` e estes READMEs.

Inicie o jogo pela Steam, não pelo .exe: sem a Steam ele começa em inglês e sem conexão. O mod diz "SamSho Reader" assim que está funcionando; se você não ouvir, F8 diz o nome do leitor de tela encontrado. Nenhum arquivo do jogo é modificado.

Para desinstalar, apague `dwmapi.dll` e a pasta `ue4ss`. O UE4SS e o PRISM, a biblioteca que fala com o leitor de tela, têm licenças próprias: veja `THIRD-PARTY.md`.

## Teclas

Fora de uma luta:

| Tecla | Controle | O que faz |
|---|---|---|
| F1 | Analógico direito esquerda ou direita | Diz tudo o que está retido (uma lista de comandos, uma tabela, um resultado) |
| F2 / F3 | Analógico direito cima / baixo | Parte anterior / seguinte do que está retido |
| F10 | Clique do analógico direito | Muda a notação dos comandos (Normal, Arcade, Arcade simplificada, FGC, FGC simplificada). A escolha fica salva |
| F4 | Clique do analógico direito, quando nada está retido | Lê a legenda de botões da tela ("9 ou A Confirmar, 0 ou B Voltar") |

Em uma luta:

Nada fala sozinho: a luta já se ouve. Com o analógico direito você pede o dado que precisa:

| Analógico direito | Diz |
|---|---|
| Esquerda | Vida dos dois lados: "vida 71%, 80%" (primeiro o seu lado) |
| Cima | Fúria: "fúria 41%, máxima" |
| Baixo | Rounds vencidos: "ROUNDS 1, 0". Em Sobrevivência, Contra o tempo e Ironman, suas vitórias seguidas |
| Direita | O tempo do round |
| Clique | Tudo junto |

Teclado: F2 vida, F3 fúria, F10 rounds, F1 tudo.

Em Sobrevivência, Contra o tempo e Ironman só o seu lado é dito.

Sempre:

| Tecla | Controle | O que faz |
|---|---|---|
| F6 | L3 + R3 (os dois analógicos pressionados juntos) | Desliga o mod e liga de novo; confirma com as palavras do jogo para ativado e desativado. Não é salvo: ele sempre começa ligado |
| F8 | | Diz qual leitor de tela o mod usa |

## O que F1, F2, F3 e o analógico direito leem

Muitas telas mostram mais do que está sob o cursor: uma lista de comandos, as pontuações de um resultado, uma tabela de recordes, uma lição. O mod não lê tudo isso ao chegar: ele guarda e entrega com estas teclas: F3 avança uma peça, F2 volta à anterior e F1 diz tudo de uma vez. No fim, F3 não diz nada: assim se sabe que não há mais. No controle, o analógico direito faz o mesmo: baixo é F3, cima é F2, esquerda ou direita é F1.

O que é uma peça depende da tela:

- **Lista de comandos**: cada golpe com seu comando, na notação escolhida com F10 ou o clique do analógico; ao mudá-la, o golpe é repetido na nova. Ao entrar, o personagem e a categoria são ditos.
- **Tutorial**: cada frase da explicação e da tarefa, com as entradas postas em palavras; o clique também muda a notação delas.
- **Resultado**, ao fim de uma luta: a frase do vencedor é dita sozinha; as pontuações esperam nas teclas, de propósito, para que a frase não fique enterrada sob os números.
- **Resultado do versus**: vitórias, derrotas, empates, taxa e pontos de cada lado.
- **Dados do jogador**: as tabelas de recordes e rankings, uma linha por peça; ao chegar, o título e a primeira linha são ditos.
- **Legenda dos botões**: sem nada guardado, o clique do analógico (ou F4) lê a legenda de botões da própria tela.

## A lista de comandos e suas notações

No jogo, um comando é uma fileira de desenhos: setas, botões, um "mais", condições. O mod os transforma em palavras e, como cada jogador chega a uma lista de comandos de um lugar diferente (o fliperama, os fóruns, ou nenhum dos dois), oferece cinco jeitos de dizê-los. Muda-se com F10 ou com o clique do analógico direito, e a escolha fica salva. O mesmo comando, quarto de círculo para frente e corte forte, em cada uma:

| Notação | Como soa |
|---|---|
| Normal | baixo, diagonal baixo frente, frente mais Corte forte |
| Arcade | quarto de círculo para frente, Corte forte |
| Arcade simplificada | quarto de círculo para frente, C |
| FGC | 2 3 6, Corte forte |
| FGC simplificada | 2 3 6, C |

- **Normal** diz cada direção com sua palavra. A mais longa, e a que não supõe nada.
- **Arcade** nomeia a figura: quarto de círculo, meio círculo, dragon punch e seus inversos. É como se dizem os comandos em voz alta.
- **FGC** usa os números do teclado numérico, a notação da comunidade: 6 é frente, 2 baixo, 3 a diagonal baixo frente; sempre olhando para a direita.
- As variantes **simplificadas** trocam os nomes dos botões pelas letras do gabinete: A corte leve, B médio, C forte, D chute.

Como a leitura foi pensada, porque um desenho diz com a forma coisas que as palavras precisam dizer em voz alta:

- Uma diagonal é uma entrada só, por isso se chama "diagonal": "baixo, diagonal baixo frente, frente". Dito como "baixo, baixo frente, frente" não dá para saber se são duas entradas ou uma.
- Dois botões desenhados colados se apertam juntos, por isso vão com "mais" em todas as notações.
- Uma condição que o jogo desenha em volta do nome do golpe ("durante ~") é dita uma vez, não em duas metades.
- Uma condição como "repetidamente" é dita depois dos botões a que se refere: "frente mais Corte leve, repetidamente" - como se fala, não como se desenha.
- Os nomes dos botões e das condições são as palavras do jogo, tiradas da legenda da sua própria lista de comandos; direções, figuras, "mais" e "ou" são do mod, nos onze idiomas.
- "Ou" tem várias formas no jogo (dois botões alternativos, dois comandos, uma lista); todas são ditas com a mesma palavra.

A lista é percorrida com o analógico direito (cima e baixo, golpe por golpe; esquerda ou direita, inteira) ou com F2, F3 e F1. Ao entrar, diz o lutador e a categoria ("SHIKI, GOLPES ESPECIAIS") e depois cada golpe como "nome, condição se houver: comando", por exemplo "Elysium Halo: frente, baixo, diagonal baixo frente mais Corte leve ou Corte médio ou Corte forte".

## Relatar um problema

Feche o jogo normalmente e envie `SamuraiShodown\Binaries\Win64\ue4ss\UE4SS.log`: ele registra o que o jogo mostrou e o que o mod disse a respeito, com as palavras exatas, então não é preciso anotar o que você ouviu. Diga qual era a tela e o que esperava ouvir.

## Compilação

O mod é Lua, carregado pelo UE4SS; nada é compilado além de `prism_bridge.dll`, o pequeno módulo nativo que entrega a fala ao PRISM e lê o controle (`native\prism_bridge\build.ps1`, requer MSVC). `python tools\package.py` monta o zip da release a partir da pasta do jogo.

## Traduções

Este README sai em todos os idiomas que o jogo suporta. Só as versões em inglês e em espanhol foram revisadas por um falante; correções às demais são bem-vindas. O mod em si fala no idioma do jogo: quase tudo o que diz é texto do próprio jogo, e suas poucas palavras próprias (direções, nomes de teclas, "vida", "fúria") só foram conferidas de ouvido em espanhol.
