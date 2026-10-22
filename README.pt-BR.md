# SamShoAccess

> Tradução sem revisão de um falante nativo. Uma palavra errada é um erro que vale a pena relatar.

Mod de acessibilidade para **SAMURAI SHODOWN** (2019, Steam): faz o jogo ser lido pelo seu leitor de tela. Menus, opções, seleção de personagem e cenário, legendas da história, tutorial, lista de comandos, banco de dados, galeria, online, resultados e os números da luta.

Quase todas as palavras que você vai ouvir são as do próprio jogo, no idioma em que ele estiver configurado. As poucas palavras que o jogo não tem (direções dos comandos, nomes de teclas, "vida", "fúria") estão traduzidas para os onze idiomas do jogo.

Autor: **Bruno Broiero**. Feito com Claude.

## Requisitos

- SAMURAI SHODOWN para Steam (Windows).
- Um leitor de tela em execução: NVDA ou JAWS. O mod fala através do PRISM.
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), o carregador de mods para jogos Unreal. Ele vem dentro do download, na versão que funciona com este jogo (experimental, 21 de setembro de 2026): não há nada para baixar à parte.
- Um controle XInput (tipo Xbox) é opcional, mas o mod foi pensado para ele.

## Instalação

1. Baixe o `SamShoAccess-x.y.z.zip` mais recente da página de Releases.
2. Extraia todo o conteúdo em `SamuraiShodown\Binaries\Win64\` (a pasta do jogo; na Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, a pasta `ue4ss` e os READMEs.
3. Abra o jogo **pela Steam** (não pelo .exe: sem a Steam ele inicia em inglês e sem conexão).
4. Ao carregar, o mod diz "SamShoAccess". Se você não ouvir, aperte F8: ele diz o nome do leitor de tela encontrado.

## Teclas do mod

| Tecla | Controle | O que faz |
|---|---|---|
| F1 | Analógico direito esquerda ou direita | Diz tudo o que está retido (uma lista de comandos, uma tabela, um resultado) |
| F2 / F3 | Analógico direito cima / baixo | Parte anterior / seguinte do que está retido |
| F10 | Clique do analógico direito | Muda a notação dos comandos (Normal, Arcade, Arcade simplificada, FGC, FGC simplificada). A escolha fica salva |
| F4 | Clique do analógico direito, quando nada está retido | Lê a legenda de botões da tela ("9 ou A Confirmar, 0 ou B Voltar") |
| F8 | | Diz qual leitor de tela o mod usa |
| Ctrl + Esc | | Silencia a voz |

As setas, Enter e Backspace são do jogo, não do mod.

## Na luta

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

## O que é lido

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

## O que não é lido

- A tela de parabéns no fim da história é uma imagem sem texto.
- As salas e o chat online não foram testados com adversários.

## Idiomas

O mod fala no idioma do jogo. As palavras próprias do mod foram conferidas de ouvido só em espanhol; nos outros idiomas estão traduzidas sem revisão de um falante. Uma palavra errada é um erro que vale a pena relatar.

## Notas

- O mod não altera nenhum arquivo do jogo.
- O UE4SS é da equipe RE-UE4SS, sob licença MIT; `prism.dll` e `tolk.dll` vêm do [PRISM](https://github.com/ethindp/prism), sob MPL 2.0. Veja `THIRD-PARTY.md`.
- Para desinstalar, apague `dwmapi.dll` e a pasta `ue4ss`.
- O código-fonte do mod ainda não é público; será quando o mod se assentar com o uso. O download é livre para usar.
