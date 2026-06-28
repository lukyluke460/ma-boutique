<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Test Supabase</title>
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
<style>
body{background:#0a0a0a;color:#fff;font-family:Arial;padding:24px;}
h1{font-size:1.2rem;margin-bottom:20px;}
input{width:100%;padding:14px;background:#161616;border:1px solid #333;border-radius:10px;color:#fff;font-size:1rem;margin-bottom:12px;box-sizing:border-box;}
button{width:100%;padding:16px;background:#00ff87;color:#000;border:none;border-radius:10px;font-size:1rem;font-weight:bold;cursor:pointer;margin-bottom:20px;}
#log{background:#111;border:1px solid #333;border-radius:10px;padding:16px;font-size:.85rem;line-height:1.8;white-space:pre-wrap;word-break:break-word;min-height:200px;}
.ok{color:#00ff87;}
.err{color:#ff4444;}
.info{color:#888;}
</style>
</head>
<body>
<h1>🔬 Test Supabase BarryShop</h1>
<input id="cat-name" placeholder="Nom de catégorie test"/>
<button id="test-btn">Tester la création</button>
<div id="log">En attente...</div>

<script>
const SUPA_URL='https://xyseyzlclcagqmhqanvd.supabase.co';
const SUPA_KEY='eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Inh5c2V5emxjbGNhZ3FtaHFhbnZkIiwicm9sZSI6ImFub24iLCJpYXQiOjE3ODI1ODEyNzQsImV4cCI6MjA5ODE1NzI3NH0.NaTEYCipXKpZlwyq3hmQyQ-tKS0BTVqWtQt27qp8ZKA';

const log = document.getElementById('log');
function add(msg, cls='info'){ log.innerHTML += `\n<span class="${cls}">${msg}</span>`; }

log.innerHTML = '';
add('1. Démarrage du test...', 'info');

let sb;
try {
  if(typeof supabase === 'undefined'){
    add('❌ ERREUR: la librairie Supabase n\'a pas chargé (problème internet ou CDN bloqué)', 'err');
  } else {
    add('2. ✓ Librairie Supabase chargée', 'ok');
    const { createClient } = supabase;
    sb = createClient(SUPA_URL, SUPA_KEY);
    add('3. ✓ Client Supabase créé', 'ok');

    // Test lecture
    sb.from('categories').select('*').then(({data,error})=>{
      if(error){ add('4. ❌ Lecture échouée: '+error.message, 'err'); }
      else { add('4. ✓ Lecture OK — '+(data?.length||0)+' catégorie(s) existante(s)', 'ok'); }
    });
  }
} catch(e){
  add('❌ ERREUR init: '+e.message, 'err');
}

document.getElementById('test-btn').addEventListener('click', async ()=>{
  const name = document.getElementById('cat-name').value.trim();
  if(!name){ add('⚠️ Entre un nom d\'abord', 'err'); return; }
  if(!sb){ add('❌ Client Supabase non initialisé', 'err'); return; }
  add('--- Test création: "'+name+'" ---', 'info');
  try {
    const { data, error } = await sb.from('categories').insert({name}).select();
    if(error){
      add('❌ ÉCHEC: '+error.message, 'err');
      add('Code: '+(error.code||'?')+' | Détails: '+(error.details||'aucun'), 'err');
    } else {
      add('✅ SUCCÈS ! Catégorie créée: '+JSON.stringify(data), 'ok');
    }
  } catch(e){
    add('❌ EXCEPTION: '+e.message, 'err');
  }
});
</script>
</body>
</html>
