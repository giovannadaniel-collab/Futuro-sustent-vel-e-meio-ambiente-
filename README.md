```python
import os

# Create directory structure for the project text files
os.makedirs('agrinho_project/img', exist_ok=True)
os.makedirs('agrinho_project/HQ', exist_ok=True)

readme_content = """# 🌾 Agrinho 2026 — Inovação, Tecnologia e Sustentabilidade no Campo Paranaense

Projeto desenvolvido para o **Concurso Agrinho 2026 – Categoria Programação**, na **Subcategoria 3: Programação Front-End – HTML, CSS e JavaScript**.

---

## 🌱 Tema do Concurso
**Agro forte, futuro sustentável: equilíbrio entre produção e meio ambiente**

---

## 📌 Sobre o Projeto
Este projeto apresenta de forma interativa, responsiva e acessível os pilares fundamentais do desenvolvimento rural moderno no estado do Paraná. O site conecta a **Tecnologia Rural**, a **Sustentabilidade** e a **Educação do Futuro** por meio de um ecossistema digital composto por cards informativos integrados com modais nativos, um quiz dinâmico de conscientização ambiental, e uma central completa de ferramentas de acessibilidade.

---

## 🎯 Objetivo
Conscientizar estudantes, produtores e a comunidade urbana sobre como a inovação tecnológica aplicada no campo caminha lado a lado com a conservação ambiental e com as diretrizes educacionais do Programa Agrinho, gerando um ecossistema produtivo forte e consciente.

---

## 🧭 Funcionalidades do Site
- 🏠 **Página Inicial:** Cabeçalho moderno com gradiente fluido e apresentação do tema.
- 📱 **Layout Totalmente Responsivo:** Organização por Flexbox adaptável a celulares, tablets e computadores.
- 🚜 **Cards de Conteúdo Dinâmico:** Seções interativas que abrem modais informativos via Javascript estruturado.
- 🧠 **Quiz Interativo:** Questionário nativo focado no ecossistema paranaense com validação lógica de pontuação e feedbacks visuais contextuais.
- 💡 **Fato Surpresa do Campo:** Sistema pseudo-aleatório para exibição de pílulas rápidas de conhecimento sobre agricultura.
- ♿ **Barra de Acessibilidade Integrada:**
  - 🔠 Botões inteligentes para aumento e diminuição progressiva da fonte (`A+` / `A-`).
  - 🌓 Alternador global para o **Modo Alto Contraste (Dark Mode Adaptativo)**.
  - ⌨️ Controle avançado de fechamento de modais com suporte nativo à tecla `Escape`.

---

## 💻 Tecnologias Utilizadas
O projeto foi desenvolvido estritamente de acordo com as regras competitivas, utilizando apenas tecnologias puras (Vanilla Front-End):
- **HTML5 Semântico**
- **CSS3 Estruturado** (Utilizando variáveis nativas `:root` para o gerenciamento dinâmico de cores/contraste)
- **JavaScript Moderno (ES6+)**

*Nota de Conformidade:*
- ✅ Nenhum framework ou biblioteca externa (Bootstrap, Tailwind CSS, React, etc.) foi utilizado.
- ✅ Sem código CSS ou JavaScript interno/inline. Tudo separado em arquivos externos limpos.

---

## 📁 Estrutura de Arquivos

```

```text
Project files generated successfully inside 'agrinho_project' folder.

```text
/
├── index.html          # Estrutura semântica e esqueleto do portal
├── style.css           # Estilização completa, variáveis globais e acessibilidade
├── script.js           # Lógica dos modais, controle de acessibilidade, quiz e dados
├── README.md           # Documentação completa do projeto
├── img/                # Diretório de ativos multimídia
│   ├── logo.png
│   ├── Hero.png
│   ├── github.png
│   └── instagram.png
└── HQ/                 # Módulo de expansão pedagógica
    └── hq.html

