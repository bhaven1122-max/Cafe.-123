<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Aesthetic Smart Cafe SaaS Platform</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Plus Jakarta Sans', sans-serif; background-color: #FBF9F5; color: #1C130E; }
    .no-scrollbar::-webkit-scrollbar { display: none; }
    .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    @keyframes pulse-border { 0%, 100% { border-color: #ef4444; } 50% { border-color: transparent; } }
    .animate-pulse-red { animation: pulse-border 1.5s infinite; }
  </style>
</head>
<body class="min-h-screen pb-24">

  <div id="app">
    <div class="min-h-screen flex flex-col items-center justify-center font-bold text-amber-800 bg-[#FBF9F5]">
      <div class="w-10 h-10 border-4 border-amber-600 border-t-transparent rounded-full animate-spin mb-3"></div>
      Loading Aesthetic Cafe Cloud... ☕
    </div>
  </div>

  <script>
    const SUPABASE_URL = "https://qmrqlxyykagdyvsqvifv.supabase.co";
    const SUPABASE_KEY = "sb_secret_bXtBrKJY7SWVN0lySJCy-A_79B3tD7V";
    const supabaseClient = window.supabase.createClient(SUPABASE_URL, SUPABASE_KEY);

    const SUPER_ADMIN_PIN = "9999";

    const defaultMenuTemplate = [
      { id: 1, name: "Signature Hazelnut Cold Coffee", category: "Coffee", price: 149, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1517701604599-bb29b565090c?w=500&q=80" },
      { id: 2, name: "Classic Caramel Frappe", category: "Coffee", price: 159, is_veg: true, is_bestseller: false, in_stock: true, img: "https://images.unsplash.com/photo-1572490122747-3968b75cc699?w=500&q=80" },
      { id: 3, name: "Hot Cappuccino with Cocoa Dust", category: "Coffee", price: 119, is_veg: true, is_bestseller: false, in_stock: true, img: "https://images.unsplash.com/photo-1534778101976-62847782c213?w=500&q=80" },
      { id: 4, name: "Belgian Dark Chocolate Shake", category: "Coffee", price: 169, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1577805947697-89e18249d767?w=500&q=80" },
      { id: 5, name: "Kulhad Masala Adrak Chai", category: "Chai & Coolers", price: 49, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1561336313-0bd5e0b27ec8?w=500&q=80" },
      { id: 6, name: "Maharaja Double Cheese Burger", category: "Burgers & Sandwiches", price: 169, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=500&q=80" },
      { id: 7, name: "Tandoori Paneer Tikka Sandwich", category: "Burgers & Sandwiches", price: 159, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1528735602780-2552fd46c7af?w=500&q=80" },
      { id: 8, name: "Farmhouse Loaded Cheese Pizza [8 Inch]", category: "Pizza & Pasta", price: 249, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1513104890138-7c749659a591?w=500&q=80" },
      { id: 9, name: "Kurkure Cheese Burst Paneer Momos", category: "Snacks & Momos", price: 149, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1625220194771-7ebdea0b70b9?w=500&q=80" },
      { id: 10, name: "Sizzling Hot Chocolate Walnut Brownie", category: "Desserts", price: 179, is_veg: true, is_bestseller: true, in_stock: true, img: "https://images.unsplash.com/photo-1606313564200-e75d5e30476c?w=500&q=80" }
    ];

    const initialSaaSData = {
      gemini_api_key: "",
      cafes: {
        "sukoon": {
          slug: "sukoon",
          is_active: true,
          cafe_name: "Sukoon The Cafe",
          tagline: "Sip, Bite & Find Your Sukoon",
          upi_id: "sukooncafe@upi",
          whatsapp_number: "919876543210",
          chef_pin: "1122",
          owner_pin: "8899",
          total_tables: 12,
          google_review_link: "https://g.page/r/sukoon-cafe/review",
          rush_hour_discount: false,
          loyalty_target: 5,
          loyalty_reward: "Free Sizzling Brownie or Cold Coffee",
          menu: JSON.parse(JSON.stringify(defaultMenuTemplate)),
          orders: []
        }
      }
    };

    let saasDB = null;
    let customerStamps = parseInt(localStorage.getItem("customer_stamps") || "0");

    async function loadFromCloud() {
      try {
        const { data } = await supabaseClient.from('cafe_saas_store').select('*').eq('id', 'main_db').single();
        if (data && data.data) saasDB = data.data;
        else { saasDB = initialSaaSData; await saveToCloud(); }
      } catch (err) {
        saasDB = JSON.parse(localStorage.getItem("multi_cafe_saas_db")) || initialSaaSData;
      }
      initApp();
    }

    async function saveToCloud() {
      if (!saasDB) return;
      localStorage.setItem("multi_cafe_saas_db", JSON.stringify(saasDB));
      try {
        await supabaseClient.from('cafe_saas_store').upsert({ id: 'main_db', data: saasDB, updated_at: new Date() });
      } catch (err) {}
    }

    const urlParams = new URLSearchParams(window.location.search);
    let activeCafeSlug = (urlParams.get("cafe") || "sukoon").toLowerCase();
    let currentTable = urlParams.get("table") || "1";

    function currentCafe() {
      if (!saasDB || !saasDB.cafes) return initialSaaSData.cafes["sukoon"];
      if (!saasDB.cafes[activeCafeSlug]) activeCafeSlug = Object.keys(saasDB.cafes)[0] || "sukoon";
      return saasDB.cafes[activeCafeSlug];
    }

    let cart = {};
    let selectedCategory = "All";
    let searchQuery = "";
    let bestsellerOnly = false;
    let activeOrderId = null;
    let cartStep = 0;
    let customerName = "";
    let paymentMode = "COUNTER";
    let soundEnabled = false;
    let pinUnlocked = false;
    let ownerTab = "sales";
    let showScannerModal = false;
    let isScanningMenu = false;
    let bulkMenuText = "";

    function getAutoFoodImage(nameOrCat) {
      const q = (nameOrCat || "").toLowerCase();
      if (q.includes("coffee") || q.includes("latte") || q.includes("shake")) return "https://images.unsplash.com/photo-1517701604599-bb29b565090c?w=500&q=80";
      if (q.includes("chai") || q.includes("tea") || q.includes("mojito")) return "https://images.unsplash.com/photo-1561336313-0bd5e0b27ec8?w=500&q=80";
      if (q.includes("burger") || q.includes("sandwich")) return "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=500&q=80";
      if (q.includes("pizza") || q.includes("pasta")) return "https://images.unsplash.com/photo-1513104890138-7c749659a591?w=500&q=80";
      return "https://images.unsplash.com/photo-1504674900247-0877df9cc836?w=500&q=80";
    }

    function setupRealtimeSync() {
      supabaseClient.channel('public:cafe_saas_store')
        .on('postgres_changes', { event: 'UPDATE', schema: 'public', table: 'cafe_saas_store' }, payload => {
          if (payload.new && payload.new.data) {
            const oldLen = currentCafe().orders.length;
            saasDB = payload.new.data;
            const newLen = currentCafe().orders.length;
            if (newLen > oldLen && soundEnabled) playKitchenBell();
            render();
          }
        }).subscribe();
    }

    function playKitchenBell() {
      try {
        const ctx = new (window.AudioContext || window.webkitAudioContext)();
        const playTone = (freq, start, duration) => {
          const osc = ctx.createOscillator(); const gain = ctx.createGain();
          osc.type = "sine"; osc.frequency.setValueAtTime(freq, ctx.currentTime + start);
          gain.gain.setValueAtTime(0.4, ctx.currentTime + start);
          gain.gain.exponentialRampToValueAtTime(0.001, ctx.currentTime + start + duration);
          osc.connect(gain); gain.connect(ctx.destination);
          osc.start(ctx.currentTime + start); osc.stop(ctx.currentTime + start + duration);
        };
        playTone(880, 0, 0.35); playTone(660, 0.3, 0.6);
      } catch (e) {}
    }

    function getDiscountedPrice(price) {
      return currentCafe().rush_hour_discount ? Math.round(price * 0.9) : price;
    }

    function getRoute() {
      const mode = urlParams.get("mode");
      const hash = window.location.hash;
      if (mode === "superadmin" || hash === "#superadmin") return "SUPERADMIN";
      if (mode === "kitchen" || hash === "#kitchen-kds") return "KDS";
      if (mode === "owner" || hash === "#owner-boss") return "OWNER";
      return "CUSTOMER";
    }

    function renderScannerModal() {
      if (!showScannerModal) return "";
      return `
        <div class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm flex items-center justify-center p-4">
          <div class="bg-white text-stone-900 w-full max-w-lg rounded-3xl p-6 shadow-2xl border border-stone-100">
            <div class="flex justify-between items-center pb-3 border-b">
              <h3 class="text-base font-extrabold text-amber-800">📸 AI Menu Photo Scanner</h3>
              <button onclick="showScannerModal=false; render()" class="text-stone-400 font-bold text-lg">✕</button>
            </div>
            <div class="my-4 p-4 bg-amber-50/60 border-2 border-amber-300 border-dashed rounded-2xl text-center">
              <input type="password" placeholder="Gemini API Key" value="${saasDB.gemini_api_key || ''}" onchange="saasDB.gemini_api_key=this.value.trim(); saveToCloud()" class="w-full border rounded-xl px-3 py-2 text-xs mb-3 bg-white" />
              <label class="cursor-pointer inline-block bg-[#1C130E] text-amber-400 font-extrabold text-xs px-5 py-3 rounded-xl shadow">
                ${isScanningMenu ? '⏳ Reading Photo...' : 'Upload Menu Photo'}
                <input type="file" accept="image/*" capture="environment" class="hidden" onchange="handleMenuPhotoUpload(event)" />
              </label>
            </div>
            <textarea id="bulkMenuInput" rows="4" oninput="bulkMenuText=this.value" placeholder="Category | Dish Name | Price" class="w-full border rounded-xl p-3 text-xs font-mono">${bulkMenuText}</textarea>
            <div class="flex gap-2 mt-4">
              <button onclick="importBulkMenu(false)" class="flex-1 bg-amber-700 hover:bg-amber-800 text-white font-extrabold py-3 rounded-xl text-xs shadow">➕ Add to Menu</button>
              <button onclick="importBulkMenu(true)" class="flex-1 bg-[#1C130E] text-amber-400 font-extrabold py-3 rounded-xl text-xs shadow">🔄 Replace Full</button>
            </div>
          </div>
        </div>
      `;
    }

    async function handleMenuPhotoUpload(event) {
      const file = event.target.files[0];
      if (!file) return;
      if (!saasDB.gemini_api_key) return alert("Enter Gemini API Key first!");
      isScanningMenu = true; render();
      try {
        const base64Data = await new Promise((resolve, reject) => {
          const reader = new FileReader();
          reader.onload = () => resolve(reader.result.split(",")[1]);
          reader.onerror = reject;
          reader.readAsDataURL(file);
        });
        const res = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${saasDB.gemini_api_key}`, {
          method: "POST", headers: { "Content-Type": "application/json" },
          body: JSON.stringify({ contents: [{ parts: [{ text: "Extract menu items as: Category | Name | Price" }, { inline_data: { mime_type: file.type || "image/jpeg", data: base64Data } }] }] })
        });
        const d = await res.json();
        bulkMenuText = d?.candidates?.[0]?.content?.parts?.[0]?.text || "";
      } catch (e) { alert("Scan failed"); }
      isScanningMenu = false; render();
    }

    function importBulkMenu(replace) {
      const raw = (document.getElementById("bulkMenuInput")?.value || bulkMenuText).trim();
      if (!raw) return alert("Provide menu data!");
      const lines = raw.split("\n").map(l => l.trim()).filter(Boolean);
      const newItems = lines.map((l, idx) => {
        let [cat, name, price] = l.includes("|") ? l.split("|").map(p => p.trim()) : ["Specials", l, "99"];
        return { id: Date.now() + idx, name: name || l, category: cat || "Specials", price: parseInt(price) || 99, is_veg: true, is_bestseller: idx < 2, in_stock: true, img: getAutoFoodImage(cat + " " + name) };
      });
      if (replace) currentCafe().menu = newItems;
      else currentCafe().menu = [...newItems, ...currentCafe().menu];
      saveToCloud(); showScannerModal = false; bulkMenuText = ""; alert("Success!"); render();
    }

    function renderSuperAdmin() {
      if (!pinUnlocked) {
        return `
          <div class="min-h-screen bg-stone-950 text-white flex items-center justify-center p-4">
            <div class="bg-stone-900 p-8 rounded-3xl max-w-sm w-full text-center border border-amber-500/40 shadow-2xl">
              <span class="text-[10px] font-extrabold uppercase px-3 py-1 bg-amber-500 text-black rounded-full">Master Access</span>
              <h2 class="text-xl font-extrabold text-amber-400 mt-4 mb-1">🚀 Super Admin Panel</h2>
              <p class="text-xs text-stone-400 mb-6">Enter Developer PIN (9999)</p>
              <input id="superPin" type="password" maxlength="4" placeholder="••••" class="w-full text-center text-3xl tracking-widest bg-stone-800 rounded-2xl py-3 mb-4 text-white border border-stone-700 focus:outline-none focus:border-amber-500" />
              <button onclick="if(document.getElementById('superPin').value === SUPER_ADMIN_PIN){pinUnlocked=true; render();}else{alert('Wrong PIN');}" class="w-full bg-amber-500 hover:bg-amber-400 text-black font-extrabold py-3.5 rounded-2xl shadow">Unlock Master Control</button>
            </div>
          </div>
        `;
      }
      const cafeList = Object.values(saasDB.cafes);
      const baseUrl = window.location.origin + window.location.pathname;

      return `
        <div class="min-h-screen bg-stone-950 text-white p-4 sm:p-6">
          <div class="max-w-6xl mx-auto">
            <div class="bg-stone-900 p-6 rounded-3xl border border-amber-500/30 flex flex-wrap justify-between items-center gap-4 mb-6 shadow-xl">
              <div>
                <h1 class="text-2xl font-extrabold text-amber-400">🚀 Super Admin Control Center</h1>
                <p class="text-xs text-stone-400">Complete setup & credential management for all cafes</p>
              </div>
              <span class="text-xs bg-stone-800 px-4 py-2 rounded-xl border border-stone-700">Total Active Cafes: <b class="text-amber-400">${cafeList.length}</b></span>
            </div>

            <!-- Full Setup Wizard for New Cafe -->
            <div class="bg-stone-900 p-6 rounded-3xl border border-stone-800 mb-8 shadow-xl">
              <h2 class="text-base font-extrabold text-amber-400 mb-4">➕ Launch New Cafe (Complete Setup Wizard)</h2>
              <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-3 mb-3">
                <input id="newSlug" type="text" placeholder="Cafe ID (e.g. moonlight)" class="bg-stone-800 border border-stone-700 rounded-xl px-3 py-3 text-xs text-white" />
                <input id="newName" type="text" placeholder="Cafe Name" class="bg-stone-800 border border-stone-700 rounded-xl px-3 py-3 text-xs text-white" />
                <input id="newUpi" type="text" placeholder="UPI ID (e.g. cafe@upi)" class="bg-stone-800 border border-stone-700 rounded-xl px-3 py-3 text-xs text-white" />
                <input id="newPhone" type="text" placeholder="WhatsApp Number" class="bg-stone-800 border border-stone-700 rounded-xl px-3 py-3 text-xs text-white" />
              </div>
              <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
                <input id="newChefPin" type="text" maxlength="4" placeholder="Chef PIN (e.g. 1122)" class="bg-stone-800 border border-stone-700 rounded-xl px-3 py-3 text-xs text-white" />
                <input id="newOwnerPin" type="text" maxlength="4" placeholder="Owner PIN (e.g. 8899)" class="bg-stone-800 border border-stone-700 rounded-xl px-3 py-3 text-xs text-white" />
                <button onclick="createNewCafeClient()" class="bg-amber-500 hover:bg-amber-400 text-black font-extrabold rounded-xl py-3 text-xs shadow">⚡ Create Cafe Website</button>
              </div>
            </div>

            <div class="space-y-4">
              ${cafeList.map(c => `
                <div class="bg-stone-900 rounded-3xl p-6 border border-stone-800 shadow-lg">
                  <div class="flex flex-wrap justify-between items-start gap-4 pb-4 border-b border-stone-800">
                    <div>
                      <div class="flex items-center gap-2">
                        <h3 class="text-xl font-extrabold text-white">${c.cafe_name}</h3>
                        <span class="text-[11px] font-mono bg-stone-800 text-amber-400 px-2.5 py-0.5 rounded-full">ID: ${c.slug}</span>
                      </div>
                      <p class="text-xs text-stone-400 mt-1">UPI: <b>${c.upi_id}</b> • Chef PIN: <b class="text-green-400 font-mono">${c.chef_pin}</b> • Owner PIN: <b class="text-purple-400 font-mono">${c.owner_pin}</b></p>
                    </div>
                    <div class="flex gap-2">
                      <button onclick="activeCafeSlug='${c.slug}'; showScannerModal=true; render()" class="bg-amber-500 text-black px-3.5 py-2 rounded-xl text-xs font-bold shadow">📸 Scan Menu</button>
                      <button onclick="toggleCafeActive('${c.slug}')" class="px-3.5 py-2 rounded-xl text-xs font-bold ${c.is_active ? 'bg-red-950 text-red-300 border border-red-800' : 'bg-green-700 text-white'}">${c.is_active ? 'Suspend' : 'Activate'}</button>
                    </div>
                  </div>

                  <!-- Quick Credential & PIN Editor for Super Admin -->
                  <div class="my-4 p-4 bg-stone-950 rounded-2xl border border-stone-800 flex flex-wrap gap-4 items-center justify-between text-xs">
                    <div>
                      <span class="text-stone-400">Update Pins & UPI for ${c.cafe_name}:</span>
                    </div>
                    <div class="flex flex-wrap gap-2 items-center">
                      <input id="up_chef_${c.slug}" type="text" maxlength="4" value="${c.chef_pin}" placeholder="Chef PIN" class="bg-stone-900 border border-stone-700 px-2 py-1.5 rounded-lg text-center w-20 text-white font-mono" />
                      <input id="up_owner_${c.slug}" type="text" maxlength="4" value="${c.owner_pin}" placeholder="Owner PIN" class="bg-stone-900 border border-stone-700 px-2 py-1.5 rounded-lg text-center w-20 text-white font-mono" />
                      <button onclick="updateCafePins('${c.slug}')" class="bg-stone-800 hover:bg-stone-700 text-amber-400 px-3 py-1.5 rounded-lg font-bold">💾 Save Pins</button>
                    </div>
                  </div>

                  <div class="grid grid-cols-1 md:grid-cols-3 gap-3 text-xs">
                    <div class="bg-stone-950 p-3 rounded-2xl border border-stone-800">
                      <div class="font-bold text-amber-400 mb-1">Customer Menu</div>
                      <a href="${baseUrl}?cafe=${c.slug}&table=1" target="_blank" class="block text-center bg-amber-600/20 text-amber-300 py-2 rounded-xl font-bold">Open Menu ↗</a>
                    </div>
                    <div class="bg-stone-950 p-3 rounded-2xl border border-stone-800">
                      <div class="font-bold text-green-400 mb-1">Kitchen KDS</div>
                      <a href="${baseUrl}?cafe=${c.slug}&mode=kitchen" target="_blank" class="block text-center bg-green-600/20 text-green-300 py-2 rounded-xl font-bold">Open KDS ↗</a>
                    </div>
                    <div class="bg-stone-950 p-3 rounded-2xl border border-stone-800">
                      <div class="font-bold text-purple-400 mb-1">Owner Panel</div>
                      <a href="${baseUrl}?cafe=${c.slug}&mode=owner" target="_blank" class="block text-center bg-purple-600/20 text-purple-300 py-2 rounded-xl font-bold">Open Panel ↗</a>
                    </div>
                  </div>
                </div>
              `).join('')}
            </div>
          </div>
        </div>
        ${renderScannerModal()}
      `;
    }

    function createNewCafeClient() {
      const slug = (document.getElementById("newSlug").value || "").trim().toLowerCase().replace(/[^a-z0-9]/g, "");
      const name = (document.getElementById("newName").value || "").trim();
      const upi = (document.getElementById("newUpi").value || "").trim() || "merchant@upi";
      const phone = (document.getElementById("newPhone").value || "").trim() || "919876543210";
      const chefPin = (document.getElementById("newChefPin").value || "").trim() || "1122";
      const ownerPin = (document.getElementById("newOwnerPin").value || "").trim() || "8899";

      if (!slug || !name) return alert("Fill Cafe ID and Name!");
      if (saasDB.cafes[slug]) return alert("Cafe ID already exists!");

      saasDB.cafes[slug] = {
        slug, is_active: true, cafe_name: name, tagline: "Fresh Food & Quick Ordering", upi_id: upi, whatsapp_number: phone,
        chef_pin: chefPin, owner_pin: ownerPin, total_tables: 15, google_review_link: "https://google.com",
        rush_hour_discount: false, loyalty_target: 5, loyalty_reward: "Free Sizzling Brownie or Cold Coffee",
        menu: JSON.parse(JSON.stringify(defaultMenuTemplate)), orders: []
      };
      saveToCloud(); render();
      alert(`🎉 Cafe "${name}" launched successfully!`);
    }

    function updateCafePins(slug) {
      const newChef = document.getElementById(`up_chef_${slug}`).value.trim();
      const newOwner = document.getElementById(`up_owner_${slug}`).value.trim();
      if (!newChef || !newOwner) return alert("Pins cannot be empty!");
      saasDB.cafes[slug].chef_pin = newChef;
      saasDB.cafes[slug].owner_pin = newOwner;
      saveToCloud();
      alert("🔒 Pins updated securely by Super Admin!");
      render();
    }

    function toggleCafeActive(slug) {
      if (saasDB.cafes[slug]) {
        saasDB.cafes[slug].is_active = !saasDB.cafes[slug].is_active;
        saveToCloud(); render();
      }
    }

    function renderCustomer() {
      const cafe = currentCafe();
      if (!cafe.is_active) return `<div class="min-h-screen flex items-center justify-center p-6 text-center font-bold text-red-600 bg-[#FBF9F5]">⚠️ This cafe service is currently paused.</div>`;

      const menu = cafe.menu;
      const categories = ["All", ...new Set(menu.map(i => i.category))];
      const filtered = menu.filter(item => (selectedCategory === "All" || item.category === selectedCategory) && item.name.toLowerCase().includes(searchQuery.toLowerCase()) && (!bestsellerOnly || item.is_bestseller));
      const cartItems = Object.values(cart);
      const totalQty = cartItems.reduce((s, i) => s + i.qty, 0);
      const subtotal = cartItems.reduce((s, i) => s + (getDiscountedPrice(i.price) * i.qty), 0);
      const grandTotal = subtotal + Math.round(subtotal * 0.05);
      const activeOrder = cafe.orders.find(o => o.id === activeOrderId);

      return `
        <!-- Aesthetic Header -->
        <header class="sticky top-0 z-30 bg-[#1C130E] text-[#FBF9F5] px-4 py-3.5 shadow-xl">
          <div class="max-w-xl mx-auto flex items-center justify-between">
            <div>
              <h1 class="text-base font-extrabold tracking-wide text-amber-400">${cafe.cafe_name}</h1>
              <p class="text-[11px] text-stone-300">⭐ ${customerStamps}/${cafe.loyalty_target} Loyalty Stamps Collected</p>
            </div>
            <div class="flex items-center gap-1.5 bg-stone-800/90 px-3 py-1.5 rounded-full border border-amber-500/30 shadow-inner">
              <span class="text-xs font-bold text-amber-300">Table</span>
              <select onchange="currentTable=this.value; render()" class="bg-transparent text-white text-xs font-extrabold focus:outline-none cursor-pointer">
                ${Array.from({length: cafe.total_tables}, (_, i) => `<option value="${i+1}" class="text-black" ${currentTable == i+1 ? 'selected' : ''}>#${i+1}</option>`).join('')}
              </select>
            </div>
          </div>
          ${customerStamps >= cafe.loyalty_target ? `<div class="max-w-xl mx-auto mt-2 bg-gradient-to-r from-emerald-600 to-teal-600 text-white text-xs font-bold px-3 py-1.5 rounded-xl text-center shadow">🎉 Reward Unlocked! Claim: ${cafe.loyalty_reward}</div>` : ''}
        </header>

        <main class="max-w-xl mx-auto px-4 pt-4">
          ${activeOrder ? `
            <div class="mb-6 bg-white rounded-3xl p-4 shadow-md border-2 border-amber-500">
              <div class="flex justify-between items-center mb-2">
                <span class="text-xs font-extrabold bg-amber-100 text-amber-900 px-3 py-1 rounded-full">Order #${activeOrder.order_number} • Table ${activeOrder.table_number}</span>
                <button onclick="activeOrderId=null; render()" class="text-xs text-stone-400 font-bold underline">Dismiss</button>
              </div>
              <div class="grid grid-cols-3 gap-2 my-3 text-center text-xs">
                <div class="p-2.5 rounded-2xl ${activeOrder.order_status === 'new' ? 'bg-amber-600 text-white font-bold shadow' : 'bg-stone-100 text-stone-500'}">1. 🔔 Sent</div>
                <div class="p-2.5 rounded-2xl ${activeOrder.order_status === 'preparing' ? 'bg-amber-600 text-white font-bold shadow' : 'bg-stone-100 text-stone-500'}">2. 👨‍🍳 Preparing</div>
                <div class="p-2.5 rounded-2xl ${activeOrder.order_status === 'ready' ? 'bg-green-600 text-white font-bold shadow' : 'bg-stone-100 text-stone-500'}">3. 🍽️ Ready!</div>
              </div>
              <a href="${cafe.google_review_link}" target="_blank" class="block text-center bg-amber-50 text-amber-900 border border-amber-300 text-xs font-bold py-2.5 rounded-2xl mt-3 shadow-sm">⭐ Rate us on Google & Get Rewards!</a>
            </div>
          ` : ''}

          <div class="flex gap-2 mb-3">
            <input type="text" placeholder="Search delicious food..." value="${searchQuery}" oninput="searchQuery=this.value; render()" class="flex-1 bg-white px-4 py-3 rounded-2xl border border-stone-200 text-xs shadow-sm focus:outline-none focus:border-amber-600" />
            <button onclick="bestsellerOnly=!bestsellerOnly; render()" class="px-4 py-3 rounded-2xl text-xs font-extrabold border shadow-sm ${bestsellerOnly ? 'bg-amber-700 text-white border-amber-700' : 'bg-white text-stone-700 border-stone-200'}">🔥 Hot</button>
          </div>

          <div class="flex gap-2 overflow-x-auto no-scrollbar pb-3 mb-2">
            ${categories.map(cat => `<button onclick="selectedCategory='${cat}'; render()" class="whitespace-nowrap px-4 py-2.5 rounded-full text-xs font-bold shadow-sm ${selectedCategory === cat ? 'bg-[#1C130E] text-amber-400' : 'bg-white text-stone-700 border border-stone-200'}">${cat}</button>`).join('')}
          </div>

          <!-- Aesthetic Food Grid / List -->
          <div class="space-y-3.5">
            ${filtered.map(item => {
              const inCart = cart[item.id]?.qty || 0;
              return `
                <div class="bg-white rounded-3xl p-3.5 shadow-sm border border-stone-200/70 flex gap-3.5 items-center transition hover:shadow-md">
                  <img src="${item.img}" class="w-20 h-20 rounded-2xl object-cover bg-stone-100 flex-shrink-0 shadow-inner" />
                  <div class="flex-1 min-w-0">
                    <div class="flex items-center gap-1.5 mb-0.5">
                      <span class="w-3 h-3 border border-green-600 flex items-center justify-center rounded-sm"><span class="w-1.5 h-1.5 bg-green-600 rounded-full"></span></span>
                      ${item.is_bestseller ? `<span class="text-[10px] font-extrabold bg-amber-100 text-amber-800 px-2 py-0.5 rounded-full">🔥 Bestseller</span>` : ''}
                    </div>
                    <h3 class="font-extrabold text-sm text-stone-900 truncate">${item.name}</h3>
                    <p class="font-extrabold text-base text-stone-900 mt-1">₹${getDiscountedPrice(item.price)}</p>
                  </div>
                  <div>
                    ${inCart === 0 ? `<button onclick="updateCart(${item.id}, 1)" class="bg-amber-50 hover:bg-amber-100 text-amber-900 border border-amber-500 font-extrabold text-xs px-4 py-2.5 rounded-2xl shadow-sm">+ ADD</button>` : `<div class="flex items-center bg-[#1C130E] text-white rounded-2xl overflow-hidden shadow"><button onclick="updateCart(${item.id}, -1)" class="px-3 py-2 font-bold text-amber-400">-</button><span class="px-2.5 text-xs font-extrabold">${inCart}</span><button onclick="updateCart(${item.id}, 1)" class="px-3 py-2 font-bold text-amber-400">+</button></div>`}
                  </div>
                </div>
              `;
            }).join('')}
          </div>
        </main>

        ${totalQty > 0 ? `<button onclick="cartStep=1; render()" class="fixed left-4 bottom-4 z-40 bg-[#1C130E] text-white px-6 py-4 rounded-2xl shadow-2xl border-2 border-amber-500 flex items-center justify-between gap-4"><div class="text-left"><div class="text-[10px] text-amber-400 font-extrabold uppercase tracking-wider">${totalQty} Item${totalQty > 1 ? 's' : ''} in Cart</div><div class="text-sm font-extrabold">₹${grandTotal}</div></div><span class="text-amber-400 font-extrabold text-sm">View Cart ➔</span></button>` : ''}

        ${cartStep > 0 ? `
          <div class="fixed inset-0 z-50 bg-black/70 backdrop-blur-sm flex items-end justify-center p-0 sm:p-4">
            <div class="bg-white w-full max-w-lg rounded-t-3xl sm:rounded-3xl p-6 shadow-2xl">
              ${cartStep === 1 ? `
                <div class="flex justify-between items-center pb-3 border-b"><h2 class="font-extrabold text-base text-stone-900">Review Order (Table #${currentTable})</h2><button onclick="cartStep=0; render()" class="text-xl font-bold">✕</button></div>
                <div class="divide-y my-3 max-h-60 overflow-y-auto">
                  ${cartItems.map(i => `<div class="py-2.5 flex justify-between text-sm"><span>${i.qty}x ${i.name}</span><b class="text-stone-900">₹${getDiscountedPrice(i.price) * i.qty}</b></div>`).join('')}
                </div>
                <input type="text" placeholder="Your Name (Optional)" value="${customerName}" oninput="customerName=this.value" class="w-full border border-stone-200 rounded-2xl px-4 py-3 text-xs mb-4 focus:outline-none focus:border-amber-600" />
                <button onclick="cartStep=2; render()" class="w-full bg-amber-700 hover:bg-amber-800 text-white font-extrabold py-3.5 rounded-2xl text-xs shadow">Proceed to Payment ➔</button>
              ` : `
                <div class="flex justify-between items-center pb-3 border-b"><h2 class="font-extrabold text-base text-stone-900">Payment & Confirm</h2><button onclick="cartStep=1; render()" class="text-xs text-amber-800 font-bold">← Back</button></div>
                <div class="my-4 space-y-3 text-xs">
                  <label class="flex items-center gap-3 p-3.5 border-2 rounded-2xl cursor-pointer hover:border-amber-600"><input type="radio" name="pay" checked onchange="paymentMode='COUNTER'" /> Pay at Counter / After Meal</label>
                  <label class="flex items-center gap-3 p-3.5 border-2 rounded-2xl cursor-pointer hover:border-amber-600"><input type="radio" name="pay" onchange="paymentMode='UPI'" /> Pay Now via Direct UPI (₹${grandTotal})</label>
                </div>
                <button onclick="placeFinalOrder(${subtotal}, ${grandTotal})" class="w-full bg-[#1C130E] text-amber-400 font-extrabold py-4 rounded-2xl text-sm shadow-xl">🔔 Confirm & Send to Kitchen</button>
              `}
            </div>
          </div>
        ` : ''}
      `;
    }

    function updateCart(id, delta) {
      const item = currentCafe().menu.find(x => x.id === id);
      if (!item) return;
      if (!cart[id]) cart[id] = { ...item, qty: 0 };
      cart[id].qty += delta;
      if (cart[id].qty <= 0) delete cart[id];
      render();
    }

    function placeFinalOrder(subtotal, total) {
      const cafe = currentCafe();
      const newOrder = {
        id: "ord_" + Date.now(), order_number: Math.floor(100 + Math.random() * 900), table_number: currentTable,
        customer_name: customerName || "Guest", items: Object.values(cart).map(i => ({ name: i.name, price: getDiscountedPrice(i.price), qty: i.qty })),
        total_amount: total, payment_method: paymentMode, order_status: "new", created_at: new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' })
      };
      cafe.orders.unshift(newOrder);
      activeOrderId = newOrder.id;
      
      customerStamps += 1;
      localStorage.setItem("customer_stamps", customerStamps);

      cart = {}; cartStep = 0; saveToCloud(); render();
    }

    function renderKDS() {
      const cafe = currentCafe();
      if (!pinUnlocked) {
        return `
          <div class="min-h-screen bg-[#1C130E] text-white flex items-center justify-center p-4">
            <div class="bg-stone-900 p-8 rounded-3xl max-w-sm w-full text-center border border-stone-800 shadow-2xl">
              <h2 class="text-xl font-extrabold text-amber-400 mb-1">👨‍🍳 Kitchen KDS</h2>
              <p class="text-xs text-stone-400 mb-6">Enter secure Chef PIN provided by Admin</p>
              <input id="pinInput" type="password" maxlength="4" placeholder="••••" class="w-full text-center text-3xl tracking-widest bg-stone-800 rounded-2xl py-3 mb-4 text-white border border-stone-700 focus:outline-none focus:border-amber-500" />
              <button onclick="if(document.getElementById('pinInput').value === '${cafe.chef_pin}'){pinUnlocked=true; render();}else{alert('Wrong PIN');}" class="w-full bg-amber-600 hover:bg-amber-500 py-3.5 rounded-2xl font-extrabold text-black">Unlock Kitchen</button>
            </div>
          </div>
        `;
      }
      return `
        <div class="min-h-screen bg-stone-950 text-white p-4 sm:p-6">
          <div class="max-w-6xl mx-auto flex justify-between items-center pb-4 border-b border-stone-800">
            <h1 class="text-xl font-extrabold text-amber-400">👨‍🍳 Kitchen KDS — ${cafe.cafe_name}</h1>
            <button onclick="soundEnabled=!soundEnabled; render()" class="bg-stone-800 px-4 py-2 rounded-xl text-xs font-extrabold border border-stone-700">${soundEnabled ? '🔊 Sound ON' : '🔇 Enable Kitchen Bell'}</button>
          </div>
          <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-4 mt-6">
            ${cafe.orders.length === 0 ? `<p class="text-stone-500 col-span-3 text-center py-12">No orders right now...</p>` : ''}
            ${cafe.orders.map(o => `
              <div class="bg-stone-900 rounded-3xl p-5 border-2 ${o.order_status === 'new' ? 'border-red-500 animate-pulse-red shadow-lg' : o.order_status === 'preparing' ? 'border-amber-500' : 'border-stone-800 opacity-75'}">
                <div class="flex justify-between font-extrabold text-amber-400 mb-3"><span>Table #${o.table_number}</span><span class="text-xs bg-stone-800 px-2.5 py-1 rounded-full text-stone-300">#${o.order_number}</span></div>
                <div class="divide-y divide-stone-800 text-sm mb-4">${o.items.map(i => `<div class="py-1.5 font-bold">${i.qty}x ${i.name}</div>`).join('')}</div>
                ${o.order_status === 'new' ? `<button onclick="updateOrderStatus('${o.id}', 'preparing')" class="w-full bg-amber-600 hover:bg-amber-500 text-white py-3 rounded-2xl text-xs font-extrabold shadow">Start Preparing</button>` : o.order_status === 'preparing' ? `<button onclick="updateOrderStatus('${o.id}', 'ready')" class="w-full bg-green-600 hover:bg-green-500 text-white py-3 rounded-2xl text-xs font-extrabold shadow">Mark Ready / Completed</button>` : `<span class="block text-center text-green-400 text-xs font-bold py-2 bg-stone-950 rounded-xl">✔ Completed & Saved</span>`}
              </div>
            `).join('')}
          </div>
        </div>
      `;
    }

    function updateOrderStatus(id, st) {
      const o = currentCafe().orders.find(x => x.id === id);
      if (o) { o.order_status = st; saveToCloud(); render(); }
    }

    function renderOwner() {
      const cafe = currentCafe();
      if (!pinUnlocked) {
        return `
          <div class="min-h-screen bg-[#1C130E] text-white flex items-center justify-center p-4">
            <div class="bg-stone-900 p-8 rounded-3xl max-w-sm w-full text-center border border-stone-800 shadow-2xl">
              <h2 class="text-xl font-extrabold text-amber-400 mb-1">👑 Owner Panel</h2>
              <p class="text-xs text-stone-400 mb-6">Enter secure Owner PIN provided by Admin</p>
              <input id="ownerPin" type="password" maxlength="4" placeholder="••••" class="w-full text-center text-3xl tracking-widest bg-stone-800 rounded-2xl py-3 mb-4 text-white border border-stone-700 focus:outline-none focus:border-amber-500" />
              <button onclick="if(document.getElementById('ownerPin').value === '${cafe.owner_pin}'){pinUnlocked=true; render();}else{alert('Wrong PIN');}" class="w-full bg-amber-600 hover:bg-amber-500 py-3.5 rounded-2xl font-extrabold text-black">Unlock Owner Dashboard</button>
            </div>
          </div>
        `;
      }
      const totalRev = cafe.orders.reduce((s, o) => s + o.total_amount, 0);

      return `
        <div class="max-w-5xl mx-auto p-4 sm:p-6">
          <div class="bg-[#1C130E] text-white p-5 rounded-3xl flex flex-wrap justify-between items-center gap-4 mb-6 shadow-xl">
            <div>
              <h1 class="text-lg font-extrabold text-amber-400">👑 ${cafe.cafe_name} Owner Panel</h1>
              <p class="text-xs text-stone-300">Sales Cashbook & Loyalty Rewards Manager</p>
            </div>
            <div class="flex gap-2">
              <button onclick="ownerTab='sales'; render()" class="px-4 py-2 rounded-xl text-xs font-bold ${ownerTab==='sales'?'bg-amber-500 text-black':'bg-stone-800'}">📊 Sales</button>
              <button onclick="ownerTab='loyalty'; render()" class="px-4 py-2 rounded-xl text-xs font-bold ${ownerTab==='loyalty'?'bg-amber-500 text-black':'bg-stone-800'}">🎁 Loyalty Setup</button>
            </div>
          </div>
          ${ownerTab === 'sales' ? `
            <div class="bg-white p-5 rounded-3xl border border-stone-200 mb-6 shadow-sm">
              <div class="text-xs text-stone-500 uppercase tracking-wider font-extrabold mb-1">Total Revenue Recorded</div>
              <div class="text-3xl font-extrabold text-stone-900">₹${totalRev} <span class="text-sm font-normal text-stone-500">(${cafe.orders.length} Orders)</span></div>
            </div>
            <div class="bg-white rounded-3xl p-5 border border-stone-200 shadow-sm space-y-3">
              <h3 class="font-extrabold text-sm text-stone-900">Permanent Order History (Secured)</h3>
              <div class="divide-y max-h-96 overflow-y-auto">
                ${cafe.orders.length === 0 ? `<p class="text-stone-400 text-xs py-4 text-center">No orders recorded yet.</p>` : ''}
                ${cafe.orders.map(o => `<div class="py-3 flex justify-between items-center text-xs"><div><b class="text-stone-900">Table #${o.table_number}</b> • ${o.items.map(x=>x.name).join(', ')}<div class="text-stone-400">${o.created_at}</div></div><b class="text-sm text-stone-900">₹${o.total_amount}</b></div>`).join('')}
              </div>
            </div>
          ` : `
            <div class="bg-white p-6 rounded-3xl border border-stone-200 shadow-sm space-y-4 text-xs">
              <h3 class="font-extrabold text-base text-stone-900">🎁 Loyalty Stamp Reward Setup</h3>
              <div><label class="font-bold text-stone-700">Stamps needed for Free Reward:</label><input type="number" value="${cafe.loyalty_target}" onchange="cafe.loyalty_target=parseInt(this.value)||5; saveToCloud()" class="w-full border border-stone-200 rounded-xl p-3 mt-1.5 font-bold text-sm" /></div>
              <div><label class="font-bold text-stone-700">Free Reward Description:</label><input type="text" value="${cafe.loyalty_reward}" onchange="cafe.loyalty_reward=this.value; saveToCloud()" class="w-full border border-stone-200 rounded-xl p-3 mt-1.5 font-bold text-sm" /></div>
            </div>
          `}
        </div>
      `;
    }

    function render() {
      if (!saasDB) return;
      const route = getRoute();
      const root = document.getElementById("app");
      if (route === "SUPERADMIN") root.innerHTML = renderSuperAdmin();
      else if (route === "KDS") root.innerHTML = renderKDS();
      else if (route === "OWNER") root.innerHTML = renderOwner();
      else root.innerHTML = renderCustomer();
    }

    function initApp() {
      render();
      setupRealtimeSync();
    }

    window.addEventListener("hashchange", () => { pinUnlocked = false; render(); });
    loadFromCloud();
  </script>
</body>
</html>
