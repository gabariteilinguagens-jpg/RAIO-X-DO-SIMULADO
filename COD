export default function AutoAnaliseSimulado() {
  const blocos = [
    {
      titulo: "Estratégia de Prova",
      perguntas: [
        "Comecei pelas questões mais fáceis ou fui na ordem?",
        "Perdi muito tempo em poucas questões?",
        "Pulei questões quando necessário ou insisti demais?",
        "Consegui administrar bem o tempo até o final?",
        "Marquei o gabarito com tranquilidade ou no desespero?"
      ]
    },
    {
      titulo: "Leitura e Interpretação",
      perguntas: [
        "Tive dificuldade com textos longos?",
        "Precisei reler textos por falta de atenção?",
        "Interpretei mal o comando da questão?",
        "Tive dificuldade com imagens, gráficos ou charges?",
        "Faltou repertório visual ou artístico?"
      ]
    },
    {
      titulo: "Conteúdo e Base Teórica",
      perguntas: [
        "Minha maior dificuldade foi Literatura ou Português?",
        "Errei por falta de conteúdo ou por distração?",
        "Percebi padrões de erro repetidos?",
        "Faltou revisão de conteúdos importantes?",
        "O conteúdo parecia familiar, mas não consegui aplicar?"
      ]
    },
    {
      titulo: "Emocional e Resistência",
      perguntas: [
        "Me senti ansioso(a) antes ou durante a prova?",
        "O nervosismo atrapalhou meu raciocínio?",
        "Senti exaustão mental antes do final?",
        "Minha confiança caiu durante a prova?",
        "Fiquei travado(a) por medo de errar?"
      ]
    },
    {
      titulo: "Pós-Prova Estratégico",
      perguntas: [
        "Se eu repetisse essa prova amanhã, o que faria diferente?",
        "Meu maior erro foi conteúdo, estratégia ou emocional?",
        "Qual hábito preciso mudar imediatamente?",
        "O que preciso ajustar para o próximo simulado?",
        "Qual será minha meta concreta para a próxima prova?"
      ]
    }
  ];

  const respostasPorPergunta = {
    "Comecei pelas questões mais fáceis ou fui na ordem?": [
      "Fui direto nas mais fáceis e estratégicas",
      "Misturei estratégia com a ordem da prova",
      "Fiz quase tudo na ordem e perdi tempo",
      "Fiz totalmente na ordem e isso me prejudicou muito"
    ],
    "Perdi muito tempo em poucas questões?": [
      "Não, administrei bem meu tempo",
      "Um pouco, mas consegui recuperar depois",
      "Sim, isso atrapalhou bastante meu ritmo",
      "Sim, perdi totalmente o controle do tempo"
    ],
    "Pulei questões quando necessário ou insisti demais?": [
      "Pulei com estratégia e voltei depois",
      "Às vezes soube a hora de pular",
      "Insisti mais do que deveria",
      "Fiquei preso(a) em várias questões"
    ],
    "Consegui administrar bem o tempo até o final?": [
      "Sim, finalizei com tranquilidade",
      "Quase, mas o final ficou apertado",
      "Não, faltou bastante tempo",
      "Foi um verdadeiro desespero até o fim"
    ],
    "Marquei o gabarito com tranquilidade ou no desespero?": [
      "Com calma e segurança",
      "Com alguma pressa, mas controlado",
      "Muito corrido e inseguro",
      "No puro desespero"
    ],
    "Tive dificuldade com textos longos?": [
      "Não, li com tranquilidade",
      "Um pouco, mas consegui manter o foco",
      "Sim, senti bastante dificuldade",
      "Sim, isso comprometeu muito minha prova"
    ],
    "Precisei reler textos por falta de atenção?": [
      "Quase nunca",
      "Algumas vezes",
      "Muitas vezes",
      "O tempo todo"
    ],
    "Interpretei mal o comando da questão?": [
      "Não, compreendi bem o que era pedido",
      "Em poucas questões",
      "Em várias questões",
      "Isso foi um grande problema na prova"
    ],
    "Tive dificuldade com imagens, gráficos ou charges?": [
      "Não, interpretei bem",
      "Algumas vezes senti dificuldade",
      "Sim, isso aconteceu com frequência",
      "Sim, foi uma grande dificuldade"
    ],
    "Faltou repertório visual ou artístico?": [
      "Não, consegui relacionar bem",
      "Um pouco, em algumas questões",
      "Sim, senti bastante falta",
      "Sim, isso prejudicou muito meu desempenho"
    ],
    "Minha maior dificuldade foi Literatura ou Português?": [
      "Nenhuma das duas foi um grande problema",
      "Tive dificuldade leve em uma delas",
      "Uma delas me prejudicou bastante",
      "Ambas foram grandes dificuldades"
    ],
    "Errei por falta de conteúdo ou por distração?": [
      "Mais por distração do que por conteúdo",
      "Houve equilíbrio entre os dois",
      "Mais por falta de conteúdo",
      "Errei muito por ambos"
    ],
    "Percebi padrões de erro repetidos?": [
      "Não, meus erros foram pontuais",
      "Sim, mas em poucos momentos",
      "Sim, percebi vários padrões repetidos",
      "Sim, os mesmos erros se repetiram o tempo todo"
    ],
    "Faltou revisão de conteúdos importantes?": [
      "Não, me senti bem preparado(a)",
      "Um pouco, senti falta de alguns tópicos",
      "Sim, faltou bastante revisão",
      "Sim, isso comprometeu fortemente minha prova"
    ],
    "O conteúdo parecia familiar, mas não consegui aplicar?": [
      "Não, consegui aplicar com segurança",
      "Em poucas questões aconteceu isso",
      "Sim, aconteceu várias vezes",
      "Sim, isso foi um grande problema"
    ],
    "Me senti ansioso(a) antes ou durante a prova?": [
      "Não, me senti tranquilo(a)",
      "Um pouco, mas consegui controlar",
      "Sim, isso atrapalhou em alguns momentos",
      "Sim, a ansiedade dominou minha prova"
    ],
    "O nervosismo atrapalhou meu raciocínio?": [
      "Não, consegui pensar com clareza",
      "Um pouco, nas questões mais difíceis",
      "Sim, atrapalhou bastante",
      "Sim, fiquei travado(a) várias vezes"
    ],
    "Senti exaustão mental antes do final?": [
      "Não, mantive o ritmo até o fim",
      "Um pouco no final",
      "Sim, senti forte desgaste",
      "Sim, terminei completamente esgotado(a)"
    ],
    "Minha confiança caiu durante a prova?": [
      "Não, mantive segurança",
      "Em alguns momentos",
      "Sim, perdi bastante confiança",
      "Sim, achei que tinha ido muito mal"
    ],
    "Fiquei travado(a) por medo de errar?": [
      "Não, consegui seguir com segurança",
      "Algumas vezes",
      "Sim, aconteceu com frequência",
      "Sim, isso prejudicou muito meu desempenho"
    ],
    "Se eu repetisse essa prova amanhã, o que faria diferente?": [
      "Mudaria minha estratégia de resolução",
      "Melhoraria minha gestão de tempo",
      "Controlaria melhor meu emocional",
      "Preciso rever tudo isso"
    ],
    "Meu maior erro foi conteúdo, estratégia ou emocional?": [
      "Principalmente conteúdo",
      "Principalmente estratégia de prova",
      "Principalmente emocional e ansiedade",
      "Foi uma mistura dos três"
    ],
    "Qual hábito preciso mudar imediatamente?": [
      "Minha rotina de revisão",
      "Minha gestão de tempo nos simulados",
      "Meu controle emocional durante a prova",
      "Minha disciplina de estudo como um todo"
    ],
    "O que preciso ajustar para o próximo simulado?": [
      "Estratégia de prova",
      "Interpretação e leitura",
      "Revisão de conteúdo",
      "Resistência emocional e mental"
    ],
    "Qual será minha meta concreta para a próxima prova?": [
      "Melhorar meu tempo de prova",
      "Reduzir erros por distração",
      "Aumentar minha segurança nas questões",
      "Fazer uma prova mais estratégica e consciente"
    ]
  };

  return (
    <div className="min-h-screen bg-[#f3f0eb] text-[#3b2a2a] p-6">
      <div className="max-w-6xl mx-auto">
        <header className="bg-white rounded-3xl shadow-lg p-8 mb-8 border border-[#d9cfc3]">
          <p className="text-sm font-semibold text-[#7a2e1f]">Mentoria Prof. Maria Hellen • Raio-X do Simulado</p>
          <h1 className="text-5xl font-bold mt-2 text-[#c98b00]">RAIO-X DO SIMULADO</h1>
          <p className="text-xl mt-2 font-medium">Estratégia e Leitura — Autoanálise Pós-Simulado</p>
          <p className="mt-4 text-base leading-relaxed">
            Descubra se seu verdadeiro problema está no conteúdo, na estratégia, na leitura, na resistência ou no emocional.
            Responda cada etapa, acompanhe sua evolução e receba um diagnóstico estratégico completo do seu desempenho.
          </p>
        </header>

        <section className="mb-8 bg-white rounded-3xl p-6 shadow-md border border-[#e2d8cb]">
          <h2 className="text-xl font-bold text-[#7a2e1f] mb-2">Missão em andamento</h2>
          <p className="mb-3">Etapa 1 de 5 — Seu objetivo não é apenas terminar a prova, é dominar a estratégia.</p>
          <div className="w-full bg-[#eee4d8] rounded-full h-4">
            <div className="bg-[#c98b00] h-4 rounded-full w-3/5"></div>
          </div>
        </section>

        <div className="space-y-8">
          {blocos.map((bloco, blocoIndex) => (
            <section key={blocoIndex} className="bg-white rounded-3xl p-8 shadow-md border border-[#e2d8cb]">
              <h2 className="text-2xl font-bold text-[#7a2e1f] mb-6">{bloco.titulo}</h2>

              <div className="space-y-6">
                {bloco.perguntas.map((pergunta, index) => (
                  <div key={index} className="border-b border-[#eee4d8] pb-6 last:border-none">
                    <h3 className="text-lg font-semibold mb-4">{index + 1}. {pergunta}</h3>

                    <div className="grid grid-cols-2 md:grid-cols-4 gap-3">
                      {(respostasPorPergunta[pergunta] || [
                        "Resposta muito positiva",
                        "Consigo, mas ainda com falhas",
                        "Isso me prejudica bastante",
                        "Esse é um dos meus maiores gargalos"
                      ]).map((opcao) => (
                        <button
                          key={opcao}
                          className="rounded-2xl border border-[#c98b00] px-4 py-3 font-medium hover:bg-[#c98b00] hover:text-white transition"
                        >
                          {opcao}
                        </button>
                      ))}
                    </div>
                  </div>
                ))}
              </div>
            </section>
          ))}
        </div>

        <section className="mt-10 bg-[#7a2e1f] text-white rounded-3xl p-8 shadow-xl">
          <h2 className="text-3xl font-bold mb-3">Seu Perfil Estratégico</h2>
          <p className="mb-4 text-lg">🥈 Estrategista em Construção</p>
          <p className="mb-6">Você sabe mais do que consegue demonstrar sob pressão. Seu principal gargalo pode não ser conteúdo, mas execução e controle emocional.</p>

          <h3 className="text-2xl font-bold mb-3">Plano de Ação Imediato</h3>
          <ul className="space-y-2 mb-8 text-lg">
            <li>• Treinar simulados com controle real de tempo</li>
            <li>• Reduzir erros por distração e releitura excessiva</li>
            <li>• Fortalecer resistência mental até o fim da prova</li>
            <li>• Melhorar estratégia de escolha e abandono de questões</li>
          </ul>

          <div className="bg-white/10 rounded-2xl p-5 mb-8">
            <p className="text-lg italic">“Seu resultado não mostra sua capacidade. Mostra sua estratégia.”</p>
          </div>

          <div className="bg-white/10 rounded-2xl p-6 mb-8">
            <h3 className="text-2xl font-bold mb-4">Um lembrete importante</h3>
            <p className="text-lg italic leading-relaxed mb-4">
              “Não precisa ser feliz sequer.<br />
              Basta ano novo.<br />
              E é tão difícil mudar.<br />
              Às vezes escorre sangue.”
            </p>
            <p className="mb-4">— Clarice Lispector</p>
            <p className="leading-relaxed">
              Mudar estratégia dói. Criar disciplina dói. Sair do automático dói.
              Mas repetir os mesmos erros também.
              Seu próximo simulado não precisa ser perfeito. Precisa ser diferente.
            </p>
          </div>

          <h3 className="text-2xl font-bold mb-3">Compromisso para o próximo simulado</h3>
          <div className="bg-white rounded-2xl p-4 text-[#3b2a2a] mb-8">
            Eu me comprometo a: _______________________________
          </div>

          <div className="border-t border-white/20 pt-8">
          <h2 className="text-3xl font-bold mb-3">Diagnóstico Final</h2>
          <p className="mb-4 text-lg">
            Seu problema foi realmente conteúdo — ou estratégia, ansiedade e gestão de prova?
          </p>
          <p className="mb-6">
            Ao finalizar, você recebe um raio-x estratégico com seus principais gargalos e um plano de ação para o próximo simulado.
          </p>
          <button className="bg-[#c98b00] px-8 py-4 rounded-2xl font-semibold hover:scale-105 transition">
            Ver Meu Resultado
          </button>
        </div>
        </section>
      </div>
    </div>
  );
}
