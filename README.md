<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PCH em Território Indígena — Análise Jurídica</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700&family=Source+Serif+4:ital,wght@0,300;0,400;0,600;1,400&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root {
  --terra-900: #1C1208;
  --terra-800: #2E1F0E;
  --terra-700: #4A3018;
  --terra-600: #6B4423;
  --terra-500: #8B5E34;
  --terra-400: #B07D52;
  --terra-300: #C9A07A;
  --terra-200: #E0C4A0;
  --terra-100: #F0DFC4;
  --terra-50:  #FAF3E8;
  --areia-100: #F5ECD8;
  --areia-50:  #FBF7EF;
  --ocre:      #C17F3A;
  --ocre-dark: #9A5F1E;
  --ocre-light:#E8C07A;
  --critico:   #8B1A1A;
  --critico-bg:#FDF0F0;
  --critico-bd:#D9A0A0;
  --grave:     #7A5000;
  --grave-bg:  #FDF6E8;
  --grave-bd:  #D4B060;
  --relevante: #1A4A6B;
  --relevante-bg:#EEF4FA;
  --relevante-bd:#88AECB;
  --ok-text:   #1E5C2A;
  --ok-bg:     #EDF5EF;
  --ok-bd:     #7BBB88;
  --bg:        #F7F2EA;
  --surface:   #FDFAF5;
  --surface2:  #F3ECD9;
  --border:    #D4C4A8;
  --border-lt: #E6DCCB;
  --text:      #1C1208;
  --text-2:    #4A3018;
  --text-3:    #7A6048;
  --text-4:    #A08060;
  --radius-sm: 4px;
  --radius-md: 6px;
  --radius-lg: 10px;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Source Serif 4', Georgia, serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  font-size: 15px;
  line-height: 1.6;
}

/* ── LAYOUT ── */
.page { max-width: 960px; margin: 0 auto; padding: 0 1.25rem 3rem; }

/* ── HEADER ── */
.masthead {
  background: var(--terra-800);
  padding: 0;
  margin-bottom: 0;
  border-bottom: 3px solid var(--ocre);
}
.masthead-inner {
  max-width: 960px;
  margin: 0 auto;
  padding: 1.5rem 1.25rem 1.25rem;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 1rem;
  flex-wrap: wrap;
}
.masthead-left { flex: 1; min-width: 200px; }
.masthead-eyebrow {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--ocre-light);
  margin-bottom: 6px;
}
.masthead-title {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 22px;
  font-weight: 700;
  color: #F5ECD8;
  line-height: 1.2;
  letter-spacing: -0.01em;
}
.masthead-title span { color: var(--ocre-light); }
.masthead-sub {
  font-size: 12px;
  color: var(--terra-300);
  margin-top: 5px;
  font-style: italic;
}
.masthead-right {
  display: flex;
  gap: 8px;
  align-items: center;
  flex-wrap: wrap;
  padding-top: 4px;
}
.masthead-input {
  font-family: 'Source Serif 4', serif;
  font-size: 13px;
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.2);
  border-radius: var(--radius-md);
  color: #F5ECD8;
  padding: 7px 12px;
  width: 200px;
  outline: none;
  transition: border-color 0.2s;
}
.masthead-input::placeholder { color: var(--terra-300); }
.masthead-input:focus { border-color: var(--ocre-light); }
.btn-resumo {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.05em;
  background: var(--ocre);
  color: #FBF7EF;
  border: none;
  border-radius: var(--radius-md);
  padding: 8px 14px;
  cursor: pointer;
  transition: background 0.2s;
  white-space: nowrap;
}
.btn-resumo:hover { background: var(--ocre-dark); }

/* ── METRICS BAND ── */
.metrics-band {
  background: var(--terra-700);
  border-bottom: 1px solid var(--terra-600);
  margin-bottom: 0;
}
.metrics-band-inner {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 1.25rem;
  display: grid;
  grid-template-columns: repeat(4, minmax(0,1fr));
}
.metric-cell {
  padding: 14px 16px;
  border-right: 1px solid rgba(255,255,255,0.08);
  position: relative;
}
.metric-cell:last-child { border-right: none; }
.metric-cell-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--terra-300);
  margin-bottom: 5px;
}
.metric-cell-val {
  font-family: 'Playfair Display', serif;
  font-size: 26px;
  font-weight: 600;
  color: var(--areia-100);
  line-height: 1;
}
.metric-cell-sub {
  font-size: 11px;
  color: var(--terra-300);
  margin-top: 3px;
}
.metric-bar {
  height: 3px;
  background: rgba(255,255,255,0.1);
  border-radius: 2px;
  margin-top: 8px;
  overflow: hidden;
}
.metric-bar-fill {
  height: 100%;
  background: var(--ocre-light);
  border-radius: 2px;
  transition: width 0.4s ease;
}

