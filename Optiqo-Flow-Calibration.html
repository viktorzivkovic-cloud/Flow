<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Optiqo Flow – Calibration Progress</title>
<style>
  :root { color-scheme: light; }
  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    background: #f7f8fb;
    color: #1a2233;
    font-size: 14px;
    line-height: 1.45;
  }
  .wrap { max-width: 1400px; margin: 0 auto; padding: 20px 24px 60px; }
  header { display: flex; justify-content: space-between; align-items: flex-start; gap: 16px; flex-wrap: wrap; }
  header h1 { margin: 0 0 4px; font-size: 22px; font-weight: 600; }
  header .sub { color: #6b7280; font-size: 13px; }
  .refresh-box { text-align: right; font-size: 12px; color: #6b7280; }
  .refresh-box button {
    background: #fff; border: 1px solid #d1d5db; border-radius: 8px;
    padding: 6px 10px; font-size: 12px; cursor: pointer; color: #0f172a;
  }
  .refresh-box button:hover { background: #f3f4f6; }
  .note-banner {
    margin-top: 10px;
    background: #fff7ed;
    border: 1px solid #fed7aa;
    color: #7c2d12;
    padding: 8px 12px;
    border-radius: 8px;
    font-size: 12.5px;
    line-height: 1.5;
  }
  .cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 12px;
    margin: 20px 0 24px;
  }
  .card { background: #fff; border: 1px solid #e5e7eb; border-radius: 10px; padding: 14px 16px; }
  .card .label { color: #6b7280; font-size: 12px; text-transform: uppercase; letter-spacing: 0.04em; }
  .card .value { font-size: 26px; font-weight: 600; margin-top: 4px; color: #0f172a; }
  .card .sub { color: #6b7280; font-size: 12px; margin-top: 2px; }

  section { background: #fff; border: 1px solid #e5e7eb; border-radius: 10px; padding: 18px 20px; margin-bottom: 18px; }
  section h2 { margin: 0 0 14px; font-size: 15px; font-weight: 600; color: #0f172a; }

  .legend { display: flex; gap: 14px; font-size: 12px; color: #475569; margin-bottom: 12px; flex-wrap: wrap; }
  .legend span { display: inline-flex; align-items: center; gap: 6px; }
  .legend .sw { width: 12px; height: 12px; border-radius: 3px; display: inline-block; }
  .legend .sw.done { background: #16a34a; }
  .legend .sw.ongoing { background: #f59e0b; }
  .legend .sw.empty { background: #eef0f4; }

  .area-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 14px 28px; }
  .area-row { display: flex; flex-direction: column; gap: 4px; }
  .area-head { display: flex; justify-content: space-between; font-size: 13px; }
  .area-name { font-weight: 500; }
  .area-pct { color: #6b7280; font-variant-numeric: tabular-nums; }
  .bar { background: #eef0f4; border-radius: 999px; height: 8px; overflow: hidden; display: flex; }
  .bar > .seg { height: 100%; }
  .bar > .seg.done { background: #16a34a; }
  .bar > .seg.ongoing { background: #f59e0b; }

  .toolbar { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 12px; align-items: center; }
  .toolbar input, .toolbar select {
    padding: 8px 10px; border: 1px solid #d1d5db; border-radius: 8px;
    font-size: 13px; background: #fff; color: #0f172a;
  }
  .toolbar input { min-width: 220px; }
  .toolbar .count { color: #6b7280; font-size: 12px; margin-left: auto; }

  .table-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: separate; border-spacing: 0; font-size: 12.5px; }
  th, td { padding: 8px 8px; border-bottom: 1px solid #f1f3f7; text-align: left; vertical-align: middle; white-space: nowrap; }
  thead th {
    position: sticky; top: 0; background: #f7f8fb;
    font-weight: 600; color: #475569; font-size: 11.5px;
    text-transform: uppercase; letter-spacing: 0.03em; cursor: pointer; user-select: none;
  }
  thead th.area { writing-mode: vertical-rl; transform: rotate(180deg); padding: 8px 4px; min-width: 28px; text-transform: none; letter-spacing: 0; font-size: 11px; }
  td.kund { font-weight: 500; color: #0f172a; max-width: 220px; white-space: normal; }
  td.kund.done-all { color: #15803d; }
  td.kund.in-progress .kund-dot { background: #f59e0b; }
  td.kund.done-all .kund-dot { background: #16a34a; }
  td.kund.not-started .kund-dot { background: #d1d5db; }
  td.kund .kund-dot { display: inline-block; width: 8px; height: 8px; border-radius: 50%; margin-right: 6px; vertical-align: middle; }
  td.area { text-align: center; }
  td.area .pill { display: inline-block; min-width: 18px; padding: 1px 7px; border-radius: 999px; font-size: 10.5px; font-weight: 600; letter-spacing: 0.02em; }
  td.area .pill.done { background: #dcfce7; color: #15803d; }
  td.area .pill.ongoing { background: #fef3c7; color: #b45309; }
  td.area .pill.other { background: #e0e7ff; color: #4338ca; }
  td.area .empty { color: #d1d5db; }
  td.note { white-space: normal; max-width: 260px; color: #6b7280; font-size: 12px; }
  td.owner { color: #475569; }

  .badge { display: inline-block; padding: 2px 8px; border-radius: 999px; font-size: 11px; font-weight: 500; }
  .b-klar { background: #dcfce7; color: #15803d; }
  .b-fardig { background: #e0f2fe; color: #0369a1; }
  .b-pabrjad { background: #fef3c7; color: #b45309; }
  .b-ej { background: #fee2e2; color: #b91c1c; }
  .b-none { color: #9ca3af; }

  .loading { padding: 24px; text-align: center; color: #6b7280; }
  .error { padding: 16px; background: #fef2f2; color: #b91c1c; border-radius: 8px; line-height: 1.5; }
  .error code { background: #fff; padding: 1px 6px; border-radius: 4px; border: 1px solid #fecaca; }
  tr.row:hover td { background: #fafbfd; }
</style>
</head>
<body>
<div class="wrap">
  <header>
    <div>
      <h1>Optiqo Flow – Calibration Progress, v1.0</h1>
      <div class="sub" id="subtitle">Live from the Optiqo Kanon Kallibrering sheet · auto-refreshes every 5 min</div>
    </div>
    <div class="refresh-box">
      <button id="refresh-btn">↻ Refresh now</button>
      <div id="last-updated" style="margin-top:6px"></div>
    </div>
  </header>
  <div class="note-banner">
    Customer rows turn <b style="color:#15803d">green</b> when every in-scope area is <b>Done</b>,
    <b style="color:#b45309">amber</b> while any area is <b>Ongoing</b>, grey before work starts.
  </div>

  <div id="content" class="loading">Loading data from the calibration sheet…</div>
</div>

<script>
const SHEET_ID = "1ASJYiyBMYK3rjPtZA6jApWMJdJ1Dbd1Zh9O0-h_fC7U";
const SHEET_NAME = "Overview";
const REFRESH_MS = 5 * 60 * 1000; // 5 minutes

// Public JSONP endpoint — bypasses CORS (works from file:// too).
// Requires sheet to be shared with "Anyone with the link" (Viewer).
// Try sheet-name first, fall back to gid=0 (first tab) if that fails.
let _jsonpCounter = 0;
function jsonpOnce(url) {
  return new Promise((resolve, reject) => {
    const cbName = "_optiqoCb_" + (++_jsonpCounter) + "_" + Date.now();
    let done = false;
    function cleanup() {
      try { delete window[cbName]; } catch (_) { window[cbName] = undefined; }
      if (script.parentNode) script.parentNode.removeChild(script);
    }
    const timer = setTimeout(() => {
      if (done) return; done = true; cleanup();
      reject(new Error("Timed out — is the sheet shared with 'Anyone with the link'?"));
    }, 15000);
    window[cbName] = (payload) => {
      if (done) return; done = true; clearTimeout(timer); cleanup();
      resolve(payload);
    };
    const script = document.createElement("script");
    // tqx uses colon-separated key:value pairs joined with semicolons
    script.src = url.replace("__CB__", cbName);
    script.onerror = () => {
      if (done) return; done = true; clearTimeout(timer); cleanup();
      reject(new Error("Couldn't reach the sheet."));
    };
    document.head.appendChild(script);
  });
}

async function fetchSheetJSONP() {
  const base = `https://docs.google.com/spreadsheets/d/${SHEET_ID}/gviz/tq`;
  const tqx = `tqx=out:json;responseHandler:__CB__`;
  // 1) try by sheet name
  const byName = `${base}?${tqx}&sheet=${encodeURIComponent(SHEET_NAME)}&_=${Date.now()}`;
  try {
    return await jsonpOnce(byName);
  } catch (e1) {
    // 2) try first tab (gid=0)
    const byGid = `${base}?${tqx}&gid=0&_=${Date.now()}`;
    try {
      return await jsonpOnce(byGid);
    } catch (e2) {
      throw e2;
    }
  }
}

// Convert gviz JSON table → array of row objects keyed by header label.
function recordsFromGviz(payload) {
  if (!payload || payload.status !== "ok" || !payload.table) {
    throw new Error("Sheet response not OK: " + (payload && payload.status));
  }
  const cols = payload.table.cols.map(c => (c.label || c.id || "").trim());
  // If the first data row is the actual header (sometimes happens when sheet has no
  // explicit header row), promote it.
  let headerRow = cols;
  let startRow = 0;
  if (!cols.some(c => /^kund$/i.test(c))) {
    const first = (payload.table.rows[0] && payload.table.rows[0].c) || [];
    const candidate = first.map(x => (x && (x.f || x.v) != null ? String(x.f || x.v).trim() : ""));
    if (candidate.some(c => /^kund$/i.test(c))) {
      headerRow = candidate;
      startRow = 1;
    }
  }
  const records = payload.table.rows.slice(startRow).map(row => {
    const cells = row.c || [];
    const obj = {};
    headerRow.forEach((h, i) => {
      const cell = cells[i];
      let v = "";
      if (cell != null) v = cell.f != null ? cell.f : (cell.v != null ? cell.v : "");
      obj[h] = String(v).trim();
    });
    return obj;
  }).filter(r => r["Kund"]);
  return { header: headerRow, records };
}

// Areas are auto-detected: any header that isn't Kund / Notes / a "Vem -" owner
// column / a known status column is treated as a calibration area.
// This way new columns (like "Problem with some rooms") show up automatically.
let AREAS = [];
const OWNER_COLS = ["Vem - Checklistor", "Vem - Arbetsordrar", "Vem - Kontroller"];
const STATUS_COLS = ["Status Arbetsordrar", "Kontroller"];
const META_COLS = new Set(["Kund", "Notes", ...OWNER_COLS, ...STATUS_COLS]);

function detectAreas(header) {
  return header.filter(h => h && !META_COLS.has(h) && !/^Vem\b/i.test(h));
}

function escapeHtml(s) {
  return String(s ?? "").replace(/[&<>"']/g, c => ({"&":"&amp;","<":"&lt;",">":"&gt;","\"":"&quot;","'":"&#39;"}[c]));
}

function cellState(v) {
  if (!v) return "none";
  const t = String(v).trim().toLowerCase();
  if (!t) return "none";
  if (t === "done" || t === "klar" || t === "färdig") return "done";
  if (t === "ongoing" || t === "påbörjad" || t === "pågår") return "ongoing";
  return "other";
}
function isSet(v) { return cellState(v) !== "none"; }

function customerStatus(r) {
  const states = AREAS.map(a => cellState(r[a]));
  const inScope = states.filter(s => s !== "none");
  if (!inScope.length) return "not-started";
  if (inScope.every(s => s === "done")) return "done-all";
  return "in-progress";
}

function statusBadge(v) {
  if (!v) return '<span class="b-none">–</span>';
  const t = v.trim().toLowerCase();
  if (t === "klar" || t === "helt färdig" || t === "färdig") return `<span class="badge b-klar">${escapeHtml(v)}</span>`;
  if (t === "påbörjad") return `<span class="badge b-pabrjad">${escapeHtml(v)}</span>`;
  if (t === "ej påbörjad") return `<span class="badge b-ej">${escapeHtml(v)}</span>`;
  if (t.includes("färdig")) return `<span class="badge b-fardig">${escapeHtml(v)}</span>`;
  return `<span class="badge b-none">${escapeHtml(v)}</span>`;
}

// Robust CSV parser (handles quotes, embedded commas, newlines, escaped quotes)
function parseCsv(text) {
  const rows = [];
  let cur = [];
  let field = "";
  let inQ = false;
  for (let i = 0; i < text.length; i++) {
    const c = text[i];
    if (inQ) {
      if (c === '"' && text[i + 1] === '"') { field += '"'; i++; }
      else if (c === '"') inQ = false;
      else field += c;
    } else {
      if (c === '"') inQ = true;
      else if (c === ",") { cur.push(field); field = ""; }
      else if (c === "\n") { cur.push(field); rows.push(cur); cur = []; field = ""; }
      else if (c === "\r") { /* skip */ }
      else field += c;
    }
  }
  // last field/row
  if (field.length || cur.length) { cur.push(field); rows.push(cur); }
  return rows.filter(r => r.some(x => x !== ""));
}

function buildRecords(rows) {
  if (!rows.length) return { header: [], records: [] };
  const header = rows[0].map(h => (h || "").trim());
  // Find Kund column (handle case where first row is not the header)
  let headerIdx = 0;
  for (let i = 0; i < Math.min(3, rows.length); i++) {
    if (rows[i].some(c => /^kund$/i.test((c || "").trim()))) {
      headerIdx = i; break;
    }
  }
  const h = rows[headerIdx].map(x => (x || "").trim());
  const records = rows.slice(headerIdx + 1).map(r => {
    const o = {};
    h.forEach((k, i) => { o[k] = (r[i] || "").trim(); });
    return o;
  }).filter(o => o["Kund"]);
  return { header: h, records };
}

function timeAgo(ts) {
  const s = Math.round((Date.now() - ts) / 1000);
  if (s < 60) return `${s}s ago`;
  if (s < 3600) return `${Math.round(s/60)}m ago`;
  return `${Math.round(s/3600)}h ago`;
}

let lastLoadedAt = null;

function render(parsed) {
  const root = document.getElementById("content");
  if (!parsed || !parsed.records.length) {
    root.outerHTML = '<div id="content" class="error">Could not parse the Overview sheet. Make sure column A is "Kund" and the sheet name is exactly "Overview".</div>';
    return;
  }
  const { records } = parsed;
  const total = records.length;
  AREAS = detectAreas(parsed.header);
  if (!AREAS.length) {
    root.outerHTML = '<div id="content" class="error">No calibration areas found in the sheet header.</div>';
    return;
  }

  const areaStats = AREAS.map(a => {
    let done = 0, ongoing = 0, other = 0;
    records.forEach(r => {
      const s = cellState(r[a]);
      if (s === "done") done++;
      else if (s === "ongoing") ongoing++;
      else if (s === "other") other++;
    });
    return {
      area: a, done, ongoing, other,
      donePct: total ? Math.round((done / total) * 100) : 0,
      ongoingPct: total ? Math.round((ongoing / total) * 100) : 0,
    };
  });

  let totalDone = 0, totalInScope = 0;
  records.forEach(r => AREAS.forEach(a => {
    const s = cellState(r[a]);
    if (s === "done") { totalDone++; totalInScope++; }
    else if (s === "ongoing" || s === "other") totalInScope++;
  }));
  const overallPct = totalInScope ? Math.round((totalDone / totalInScope) * 100) : 0;

  const custStatuses = records.map(customerStatus);
  const doneCust = custStatuses.filter(s => s === "done-all").length;
  const inProgCust = custStatuses.filter(s => s === "in-progress").length;
  const notStartedCust = custStatuses.filter(s => s === "not-started").length;

  const html = `
    <div class="cards">
      <div class="card">
        <div class="label">Customers in scope</div>
        <div class="value">${total}</div>
        <div class="sub">on the Overview sheet</div>
      </div>
      <div class="card">
        <div class="label">Overall completion</div>
        <div class="value">${overallPct}%</div>
        <div class="sub">${totalDone} done of ${totalInScope} in-scope cells</div>
      </div>
      <div class="card">
        <div class="label">Customers done (100%)</div>
        <div class="value" style="color:#15803d">${doneCust}</div>
        <div class="sub">every in-scope area marked Done</div>
      </div>
      <div class="card">
        <div class="label">In progress</div>
        <div class="value" style="color:#b45309">${inProgCust}</div>
        <div class="sub">${notStartedCust} not started yet</div>
      </div>
    </div>

    <section>
      <h2>Calibration progress by area</h2>
      <div class="legend">
        <span><span class="sw done"></span>Done</span>
        <span><span class="sw ongoing"></span>Ongoing</span>
        <span><span class="sw empty"></span>Not in scope / blank</span>
      </div>
      <div class="area-grid">
        ${areaStats.map(a => `
          <div class="area-row">
            <div class="area-head">
              <span class="area-name">${escapeHtml(a.area)}</span>
              <span class="area-pct">${a.done} done · ${a.ongoing} ongoing${a.other ? ` · ${a.other} todo` : ""}</span>
            </div>
            <div class="bar">
              <div class="seg done" style="width:${a.donePct}%"></div>
              <div class="seg ongoing" style="width:${a.ongoingPct}%"></div>
            </div>
          </div>
        `).join("")}
      </div>
    </section>

    <section>
      <h2>Customers</h2>
      <div class="toolbar">
        <input id="q" type="search" placeholder="Search customer or owner…" />
        <select id="filterCustStatus">
          <option value="">All customers</option>
          <option value="done-all">Done (100%)</option>
          <option value="in-progress">In progress</option>
          <option value="not-started">Not started</option>
        </select>
        <select id="filterArea">
          <option value="">All areas</option>
          ${AREAS.map(a => `<option value="${escapeHtml(a)}">${escapeHtml(a)} in scope</option>`).join("")}
        </select>
        <select id="filterAreaState">
          <option value="">Any state</option>
          <option value="done">Done only</option>
          <option value="ongoing">Ongoing only</option>
        </select>
        <select id="filterOwner">
          <option value="">All owners</option>
        </select>
        <span class="count" id="rowCount"></span>
      </div>
      <div class="table-wrap">
        <table id="tbl">
          <thead>
            <tr>
              <th data-key="Kund">Customer</th>
              ${AREAS.map(a => `<th class="area" data-key="${escapeHtml(a)}">${escapeHtml(a)}</th>`).join("")}
              <th data-key="Vem - Checklistor">Owner – Checklists</th>
              <th data-key="Vem - Arbetsordrar">Owner – WO</th>
              <th data-key="Status Arbetsordrar">Status WO</th>
              <th data-key="Vem - Kontroller">Owner – Controls</th>
              <th data-key="Kontroller">Status Controls</th>
              <th data-key="Notes">Notes</th>
            </tr>
          </thead>
          <tbody id="tbody"></tbody>
        </table>
      </div>
    </section>
  `;
  root.outerHTML = `<div id="content">${html}</div>`;

  // Owners filter
  const ownerSet = new Set();
  records.forEach(r => OWNER_COLS.forEach(c => {
    const v = (r[c] || "").trim();
    if (v) v.split(/[,/]/).forEach(o => { const t = o.trim(); if (t) ownerSet.add(t); });
  }));
  const ownerSelect = document.getElementById("filterOwner");
  [...ownerSet].sort().forEach(o => {
    const opt = document.createElement("option");
    opt.value = o.toLowerCase();
    opt.textContent = o;
    ownerSelect.appendChild(opt);
  });

  let sortKey = "Kund";
  let sortDir = 1;
  const tbody = document.getElementById("tbody");
  const rowCount = document.getElementById("rowCount");

  function areaCell(v) {
    const s = cellState(v);
    if (s === "done") return '<span class="pill done">Done</span>';
    if (s === "ongoing") return '<span class="pill ongoing">Ongoing</span>';
    if (s === "other") return `<span class="pill other">${escapeHtml(v)}</span>`;
    return '<span class="empty">·</span>';
  }

  function renderRows() {
    const q = document.getElementById("q").value.trim().toLowerCase();
    const fa = document.getElementById("filterArea").value;
    const fas = document.getElementById("filterAreaState").value;
    const fo = document.getElementById("filterOwner").value;
    const fcs = document.getElementById("filterCustStatus").value;

    let rows = records.slice();
    if (q) rows = rows.filter(r => {
      const hay = [r["Kund"], ...OWNER_COLS.map(c => r[c]), r["Notes"]].join(" ").toLowerCase();
      return hay.includes(q);
    });
    if (fcs) rows = rows.filter(r => customerStatus(r) === fcs);
    if (fa && fas) rows = rows.filter(r => cellState(r[fa]) === fas);
    else if (fa) rows = rows.filter(r => isSet(r[fa]));
    else if (fas) rows = rows.filter(r => AREAS.some(a => cellState(r[a]) === fas));
    if (fo) rows = rows.filter(r => OWNER_COLS.some(c => (r[c] || "").toLowerCase().includes(fo)));

    rows.sort((x, y) => {
      const a = (x[sortKey] || "").toLowerCase();
      const b = (y[sortKey] || "").toLowerCase();
      if (a < b) return -1 * sortDir;
      if (a > b) return 1 * sortDir;
      return 0;
    });

    tbody.innerHTML = rows.map(r => {
      const cs = customerStatus(r);
      return `
      <tr class="row">
        <td class="kund ${cs}"><span class="kund-dot"></span>${escapeHtml(r["Kund"])}</td>
        ${AREAS.map(a => `<td class="area">${areaCell(r[a])}</td>`).join("")}
        <td class="owner">${escapeHtml(r["Vem - Checklistor"] || "")}</td>
        <td class="owner">${escapeHtml(r["Vem - Arbetsordrar"] || "")}</td>
        <td>${statusBadge(r["Status Arbetsordrar"] || "")}</td>
        <td class="owner">${escapeHtml(r["Vem - Kontroller"] || "")}</td>
        <td>${statusBadge(r["Kontroller"] || "")}</td>
        <td class="note">${escapeHtml(r["Notes"] || "")}</td>
      </tr>`;
    }).join("");
    rowCount.textContent = `${rows.length} of ${total} customers`;
  }

  document.querySelectorAll("thead th").forEach(th => {
    th.addEventListener("click", () => {
      const k = th.dataset.key;
      if (!k) return;
      if (k === sortKey) sortDir *= -1; else { sortKey = k; sortDir = 1; }
      renderRows();
    });
  });
  ["q","filterArea","filterAreaState","filterOwner","filterCustStatus"].forEach(id => {
    document.getElementById(id).addEventListener("input", renderRows);
    document.getElementById(id).addEventListener("change", renderRows);
  });
  renderRows();
}

async function load() {
  const stamp = document.getElementById("last-updated");
  stamp.textContent = "Loading…";
  try {
    const payload = await fetchSheetJSONP();
    const parsed = recordsFromGviz(payload);
    render(parsed);
    lastLoadedAt = Date.now();
    updateStamp();
  } catch (e) {
    document.getElementById("content").outerHTML =
      `<div id="content" class="error">Couldn't load the sheet: ${escapeHtml(String(e && e.message || e))}<br><br>
      <b>Checklist:</b><br>
      1. Sheet → Share → General access → <code>Anyone with the link</code> (Viewer)<br>
      2. First tab named exactly <code>Overview</code> with <code>Kund</code> in column A.</div>`;
    stamp.textContent = "";
  }
}

function updateStamp() {
  if (!lastLoadedAt) return;
  document.getElementById("last-updated").textContent = "Updated " + timeAgo(lastLoadedAt);
}

document.getElementById("refresh-btn").addEventListener("click", load);
load();
setInterval(load, REFRESH_MS);
setInterval(updateStamp, 30 * 1000);
</script>
</body>
</html>
