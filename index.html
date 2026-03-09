<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <title>Staff Scheduler</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.23.2/babel.min.js"></script>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
    body { font-family: 'Segoe UI', Tahoma, sans-serif; background: #EDEDED; min-height: 100vh; }
    table { border-collapse: collapse; }
    input, button, select { font-family: inherit; }
    ::-webkit-scrollbar { height: 4px; } 
    ::-webkit-scrollbar-thumb { background: #ccc; border-radius: 4px; }
  </style>
</head>
<body>
  <div id="root"></div>

  <script type="text/babel">
    const { useState, useMemo } = React;

    const DAY_COLORS = {
      MON: { bg: "#FFD966", text: "#5a3e00" },
      TUE: { bg: "#FF6B35", text: "#fff" },
      WED: { bg: "#70AD47", text: "#fff" },
      THU: { bg: "#4BACC6", text: "#fff" },
      FRI: { bg: "#4472C4", text: "#fff" },
      SAT: { bg: "#7030A0", text: "#fff" },
      SUN: { bg: "#FF0000", text: "#fff" },
    };

    const DAYS = ["MON", "TUE", "WED", "THU", "FRI", "SAT", "SUN"];
    const SHIFTS = ["Lunch", "Dinner"];
    const CYCLE = ["", "x", "Off", "?"];
    const NAME_W = 72;
    const CELL_W = 38;

    const getShortName = (title) => title.split(/\s+/)[0];
    const cellKey = (name, day, shift) => `${name}_${day}_${shift}`;

    const INITIAL_SCHEDULES = [
      {
        id: 1,
        title: "Aunty Katie  9-15 Mar 26",
        groups: [
          { id: "ak_boh", name: "BOH", people: [{ name: "กอล์ฟ" }, { name: "Benz" }, { name: "นัท" }, { name: "นิก" }, { name: "เป้า" }, { name: "แชมมี่" }] },
          { id: "ak_foh", name: "FOH", people: [{ name: "พีโอน" }, { name: "ทราย" }, { name: "นุช" }, { name: "เดมี่" }] },
        ],
        cells: {
          "กอล์ฟ_TUE_Lunch":"x","กอล์ฟ_TUE_Dinner":"x","กอล์ฟ_WED_Lunch":"x","กอล์ฟ_WED_Dinner":"x","กอล์ฟ_THU_Lunch":"x","กอล์ฟ_THU_Dinner":"x","กอล์ฟ_FRI_Lunch":"x","กอล์ฟ_FRI_Dinner":"x","กอล์ฟ_SAT_Lunch":"x","กอล์ฟ_SAT_Dinner":"x","กอล์ฟ_SUN_Lunch":"x","กอล์ฟ_SUN_Dinner":"x",
          "Benz_TUE_Lunch":"x","Benz_TUE_Dinner":"x","Benz_WED_Lunch":"Off","Benz_WED_Dinner":"Off","Benz_THU_Lunch":"x","Benz_THU_Dinner":"x","Benz_FRI_Lunch":"x","Benz_FRI_Dinner":"x","Benz_SAT_Lunch":"x","Benz_SAT_Dinner":"x","Benz_SUN_Lunch":"x","Benz_SUN_Dinner":"x",
          "นัท_TUE_Lunch":"x","นัท_TUE_Dinner":"x","นัท_WED_Lunch":"Off","นัท_WED_Dinner":"x","นัท_THU_Lunch":"x","นัท_THU_Dinner":"x","นัท_FRI_Lunch":"x","นัท_FRI_Dinner":"x","นัท_SAT_Lunch":"x","นัท_SAT_Dinner":"x","นัท_SUN_Lunch":"x","นัท_SUN_Dinner":"x",
          "นิก_TUE_Lunch":"x","นิก_TUE_Dinner":"x","นิก_WED_Lunch":"x","นิก_WED_Dinner":"x","นิก_THU_Lunch":"x","นิก_THU_Dinner":"x","นิก_FRI_Lunch":"x","นิก_FRI_Dinner":"x","นิก_SAT_Lunch":"x","นิก_SAT_Dinner":"x","นิก_SUN_Lunch":"x","นิก_SUN_Dinner":"x",
          "เป้า_TUE_Lunch":"x","เป้า_TUE_Dinner":"x","เป้า_WED_Lunch":"x","เป้า_WED_Dinner":"x","เป้า_THU_Lunch":"x","เป้า_THU_Dinner":"x","เป้า_FRI_Lunch":"x","เป้า_FRI_Dinner":"x","เป้า_SAT_Lunch":"x","เป้า_SAT_Dinner":"x","เป้า_SUN_Lunch":"x","เป้า_SUN_Dinner":"x",
          "แชมมี่_WED_Lunch":"x",
          "พีโอน_MON_Lunch":"Off","พีโอน_MON_Dinner":"Off","พีโอน_TUE_Lunch":"x","พีโอน_TUE_Dinner":"x","พีโอน_WED_Lunch":"x","พีโอน_WED_Dinner":"x","พีโอน_THU_Lunch":"x","พีโอน_THU_Dinner":"x","พีโอน_FRI_Lunch":"x","พีโอน_FRI_Dinner":"x","พีโอน_SAT_Lunch":"x","พีโอน_SAT_Dinner":"x","พีโอน_SUN_Lunch":"x","พีโอน_SUN_Dinner":"x",
          "ทราย_MON_Lunch":"Off","ทราย_MON_Dinner":"Off","ทราย_TUE_Lunch":"x","ทราย_TUE_Dinner":"x","ทราย_WED_Lunch":"x","ทราย_WED_Dinner":"x","ทราย_THU_Lunch":"x","ทราย_THU_Dinner":"x","ทราย_FRI_Lunch":"x","ทราย_FRI_Dinner":"x","ทราย_SAT_Lunch":"x","ทราย_SAT_Dinner":"x","ทราย_SUN_Lunch":"x","ทราย_SUN_Dinner":"x",
          "นุช_TUE_Lunch":"x","นุช_TUE_Dinner":"x","นุช_WED_Lunch":"x","นุช_WED_Dinner":"x","นุช_THU_Lunch":"x","นุช_THU_Dinner":"x","นุช_FRI_Lunch":"x","นุช_FRI_Dinner":"x","นุช_SAT_Lunch":"x","นุช_SAT_Dinner":"x","นุช_SUN_Lunch":"x","นุช_SUN_Dinner":"x",
          "เดมี่_TUE_Lunch":"x","เดมี่_TUE_Dinner":"x","เดมี่_WED_Lunch":"x","เดมี่_WED_Dinner":"x","เดมี่_THU_Lunch":"x","เดมี่_THU_Dinner":"x","เดมี่_FRI_Lunch":"x","เดมี่_FRI_Dinner":"x","เดมี่_SAT_Lunch":"x","เดมี่_SAT_Dinner":"x","เดมี่_SUN_Lunch":"x","เดมี่_SUN_Dinner":"x",
        },
      },
      {
        id: 2,
        title: "EATSY  9-15 Mar 26",
        groups: [
          { id: "ea_boh", name: "BOH", people: [{ name: "พีศักดิ์" }, { name: "พีรงค์" }, { name: "แทน" }, { name: "ปรีชา" }, { name: "ฟร้องค์" }, { name: "แชมมี่" }] },
          { id: "ea_foh", name: "FOH", people: [{ name: "ฟ้า" }, { name: "พีแอ็ก" }, { name: "Supa" }, { name: "ทราย" }, { name: "เกวน" }, { name: "มิโฮะ" }, { name: "Train" }, { name: "เดมี่" }] },
        ],
        cells: {
          "พีศักดิ์_MON_Lunch":"x","พีศักดิ์_MON_Dinner":"x","พีศักดิ์_TUE_Lunch":"x","พีศักดิ์_TUE_Dinner":"x","พีศักดิ์_WED_Lunch":"x","พีศักดิ์_WED_Dinner":"x","พีศักดิ์_THU_Lunch":"Off","พีศักดิ์_THU_Dinner":"Off","พีศักดิ์_FRI_Lunch":"x","พีศักดิ์_FRI_Dinner":"x","พีศักดิ์_SAT_Lunch":"x","พีศักดิ์_SAT_Dinner":"x","พีศักดิ์_SUN_Lunch":"x","พีศักดิ์_SUN_Dinner":"x",
          "พีรงค์_MON_Lunch":"x","พีรงค์_MON_Dinner":"x","พีรงค์_TUE_Lunch":"x","พีรงค์_TUE_Dinner":"x","พีรงค์_WED_Lunch":"x","พีรงค์_WED_Dinner":"x","พีรงค์_THU_Lunch":"x","พีรงค์_THU_Dinner":"x","พีรงค์_FRI_Lunch":"x","พีรงค์_FRI_Dinner":"x","พีรงค์_SAT_Lunch":"x","พีรงค์_SAT_Dinner":"x","พีรงค์_SUN_Lunch":"Off","พีรงค์_SUN_Dinner":"Off",
          "แทน_MON_Lunch":"x","แทน_MON_Dinner":"x","แทน_TUE_Lunch":"Off","แทน_TUE_Dinner":"Off","แทน_WED_Lunch":"x","แทน_WED_Dinner":"x","แทน_THU_Lunch":"x","แทน_THU_Dinner":"x","แทน_FRI_Lunch":"x","แทน_FRI_Dinner":"x","แทน_SAT_Lunch":"x","แทน_SAT_Dinner":"x","แทน_SUN_Lunch":"x","แทน_SUN_Dinner":"x",
          "ปรีชา_MON_Lunch":"x","ปรีชา_MON_Dinner":"x","ปรีชา_TUE_Lunch":"x","ปรีชา_TUE_Dinner":"x","ปรีชา_WED_Lunch":"Off","ปรีชา_WED_Dinner":"Off","ปรีชา_THU_Lunch":"x","ปรีชา_THU_Dinner":"x","ปรีชา_FRI_Lunch":"x","ปรีชา_FRI_Dinner":"x","ปรีชา_SAT_Lunch":"x","ปรีชา_SAT_Dinner":"x","ปรีชา_SUN_Lunch":"x","ปรีชา_SUN_Dinner":"x",
          "ฟร้องค์_MON_Lunch":"x","ฟร้องค์_MON_Dinner":"x","ฟร้องค์_TUE_Lunch":"x","ฟร้องค์_TUE_Dinner":"x","ฟร้องค์_WED_Lunch":"x","ฟร้องค์_WED_Dinner":"x","ฟร้องค์_THU_Lunch":"Off","ฟร้องค์_THU_Dinner":"Off","ฟร้องค์_FRI_Lunch":"x","ฟร้องค์_FRI_Dinner":"x","ฟร้องค์_SAT_Lunch":"x","ฟร้องค์_SAT_Dinner":"x","ฟร้องค์_SUN_Lunch":"x","ฟร้องค์_SUN_Dinner":"x",
          "แชมมี่_TUE_Lunch":"x","แชมมี่_TUE_Dinner":"x","แชมมี่_WED_Lunch":"x","แชมมี่_THU_Lunch":"x","แชมมี่_THU_Dinner":"x",
          "ฟ้า_MON_Lunch":"x","ฟ้า_MON_Dinner":"x","ฟ้า_TUE_Lunch":"x","ฟ้า_TUE_Dinner":"x","ฟ้า_WED_Lunch":"x","ฟ้า_WED_Dinner":"x","ฟ้า_THU_Lunch":"x","ฟ้า_THU_Dinner":"x","ฟ้า_FRI_Lunch":"Off","ฟ้า_FRI_Dinner":"Off","ฟ้า_SAT_Lunch":"x","ฟ้า_SAT_Dinner":"x","ฟ้า_SUN_Lunch":"x","ฟ้า_SUN_Dinner":"x",
          "Supa_MON_Dinner":"x","Supa_TUE_Dinner":"x","Supa_FRI_Lunch":"x","Supa_SAT_Dinner":"x",
          "ทราย_MON_Lunch":"Off","ทราย_MON_Dinner":"Off",
          "เกวน_MON_Dinner":"signature","เกวน_TUE_Dinner":"signature","เกวน_WED_Lunch":"x","เกวน_THU_Lunch":"x","เกวน_FRI_Lunch":"x","เกวน_FRI_Dinner":"signature","เกวน_SAT_Lunch":"x","เกวน_SAT_Dinner":"signature",
          "Train_FRI_Dinner":"x","Train_SAT_Dinner":"x",
          "เดมี่_SUN_Lunch":"x",
        },
      },
    ];

    function buildPersonOutletMap(schedules) {
      const map = {};
      schedules.forEach((s, si) => {
        s.groups.forEach(g => {
          g.people.forEach(p => {
            if (!map[p.name]) map[p.name] = [];
            if (!map[p.name].includes(si)) map[p.name].push(si);
          });
        });
      });
      return map;
    }

    function getLinkedState(schedules, personOutletMap, name, day, shift, currentSchedIdx) {
      const others = (personOutletMap[name] || []).filter(i => i !== currentSchedIdx);
      if (others.length === 0) return null;
      const hits = others
        .map(i => ({ val: schedules[i].cells[cellKey(name, day, shift)] || "", title: getShortName(schedules[i].title) }))
        .filter(h => h.val !== "");
      if (hits.length === 0) return null;
      const offHit = hits.find(h => h.val === "Off");
      if (offHit) return { display: "Off", type: "Off", source: offHit.title };
      const qHit = hits.find(h => h.val === "?");
      if (qHit) return { display: "?", type: "?", source: qHit.title };
      const xHits = hits.filter(h => h.val === "x");
      if (xHits.length > 0) return { display: xHits.map(h => h.title).join("+"), type: "x", source: xHits.map(h => h.title).join(", ") };
      return null;
    }

    const iStyle = { width: "100%", padding: "11px 13px", borderRadius: 10, border: "1.5px solid #E5E7EB", fontSize: 15, boxSizing: "border-box" };
    const primaryBtn = { flex: 1, padding: "12px", borderRadius: 12, border: "none", background: "#1a1a2e", color: "#fff", fontWeight: 700, cursor: "pointer", fontSize: 14 };
    const cancelBtn  = { flex: 1, padding: "12px", borderRadius: 12, border: "1.5px solid #E5E7EB", background: "#fff", color: "#555", fontWeight: 600, cursor: "pointer", fontSize: 14 };
    const dangerBtn  = { width: "100%", padding: "12px", borderRadius: 12, border: "none", background: "#FEF2F2", color: "#E53E3E", fontWeight: 700, cursor: "pointer", fontSize: 14, marginBottom: 8 };

    function Modal({ children, onClose }) {
      return (
        <div style={{ position: "fixed", inset: 0, background: "rgba(0,0,0,0.45)", display: "flex", alignItems: "flex-end", justifyContent: "center", zIndex: 500, padding: 16 }}
          onClick={e => e.target === e.currentTarget && onClose()}>
          <div style={{ background: "#fff", borderRadius: 20, padding: 24, width: "100%", maxWidth: 430 }}>
            {children}
          </div>
        </div>
      );
    }

    const STORAGE_KEY = "staff_scheduler_v1";
    function loadSaved() {
      try { const s = localStorage.getItem(STORAGE_KEY); if (s) return JSON.parse(s); } catch(e) {}
      return INITIAL_SCHEDULES;
    }
    function saveSched(s) {
      try { localStorage.setItem(STORAGE_KEY, JSON.stringify(s)); } catch(e) {}
    }

    function App() {
      const [schedules, setSchedules] = useState(() => loadSaved());
      const [activeTab, setActiveTab]   = useState(0);
      const [editModal, setEditModal]   = useState(null);
      const [addPersonModal, setAddPersonModal] = useState(null);
      const [newPersonName, setNewPersonName]   = useState("");
      const [showAddSched, setShowAddSched]     = useState(false);
      const [newSchedTitle, setNewSchedTitle]   = useState("");
      const [toast, setToast] = useState(null);
      const [confirmReset, setConfirmReset] = useState(false);

      const showToast = (msg) => { setToast(msg); setTimeout(() => setToast(null), 2800); };
      const personOutletMap = useMemo(() => buildPersonOutletMap(schedules), [schedules]);

      React.useEffect(() => { saveSched(schedules); }, [schedules]);

      const resetAll = () => {
        setSchedules(INITIAL_SCHEDULES);
        localStorage.removeItem(STORAGE_KEY);
        setConfirmReset(false);
        setActiveTab(0);
        showToast("Reset to default template!");
      };

      const cycleCell = (schedIdx, name, day, shift) => {
        const key = cellKey(name, day, shift);
        setSchedules(prev => prev.map((s, si) => {
          if (si !== schedIdx) return s;
          const cur = s.cells[key] || "";
          const next = CYCLE[(CYCLE.indexOf(cur) + 1) % CYCLE.length];
          return { ...s, cells: { ...s.cells, [key]: next } };
        }));
      };

      const addPerson = () => {
        if (!newPersonName.trim()) return;
        const { schedIdx, groupIdx } = addPersonModal;
        setSchedules(prev => prev.map((s, si) => {
          if (si !== schedIdx) return s;
          const groups = s.groups.map((g, gi) =>
            gi !== groupIdx ? g : { ...g, people: [...g.people, { name: newPersonName.trim() }] }
          );
          return { ...s, groups };
        }));
        showToast(`${newPersonName.trim()} added!`);
        setNewPersonName(""); setAddPersonModal(null);
      };

      const removePerson = ({ schedIdx, groupIdx, personIdx }) => {
        setSchedules(prev => prev.map((s, si) => {
          if (si !== schedIdx) return s;
          const groups = s.groups.map((g, gi) =>
            gi !== groupIdx ? g : { ...g, people: g.people.filter((_, pi) => pi !== personIdx) }
          );
          return { ...s, groups };
        }));
        setEditModal(null); showToast("Person removed");
      };

      const addSchedule = () => {
        if (!newSchedTitle.trim()) return;
        const ts = Date.now();
        setSchedules(prev => [...prev, {
          id: ts, title: newSchedTitle.trim(),
          groups: [
            { id: `boh_${ts}`, name: "BOH", people: [] },
            { id: `foh_${ts}`, name: "FOH", people: [] },
          ],
          cells: {},
        }]);
        setActiveTab(schedules.length);
        setNewSchedTitle(""); setShowAddSched(false);
        showToast("New schedule created!");
      };

      const sched = schedules[activeTab];
      const totalCols = DAYS.length * SHIFTS.length;

      return (
        <div style={{ fontFamily: "'Segoe UI', Tahoma, sans-serif", background: "#EDEDED", minHeight: "100vh" }}>

          {/* Nav */}
          <div style={{ background: "#1a1a2e", padding: "10px 12px", display: "flex", alignItems: "center", gap: 8, flexWrap: "wrap", position: "sticky", top: 0, zIndex: 100 }}>
            <span style={{ color: "#fff", fontWeight: 800, fontSize: 13, letterSpacing: 1, marginRight: 4 }}>📅 SCHEDULER</span>
            {schedules.map((s, i) => (
              <button key={s.id} onClick={() => setActiveTab(i)} style={{
                padding: "5px 14px", borderRadius: 20, border: "none", cursor: "pointer",
                fontWeight: 700, fontSize: 12,
                background: activeTab === i ? "#7C3AED" : "rgba(255,255,255,0.12)", color: "#fff",
                boxShadow: activeTab === i ? "0 2px 8px rgba(124,58,237,0.5)" : "none"
              }}>{getShortName(s.title)}</button>
            ))}
            <button onClick={() => setShowAddSched(true)} style={{ padding: "5px 12px", borderRadius: 20, border: "1px dashed rgba(255,255,255,0.35)", background: "none", color: "rgba(255,255,255,0.55)", cursor: "pointer", fontSize: 12 }}>+ New</button>
            <div style={{ marginLeft: "auto", display: "flex", alignItems: "center", gap: 8 }}>
              <span style={{ fontSize: 10, color: "#6EE7B7", fontWeight: 700 }}>💾 Auto-saved</span>
              <button onClick={() => setConfirmReset(true)} style={{ padding: "4px 10px", borderRadius: 20, border: "1px solid rgba(255,100,100,0.4)", background: "none", color: "rgba(255,150,150,0.8)", cursor: "pointer", fontSize: 11 }}>Reset</button>
            </div>
          </div>

          {/* Link banner */}
          <div style={{ background: "#F3F0FF", borderBottom: "2px solid #C4B5FD", padding: "6px 14px", display: "flex", alignItems: "center", gap: 10, flexWrap: "wrap" }}>
            <span style={{ fontSize: 11, fontWeight: 800, color: "#6D28D9" }}>🔗 CROSS-OUTLET AUTO-LINK ON</span>
            <span style={{ fontSize: 11, color: "#7C3AED" }}>Purple/coloured cells = auto-filled from another outlet.</span>
          </div>

          {/* Table */}
          <div style={{ overflowX: "auto", padding: "10px 8px 30px" }}>
            <table style={{ borderCollapse: "collapse", tableLayout: "fixed", minWidth: NAME_W + totalCols * CELL_W }}>
              <colgroup>
                <col style={{ width: NAME_W }} />
                {DAYS.flatMap(d => SHIFTS.map(sh => <col key={`${d}${sh}`} style={{ width: CELL_W }} />))}
              </colgroup>
              <thead>
                <tr>
                  <td colSpan={1 + totalCols} style={{ background: "#C00000", color: "#fff", textAlign: "center", fontWeight: 800, fontSize: 13, padding: "6px 8px", border: "1px solid #aaa" }}>
                    {sched.title}
                  </td>
                </tr>
                <tr>
                  <td style={{ border: "1px solid #ccc", background: "#fff" }} />
                  {DAYS.map(day => (
                    <td key={day} colSpan={2} style={{ background: DAY_COLORS[day].bg, color: DAY_COLORS[day].text, textAlign: "center", fontWeight: 800, fontSize: 12, border: "1px solid #999", padding: "4px 0" }}>{day}</td>
                  ))}
                </tr>
                <tr>
                  <td style={{ background: "#F0F0F0", border: "1px solid #ccc", fontSize: 10, fontWeight: 700, textAlign: "center", color: "#666", padding: "3px" }}>Name</td>
                  {DAYS.flatMap(day => SHIFTS.map(sh => (
                    <td key={`${day}${sh}`} style={{ background: DAY_COLORS[day].bg + "99", textAlign: "center", fontSize: 9, fontWeight: 700, border: "1px solid #bbb", padding: "3px 1px", color: "#333" }}>{sh}</td>
                  )))}
                </tr>
              </thead>
              <tbody>
                {sched.groups.map((group, gi) => (
                  <React.Fragment key={group.id}>
                    <tr>
                      <td colSpan={1 + totalCols} style={{ background: "#D9D9D9", fontWeight: 800, fontSize: 12, padding: "4px 8px", border: "1px solid #bbb", color: "#222" }}>{group.name}</td>
                    </tr>

                    {group.people.map((person, pi) => {
                      const sharedWith = (personOutletMap[person.name] || []).filter(i => i !== activeTab);
                      const isShared = sharedWith.length > 0;
                      return (
                        <tr key={`${person.name}_${pi}`} style={{ background: pi % 2 === 0 ? "#fff" : "#F9F9F9" }}>
                          <td
                            onClick={() => setEditModal({ schedIdx: activeTab, groupIdx: gi, personIdx: pi, person })}
                            title={isShared ? `Shared with: ${sharedWith.map(i => getShortName(schedules[i].title)).join(", ")}` : person.name}
                            style={{ fontWeight: 700, fontSize: 11, padding: "3px 5px", border: "1px solid #ddd", whiteSpace: "nowrap", overflow: "hidden", textOverflow: "ellipsis", cursor: "pointer", maxWidth: NAME_W, color: isShared ? "#6D28D9" : "#1a1a2e" }}>
                            {isShared && "🔗 "}{person.name}
                          </td>

                          {DAYS.flatMap(day => SHIFTS.map(sh => {
                            const key = cellKey(person.name, day, sh);
                            const manual = sched.cells[key] || "";
                            const linkedState = manual === "" ? getLinkedState(schedules, personOutletMap, person.name, day, sh, activeTab) : null;
                            const isLinked = linkedState !== null;
                            const display = isLinked ? linkedState.display : manual;

                            let bg = "#fff", color = "#ccc", fw = 400, fs = 11, border = "1px solid #ddd";
                            let title = undefined;

                            if (isLinked) {
                              title = `🔗 Linked from ${linkedState.source}`;
                              if (linkedState.type === "Off") {
                                bg = "#FFE4E4"; color = "#C53030"; fw = 800; fs = 9; border = "1px solid #FCA5A5";
                              } else if (linkedState.type === "?") {
                                bg = "#FEF3C7"; color = "#92400E"; fw = 800; fs = 11; border = "1px solid #FCD34D";
                              } else {
                                bg = "#EDE9FE"; color = "#6D28D9"; fw = 800; fs = 8; border = "1px solid #C4B5FD";
                                title = `🔗 ${person.name} is working at ${display} this shift`;
                              }
                            } else if (manual === "x")    { bg = "#F0FFF4"; color = "#276749"; fw = 700; }
                            else if (manual === "Off") { bg = "#FFF5F5"; color = "#C53030"; fw = 700; fs = 9; }
                            else if (manual === "?")   { bg = "#FFFBEB"; color = "#B7791F"; fw = 700; }
                            else if (manual.length > 2){ bg = "#F5F0FF"; color = "#553C9A"; fw = 700; fs = 8; }

                            return (
                              <td key={`${person.name}_${day}_${sh}`}
                                onClick={() => !isLinked && cycleCell(activeTab, person.name, day, sh)}
                                title={title}
                                style={{ textAlign: "center", border, cursor: isLinked ? "not-allowed" : "pointer", fontSize: fs, fontWeight: fw, color, background: bg, padding: "3px 1px", userSelect: "none" }}>
                                {display}
                              </td>
                            );
                          }))}
                        </tr>
                      );
                    })}

                    <tr>
                      <td colSpan={1 + totalCols}
                        onClick={() => { setAddPersonModal({ schedIdx: activeTab, groupIdx: gi }); setNewPersonName(""); }}
                        style={{ textAlign: "left", padding: "3px 8px", border: "1px solid #eee", color: "#aaa", fontSize: 10, cursor: "pointer", background: "#FAFAFA" }}>
                        + Add to {group.name}
                      </td>
                    </tr>
                    <tr><td colSpan={1 + totalCols} style={{ height: 10, background: "transparent", border: "none" }} /></tr>
                  </React.Fragment>
                ))}
              </tbody>
            </table>

            {/* Legend */}
            <div style={{ display: "flex", gap: 10, marginTop: 14, flexWrap: "wrap" }}>
              {[
                { bg: "#F0FFF4", color: "#276749", label: "x",      desc: "Working" },
                { bg: "#FFF5F5", color: "#C53030", label: "Off",    desc: "Day Off" },
                { bg: "#FFFBEB", color: "#B7791F", label: "?",      desc: "Uncertain" },
                { bg: "#EDE9FE", color: "#6D28D9", label: "🔗 Name", desc: "At another outlet (auto)" },
                { bg: "#FFE4E4", color: "#C53030", label: "🔗 Off",  desc: "Off in another outlet (auto)" },
                { bg: "#FEF3C7", color: "#92400E", label: "🔗 ?",    desc: "Uncertain elsewhere (auto)" },
              ].map(l => (
                <div key={l.label} style={{ display: "flex", alignItems: "center", gap: 5 }}>
                  <div style={{ minWidth: 36, height: 18, background: l.bg, border: "1px solid #ddd", borderRadius: 3, display: "flex", alignItems: "center", justifyContent: "center", color: l.color, fontWeight: 700, fontSize: 8, padding: "0 3px" }}>{l.label}</div>
                  <span style={{ fontSize: 10, color: "#666" }}>{l.desc}</span>
                </div>
              ))}
            </div>
            <div style={{ marginTop: 6, fontSize: 10, color: "#999" }}>
              💡 Tap a cell to cycle: empty → x → Off → ? → empty. Coloured auto-cells are locked. Tap a name to manage.
            </div>
          </div>

          {/* Edit person modal */}
          {editModal && (
            <Modal onClose={() => setEditModal(null)}>
              <div style={{ fontWeight: 700, fontSize: 17, marginBottom: 8 }}>{editModal.person.name}</div>
              {(() => {
                const shared = (personOutletMap[editModal.person.name] || []).filter(i => i !== activeTab);
                return shared.length > 0 ? (
                  <div style={{ background: "#EDE9FE", borderRadius: 8, padding: "8px 12px", marginBottom: 14, fontSize: 12, color: "#6D28D9" }}>
                    🔗 Also scheduled in: <b>{shared.map(i => getShortName(schedules[i].title)).join(", ")}</b>
                  </div>
                ) : null;
              })()}
              <button onClick={() => removePerson(editModal)} style={dangerBtn}>Remove from this outlet</button>
              <button onClick={() => setEditModal(null)} style={cancelBtn}>Close</button>
            </Modal>
          )}

          {addPersonModal && (
            <Modal onClose={() => setAddPersonModal(null)}>
              <div style={{ fontWeight: 700, fontSize: 17, marginBottom: 14 }}>Add Person</div>
              <input autoFocus value={newPersonName} onChange={e => setNewPersonName(e.target.value)}
                onKeyDown={e => e.key === "Enter" && addPerson()}
                placeholder="Full name…" style={iStyle} />
              <div style={{ fontSize: 11, color: "#9CA3AF", marginTop: 6 }}>
                💡 Same spelling as in other outlets = auto-linking enabled.
              </div>
              <div style={{ display: "flex", gap: 8, marginTop: 12 }}>
                <button onClick={() => setAddPersonModal(null)} style={cancelBtn}>Cancel</button>
                <button onClick={addPerson} style={primaryBtn}>Add</button>
              </div>
            </Modal>
          )}

          {showAddSched && (
            <Modal onClose={() => setShowAddSched(false)}>
              <div style={{ fontWeight: 700, fontSize: 17, marginBottom: 14 }}>New Outlet Schedule</div>
              <input autoFocus value={newSchedTitle} onChange={e => setNewSchedTitle(e.target.value)}
                onKeyDown={e => e.key === "Enter" && addSchedule()}
                placeholder="e.g. Signature  9-15 Mar 26" style={iStyle} />
              <div style={{ display: "flex", gap: 8, marginTop: 12 }}>
                <button onClick={() => setShowAddSched(false)} style={cancelBtn}>Cancel</button>
                <button onClick={addSchedule} style={primaryBtn}>Create</button>
              </div>
            </Modal>
          )}

          {confirmReset && (
            <Modal onClose={() => setConfirmReset(false)}>
              <div style={{ fontWeight: 700, fontSize: 17, marginBottom: 10 }}>Reset everything?</div>
              <div style={{ fontSize: 13, color: "#6B7280", marginBottom: 20 }}>This will clear all your changes and restore the original template. This cannot be undone.</div>
              <div style={{ display: "flex", gap: 8 }}>
                <button onClick={() => setConfirmReset(false)} style={cancelBtn}>Cancel</button>
                <button onClick={resetAll} style={{ flex: 1, padding: "12px", borderRadius: 12, border: "none", background: "#EF4444", color: "#fff", fontWeight: 700, cursor: "pointer", fontSize: 14 }}>Reset</button>
              </div>
            </Modal>
          )}

          {toast && (
            <div style={{ position: "fixed", bottom: 20, left: "50%", transform: "translateX(-50%)", background: "#1a1a2e", color: "#fff", padding: "10px 22px", borderRadius: 30, fontSize: 13, fontWeight: 700, zIndex: 999, boxShadow: "0 4px 20px rgba(0,0,0,0.25)", whiteSpace: "nowrap" }}>
              {toast}
            </div>
          )}
        </div>
      );
    }

    ReactDOM.createRoot(document.getElementById("root")).render(<App />);
  </script>
</body>
</html>