/* ── TABS ── */
.tabs-bar {
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: 0 2px 8px rgba(28,18,8,0.06);
}
.tabs-inner {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 1.25rem;
  display: flex;
  gap: 0;
  overflow-x: auto;
  scrollbar-width: none;
}
.tabs-inner::-webkit-scrollbar { display: none; }
.tab {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 13px 18px;
  border: none;
  background: none;
  cursor: pointer;
  color: var(--text-3);
  border-bottom: 2px solid transparent;
  margin-bottom: -1px;
  white-space: nowrap;
  transition: color 0.15s, border-color 0.15s;
}
.tab:hover { color: var(--text-2); }
.tab.active {
  color: var(--terra-700);
  border-bottom-color: var(--ocre);
  font-weight: 500;
}

/* ── PANEL ── */
.panel { display: none; padding: 1.75rem 0; }
.panel.active { display: block; }

/* ── SECTION TITLE ── */
.section-title {
  font-family: 'Playfair Display', serif;
  font-size: 15px;
  font-weight: 600;
  color: var(--terra-700);
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.section-title::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border-lt);
}

/* ── LEGEND ── */
.legend {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  margin-bottom: 14px;
}
.legend-item {
  display: flex;
  align-items: center;
  gap: 6px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-3);
}
.legend-dot {
  width: 10px; height: 10px;
  border-radius: 2px;
  flex-shrink: 0;
}

/* ── VOLUME GRID ── */
.vol-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(88px, 1fr));
  gap: 8px;
  margin-bottom: 1.75rem;
}
.vol-card {
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  padding: 11px 8px;
  cursor: pointer;
  text-align: center;
  position: relative;
  transition: border-color 0.15s, transform 0.1s, box-shadow 0.15s;
  background: var(--surface);
}
.vol-card:hover {
  border-color: var(--terra-400);
  transform: translateY(-1px);
  box-shadow: 0 3px 10px rgba(28,18,8,0.1);
}
.vol-card.lido { background: var(--ok-bg); border-color: var(--ok-bd); }
.vol-card.parcial { background: var(--grave-bg); border-color: var(--grave-bd); }
.vol-card.critico { background: var(--critico-bg); border-color: var(--critico-bd); }
.vol-card.pendente { background: var(--surface); }
.vol-num {
  font-family: 'Playfair Display', serif;
  font-size: 15px;
  font-weight: 600;
  color: var(--text);
}
.vol-status {
  font-family: 'JetBrains Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text-3);
  margin-top: 4px;
}
.vol-flag {
  position: absolute; top: 5px; right: 5px;
  width: 7px; height: 7px; border-radius: 50%;
}
.flag-ok { background: var(--ok-text); }
.flag-warn { background: var(--grave); }
.flag-danger { background: var(--critico); }

/* ── CARDS & FORMS ── */
.card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: 18px 20px;
  margin-bottom: 1.25rem;
}
.card-title {
  font-family: 'Playfair Display', serif;
  font-size: 14px;
  font-weight: 600;
  color: var(--terra-700);
  margin-bottom: 14px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border-lt);
}
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 12px; }
.form-row.full { grid-template-columns: 1fr; }
.form-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--text-3);
  margin-bottom: 5px;
  display: block;
}
input[type=text], select, textarea {
  width: 100%;
  font-family: 'Source Serif 4', serif;
  font-size: 13px;
  color: var(--text);
  background: var(--areia-50);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 8px 10px;
  outline: none;
  transition: border-color 0.15s, background 0.15s;
  appearance: none;
}
input[type=text]:focus, select:focus, textarea:focus {
  border-color: var(--terra-400);
  background: #fff;
}
textarea { min-height: 75px; resize: vertical; line-height: 1.5; }
select { background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6'%3E%3Cpath d='M0 0l5 6 5-6z' fill='%236B4423'/%3E%3C/svg%3E"); background-repeat: no-repeat; background-position: right 10px center; padding-right: 28px; cursor: pointer; }

/* ── BUTTONS ── */
.btn {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.07em;
  text-transform: uppercase;
  padding: 9px 18px;
  border-radius: var(--radius-md);
  cursor: pointer;
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text-2);
  transition: background 0.15s, border-color 0.15s;
}
.btn:hover { background: var(--areia-100); border-color: var(--terra-300); }
.btn-primary {
  background: var(--terra-700);
  color: var(--areia-100);
  border-color: var(--terra-700);
}
.btn-primary:hover { background: var(--terra-600); border-color: var(--terra-600); }
.btn-sm { padding: 6px 12px; font-size: 10px; }
.link-btn {
  background: none;
  border: none;
  cursor: pointer;
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.05em;
  color: var(--ocre-dark);
  padding: 2px 0;
  display: inline-flex;
  align-items: center;
  gap: 4px;
  text-decoration: underline;
  text-decoration-style: dotted;
  text-underline-offset: 3px;
  transition: color 0.15s;
}
.link-btn:hover { color: var(--terra-600); }

