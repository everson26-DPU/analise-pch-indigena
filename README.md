# analise-pch-indigena
Relatório jurídico sobre licenciamento ambiental e terras indígenas


<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: var(--font-sans); }
:root {
  --c-danger: var(--color-background-danger);
  --t-danger: var(--color-text-danger);
  --c-warn: var(--color-background-warning);
  --t-warn: var(--color-text-warning);
  --c-ok: var(--color-background-success);
  --t-ok: var(--color-text-success);
  --c-info: var(--color-background-info);
  --t-info: var(--color-text-info);
}
.wrap { padding: 1rem 0; }
.header { margin-bottom: 1.5rem; }
.case-title { font-size: 18px; font-weight: 500; color: var(--color-text-primary); }
.case-sub { font-size: 13px; color: var(--color-text-secondary); margin-top: 4px; }
.tabs { display: flex; gap: 4px; border-bottom: 0.5px solid var(--color-border-tertiary); margin-bottom: 1.25rem; flex-wrap: wrap; }
.tab { padding: 7px 14px; font-size: 13px; border: none; background: none; cursor: pointer; color: var(--color-text-secondary); border-bottom: 2px solid transparent; margin-bottom: -0.5px; }
.tab.active { color: var(--color-text-primary); border-bottom-color: var(--color-text-primary); font-weight: 500; }
.panel { display: none; }
.panel.active { display: block; }
.metrics { display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 10px; margin-bottom: 1.25rem; }
.metric { background: var(--color-background-secondary); border-radius: var(--border-radius-md); padding: 12px 14px; }
.metric-label { font-size: 12px; color: var(--color-text-secondary); margin-bottom: 6px; }
.metric-val { font-size: 22px; font-weight: 500; color: var(--color-text-primary); }
.metric-sub { font-size: 11px; color: var(--color-text-secondary); margin-top: 3px; }
.progress-bar { height: 4px; background: var(--color-border-tertiary); border-radius: 2px; margin-top: 8px; }
.progress-fill { height: 100%; border-radius: 2px; background: var(--color-text-primary); transition: width 0.3s; }
.section-title { font-size: 14px; font-weight: 500; color: var(--color-text-primary); margin-bottom: 10px; }
.vol-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(90px, 1fr)); gap: 8px; margin-bottom: 1.5rem; }
.vol-card { border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 10px 8px; cursor: pointer; text-align: center; position: relative; transition: border-color 0.15s; }
.vol-card:hover { border-color: var(--color-border-secondary); }
.vol-card.lido { background: var(--color-background-success); border-color: var(--color-border-tertiary); }
.vol-card.parcial { background: var(--color-background-warning); }
.vol-card.critico { background: var(--color-background-danger); }
.vol-card.pendente { background: var(--color-background-primary); }
.vol-num { font-size: 13px; font-weight: 500; color: var(--color-text-primary); }
.vol-status { font-size: 10px; color: var(--color-text-secondary); margin-top: 3px; }
.vol-flag { position: absolute; top: 5px; right: 5px; width: 7px; height: 7px; border-radius: 50%; }
.flag-ok { background: var(--color-text-success); }
.flag-warn { background: var(--color-text-warning); }
.flag-danger { background: var(--color-text-danger); }
.vicio-list { display: flex; flex-direction: column; gap: 8px; margin-bottom: 1.25rem; }
.vicio-item { border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 12px 14px; background: var(--color-background-primary); }
.vicio-header { display: flex; align-items: center; gap: 10px; margin-bottom: 6px; flex-wrap: wrap; }
.badge { font-size: 11px; padding: 3px 9px; border-radius: var(--border-radius-md); font-weight: 500; white-space: nowrap; }
.badge-danger { background: var(--color-background-danger); color: var(--color-text-danger); }
.badge-warn { background: var(--color-background-warning); color: var(--color-text-warning); }
.badge-info { background: var(--color-background-info); color: var(--color-text-info); }
.vicio-desc { font-size: 13px; color: var(--color-text-secondary); line-height: 1.5; }
.vicio-ref { font-size: 11px; color: var(--color-text-tertiary); margin-top: 5px; }
.add-form { border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 14px; margin-bottom: 1.25rem; background: var(--color-background-secondary); }
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 10px; }
.form-row.full { grid-template-columns: 1fr; }
.form-label { font-size: 12px; color: var(--color-text-secondary); margin-bottom: 4px; }
input[type=text], select, textarea { width: 100%; font-size: 13px; }
textarea { min-height: 70px; resize: vertical; }
.btn { padding: 8px 16px; font-size: 13px; border: 0.5px solid var(--color-border-secondary); border-radius: var(--border-radius-md); cursor: pointer; background: var(--color-background-primary); color: var(--color-text-primary); }
.btn:hover { background: var(--color-background-secondary); }
.btn-primary { background: var(--color-text-primary); color: var(--color-background-primary); border-color: var(--color-text-primary); }
.btn-primary:hover { opacity: 0.85; }
.btn-sm { padding: 5px 11px; font-size: 12px; }
.checklist { display: flex; flex-direction: column; gap: 6px; }
.check-item { display: flex; align-items: flex-start; gap: 10px; padding: 10px 12px; border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); background: var(--color-background-primary); cursor: pointer; }
.check-item.done { background: var(--color-background-success); }
.check-icon { width: 18px; height: 18px; min-width: 18px; border: 0.5px solid var(--color-border-secondary); border-radius: 4px; display: flex; align-items: center; justify-content: center; font-size: 12px; margin-top: 1px; }
.check-item.done .check-icon { background: var(--color-text-success); border-color: var(--color-text-success); color: var(--color-background-primary); }
.check-text { font-size: 13px; color: var(--color-text-primary); line-height: 1.5; }
.check-sub { font-size: 11px; color: var(--color-text-secondary); margin-top: 2px; }
.note-area { border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 10px 12px; font-size: 13px; width: 100%; min-height: 120px; background: var(--color-background-primary); color: var(--color-text-primary); }
.two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
.strategy-card { border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 14px; background: var(--color-background-primary); }
.strategy-card h3 { font-size: 13px; font-weight: 500; color: var(--color-text-primary); margin-bottom: 10px; }
.strategy-item { font-size: 12px; color: var(--color-text-secondary); padding: 6px 0; border-bottom: 0.5px solid var(--color-border-tertiary); line-height: 1.5; }
.strategy-item:last-child { border-bottom: none; }
.send-btn { background: none; border: none; cursor: pointer; font-size: 13px; color: var(--color-text-info); padding: 2px 0; display: inline-flex; align-items: center; gap: 4px; }
.divider { height: 0.5px; background: var(--color-border-tertiary); margin: 1.25rem 0; }
@media(max-width: 600px) {
  .metrics { grid-template-columns: repeat(2, minmax(0,1fr)); }
  .two-col { grid-template-columns: 1fr; }
}
</style>

