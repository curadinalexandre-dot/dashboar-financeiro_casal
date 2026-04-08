# dashboar-financeiro_casal<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard Financeiro Completo - Vinicius & Mariana</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f5f5f5;
            padding: 20px;
            color: #333;
        }
        .container { max-width: 1600px; margin: 0 auto; }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 30px;
        }
        .header h1 { font-size: 32px; margin-bottom: 10px; }
        .header p { font-size: 16px; opacity: 0.9; }

        .status-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .status-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
        }
        .status-card h3 {
            font-size: 12px;
            color: #666;
            margin-bottom: 8px;
            text-transform: uppercase;
        }
        .status-card .value {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 5px;
        }
        .status-card .sub {
            font-size: 12px;
            color: #999;
        }

        .green { color: #27ae60; }
        .red { color: #e74c3c; }
        .orange { color: #f39c12; }
        .blue { color: #2980b9; }

        .alert-box {
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
        }
        .alert-box h3 { color: #856404; margin-bottom: 10px; }

        .success-box {
            background: #d4edda;
            border-left: 4px solid #28a745;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
        }
        .success-box h3 { color: #155724; margin-bottom: 10px; }

        .chart-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .chart-container {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
        }
        .chart-container h2 {
            font-size: 18px;
            margin-bottom: 20px;
            color: #333;
        }

        .timeline {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            margin-bottom: 30px;
        }
        .timeline h2 {
            font-size: 20px;
            margin-bottom: 20px;
        }
        .timeline-item {
            padding: 15px;
            border-left: 3px solid #667eea;
            margin-bottom: 15px;
            background: #f8f9fa;
        }
        .timeline-item h3 {
            font-size: 16px;
            margin-bottom: 8px;
            color: #667eea;
        }
        .timeline-item p {
            font-size: 14px;
            color: #666;
            margin-bottom: 5px;
        }
        .timeline-item .liberation {
            font-size: 18px;
            font-weight: bold;
            color: #27ae60;
            margin-top: 5px;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="header">
        <h1>Dashboard Financeiro Completo</h1>
        <p>Vinicius & Mariana | Março 2026 (Realizado) + Meta Abril 2026</p>
    </div>

    <!-- Cards atualizados com Março realizado + meta Abril -->
    <div class="status-cards">
        <div class="status-card">
            <h3>Março 2026 (Realizado)</h3>
            <div class="value red">R$ 19.625,93</div>
            <div class="sub">Gastos totais do mês</div>
        </div>

        <div class="status-card">
            <h3>Renda Março (estimada/recebida)</h3>
            <div class="value">R$ 15.345,93</div>
            <div class="sub">Vine: R$ 7.345,93 | Mari: R$ 8.000,00</div>
        </div>

        <div class="status-card">
            <h3>Resultado Março</h3>
            <div class="value red">-R$ 4.280,00</div>
            <div class="sub">Coberto por cartão + empréstimo</div>
        </div>

        <div class="status-card">
            <h3>Cobertura (Dívida Nova)</h3>
            <div class="value orange">R$ 4.280,00</div>
            <div class="sub">Cartão: R$ 3.280,00 | Empréstimo: R$ 1.000,00</div>
        </div>

        <div class="status-card">
            <h3>Meta Abril 2026</h3>
            <div class="value green">R$ 14.000,00</div>
            <div class="sub">Teto para não faltar grana</div>
        </div>
    </div>

    <div class="success-box">
        <h3>✅ Leitura rápida (Março)</h3>
        <p>• O déficit não foi “um gasto isolado”: foi <b>despesa maior que renda</b> e a diferença virou <b>dívida nova</b>.</p>
        <p>• O caminho para estancar é simples: <b>parar de financiar o mês com cartão</b> e trabalhar com <b>teto de gastos</b> em abril.</p>
    </div>

    <div class="alert-box">
        <h3>⚠️ Ação para estancar (Abril)</h3>
        <p><b>1)</b> Sem novas parcelas no cartão até fechar 2 meses no azul.</p>
        <p><b>2)</b> Teto mensal de <b>R$ 14.000</b> em abril (isso dá ~<b>R$ 3.500 por semana</b>).</p>
        <p><b>3)</b> Se passar do teto na 2ª/3ª semana, travar imediatamente: comida fora/eventos/compras não essenciais.</p>
    </div>

    <div class="chart-grid">
        <div class="chart-container">
            <h2>Evolução Mensal 2026 (Real + Meta)</h2>
            <canvas id="evolucaoChart"></canvas>
        </div>
        <div class="chart-container">
            <h2>Comparativo por Cartão (inclui Março)</h2>
            <canvas id="cartoesChart"></canvas>
        </div>
    </div>

    <div class="chart-grid">
        <div class="chart-container">
            <h2>Distribuição % Gastos Totais</h2>
            <canvas id="percentualGeralChart"></canvas>
        </div>
        <div class="chart-container">
            <h2>Distribuição % Cartões (Fevereiro)</h2>
            <canvas id="percentualCartoesChart"></canvas>
        </div>
    </div>

    <div class="timeline">
        <h2>📅 Cronograma de Liberação de Parcelas 2026</h2>

        <div class="timeline-item">
            <h3>MARÇO 2026 🎉</h3>
            <p>Empréstimo Casamento (R$ 2.303) + 12 outras parcelas</p>
            <div class="liberation">Liberação: R$ 4.252/mês</div>
        </div>

        <div class="timeline-item">
            <h3>ABRIL 2026</h3>
            <p>Rodas Bike, presentes Natal, Airbnb praia (7 parcelas)</p>
            <div class="liberation">Liberação: R$ 1.558/mês</div>
        </div>

        <div class="timeline-item">
            <h3>MAIO 2026</h3>
            <p>Presentes casamento (2 parcelas)</p>
            <div class="liberation">Liberação: R$ 355/mês</div>
        </div>

        <div class="timeline-item">
            <h3>JUNHO 2026</h3>
            <p>Capacete Iron, Inscrição Iron Man, IPVA</p>
            <div class="liberation">Liberação: R$ 1.021/mês</div>
        </div>

        <div class="timeline-item">
            <h3>JULHO 2026</h3>
            <p>Relógio Garmin, equipamentos (4 parcelas)</p>
            <div class="liberation">Liberação: R$ 834/mês</div>
        </div>

        <div class="timeline-item">
            <h3>SETEMBRO 2026 🎉</h3>
            <p>Lua de Mel quitada!</p>
            <div class="liberation">Liberação: R$ 1.093/mês</div>
        </div>

        <div class="timeline-item">
            <h3>DEZEMBRO 2026</h3>
            <p>TV, Seguro Carro, Adidas</p>
            <div class="liberation">Liberação: R$ 534/mês</div>
        </div>
    </div>

    <div class="chart-grid">
        <div class="chart-container">
            <h2>Projeção Despesas 2026</h2>
            <canvas id="projecaoChart"></canvas>
        </div>
        <div class="chart-container">
            <h2>Acúmulo Reserva Projetada</h2>
            <canvas id="reservaChart"></canvas>
        </div>
    </div>
</div>

<script>
    // Valores confirmados (Março realizado + meta Abril)
    const MAR_REAL_GASTOS = 19625.93;
    const MAR_RENDA = 15345.93;
    const ABR_META_GASTOS = 14000.00;

    // Cartões Março confirmados
    const MAR_CARTAO_VINE = 3284.72;
    const MAR_CARTAO_CASA = 6620.13;
    const MAR_CARTAO_MARI = 1570.05;

    // Evolução Mensal (ajuste: Mar = realizado; Abr = meta 14k)
    new Chart(document.getElementById('evolucaoChart'), {
        type: 'line',
        data: {
            labels: ['Dez/25', 'Jan/26', 'Fev/26', 'Mar/26', 'Abr/26', 'Mai/26', 'Jun/26', 'Jul/26', 'Ago/26', 'Set/26'],
            datasets: [{
                label: 'Despesas Totais (Real/Meta)',
                data: [17993, 22736, 20538, MAR_REAL_GASTOS, ABR_META_GASTOS, 12750, 13000, 13050, 13050, 12450],
                borderColor: '#e74c3c',
                backgroundColor: 'rgba(231, 76, 60, 0.1)',
                tension: 0.3,
                fill: true
            }, {
                label: 'Renda (referência)',
                data: [18000, 18000, 18000, MAR_RENDA, MAR_RENDA, 18000, 18000, 18000, 18000, 18000],
                borderColor: '#27ae60',
                borderDash: [5, 5],
                tension: 0
            }, {
                label: 'Teto Abril (meta)',
                data: [null, null, null, null, ABR_META_GASTOS, null, null, null, null, null],
                borderColor: '#2980b9',
                backgroundColor: 'rgba(41, 128, 185, 0.08)',
                tension: 0,
                pointRadius: 6,
                pointHoverRadius: 7
            }]
        },
        options: {
            responsive: true,
            plugins: {
                legend: { position: 'top' },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            const v = context.parsed.y;
                            if (v === null || v === undefined) return context.dataset.label + ': -';
                            return context.dataset.label + ': R$ ' + v.toLocaleString('pt-BR', {minimumFractionDigits: 2, maximumFractionDigits: 2});
                        }
                    }
                }
            },
            scales: {
                y: {
                    beginAtZero: true,
                    ticks: {
                        callback: function(value) {
                            return 'R$ ' + value.toLocaleString('pt-BR');
                        }
                    }
                }
            }
        }
    });

    // Comparativo Cartões (inclui Março)
    new Chart(document.getElementById('cartoesChart'), {
        type: 'bar',
        data: {
            labels: ['Dezembro', 'Janeiro', 'Fevereiro', 'Março'],
            datasets: [{
                label: 'Vinicius',
                data: [3013, 3789, 3745, MAR_CARTAO_VINE],
                backgroundColor: 'rgba(155, 89, 182, 0.8)'
            }, {
                label: 'Casa',
                data: [4856, 6865, 6511, MAR_CARTAO_CASA],
                backgroundColor: 'rgba(52, 152, 219, 0.8)'
            }, {
                label: 'Mariana',
                data: [2674, 3559, 2724, MAR_CARTAO_MARI],
                backgroundColor: 'rgba(241, 196, 15, 0.8)'
            }]
        },
        options: {
            responsive: true,
            plugins: { legend: { position: 'top' } },
            scales: {
                y: {
                    beginAtZero: true,
                    ticks: {
                        callback: function(value) {
                            return 'R$ ' + value.toLocaleString('pt-BR');
                        }
                    }
                }
            }
        }
    });

    // Percentual Gastos Totais (mantido: Jan/Fev - sem dados detalhados de Mar)
    new Chart(document.getElementById('percentualGeralChart'), {
        type: 'line',
        data: {
            labels: ['Alimentação', 'Esporte', 'Transporte', 'Presentes', 'Saúde', 'Pessoal', 'Outros'],
            datasets: [{
                label: 'Janeiro %',
                data: [19.8, 17.8, 7.9, 11.9, 1.7, 5.4, 9.2],
                borderColor: 'rgba(231, 76, 60, 0.8)',
                backgroundColor: 'rgba(231, 76, 60, 0.1)',
                tension: 0.3,
                fill: true
            }, {
                label: 'Fevereiro %',
                data: [21.5, 19.2, 9.1, 8.3, 6.5, 7.1, 6.8],
                borderColor: 'rgba(52, 152, 219, 0.8)',
                backgroundColor: 'rgba(52, 152, 219, 0.1)',
                tension: 0.3,
                fill: true
            }]
        },
        options: {
            responsive: true,
            plugins: { legend: { position: 'top' } },
            scales: {
                y: {
                    beginAtZero: true,
                    ticks: {
                        callback: function(value) {
                            return value + '%';
                        }
                    }
                }
            }
        }
    });

    // Percentual Cartões (mantido: Fevereiro)
    new Chart(document.getElementById('percentualCartoesChart'), {
        type: 'doughnut',
        data: {
            labels: ['Alimentação', 'Esporte/Saúde', 'Transporte', 'Presentes', 'Pessoal', 'Saúde', 'Trabalho', 'Outros'],
            datasets: [{
                data: [21.5, 19.2, 9.1, 8.3, 7.1, 6.5, 5.0, 23.3],
                backgroundColor: [
                    'rgba(231, 76, 60, 0.8)',
                    'rgba(52, 152, 219, 0.8)',
                    'rgba(155, 89, 182, 0.8)',
                    'rgba(241, 196, 15, 0.8)',
                    'rgba(46, 204, 113, 0.8)',
                    'rgba(230, 126, 34, 0.8)',
                    'rgba(149, 165, 166, 0.8)',
                    'rgba(127, 140, 141, 0.8)'
                ]
            }]
        },
        options: {
            responsive: true,
            plugins: {
                legend: { position: 'right' },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            return context.label + ': ' + context.parsed.toFixed(1) + '%';
                        }
                    }
                }
            }
        }
    });

    // Projeção Despesas (mantida)
    new Chart(document.getElementById('projecaoChart'), {
        type: 'bar',
        data: {
            labels: ['Mar', 'Abr', 'Mai', 'Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez'],
            datasets: [{
                label: 'Fixos',
                data: [5035, 5035, 5035, 5035, 5035, 5035, 3942, 3942, 3942, 3942],
                backgroundColor: 'rgba(52, 152, 219, 0.8)',
                stack: 'Stack 0'
            }, {
                label: 'Variáveis',
                data: [5863, 5500, 5500, 5200, 5200, 5200, 5200, 5200, 5200, 5200],
                backgroundColor: 'rgba(155, 89, 182, 0.8)',
                stack: 'Stack 0'
            }, {
                label: 'Eventos/Presentes',
                data: [500, 600, 600, 700, 700, 700, 700, 700, 700, 2000],
                backgroundColor: 'rgba(241, 196, 15, 0.8)',
                stack: 'Stack 0'
            }, {
                label: 'Reserva',
                data: [800, 1800, 2000, 2000, 2200, 2200, 2500, 2500, 2500, 2000],
                backgroundColor: 'rgba(46, 204, 113, 0.8)',
                stack: 'Stack 0'
            }]
        },
        options: {
            responsive: true,
            plugins: { legend: { position: 'top' } },
            scales: {
                y: {
                    stacked: true,
                    ticks: {
                        callback: function(value) {
                            return 'R$ ' + value.toLocaleString('pt-BR');
                        }
                    }
                },
                x: { stacked: true }
            }
        }
    });

    // Reserva Acumulada (mantida)
    new Chart(document.getElementById('reservaChart'), {
        type: 'line',
        data: {
            labels: ['Mar', 'Abr', 'Mai', 'Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez'],
            datasets: [{
                label: 'Reserva Acumulada',
                data: [1500, 3300, 5300, 7300, 9500, 11700, 14200, 16700, 19200, 21200],
                borderColor: '#27ae60',
                backgroundColor: 'rgba(46, 204, 113, 0.2)',
                tension: 0.3,
                fill: true,
                pointRadius: 5,
                pointHoverRadius: 7
            }]
        },
        options: {
            responsive: true,
            plugins: { legend: { position: 'top' } },
            scales: {
                y: {
                    beginAtZero: true,
                    ticks: {
                        callback: function(value) {
                            return 'R$ ' + value.toLocaleString('pt-BR');
                        }
                    }
                }
            }
        }
    });
</script>
</body>
</html>