/* ── BADGES ── */
.badge {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  padding: 3px 9px;
  border-radius: var(--radius-sm);
  font-weight: 500;
  white-space: nowrap;
  border: 1px solid transparent;
}
.badge-danger { background: var(--critico-bg); color: var(--critico); border-color: var(--critico-bd); }
.badge-warn { background: var(--grave-bg); color: var(--grave); border-color: var(--grave-bd); }
.badge-info { background: var(--relevante-bg); color: var(--relevante); border-color: var(--relevante-bd); }

/* ── VÍCIO ITEMS ── */
.vicio-list { display: flex; flex-direction: column; gap: 10px; margin-bottom: 1.25rem; }
.vicio-item {
  background: var(--surface);
  border: 1px solid var(--border);
  border-left: 3px solid var(--border);
  border-radius: var(--radius-md);
  padding: 14px 16px;
  transition: border-color 0.15s;
}
.vicio-item[data-grav="critico"] { border-left-color: var(--critico); }
.vicio-item[data-grav="grave"] { border-left-color: var(--grave); }
.vicio-item[data-grav="relevante"] { border-left-color: var(--relevante); }
.vicio-header { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; flex-wrap: wrap; }
.vicio-tipo { font-size: 13px; font-weight: 600; color: var(--text); font-family: 'Source Serif 4', serif; }
.vicio-desc { font-size: 13px; color: var(--text-2); line-height: 1.6; font-style: italic; }
.vicio-ref {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  color: var(--text-4);
  margin-top: 8px;
  padding-top: 8px;
  border-top: 1px solid var(--border-lt);
  letter-spacing: 0.03em;
}

/* ── CHECKLIST ── */
.checklist { display: flex; flex-direction: column; gap: 7px; }
.check-item {
  display: flex; align-items: flex-start; gap: 12px;
  padding: 11px 14px;
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  background: var(--surface);
  cursor: pointer;
  transition: background 0.15s, border-color 0.15s;
}
.check-item:hover { background: var(--areia-100); }
.check-item.done { background: var(--ok-bg); border-color: var(--ok-bd); }
.check-icon {
  width: 19px; height: 19px; min-width: 19px;
  border: 1.5px solid var(--border);
  border-radius: 3px;
  display: flex; align-items: center; justify-content: center;
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  margin-top: 1px;
  color: transparent;
  transition: background 0.15s, border-color 0.15s, color 0.15s;
}
.check-item.done .check-icon {
  background: var(--ok-text);
  border-color: var(--ok-text);
  color: white;
}
.check-text { font-size: 13px; color: var(--text); line-height: 1.5; }
.check-sub {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  color: var(--text-4);
  margin-top: 3px;
  letter-spacing: 0.04em;
}

/* ── STRATEGY GRID ── */
.two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1rem; }
.strategy-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: 16px 18px;
  display: flex;
  flex-direction: column;
}
.strategy-card h3 {
  font-family: 'Playfair Display', serif;
  font-size: 14px;
  font-weight: 600;
  color: var(--terra-700);
  margin-bottom: 12px;
  padding-bottom: 9px;
  border-bottom: 1px solid var(--border-lt);
}
.strategy-item {
  font-size: 12.5px;
  color: var(--text-2);
  padding: 7px 0;
  border-bottom: 1px solid var(--border-lt);
  line-height: 1.55;
}
.strategy-item:last-of-type { border-bottom: none; }
.divider { height: 1px; background: var(--border-lt); margin: 1.25rem 0; }

/* ── NOTAS ── */
.note-area {
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  padding: 12px 14px;
  font-family: 'Source Serif 4', serif;
  font-size: 13px;
  width: 100%;
  min-height: 140px;
  background: var(--areia-50);
  color: var(--text);
  resize: vertical;
  line-height: 1.6;
  outline: none;
  transition: border-color 0.15s;
}
.note-area:focus { border-color: var(--terra-400); background: #fff; }

/* ── VOL DETAIL ── */
.vol-detail-panel {
  display: none;
  background: var(--surface2);
  border: 1px solid var(--border);
  border-left: 3px solid var(--ocre);
  border-radius: var(--radius-lg);
  padding: 18px 20px;
  margin-bottom: 1.25rem;
}

/* ── FOOTER BAND ── */
.footer-band {
  background: var(--terra-900);
  text-align: center;
  padding: 16px;
  margin-top: 3rem;
}
.footer-band p {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--terra-400);
}

