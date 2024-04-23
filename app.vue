<script setup>

const pergunta = [
  {
    "idPergunta": 96,
    "textoPergunta": "Nos últimos 6 meses, quantos colegas de trabalho diretos deixaram o Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "1 - 2 pessoas",
        "contagem": 14,
        "proporcao": 26.92
      },
      {
        "textoOpcaoResposta": "3 - 5 pessoas",
        "contagem": 16,
        "proporcao": 30.77
      },
      {
        "textoOpcaoResposta": "Mais de 5 pessoas",
        "contagem": 11,
        "proporcao": 21.15
      },
      {
        "textoOpcaoResposta": "Nenhum",
        "contagem": 11,
        "proporcao": 21.15
      }
    ]
  },
  {
    "idPergunta": 145,
    "textoPergunta": null,
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "Murais de comunicados",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "Buritis",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "Castelo",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "Contagem",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "Cidade Nova",
        "contagem": 0,
        "proporcao": 0.00
      }
    ]
  },
  {
    "idPergunta": 146,
    "textoPergunta": "Quais canais de comunicação você considera mais eficazes no Meatz Burguer?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "Whatsapp",
        "contagem": 16,
        "proporcao": 30.77
      },
      {
        "textoOpcaoResposta": "Reuniões",
        "contagem": 19,
        "proporcao": 36.54
      },
      {
        "textoOpcaoResposta": "Murais",
        "contagem": 2,
        "proporcao": 3.85
      }
    ]
  },
  {
    "idPergunta": 82,
    "textoPergunta": "Como você avalia a qualidade da liderança no Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "Muito bom",
        "contagem": 27,
        "proporcao": 51.92
      },
      {
        "textoOpcaoResposta": "Bom",
        "contagem": 16,
        "proporcao": 30.77
      },
      {
        "textoOpcaoResposta": "Neutro",
        "contagem": 6,
        "proporcao": 11.54
      },
      {
        "textoOpcaoResposta": "Ruim",
        "contagem": 2,
        "proporcao": 3.85
      },
      {
        "textoOpcaoResposta": "Muito Ruim",
        "contagem": 1,
        "proporcao": 1.92
      }
    ]
  },
  {
    "idPergunta": 147,
    "textoPergunta": "Qual unidade você pertence?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "Santo Antônio",
        "contagem": 16,
        "proporcao": 30.77
      },
      {
        "textoOpcaoResposta": "Buritis",
        "contagem": 4,
        "proporcao": 7.69
      },
      {
        "textoOpcaoResposta": "Castelo",
        "contagem": 3,
        "proporcao": 5.77
      },
      {
        "textoOpcaoResposta": "Contagem",
        "contagem": 5,
        "proporcao": 9.62
      },
      {
        "textoOpcaoResposta": "Cidade Nova",
        "contagem": 9,
        "proporcao": 17.31
      }
    ]
  },
  {
    "idPergunta": 99,
    "textoPergunta": "Qual sua unidade de trabalho?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "1 - Centro Sul\n",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "2 - Buritis",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "3 - Castelo",
        "contagem": 3,
        "proporcao": 5.77
      },
      {
        "textoOpcaoResposta": "4 - Cidade Nova",
        "contagem": 0,
        "proporcao": 0.00
      },
      {
        "textoOpcaoResposta": "5 - Contagem",
        "contagem": 0,
        "proporcao": 0.00
      }
    ]
  },
  {
    "idPergunta": 84,
    "textoPergunta": "Você se sente motivado(a) para realizar o seu trabalho no Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "Sim",
        "contagem": 44,
        "proporcao": 84.62
      },
      {
        "textoOpcaoResposta": "Não",
        "contagem": 8,
        "proporcao": 15.38
      }
    ]
  },
  {
    "idPergunta": 86,
    "textoPergunta": "Em uma escala de 1 a 5, como você avalia os benefícios oferecidos pelo Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "5 - Muito Satisfatório",
        "contagem": 13,
        "proporcao": 25.00
      },
      {
        "textoOpcaoResposta": "4 - Satisfatório",
        "contagem": 13,
        "proporcao": 25.00
      },
      {
        "textoOpcaoResposta": "3 - Neutro",
        "contagem": 9,
        "proporcao": 17.31
      },
      {
        "textoOpcaoResposta": "2 - Pouco Satisfatório",
        "contagem": 7,
        "proporcao": 13.46
      },
      {
        "textoOpcaoResposta": "1 - Insatisfatório",
        "contagem": 7,
        "proporcao": 13.46
      }
    ]
  },
  {
    "idPergunta": 88,
    "textoPergunta": "Você sente que o Meatz Burger oferece oportunidades suficientes para o seu desenvolvimento profissional?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "Sim",
        "contagem": 45,
        "proporcao": 86.54
      },
      {
        "textoOpcaoResposta": "Não",
        "contagem": 7,
        "proporcao": 13.46
      }
    ]
  },
  {
    "idPergunta": 90,
    "textoPergunta": "Em uma escala de 1 a 5, o quanto você se sente parte da equipe do Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "5 - Totalmente parte",
        "contagem": 25,
        "proporcao": 48.08
      },
      {
        "textoOpcaoResposta": "4 - Bastante parte",
        "contagem": 14,
        "proporcao": 26.92
      },
      {
        "textoOpcaoResposta": "3 - Neutro",
        "contagem": 8,
        "proporcao": 15.38
      },
      {
        "textoOpcaoResposta": "2 - Pouco parte",
        "contagem": 1,
        "proporcao": 1.92
      },
      {
        "textoOpcaoResposta": "1 - Não me sinto parte",
        "contagem": 1,
        "proporcao": 1.92
      }
    ]
  },
  {
    "idPergunta": 92,
    "textoPergunta": "Como você avalia a comunicação interna no Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "5 - Muito Satisfatória",
        "contagem": 13,
        "proporcao": 25.00
      },
      {
        "textoOpcaoResposta": "4 - Satisfatória",
        "contagem": 27,
        "proporcao": 51.92
      },
      {
        "textoOpcaoResposta": "3 - Neutro",
        "contagem": 5,
        "proporcao": 9.62
      },
      {
        "textoOpcaoResposta": "2 - Pouco Satisfatória",
        "contagem": 2,
        "proporcao": 3.85
      },
      {
        "textoOpcaoResposta": "1 - Insatisfatória",
        "contagem": 3,
        "proporcao": 5.77
      }
    ]
  },
  {
    "idPergunta": 94,
    "textoPergunta": "Em uma escala de 1 a 5, o quanto você acha que o trabalho em equipe é valorizado no Meatz Burger?",
    "opcoesResposta": [
      {
        "textoOpcaoResposta": "5 - Muito valorizado",
        "contagem": 15,
        "proporcao": 28.85
      },
      {
        "textoOpcaoResposta": "4 - Valorizado",
        "contagem": 17,
        "proporcao": 32.69
      },
      {
        "textoOpcaoResposta": "3 - Neutro",
        "contagem": 10,
        "proporcao": 19.23
      },
      {
        "textoOpcaoResposta": "2 - Pouco valorizado",
        "contagem": 5,
        "proporcao": 9.62
      },
      {
        "textoOpcaoResposta": "1 - Não é valorizado",
        "contagem": 2,
        "proporcao": 3.85
      }
    ]
  }
]
const chartOptions = {
  chart: {
    id: "vuechart-example",
  },
  xaxis: {
    categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998],
  },
};
const series = [
  {
    name: "series-1",
    data: [30, 40, 35, 50, 49, 60, 70, 91],
  },
];
</script>

<template>
  <ClientOnly>
    <apexchart
      width="500"
      type="bar"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </ClientOnly>
  <apexchart
    width="500"
    type="bar"
    :options="chartOptions"
    :series="series"
  ></apexchart>
</template>