<div class="wrap">
  <div class="header">
    <div style="display:flex; align-items:flex-start; justify-content:space-between; flex-wrap:wrap; gap:10px;">
      <div>
        <div class="case-title" id="case-name-display">PCH em Território Indígena</div>
        <div class="case-sub">Análise jurídica · Amicus Curiae · MPF como autor</div>
      </div>
      <div style="display:flex;gap:6px;align-items:center;">
        <input type="text" id="case-name-input" placeholder="Nome do caso..." style="font-size:13px;width:200px;" oninput="document.getElementById('case-name-display').textContent=this.value||'PCH em Território Indígena'">
        <button class="btn btn-sm" onclick="sendPrompt('Gere um resumo executivo do caso PCH em terras indígenas com os principais argumentos jurídicos para amicus curiae')">Resumo ↗</button>
      </div>
    </div>
  </div>

  <div class="tabs">
    <button class="tab active" onclick="switchTab('volumes')">Volumes</button>
    <button class="tab" onclick="switchTab('vicios')">Vícios</button>
    <button class="tab" onclick="switchTab('checklist')">Checklist</button>
    <button class="tab" onclick="switchTab('estrategia')">Estratégia</button>
    <button class="tab" onclick="switchTab('campo')">Campo</button>
    <button class="tab" onclick="switchTab('notas')">Notas</button>
  </div>

  <div id="tab-volumes" class="panel active">
    <div class="metrics">
      <div class="metric">
        <div class="metric-label">Volumes totais</div>
        <div class="metric-val">20</div>
        <div class="metric-sub">75 arquivos</div>
      </div>
      <div class="metric">
        <div class="metric-label">Lidos</div>
        <div class="metric-val" id="m-lidos">0</div>
        <div class="metric-sub" id="m-lidos-pct">0%</div>
        <div class="progress-bar"><div class="progress-fill" id="prog-lidos" style="width:0%"></div></div>
      </div>
      <div class="metric">
        <div class="metric-label">Vícios encontrados</div>
        <div class="metric-val" id="m-vicios">3</div>
        <div class="metric-sub">registrados</div>
      </div>
      <div class="metric">
        <div class="metric-label">Checklist</div>
        <div class="metric-val" id="m-check">0%</div>
        <div class="metric-sub">concluído</div>
        <div class="progress-bar"><div class="progress-fill" id="prog-check" style="width:0%"></div></div>
      </div>
    </div>

    <div class="section-title">Progresso por volume</div>
    <div style="display:flex;gap:10px;flex-wrap:wrap;margin-bottom:10px;font-size:12px;color:var(--color-text-secondary);">
      <span style="display:flex;align-items:center;gap:5px;"><span style="width:10px;height:10px;background:var(--color-text-success);border-radius:2px;display:inline-block;"></span>Lido</span>
      <span style="display:flex;align-items:center;gap:5px;"><span style="width:10px;height:10px;background:var(--color-text-warning);border-radius:2px;display:inline-block;"></span>Parcial</span>
      <span style="display:flex;align-items:center;gap:5px;"><span style="width:10px;height:10px;background:var(--color-text-danger);border-radius:2px;display:inline-block;"></span>Vícios críticos</span>
      <span style="display:flex;align-items:center;gap:5px;"><span style="width:10px;height:10px;background:var(--color-border-secondary);border-radius:2px;display:inline-block;"></span>Pendente</span>
    </div>
    <div class="vol-grid" id="vol-grid"></div>

    <div id="vol-detail" style="display:none;" class="add-form">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:10px;">
        <div class="section-title" style="margin:0;" id="vol-detail-title">Volume 1</div>
        <button class="btn btn-sm" onclick="document.getElementById('vol-detail').style.display='none'">Fechar</button>
      </div>
      <div class="form-row">
        <div>
          <div class="form-label">Status</div>
          <select id="vol-status-sel">
            <option value="pendente">Pendente</option>
            <option value="parcial">Parcial</option>
            <option value="lido">Lido</option>
            <option value="critico">Crítico (vícios)</option>
          </select>
        </div>
        <div>
          <div class="form-label">Arquivos neste volume</div>
          <input type="text" id="vol-files" placeholder="Ex: 3-4 arquivos">
        </div>
      </div>
      <div class="form-row full">
        <div>
          <div class="form-label">Observações</div>
          <textarea id="vol-obs" placeholder="Notas, páginas relevantes, vícios identificados..."></textarea>
        </div>
      </div>
      <button class="btn btn-primary" onclick="saveVol()">Salvar</button>
    </div>
  </div>

  <div id="tab-vicios" class="panel">
    <div class="add-form">
      <div class="section-title" style="margin-bottom:12px;">Registrar vício ou irregularidade</div>
      <div class="form-row">
        <div>
          <div class="form-label">Tipo de vício</div>
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
        <div>
          <div class="form-label">Gravidade</div>
          <select id="v-grav">
            <option value="critico">Crítico — nulidade</option>
            <option value="grave">Grave — anulabilidade</option>
            <option value="relevante">Relevante — irregularidade</option>
          </select>
        </div>
      </div>
      <div class="form-row">
        <div>
          <div class="form-label">Volume / Arquivo / Página</div>
          <input type="text" id="v-ref" placeholder="Vol. 3, Arq. 12, p. 45">
        </div>
        <div>
          <div class="form-label">Fundamento jurídico</div>
          <input type="text" id="v-fund" placeholder="Art. 6º Conv. 169 OIT; art. 231 CF">
        </div>
      </div>
      <div class="form-row full">
        <div>
          <div class="form-label">Descrição do vício</div>
          <textarea id="v-desc" placeholder="Descreva o vício, como foi identificado e seu impacto para o processo..."></textarea>
        </div>
      </div>
      <div style="display:flex;gap:8px;">
        <button class="btn btn-primary" onclick="addVicio()">Registrar vício</button>
        <button class="send-btn" onclick="sendPrompt('Com base no seguinte vício identificado: ausência de consulta prévia (Convenção 169 OIT), quais são os argumentos jurídicos mais sólidos para invalidar o licenciamento da PCH?')">Analisar argumento ↗</button>
      </div>
    </div>

    <div class="section-title">Vícios registrados</div>
    <div class="vicio-list" id="vicio-list"></div>
  </div>

  <div id="tab-checklist" class="panel">
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;">
      <div class="section-title" style="margin:0;">Lista de verificação jurídica</div>
      <button class="send-btn" onclick="sendPrompt('Liste todos os documentos e procedimentos obrigatórios para licenciamento de PCH em terras indígenas no Brasil, incluindo Convenção 169 OIT, art. 231 CF/88, Lei 9.985/2000 e normas da ANEEL')">Complementar ↗</button>
    </div>
    <div class="checklist" id="checklist"></div>
  </div>

  <div id="tab-estrategia" class="panel">
    <div class="two-col">
      <div class="strategy-card">
        <h3>Teses principais — amicus curiae</h3>
        <div class="strategy-item">Nulidade do licenciamento por ausência de consulta livre, prévia e informada (art. 6º Conv. 169 OIT + art. 231 §3º CF)</div>
        <div class="strategy-item">Impacto zero como fraude instrumental: afastamento ilegítimo de EIA de campo (Lei 6.938/81; Res. CONAMA 001/86)</div>
        <div class="strategy-item">Incompetência da SEMA: empreendimento com impacto em TI exige IBAMA + Funai (LC 140/2011; IN Funai 02/2015)</div>
        <div class="strategy-item">Violação do direito ao território e usufruto exclusivo (art. 231 §2º CF; Dec. 5.051/2004)</div>
        <div class="strategy-item">Dano socioambiental irreversível — princípio da precaução e inversão do ônus da prova</div>
        <button class="send-btn" style="margin-top:10px;" onclick="sendPrompt('Elabore argumentação jurídica detalhada sobre a obrigatoriedade da consulta prévia aos povos indígenas no licenciamento de PCH, com base na Convenção 169 OIT, jurisprudência do STF e do STJ')">Expandir argumentação ↗</button>
      </div>
      <div class="strategy-card">
        <h3>Pedidos para o amicus curiae</h3>
        <div class="strategy-item">Declaração de nulidade absoluta do licenciamento ambiental concedido pela SEMA</div>
        <div class="strategy-item">Suspensão imediata das atividades da PCH (tutela de urgência)</div>
        <div class="strategy-item">Determinação de EIA completo com trabalho de campo e participação indígena</div>
        <div class="strategy-item">Realização de consulta prévia conforme protocolo comunitário do povo afetado</div>
        <div class="strategy-item">Reparação integral dos danos socioambientais (dano material + moral coletivo)</div>
        <div class="strategy-item">Responsabilização solidária do empreendedor e do Estado (SEMA)</div>
        <button class="send-btn" style="margin-top:10px;" onclick="sendPrompt('Redija minutas dos pedidos principais e alternativos para amicus curiae em ação do MPF sobre PCH em terras indígenas com licenciamento nulo')">Minutar pedidos ↗</button>
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
        <button class="send-btn" style="margin-top:10px;" onclick="sendPrompt('Quais são os requisitos legais para realização de perícia ambiental em terras indígenas afetadas por PCH e como ela deve ser conduzida?')">Detalhes da perícia ↗</button>
      </div>
      <div class="strategy-card">
        <h3>Jurisprudência prioritária</h3>
        <div class="strategy-item">STF — RE 466.343 (consulta prévia e Conv. 169)</div>
        <div class="strategy-item">STJ — REsp 1.797.175 (dano ambiental em TI)</div>
        <div class="strategy-item">TRF-1 — processos de PCH em TI na Amazônia</div>
        <div class="strategy-item">CIDH — caso Saramaka vs. Suriname</div>
        <div class="strategy-item">Corte IDH — caso Povo Sarayaku vs. Equador</div>
        <div class="strategy-item">ADPF 709 (STF — direitos territoriais indígenas)</div>
        <button class="send-btn" style="margin-top:10px;" onclick="sendPrompt('Quais são os principais precedentes do STF e do STJ sobre consulta prévia a povos indígenas e licenciamento de obras de infraestrutura em terras indígenas?')">Pesquisar jurisprudência ↗</button>
      </div>
    </div>
  </div>

  <div id="tab-campo" class="panel">
    <div class="add-form">
      <div class="section-title" style="margin-bottom:12px;">Registrar relato de campo</div>
      <div class="form-row">
        <div>
          <div class="form-label">Comunidade / Liderança</div>
          <input type="text" id="c-pessoa" placeholder="Nome ou cargo">
        </div>
        <div>
          <div class="form-label">Data do depoimento</div>
          <input type="text" id="c-data" placeholder="DD/MM/AAAA">
        </div>
      </div>
      <div class="form-row full">
        <div>
          <div class="form-label">Conteúdo do depoimento / anseios expressos</div>
          <textarea id="c-dep" placeholder="Registre o que foi dito, o que o povo indígena espera, impactos relatados..."></textarea>
        </div>
      </div>
      <div class="form-row">
        <div>
          <div class="form-label">Impactos relatados</div>
          <input type="text" id="c-imp" placeholder="Pesca, território, saúde...">
        </div>
        <div>
          <div class="form-label">Posicionamento sobre a PCH</div>
          <select id="c-pos">
            <option>Contrário — quer paralisação</option>
            <option>Contrário — quer reparação</option>
            <option>Condicionado — exige consulta</option>
            <option>Não informado</option>
          </select>
        </div>
      </div>
      <div style="display:flex;gap:8px;">
        <button class="btn btn-primary" onclick="addRelato()">Salvar relato</button>
        <button class="send-btn" onclick="sendPrompt('Com base nos depoimentos indígenas coletados em campo, como estruturar a prova testemunhal para uma ação do MPF sobre PCH em terras indígenas, considerando o direito ao silêncio e a proteção dos depoentes?')">Orientação probatória ↗</button>
      </div>
    </div>
    <div class="section-title">Relatos coletados</div>
    <div id="relatos-list" style="display:flex;flex-direction:column;gap:8px;"></div>
  </div>

  <div id="tab-notas" class="panel">
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:10px;">
      <div class="section-title" style="margin:0;">Notas jurídicas livres</div>
      <button class="send-btn" onclick="sendPrompt('Quais são as etapas para peticionamento de amicus curiae em ação do MPF na Justiça Federal, incluindo prazos e requisitos formais?')">Como peticionar ↗</button>
    </div>
    <textarea class="note-area" id="notas-text" placeholder="Use este espaço para anotações gerais, hipóteses jurídicas, pontos de atenção, cronograma..."></textarea>
    <div style="margin-top:8px;display:flex;gap:8px;">
      <button class="btn btn-sm" onclick="saveNota()">Salvar nota</button>
      <button class="send-btn" onclick="sendPrompt('Com base nas irregularidades identificadas no licenciamento de PCH em terras indígenas pela SEMA, elabore uma estrutura de petição inicial de amicus curiae para ser juntada à ação do MPF')">Estruturar petição ↗</button>
    </div>
    <div style="margin-top:1rem;" id="notas-saved"></div>
  </div>
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