/* ── RESPONSIVE ── */
@media(max-width: 640px) {
  .metrics-band-inner { grid-template-columns: repeat(2, 1fr); }
  .two-col { grid-template-columns: 1fr; }
  .form-row { grid-template-columns: 1fr; }
  .masthead-title { font-size: 18px; }
}
</style>
</head>
<body>

<!-- MASTHEAD -->
<header class="masthead">
  <div class="masthead-inner">
    <div class="masthead-left">
      <div class="masthead-eyebrow">Dossiê Jurídico · Licenciamento Ambiental · Terras Indígenas</div>
      <div class="masthead-title" id="case-name-display">PCH em <span>Território Indígena</span></div>
      <div class="masthead-sub">Análise de vícios · Amicus Curiae · MPF como autor da ação</div>
    </div>
    <div class="masthead-right">
      <input class="masthead-input" type="text" id="case-name-input" placeholder="Identificar o caso..." oninput="document.getElementById('case-name-display').innerHTML=this.value?('PCH em <span>'+this.value+'</span>'):'PCH em <span>Território Indígena</span>'">
      <button class="btn-resumo" onclick="window.open('https://claude.ai','_blank')">Resumo ↗</button>
    </div>
  </div>
</header>

<!-- METRICS BAND -->
<div class="metrics-band">
  <div class="metrics-band-inner">
    <div class="metric-cell">
      <div class="metric-cell-label">Volumes totais</div>
      <div class="metric-cell-val">20</div>
      <div class="metric-cell-sub">75 arquivos · ~300 p. cada</div>
    </div>
    <div class="metric-cell">
      <div class="metric-cell-label">Lidos</div>
      <div class="metric-cell-val" id="m-lidos">0</div>
      <div class="metric-cell-sub" id="m-lidos-pct">0% concluído</div>
      <div class="metric-bar"><div class="metric-bar-fill" id="prog-lidos" style="width:0%"></div></div>
    </div>
    <div class="metric-cell">
      <div class="metric-cell-label">Vícios registrados</div>
      <div class="metric-cell-val" id="m-vicios">3</div>
      <div class="metric-cell-sub">fundamentos mapeados</div>
    </div>
    <div class="metric-cell">
      <div class="metric-cell-label">Checklist</div>
      <div class="metric-cell-val" id="m-check">0%</div>
      <div class="metric-cell-sub">verificações concluídas</div>
      <div class="metric-bar"><div class="metric-bar-fill" id="prog-check" style="width:0%"></div></div>
    </div>
  </div>
</div>

<!-- TABS -->
<div class="tabs-bar">
  <div class="tabs-inner">
    <button class="tab active" onclick="switchTab('volumes',this)">I. Volumes</button>
    <button class="tab" onclick="switchTab('vicios',this)">II. Vícios</button>
    <button class="tab" onclick="switchTab('checklist',this)">III. Checklist</button>
    <button class="tab" onclick="switchTab('estrategia',this)">IV. Estratégia</button>
    <button class="tab" onclick="switchTab('campo',this)">V. Campo</button>
    <button class="tab" onclick="switchTab('notas',this)">VI. Notas</button>
  </div>
</div>

