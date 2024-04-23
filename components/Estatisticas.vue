<script setup>
const props = defineProps({
    pergunta: Object,
})
const pergunta = props.pergunta
const somaContagem = pergunta.opcoesResposta ? pergunta.opcoesResposta.reduce((acc, opcao) => acc + opcao.contagem, 0) : 0;
const chartOptions = {
    chart: {
        id: "grafico-rel-apex",
        type: 'bar',
        height: 350,
    },
    plotOptions: {
        bar: {
            borderRadius: 10,
            horizontal: false,
            columnWidth: '50%',
            distributed: true,
        }
    },
    xaxis: {
        categories: pergunta ? pergunta.opcoesResposta.map((opcao) => opcao.textoOpcaoResposta) : [],
        position: 'bottom',
        axisBorder: {
            show: false
        },
        axisTicks: {
            show: false
        },
        crosshairs: {
            fill: {
                type: 'gradient',
                gradient: {
                    colorFrom: '#D8E3F0',
                    colorTo: '#BED1E6',
                    stops: [0, 100],
                    opacityFrom: 0.4,
                    opacityTo: 0.5,
                }
            }
        },
        tooltip: {
            enabled: true,
        }
    },
    title: {
        text: `${somaContagem} Respostas`,
        style: {
            colors: ["#666"]
        }
    },
    subtitle: {
        text: 'Proporção das Respostas'
    },
    yaxis: {
        axisBorder: {
            show: false
        },
        axisTicks: {
            show: false,
        },
        labels: {
            formatter: function (val) {
                return val.toFixed(2) + '%';
            }
        }
    },
    dataLabels: {
        enabled: true,
        formatter: function (val) {
            return val + "%";
        },
        offsetY: -20,
        style: {
            fontSize: '12px',
            colors: ["#304758"]
        }
    },
};
const series = [
    {
        name: "Proporção",
        data: pergunta ? pergunta.opcoesResposta.map((opcao) => opcao.proporcao) : [],
    },
];
</script>

<template>
    <ClientOnly>
        <div class="pergunta-container">
            <h6 class="pergunta-title">{{ pergunta.textoPergunta }}</h6>
            <apexchart :options="chartOptions" :series="series" class="chart-container"></apexchart>
        </div>
    </ClientOnly>
</template>

<style>
.pergunta-container {
    margin-bottom: 20px;
    padding: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.pergunta-title {
    margin: 0;
    padding: 0;
    font-size: 18px;
    font-weight: bold;
    color: #666;
}

.chart-container {
    height: 300px;
}
</style>