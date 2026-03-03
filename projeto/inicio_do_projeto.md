<h1>1. Problema</h1>

<p>
Fraudes em cartão de crédito representam um dos maiores desafios do setor financeiro. 
Instituições financeiras processam milhões de transações diariamente, tornando inviável 
a identificação manual de atividades fraudulentas.
</p>

<p><strong>Problema central:</strong></p>

<blockquote>
Como identificar automaticamente transações fraudulentas em meio a um grande volume de operações legítimas, minimizando perdas financeiras e reduzindo falsos positivos?
</blockquote>

<p>Esse problema possui características críticas:</p>

<ul>
  <li>Alto volume de dados transacionais;</li>
  <li>Forte desbalanceamento entre transações legítimas e fraudulentas;</li>
  <li>Necessidade de resposta rápida (idealmente em tempo real);</li>
  <li>Impacto direto na experiência do cliente (bloqueios indevidos).</li>
</ul>

<p>Do ponto de vista de negócio, falhas nesse processo podem gerar:</p>

<ul>
  <li>Prejuízo financeiro direto;</li>
  <li>Perda de confiança do cliente;</li>
  <li>Custos operacionais elevados com análise manual.</li>
</ul>

<hr>

<h1>2. Contexto</h1>

<h2>Conjunto de Dados Utilizado</h2>

<p>
O projeto utiliza um dataset público de transações de cartão de crédito, 
amplamente utilizado em estudos e competições de Machine Learning.
</p>

<p><strong>Características do dataset:</strong></p>

<ul>
  <li>Transações realizadas por cartões europeus;</li>
  <li>Variáveis numéricas resultantes de transformação PCA (V1 a V28);</li>
  <li>Variáveis adicionais:
    <ul>
      <li><code>Time</code> – tempo da transação;</li>
      <li><code>Amount</code> – valor da transação;</li>
      <li><code>Class</code> – 0 = legítima, 1 = fraude.</li>
    </ul>
  </li>
</ul>

<h3>Aspecto Crítico: Desbalanceamento</h3>

<ul>
  <li>A proporção de fraudes é extremamente baixa (menos de 1%);</li>
  <li>Trata-se de um típico problema de classificação desbalanceada.</li>
</ul>

<h2>Viabilidade e Justificativa da Escolha</h2>

<p>O dataset é adequado porque:</p>

<ol>
  <li>Simula um cenário real de instituição financeira;</li>
  <li>Possui volume suficiente para treinar modelos de Machine Learning;</li>
  <li>Permite trabalhar técnicas importantes como:
    <ul>
      <li>Tratamento de dados desbalanceados;</li>
      <li>Avaliação com métricas adequadas (Precision, Recall, F1-score);</li>
      <li>Modelos supervisionados de classificação.</li>
    </ul>
  </li>
</ol>

<p>
Além disso, a anonimização via PCA garante privacidade, tornando o dataset 
seguro para uso acadêmico e experimental.
</p>

<hr>

<h1>3. Objetivos</h1>

<h2>Objetivo Geral</h2>

<p>
Construir um modelo de Machine Learning capaz de classificar transações como 
fraudulentas ou legítimas com alto desempenho, especialmente na detecção de fraudes.
</p>

<h2>Objetivos Específicos</h2>

<ol>
  <li>Realizar análise exploratória dos dados (EDA):
    <ul>
      <li>Verificar distribuição das classes;</li>
      <li>Identificar padrões e correlações;</li>
      <li>Analisar comportamento da variável <code>Amount</code>.</li>
    </ul>
  </li>

  <li>Tratar o desbalanceamento:
    <ul>
      <li>Avaliar técnicas como undersampling ou oversampling;</li>
      <li>Comparar desempenho com e sem balanceamento.</li>
    </ul>
  </li>

  <li>Treinar modelos de classificação:
    <ul>
      <li>Logistic Regression;</li>
      <li>Random Forest;</li>
      <li>Outros modelos avaliados no notebook.</li>
    </ul>
  </li>

  <li>Avaliar os modelos utilizando métricas adequadas:
    <ul>
      <li>Recall (fundamental para fraudes);</li>
      <li>Precision;</li>
      <li>F1-score;</li>
      <li>Matriz de confusão;</li>
      <li>AUC-ROC.</li>
    </ul>
  </li>
</ol>

<h2>Resultados Esperados</h2>

<h3>Do ponto de vista técnico:</h3>

<ul>
  <li>Modelo com alto <strong>recall</strong> para classe fraudulenta (reduzir fraudes não detectadas);</li>
  <li>Manter precisão razoável para evitar bloqueios indevidos;</li>
  <li>Melhor desempenho comparado a um classificador ingênuo.</li>
</ul>

<h3>Do ponto de vista de negócio:</h3>

<ul>
  <li>Redução de perdas financeiras;</li>
  <li>Diminuição da necessidade de auditoria manual;</li>
  <li>Melhoria na segurança transacional;</li>
  <li>Aumento da confiança do cliente.</li>
</ul>