<div class="page">

  <!-- VOLUMES -->
  <div id="tab-volumes" class="panel active">
    <div class="legend">
      <span class="legend-item"><span class="legend-dot" style="background:var(--ok-text)"></span>Lido</span>
      <span class="legend-item"><span class="legend-dot" style="background:var(--grave)"></span>Parcial</span>
      <span class="legend-item"><span class="legend-dot" style="background:var(--critico)"></span>Vícios críticos</span>
      <span class="legend-item"><span class="legend-dot" style="background:var(--border)"></span>Pendente</span>
    </div>
    <div class="vol-grid" id="vol-grid"></div>
    <div id="vol-detail" class="vol-detail-panel">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:14px;">
        <div class="section-title" style="margin:0;font-size:14px;" id="vol-detail-title">Volume 1</div>
        <button class="btn btn-sm" onclick="document.getElementById('vol-detail').style.display='none'">Fechar</button>
      </div>
      <div class="form-row">
        <div><label class="form-label">Status</label>
          <select id="vol-status-sel">
            <option value="pendente">Pendente</option>
            <option value="parcial">Leitura parcial</option>
            <option value="lido">Lido integralmente</option>
            <option value="critico">Crítico — vícios identificados</option>
          </select>
        </div>
        <div><label class="form-label">Arquivos neste volume</label>
          <input type="text" id="vol-files" placeholder="Ex: arq. 01 a 04">
        </div>
      </div>
      <div class="form-row full">
        <div><label class="form-label">Observações e páginas relevantes</label>
          <textarea id="vol-obs" placeholder="Notas, páginas relevantes, vícios identificados, referências cruzadas..."></textarea>
        </div>
      </div>
      <button class="btn btn-primary" onclick="saveVol()">Salvar registro</button>
    </div>
  </div>

  <!-- VÍCIOS -->
  <div id="tab-vicios" class="panel">
    <div class="card">
      <div class="card-title">Registrar vício ou irregularidade</div>
      <div class="form-row">
        <div><label class="form-label">Tipo de vício</label>
          <select id="v-tipo">
            <option>Ausência de consulta prévia (Conv. 169 OIT)</option>
            <option>EIA/RIMA irregular ou insuficiente</option>
            <option>Impacto zero indevido (afastamento de campo)</option>
            <option>Vício de competência (SEMA/IBAMA)</option>
            <option>Licença concedida sem anuência Funai</option>
            <option>Violação do art. 231 CF/88</option>
            <option>Ausência de estudo prévio de impacto</option>
            <option>Contraditório prejudicado</option>
            <option>Outro</option>
          </select>
        </div>
        <div><label class="form-label">Gravidade jurídica</label>
          <select id="v-grav">
            <option value="critico">Crítico — nulidade absoluta</option>
            <option value="grave">Grave — anulabilidade</option>
            <option value="relevante">Relevante — irregularidade</option>
          </select>
        </div>
      </div>
      <div class="form-row">
        <div><label class="form-label">Volume / Arquivo / Página</label>
          <input type="text" id="v-ref" placeholder="Vol. 3, Arq. 12, p. 45">
        </div>
        <div><label class="form-label">Fundamento jurídico</label>
          <input type="text" id="v-fund" placeholder="Art. 6º Conv. 169 OIT; art. 231 CF">
        </div>
      </div>
      <div class="form-row full">
        <div><label class="form-label">Descrição fundamentada do vício</label>
          <textarea id="v-desc" placeholder="Descreva o vício, como foi identificado, consequências processuais e impacto para as comunidades indígenas..."></textarea>
        </div>
      </div>
      <div style="display:flex;gap:10px;align-items:center;flex-wrap:wrap;">
        <button class="btn btn-primary" onclick="addVicio()">Registrar vício</button>
        <button class="link-btn" onclick="window.open('https://claude.ai','_blank')">Analisar fundamento ↗</button>
      </div>
    </div>
    <div class="section-title">Vícios registrados</div>
    <div class="vicio-list" id="vicio-list"></div>
  </div>

  <!-- CHECKLIST -->
  <div id="tab-checklist" class="panel">
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1rem;flex-wrap:wrap;gap:8px;">
      <div class="section-title" style="margin:0;">Verificação jurídica obrigatória</div>
      <button class="link-btn" onclick="window.open('https://claude.ai','_blank')">Complementar lista ↗</button>
    </div>
    <div class="checklist" id="checklist"></div>
  </div>

  <!-- ESTRATÉGIA -->
  <div id="tab-estrategia" class="panel">
    <div class="two-col">
      <div class="strategy-card">
        <h3>Teses principais — amicus curiae</h3>
        <div class="strategy-item">Nulidade do licenciamento por ausência de consulta livre, prévia e informada (art. 6º Conv. 169 OIT + art. 231 §3º CF)</div>
        <div class="strategy-item">Impacto zero como fraude instrumental: afastamento ilegítimo de EIA de campo (Lei 6.938/81; Res. CONAMA 001/86)</div>
        <div class="strategy-item">Incompetência da SEMA: empreendimento com impacto em TI exige IBAMA + Funai (LC 140/2011; IN Funai 02/2015)</div>
        <div class="strategy-item">Violação do direito ao território e usufruto exclusivo (art. 231 §2º CF; Dec. 5.051/2004)</div>
        <div class="strategy-item">Dano socioambiental irreversível — princípio da precaução e inversão do ônus da prova</div>
        <button class="link-btn" style="margin-top:12px;" onclick="window.open('https://claude.ai','_blank')">Expandir argumentação ↗</button>
      </div>
      <div class="strategy-card">
        <h3>Pedidos para o amicus curiae</h3>
        <div class="strategy-item">Declaração de nulidade absoluta do licenciamento ambiental concedido pela SEMA</div>
        <div class="strategy-item">Suspensão imediata das atividades da PCH (tutela de urgência)</div>
        <div class="strategy-item">Determinação de EIA completo com trabalho de campo e participação indígena</div>
        <div class="strategy-item">Realização de consulta prévia conforme protocolo comunitário do povo afetado</div>
        <div class="strategy-item">Reparação integral dos danos socioambientais (dano material + moral coletivo)</div>
        <div class="strategy-item">Responsabilização solidária do empreendedor e do Estado (SEMA)</div>
        <button class="link-btn" style="margin-top:12px;" onclick="window.open('https://claude.ai','_blank')">Minutar pedidos ↗</button>
      </div>
    </div>
    <div class="divider"></div>
    <div class="two-col">
      <div class="strategy-card">
        <h3>Provas a requerer</h3>
        <div class="strategy-item">Depoimentos dos povos indígenas (já em coleta em campo)</div>
        <div class="strategy-item">Perícia ambiental independente na área da PCH e TI</div>
        <div class="strategy-item">Juntada integral do processo administrativo (SEMA)</div>
        <div class="strategy-item">Documentação da Funai sobre consulta e anuência</div>
        <div class="strategy-item">Laudos antropológicos e etnobotânicos</div>
        <div class="strategy-item">Histórico de alterações no estudo de impacto</div>
        <button class="link-btn" style="margin-top:12px;" onclick="window.open('https://claude.ai','_blank')">Detalhes da perícia ↗</button>
      </div>
      <div class="strategy-card">
        <h3>Jurisprudência prioritária</h3>
        <div class="strategy-item">STF — RE 466.343 (consulta prévia e Conv. 169)</div>
        <div class="strategy-item">STJ — REsp 1.797.175 (dano ambiental em TI)</div>
        <div class="strategy-item">TRF-1 — processos de PCH em TI na Amazônia</div>
        <div class="strategy-item">CIDH — caso Saramaka vs. Suriname</div>
        <div class="strategy-item">Corte IDH — caso Povo Sarayaku vs. Equador</div>
        <div class="strategy-item">ADPF 709 (STF — direitos territoriais indígenas)</div>
        <button class="link-btn" style="margin-top:12px;" onclick="window.open('https://claude.ai','_blank')">Pesquisar jurisprudência ↗</button>
      </div>
    </div>
  </div>

  <!-- CAMPO -->
  <div id="tab-campo" class="panel">
    <div class="card">
      <div class="card-title">Registrar relato de campo</div>
      <div class="form-row">
        <div><label class="form-label">Comunidade / Liderança</label>
          <input type="text" id="c-pessoa" placeholder="Nome ou cargo">
        </div>
        <div><label class="form-label">Data do depoimento</label>
          <input type="text" id="c-data" placeholder="DD/MM/AAAA">
        </div>
      </div>
      <div class="form-row full">
        <div><label class="form-label">Conteúdo do depoimento / anseios expressos</label>
          <textarea id="c-dep" placeholder="Registre o que foi dito, o que o povo indígena espera, impactos relatados, linguagem e termos usados..."></textarea>
        </div>
      </div>
      <div class="form-row">
        <div><label class="form-label">Impactos relatados</label>
          <input type="text" id="c-imp" placeholder="Pesca, território, saúde, rituais...">
        </div>
        <div><label class="form-label">Posicionamento sobre a PCH</label>
          <select id="c-pos">
            <option>Contrário — quer paralisação imediata</option>
            <option>Contrário — quer reparação integral</option>
            <option>Condicionado — exige consulta prévia</option>
            <option>Não informado</option>
          </select>
        </div>
      </div>
      <div style="display:flex;gap:10px;align-items:center;flex-wrap:wrap;">
        <button class="btn btn-primary" onclick="addRelato()">Salvar relato</button>
        <button class="link-btn" onclick="window.open('https://claude.ai','_blank')">Orientação probatória ↗</button>
      </div>
    </div>
    <div class="section-title">Relatos coletados</div>
    <div id="relatos-list" style="display:flex;flex-direction:column;gap:10px;"></div>
  </div>

  <!-- NOTAS -->
  <div id="tab-notas" class="panel">
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1rem;flex-wrap:wrap;gap:8px;">
      <div class="section-title" style="margin:0;">Notas jurídicas</div>
      <button class="link-btn" onclick="window.open('https://claude.ai','_blank')">Como peticionar ↗</button>
    </div>
    <textarea class="note-area" id="notas-text" placeholder="Anotações gerais, hipóteses jurídicas, pontos de atenção, cronograma, articulações estratégicas..."></textarea>
    <div style="margin-top:10px;display:flex;gap:10px;align-items:center;flex-wrap:wrap;">
      <button class="btn btn-primary" onclick="saveNota()">Salvar nota</button>
      <button class="link-btn" onclick="window.open('https://claude.ai','_blank')">Estruturar petição ↗</button>
    </div>
    <div style="margin-top:1.25rem;" id="notas-saved"></div>
  </div>