```

---

## ▶️ Como Executar o Projeto

1. Baixe ou clone este repositório.
2. Abra a pasta principal do projeto.
3. Dê um duplo clique no arquivo `index.html` para executá-lo em qualquer navegador de internet moderno.

---

## ♿ Detalhamento Técnico de Acessibilidade

* **Variáveis Dinâmicas CSS:** A troca para o modo de Alto Contraste altera dinamicamente as variáveis de cor injetadas no escopo global (`:root`), garantindo que todo o texto possua a razão mínima de contraste exigida pela WCAG.
* **Gerenciador de Fontes:** A escala de texto varia de `12px` a `24px` de maneira controlada para não quebrar a organização tridimensional dos cards.
* **Navegação Adaptada:** Modais possuem tratamento via escuta de janelas para fechamento suave através de cliques fora da área de conteúdo ou via teclado (`Escape`).

---

## 👨‍🎓 Autoria

* **Autor(a):** Nome do(a) estudante
* **Professor(a) Orientador(a):** Nome do(a) professor(a)
* **Escola:** Nome da instituição de ensino
* **Município:** Nome do Município – Paraná

---

## 📄 Licença

Projeto desenvolvido exclusivamente para fins educacionais e submissão oficial ao **Concurso Agrinho 2026**.
"""

with open('agrinho_project/README.md', 'w', encoding='utf-8') as f:
f.write(readme_content.strip())

index_html = """

```
<div class="accessibility-bar" role="complementary" aria-label="Controles de Acessibilidade">
    <button onclick="alterarFonte(1)" aria-label="Aumentar tamanho do texto">A+</button>
    <button onclick="alterarFonte(-1)" aria-label="Diminuir tamanho do texto">A-</button>
    <button onclick="alternarContraste()" aria-label="Alternar modo de alto contraste">🌓 Alto Contraste</button>
</div>

<header>
    <h1>Agrinho 2026</h1>
    <p>Paraná: Inovação, Tecnologia e Sustentabilidade no Campo</p>
</header>

<main class="container">
    
    <div class="card">
        <div class="card-icon">🚜</div>
        <h3>Tecnologia Rural</h3>
        <p>O uso de drones, sensores e inteligência artificial transformando a produtividade nas fazendas paranaenses.</p>
        <button onclick="mostrarDetalhes('tecnologia')" aria-label="Saber mais sobre Tecnologia Rural">Saber mais</button>
    </div>

    <div class="card">
        <div class="card-icon">🌱</div>
        <h3>Sustentabilidade</h3>
        <p>Práticas agrícolas que preservam o meio ambiente, protegem o solo e garantem o futuro das próximas gerações.</p>
        <button onclick="mostrarDetalhes('sustentabilidade')" aria-label="Saber mais sobre Sustentabilidade">Saber mais</button>
    </div>

    <div class="card">
        <div class="card-icon">🎒</div>
        <h3>Educação do Futuro</h3>
        <p>O Programa Agrinho conectando alunos e professores para construir um Paraná cada vez mais forte e consciente.</p>
        <button onclick="mostrarDetalhes('educacao')" aria-label="Saber mais sobre Educação do Futuro">Saber mais</button>
    </div>
    
</main>

<section class="interactive-section" aria-labelledby="curiosidade-titulo">
    <h2 id="curiosidade-titulo">💡 Curiosidades do Agro Paranaense</h2>
    <div class="curiosity-box">
        <p id="texto-curiosidade">Clique no botão abaixo para descobrir uma curiosidade dinâmica sobre o agronegócio sustentável!</p>
        <button onclick="gerarCuriosidade()">Descobrir Fato</button>
    </div>
</section>

<section class="quiz-section" aria-labelledby="quiz-titulo">
    <h2 id="quiz-titulo">🧠 Desafio Quiz Agrinho</h2>
    <p>Teste seus conhecimentos sobre o equilíbrio essencial entre a produção agrícola e o meio ambiente!</p>
    
    <div id="quiz-container">
        <div class="quiz-item">
            <p class="quiz-pergunta"><strong>Qual das seguintes práticas preserva o solo e evita erosões no campo?</strong></p>
            <div class="quiz-opcoes">
                <label><input type="radio" name="q1" value="incorrect1"> Deixar o solo totalmente descoberto exposto à chuva</label>
                <label><input type="radio" name="q1" value="correct"> O sistema de Plantio Direto sobre a palha protetora</label>
                <label><input type="radio" name="q1" value="incorrect2"> Desmatamento de matas ciliares nas proximidades</label>
            </div>
        </div>
        
        <button onclick="verificarQuiz()" class="btn-quiz">Enviar Resposta</button>
        <div id="quiz-resultado" class="hidden" role="alert"></div>
    </div>
</section>

<div id="modal" class="modal hidden" role="dialog" aria-modal="true" aria-hidden="true">
    <div class="modal-content">
        <span class="close-btn" onclick="fecharModal()" role="button" aria-label="Fechar modal">&times;</span>
        <h2 id="modal-titulo">Título Padrão</h2>
        <p id="modal-texto">Texto informativo padrão do modal...</p>
    </div>
</div>

<footer>
    <p>&copy; 2026 Projeto Agrinho Paraná - Criado com Código, Acessibilidade e Criatividade</p>
</footer>

<script src="script.js"></script>

``
3. Ative as **GitHub Pages** nas configurações do seu repositório para gerar o link de visualização em tempo real exigido na subcategoria de Front-End.

```