function switchTab(id) {
  document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));
  document.getElementById('tab-'+id).classList.add('active');
  event.target.classList.add('active');
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
    d.innerHTML = flag+'<div class="vol-num">Vol. '+v.num+'</div><div class="vol-status">'+(v.status==='pendente'?'pendente':v.status==='lido'?'lido':v.status==='parcial'?'parcial':'crítico')+'</div>';
    d.onclick = ()=>openVol(v.num);
    grid.appendChild(d);
  });
  const pct = Math.round(lidos/20*100);
  document.getElementById('m-lidos').textContent = lidos;
  document.getElementById('m-lidos-pct').textContent = pct+'%';
  document.getElementById('prog-lidos').style.width = pct+'%';
}

function openVol(num) {
  state.selectedVol = num;
  const v = state.volumes[num-1];
  document.getElementById('vol-detail-title').textContent = 'Volume '+num;
  document.getElementById('vol-status-sel').value = v.status||'pendente';
  document.getElementById('vol-files').value = v.files||'';
  document.getElementById('vol-obs').value = v.obs||'';
  document.getElementById('vol-detail').style.display = 'block';
  document.getElementById('vol-detail').scrollIntoView({behavior:'smooth',block:'nearest'});
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
  state.vicios.forEach((v,i)=>{
    const gravClass = v.grav==='critico'?'badge-danger':v.grav==='grave'?'badge-warn':'badge-info';
    const gravLabel = v.grav==='critico'?'Crítico — nulidade':v.grav==='grave'?'Grave — anulabilidade':'Relevante';
    const el = document.createElement('div');
    el.className = 'vicio-item';
    el.innerHTML = '<div class="vicio-header"><span class="badge '+gravClass+'">'+gravLabel+'</span><span style="font-size:13px;font-weight:500;color:var(--color-text-primary);">'+v.tipo+'</span></div><div class="vicio-desc">'+v.desc+'</div><div class="vicio-ref">Ref.: '+v.ref+' &nbsp;|&nbsp; '+v.fund+'</div>';
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
  state.checklist.forEach((item,i)=>{
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
  document.getElementById('c-pessoa').value='';
  document.getElementById('c-data').value='';
  document.getElementById('c-dep').value='';
  document.getElementById('c-imp').value='';
  renderRelatos();
}

function renderRelatos() {
  const list = document.getElementById('relatos-list');
  list.innerHTML='';
  if(!state.relatos.length){list.innerHTML='<div style="font-size:13px;color:var(--color-text-secondary);">Nenhum relato registrado ainda.</div>';return;}
  state.relatos.forEach(r=>{
    const el = document.createElement('div');
    el.className='vicio-item';
    el.innerHTML='<div class="vicio-header"><span class="badge badge-info">'+r.data+'</span><span style="font-size:13px;font-weight:500;color:var(--color-text-primary);">'+r.pessoa+'</span></div><div class="vicio-desc">'+r.dep+'</div><div class="vicio-ref">Impactos: '+r.imp+' &nbsp;|&nbsp; Posição: '+r.pos+'</div>';
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
    el.innerHTML='<div class="vicio-ref" style="margin-bottom:5px;">'+n.date+'</div><div class="vicio-desc">'+n.txt+'</div>';
    list.appendChild(el);
  });
}

renderVolumes();
renderVicios();
renderChecklist();
renderRelatos();
</script>