</div><!-- /page -->

<div class="footer-band">
  <p>Dossiê jurídico — uso interno restrito — PCH em território indígena</p>
</div>

<script>
const state = {
  volumes: Array.from({length:20}, (_,i)=>({num:i+1, status:'pendente', files:'', obs:''})),
  vicios: [
    {tipo:'Impacto zero indevido (afastamento de campo)', grav:'critico', ref:'Vol. 1, Arq. 2, p. 18', fund:'Res. CONAMA 001/86; Lei 6.938/81', desc:'EIA declarou impacto zero para afastar obrigação de pesquisa de campo, em aparente fraude instrumental para viabilizar licença sem estudo de campo junto às comunidades indígenas.'},
    {tipo:'Ausência de consulta prévia (Conv. 169 OIT)', grav:'critico', ref:'Processo adm. SEMA', fund:'Art. 6º Conv. 169 OIT; Art. 231 §3º CF/88', desc:'Não há qualquer registro de consulta livre, prévia e informada aos povos indígenas afetados antes da emissão da licença. A anuência foi presumida sem participação efetiva.'},
    {tipo:'Vício de competência (SEMA/IBAMA)', grav:'grave', ref:'Licença nº — Vol. 2', fund:'LC 140/2011; IN Funai 02/2015', desc:'Empreendimento com impacto direto em terra indígena demanda licenciamento pelo IBAMA com participação da Funai. A SEMA não tem competência para licenciar neste caso.'},
  ],
  checklist: [
    {texto:'Verificar competência do órgão licenciador (SEMA vs. IBAMA + Funai)', sub:'LC 140/2011; IN Funai 02/2015', done:false},
    {texto:'Confirmar ausência/irregularidade da consulta prévia (Conv. 169 OIT)', sub:'Art. 6º; livre, prévia e informada', done:false},
    {texto:'Analisar o EIA/RIMA — impacto zero e ausência de campo', sub:'Res. CONAMA 001/86 e 237/97', done:false},
    {texto:'Mapear todos os atos autorizativos expedidos pela SEMA', sub:'Licenças prévia, instalação, operação', done:false},
    {texto:'Verificar participação da Funai e da SESAI no processo', sub:'Obrigatoriedade de manifestação', done:false},
    {texto:'Identificar se houve audiência pública — convocação e realização', sub:'Art. 11 Res. CONAMA 009/87', done:false},
    {texto:'Confirmar demarcação e status jurídico da TI afetada', sub:'Decreto homologatório; estágio', done:false},
    {texto:'Levantar laudos antropológicos juntados ou omitidos', sub:'Necessidade de laudo independente', done:false},
    {texto:'Verificar alterações no EIA após concessão da licença', sub:'Possível fraude documental', done:false},
    {texto:'Inventariar depoimentos coletados em campo (colega)', sub:'Coordenar com trabalho de campo', done:false},
    {texto:'Pesquisar jurisprudência: STF, STJ, TRF-1 sobre PCH em TI', sub:'ADPF 709; Conv. 169; art. 231 CF', done:false},
    {texto:'Elaborar minuta da petição de amicus curiae', sub:'Requisitos; prazo; admissibilidade', done:false},
    {texto:'Sistematizar todos os vícios em quadro-resumo', sub:'Para instrução da peça processual', done:false},
    {texto:'Verificar existência de TAC ou acordos extrajudiciais', sub:'Possível fraude à lei ou ao processo', done:false},
  ],
  relatos: [],
  notas: [],
  selectedVol: null,
};

