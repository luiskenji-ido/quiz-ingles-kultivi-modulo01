![GitHub License](https://shields.io)
![GitHub Top Language](https://shields.io)
![GitHub Pages Status](https://shields.io)


# 🏆 Quiz Interativo de Inglês: Kultivi E-Sports Edition

Um aplicativo web interativo, responsivo e totalmente autônomo (roda offline) desenvolvido para gamificar aulas de inglês. O sistema foi projetado especificamente para revisar o módulo **"O Básico para a Comunicação"** da Kultivi, trazendo uma estética moderna baseada em painéis de e-sports/gaming.

[Clique aqui para jogar o Quiz online]
(https://luiskenji-ido.github.io/quiz-ingles-kultivi-modulo01/)

---

## 🚀 Funcionalidades Principais

*   **Gerenciamento Dinâmico de Turmas:** Interface inicial que permite cadastrar até 5 alunos por partida. O sistema ignora campos em branco automaticamente, adaptando o rodízio em caso de faltas.
*   **Banco de Dados com 80 Questões:** perguntas divididas cirurgicamente entre os níveis **Fácil, Médio e Difícil**, cobrindo saudações, números, rotinas, e regras complexas do *Simple Present* (como as terminações especiais de 3ª pessoa: CH, SH, SS, X, O, Z e consoante + Y).
*   **Algoritmo de Aleatoriedade Inteligente:** A cada carregamento, as perguntas são embaralhadas via JavaScript. O jogo seleciona 45 rodadas aleatórias, garantindo que nenhuma partida seja igual à outra.
*   **Feedback Pedagógico Instantâneo:** Ao responder, o aluno recebe validação visual imediata (Verde para acerto / Vermelho para erro) e uma caixa com a explicação gramatical da questão.
*   **Métricas de Desempenho ao Vivo:** O placar computa e exibe em tempo real o saldo de **Acertos e Erros** de cada participante.
*   **Pódio de Classificação Final:** Ao atingir a 45ª rodada, o jogo exibe um ranking automatizado em ordem decrescente, coroando os vencedores com medalhas (🥇, 🥈, 🥉).
*   **Design Futurista (Dark Mode Neon):** Interface estilizada com CSS moderno, efeitos de brilho (*glow*), cantos arredondados e transições suaves que aumentam o engajamento dos alunos.

---

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido utilizando tecnologias web nativas ("Vanilla Web"), o que significa que ele não possui dependências de frameworks, internet ou bibliotecas externas:

*   **HTML5:** Estruturação semântica das telas de configuração, jogo ativo e pódio.
*   **CSS3 (Modern Dark Mode):** Estilização customizada com variáveis globais (`:root`), flexbox, gradients lineares e efeitos visuais imersivos.
*   **JavaScript (ES6):** Manipulação dinâmica do DOM, controle de arrays (métodos `concat` e `sort` para embaralhar), operadores condicionais e funções de tempo (`setInterval`).

---

## 📦 Como Executar o Projeto

Como o software é totalmente autônomo, não é necessário instalar servidores ou gerenciadores de pacotes:

1. Faça o download ou clone este repositório.
2. Dê dois cliques no arquivo `index.html` para abri-lo diretamente em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).
3. Digite os nomes dos competidores na tela inicial e clique em **Iniciar Jogo**.

---

## 🧠 Arquitetura do Código (Destaques Técnicos)

### Sistema de Seleção Cíclica de Turnos
O rodízio justo de perguntas entre os alunos cadastrados é feito utilizando o operador matemático de resto de divisão (`%`), impedindo que o índice saia do limite da lista de alunos ativos:
```javascript
indexAlunoAtual = (indexAlunoAtual + 1) % alunos.length;
```

### Embaralhamento Próprio (Fischer-Yates Adaptado)
Para garantir a imprevisibilidade sem pesar o navegador, o banco de dados é reordenado aleatoriamente no início da execução:
```javascript
perguntas.sort(function() { return 0.5 - Math.random(); });
```

---

## 📄 Licença

Este projeto está sob a licença MIT - sinta-se livre para usar, estudar e aprimorar a ferramenta para suas próprias dinâmicas pedagógicas.

---
*Desenvolvido com carinho para transformar a educação e engajar salas de aula através da tecnologia!*

#Autor: Luis Kenji Ido

#Criado em: 23/07/2026 - Criado com Google AI GEMINI

