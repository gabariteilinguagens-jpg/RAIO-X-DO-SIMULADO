<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mentoria Prof. Maria Hellen</title>
<script src="https://cdn.tailwindcss.com"></script>

<style>
@keyframes fadeIn {
  from {opacity: 0; transform: scale(0.98);}
  to {opacity: 1; transform: scale(1);}
}

@keyframes glow {
  0% { box-shadow: 0 0 5px #c98b00; }
  50% { box-shadow: 0 0 20px #c98b00; }
  100% { box-shadow: 0 0 5px #c98b00; }
}

.card-anim {
  animation: fadeIn 0.4s ease-out;
}

.glow {
  animation: glow 2s infinite;
}
</style>
</head>

<body class="bg-[#f3f0eb] min-h-screen flex items-center justify-center p-6">

<div id="app" class="w-full max-w-3xl"></div>

<script>

const perguntas = [
  {
    bloco: "Estratégia de Prova",
    pergunta: "Perdi muito tempo em poucas questões?",
    respostas: [
      "Não, administrei muito bem meu tempo",
      "Um pouco, mas consegui recuperar depois",
      "Sim, isso prejudicou bastante meu ritmo",
      "Sim, perdi totalmente o controle do tempo"
    ]
  },
  {
    bloco: "Estratégia de Prova",
    pergunta: "Comecei pelas questões mais fáceis ou fui na ordem?",
    respostas: [
      "Priorizei as mais estratégicas e ganhei tempo",
      "Misturei estratégia com a ordem da prova",
      "Fui mais pela ordem e perdi tempo",
      "Fiz totalmente na ordem e isso me prejudicou"
    ]
  },
  {
    bloco: "Leitura e Interpretação",
    pergunta: "Tive dificuldade com textos longos?",
    respostas: [
      "Não, li com tranquilidade",
      "Um pouco, mas mantive o foco",
      "Sim, isso atrapalhou bastante",
      "Sim, comprometeu fortemente minha prova"
    ]
  },
  {
    bloco: "Emocional e Resistência",
    pergunta: "Me senti ansioso(a) antes ou durante a prova?",
    respostas: [
      "Não, mantive controle emocional",
      "Um pouco, mas consegui controlar",
      "Sim, isso atrapalhou vários momentos",
      "Sim, a ansiedade dominou minha prova"
    ]
  },
  {
    bloco: "Revisão e Erros",
    pergunta: "Revisei minhas respostas antes de entregar?",
    respostas: [
      "Sim, revisei tudo com calma",
      "Revisei parcialmente",
      "Revisei só algumas questões",
      "Não tive tempo de revisar"
    ]
  },
  {
    bloco: "Revisão e Erros",
    pergunta: "Errei mais por distração ou falta de conteúdo?",
    respostas: [
      "Quase não errei",
      "Mais por distração",
      "Metade por cada motivo",
      "Principalmente por falta de conteúdo"
    ]
  },
  {
    bloco: "Performance Geral",
    pergunta: "Como você avalia seu desempenho geral?",
    respostas: [
      "Muito acima do esperado",
      "Bom desempenho",
      "Regular",
      "Abaixo do esperado"
    ]
  }
];

let indice = 0;
let pontos = 0;
let respostasUser = [];

function responder(valor, texto, i) {
  respostasUser.push({
    bloco: perguntas[i].bloco,
    score: valor
  });

  pontos += valor;
  indice++;
  render();
}

function reiniciar() {
  indice = 0;
  pontos = 0;
  respostasUser = [];
  render();
}

function resultadoFinal() {

  let estrategia = 0, emocao = 0, leitura = 0, revisao = 0;

  respostasUser.forEach(r => {
    if (r.bloco.includes("Estratégia")) estrategia += r.score;
    if (r.bloco.includes("Emocional")) emocao += r.score;
    if (r.bloco.includes("Leitura")) leitura += r.score;
    if (r.bloco.includes("Revisão")) revisao += r.score;
  });

  let perfil =
    pontos >= 22 ? "🏆 Executor Estratégico Elite" :
    pontos >= 16 ? "🥈 Estrategista em Evolução" :
    "⚠️ Reestruturação Necessária";

  const reflexao = `
    <div class="bg-[#f7f2ea] border-l-4 border-[#7a2e1f] p-5 rounded-2xl mb-6 text-left">
      <p class="text-sm text-gray-500 mb-3 font-semibold">
        Por isso, separei este trecho da Clarice pra hoje:
      </p>

      <p class="italic text-[#7a2e1f] mb-4 leading-relaxed">
        "Foi um sonho tão forte que acreditei nele por minutos como uma realidade. 
        Sonhei que aquele dia era Ano Novo. E quando abri os olhos cheguei a dizer: Feliz Ano Novo!
        <br><br>
        Não entendo de sonhos. Mas este me parece um profundo desejo de mudança de vida. 
        Não precisa ser feliz sequer. Basta ano novo. E é tão difícil mudar. Às vezes escorre sangue."
      </p>

      <p class="text-xs text-gray-600">
        Clarice Lispector in “A Descoberta do Mundo”
      </p>
    </div>
  `;

  const app = document.getElementById("app");

  app.innerHTML = `
    <div class="bg-white rounded-3xl shadow-xl p-8 text-center card-anim">

      ${reflexao}

      <div class="text-xl font-bold text-[#7a2e1f] mb-4 glow p-3 rounded-xl">
        MENTORIA PROF. MARIA HELLEN
      </div>

      <h1 class="text-3xl font-bold text-[#c98b00] mb-4">
        Diagnóstico Final
      </h1>

      <p class="text-xl font-semibold mb-4">
        ${perfil}
      </p>

      <p class="mb-6 text-gray-600">
        Análise baseada em estratégia, emoção, leitura e revisão.
      </p>

      <div class="text-left bg-[#f7f2ea] p-4 rounded-2xl mb-6">
        <p>📊 Estratégia: ${estrategia}</p>
        <p>🧠 Emoção: ${emocao}</p>
        <p>📖 Leitura: ${leitura}</p>
        <p>📝 Revisão: ${revisao}</p>
      </div>

      <div class="border-2 border-[#c98b00] rounded-2xl p-4 mb-6">
        <p class="text-sm text-gray-500">CERTIFICADO DE DESEMPENHO</p>
        <p class="text-lg font-bold text-[#7a2e1f]">
          Concedido pela Mentoria Prof. Maria Hellen
        </p>
      </div>

      <button onclick="reiniciar()" 
        class="bg-[#c98b00] text-white px-6 py-3 rounded-2xl font-semibold">
        Refazer Simulado
      </button>
    </div>
  `;
}

function render() {
  const app = document.getElementById("app");
  const total = perguntas.length;

  if (indice >= total) {
    resultadoFinal();
    return;
  }

  const atual = perguntas[indice];
  const progresso = (indice / total) * 100;

  app.innerHTML = `
    <div class="bg-white rounded-3xl shadow-xl p-8 card-anim">

      <div class="mb-4 text-center">
        <div class="inline-block px-5 py-2 bg-[#7a2e1f] text-white rounded-full text-sm font-bold glow">
          MENTORIA PROF. MARIA HELLEN
        </div>
      </div>

      <h1 class="text-3xl font-bold text-[#c98b00] mb-4">
        RAIO-X DO SIMULADO
      </h1>

      <div class="w-full bg-[#eee4d8] rounded-full h-3 mb-4">
        <div class="bg-[#c98b00] h-3 rounded-full" style="width:${progresso}%"></div>
      </div>

      <p class="text-sm mb-4">${atual.bloco}</p>

      <h2 class="text-xl font-bold mb-6">${atual.pergunta}</h2>

      <div class="grid gap-3">
        ${atual.respostas.map((opcao, i) => `
          <button 
            onclick="responder(${4 - i}, '${opcao}', ${indice})"
            class="border border-[#c98b00] rounded-2xl px-5 py-3 text-left hover:bg-[#c98b00] hover:text-white transition">
            ${opcao}
          </button>
        `).join("")}
      </div>
    </div>
  `;
}

render();

</script>
</body>
</html>