function switchTab(id, el) {
  document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));
  document.getElementById('tab-'+id).classList.add('active');
  el.classList.add('active');
}

function renderVolumes() {
  const grid = document.getElementById('vol-grid');
  grid.innerHTML = '';
  let lidos = 0;
  state.volumes.forEach(v=>{
    if(v.status==='lido') lidos++;
    const d = document.createElement('div');
    d.className = 'vol-card '+(v.status||'pendente');
    let flag = '';
    if(v.status==='critico') flag='<div class="vol-flag flag-danger"></div>';
    else if(v.status==='parcial') flag='<div class="vol-flag flag-warn"></div>';
    else if(v.status==='lido') flag='<div class="vol-flag flag-ok"></div>';
    const statusLabel = {pendente:'pendente',lido:'lido',parcial:'parcial',critico:'crítico'}[v.status]||'pendente';
    d.innerHTML = flag+'<div class="vol-num">Vol. '+v.num+'</div><div class="vol-status">'+statusLabel+'</div>';
    d.onclick = ()=>openVol(v.num);
    grid.appendChild(d);
  });
  const pct = Math.round(lidos/20*100);
  document.getElementById('m-lidos').textContent = lidos;
  document.getElementById('m-lidos-pct').textContent = pct+'% concluído';
  document.getElementById('prog-lidos').style.width = pct+'%';
}

function openVol(num) {
  state.selectedVol = num;
  const v = state.volumes[num-1];
  document.getElementById('vol-detail-title').textContent = 'Volume '+num;
  document.getElementById('vol-status-sel').value = v.status||'pendente';
  document.getElementById('vol-files').value = v.files||'';
  document.getElementById('vol-obs').value = v.obs||'';
  const panel = document.getElementById('vol-detail');
  panel.style.display = 'block';
  panel.scrollIntoView({behavior:'smooth',block:'nearest'});
}

function saveVol() {
  const v = state.volumes[state.selectedVol-1];
  v.status = document.getElementById('vol-status-sel').value;
  v.files = document.getElementById('vol-files').value;
  v.obs = document.getElementById('vol-obs').value;
  document.getElementById('vol-detail').style.display = 'none';
  renderVolumes();
}

function renderVicios() {
  const list = document.getElementById('vicio-list');
  list.innerHTML = '';
  state.vicios.forEach(v=>{
    const gravClass = v.grav==='critico'?'badge-danger':v.grav==='grave'?'badge-warn':'badge-info';
    const gravLabel = v.grav==='critico'?'Crítico — nulidade':v.grav==='grave'?'Grave — anulabilidade':'Relevante';
    const el = document.createElement('div');
    el.className = 'vicio-item';
    el.setAttribute('data-grav', v.grav);
    el.innerHTML = '<div class="vicio-header"><span class="badge '+gravClass+'">'+gravLabel+'</span><span class="vicio-tipo">'+v.tipo+'</span></div><div class="vicio-desc">'+v.desc+'</div><div class="vicio-ref">Ref.: '+v.ref+' &nbsp;·&nbsp; '+v.fund+'</div>';
    list.appendChild(el);
  });
  document.getElementById('m-vicios').textContent = state.vicios.length;
}

function addVicio() {
  const v = {
    tipo: document.getElementById('v-tipo').value,
    grav: document.getElementById('v-grav').value,
    ref: document.getElementById('v-ref').value||'Não informado',
    fund: document.getElementById('v-fund').value||'—',
    desc: document.getElementById('v-desc').value||'Sem descrição.'
  };
  state.vicios.unshift(v);
  document.getElementById('v-ref').value='';
  document.getElementById('v-fund').value='';
  document.getElementById('v-desc').value='';
  renderVicios();
}

function renderChecklist() {
  const list = document.getElementById('checklist');
  list.innerHTML = '';
  let done = 0;
  state.checklist.forEach((item)=>{
    if(item.done) done++;
    const el = document.createElement('div');
    el.className = 'check-item'+(item.done?' done':'');
    el.innerHTML = '<div class="check-icon">'+(item.done?'✓':'')+'</div><div><div class="check-text">'+item.texto+'</div><div class="check-sub">'+item.sub+'</div></div>';
    el.onclick = ()=>{item.done=!item.done;renderChecklist();};
    list.appendChild(el);
  });
  const pct = Math.round(done/state.checklist.length*100);
  document.getElementById('m-check').textContent = pct+'%';
  document.getElementById('prog-check').style.width = pct+'%';
}

function addRelato() {
  const r = {
    pessoa: document.getElementById('c-pessoa').value||'Não identificado',
    data: document.getElementById('c-data').value||'—',
    dep: document.getElementById('c-dep').value||'',
    imp: document.getElementById('c-imp').value||'—',
    pos: document.getElementById('c-pos').value,
  };
  state.relatos.unshift(r);
  ['c-pessoa','c-data','c-dep','c-imp'].forEach(id=>document.getElementById(id).value='');
  renderRelatos();
}

function renderRelatos() {
  const list = document.getElementById('relatos-list');
  list.innerHTML='';
  if(!state.relatos.length){
    list.innerHTML='<div style="font-size:13px;color:var(--text-4);font-style:italic;">Nenhum relato registrado ainda.</div>';
    return;
  }
  state.relatos.forEach(r=>{
    const el = document.createElement('div');
    el.className='vicio-item';
    el.setAttribute('data-grav','relevante');
    el.innerHTML='<div class="vicio-header"><span class="badge badge-info">'+r.data+'</span><span class="vicio-tipo">'+r.pessoa+'</span></div><div class="vicio-desc">'+r.dep+'</div><div class="vicio-ref">Impactos: '+r.imp+' &nbsp;·&nbsp; Posição: '+r.pos+'</div>';
    list.appendChild(el);
  });
}

function saveNota() {
  const txt = document.getElementById('notas-text').value.trim();
  if(!txt) return;
  state.notas.unshift({txt, date: new Date().toLocaleDateString('pt-BR')});
  document.getElementById('notas-text').value='';
  renderNotas();
}

function renderNotas() {
  const list = document.getElementById('notas-saved');
  list.innerHTML='';
  state.notas.forEach(n=>{
    const el = document.createElement('div');
    el.className='vicio-item';
    el.setAttribute('data-grav','relevante');
    el.innerHTML='<div class="vicio-ref" style="margin-bottom:6px;">'+n.date+'</div><div class="vicio-desc" style="font-style:normal;">'+n.txt+'</div>';
    list.appendChild(el);
  });
}

renderVolumes();
renderVicios();
renderChecklist();
renderRelatos();
</script>
</body>
</html>
