# reims-volley-crm[Uploading index.ht<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CRM Reims Volley 51</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #1e293b 0%, #1e40af 50%, #1e293b 100%);
            min-height: 100vh;
            color: white;
        }

        .header {
            background: linear-gradient(90deg, #1e293b 0%, #1e40af 50%, #1e293b 100%);
            padding: 24px;
            border-bottom: 2px solid rgba(251, 191, 36, 0.2);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-section {
            display: flex;
            align-items: center;
        }

        .logo {
            width: 50px;
            height: 60px;
            background: linear-gradient(45deg, #fbbf24, #f59e0b);
            border-radius: 10px;
            margin-right: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #1e293b;
            font-size: 14px;
        }

        .title {
            background: linear-gradient(90deg, #fbbf24, #fde047, #fbbf24);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-size: 32px;
            font-weight: bold;
        }

        .subtitle {
            color: #bfdbfe;
            margin-top: 4px;
        }

        .controls {
            display: flex;
            gap: 12px;
            align-items: center;
        }

        .search-box {
            padding: 10px 16px;
            background: rgba(51, 65, 85, 0.5);
            border: 1px solid rgba(59, 130, 246, 0.3);
            border-radius: 8px;
            color: white;
            outline: none;
            width: 200px;
        }

        .btn {
            padding: 10px 16px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .btn-primary {
            background: linear-gradient(90deg, #f59e0b, #fbbf24);
            color: #1e293b;
        }

        .btn-primary:hover {
            background: linear-gradient(90deg, #f97316, #f59e0b);
        }

        .btn-secondary {
            background: rgba(59, 130, 246, 0.8);
            color: white;
        }

        .btn-secondary:hover {
            background: rgba(59, 130, 246, 1);
        }

        .main-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 24px;
        }

        .tabs {
            background: rgba(51, 65, 85, 0.3);
            border-radius: 12px;
            padding: 8px;
            margin-bottom: 24px;
            display: flex;
            gap: 8px;
        }

        .tab {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            background: transparent;
            color: #bfdbfe;
            cursor: pointer;
            transition: all 0.2s;
            font-weight: 500;
        }

        .tab.active {
            background: linear-gradient(90deg, #f59e0b, #fbbf24);
            color: #1e293b;
        }

        .tab:hover:not(.active) {
            background: rgba(51, 65, 85, 0.5);
            color: white;
        }

        .filters {
            background: rgba(51, 65, 85, 0.4);
            border: 1px solid rgba(59, 130, 246, 0.2);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 24px;
        }

        .filters h4 {
            color: #fbbf24;
            margin-bottom: 16px;
            font-size: 14px;
        }

        .filter-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 16px;
            margin-bottom: 16px;
        }

        .filter-input, .filter-select {
            padding: 12px;
            background: rgba(51, 65, 85, 0.6);
            border: 1px solid rgba(59, 130, 246, 0.3);
            border-radius: 8px;
            color: white;
            outline: none;
            font-size: 14px;
        }

        .filter-input::placeholder {
            color: #94a3b8;
        }

        .card {
            background: linear-gradient(135deg, rgba(51, 65, 85, 0.8), rgba(71, 85, 105, 0.8));
            border: 1px solid rgba(59, 130, 246, 0.2);
            border-radius: 12px;
            padding: 24px;
            margin-bottom: 16px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 16px;
        }

        .card-title {
            font-size: 20px;
            font-weight: 600;
            color: white;
            margin-bottom: 12px;
        }

        .badge {
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            margin-left: 12px;
        }

        .badge-prospect { background: #f3f4f6; color: #374151; }
        .badge-contacte { background: #dbeafe; color: #1e40af; }
        .badge-rencontre { background: #e0e7ff; color: #3730a3; }
        .badge-negociation { background: #fef3c7; color: #92400e; }
        .badge-partenaire { background: #d1fae5; color: #065f46; }
        .badge-mecene { 
            background: linear-gradient(90deg, #fef3c7, #fde68a); 
            color: #92400e; 
            font-weight: bold;
        }
        .badge-refuse { background: #fee2e2; color: #991b1b; }

        .badge-montant {
            background: linear-gradient(90deg, rgba(251, 191, 36, 0.2), rgba(253, 224, 71, 0.2));
            color: #fbbf24;
            border: 1px solid rgba(251, 191, 36, 0.3);
        }

        .card-info {
            display: grid;
            gap: 8px;
            color: #bfdbfe;
            font-size: 14px;
        }

        .info-row {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .card-actions {
            display: flex;
            gap: 8px;
        }

        .btn-icon {
            padding: 8px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.2s;
            color: #94a3b8;
        }

        .btn-icon:hover {
            background: rgba(51, 65, 85, 0.5);
            color: #fbbf24;
        }

        .btn-delete:hover {
            color: #ef4444;
        }

        .modal {
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(5px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }

        .modal-content {
            background: linear-gradient(135deg, #1e293b, #374151);
            border: 1px solid rgba(251, 191, 36, 0.3);
            border-radius: 16px;
            padding: 24px;
            width: 90%;
            max-width: 500px;
            max-height: 90vh;
            overflow-y: auto;
        }

        .modal-title {
            color: white;
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 16px;
        }

        .form-input, .form-select, .form-textarea {
            width: 100%;
            padding: 12px;
            background: rgba(51, 65, 85, 0.5);
            border: 1px solid rgba(59, 130, 246, 0.3);
            border-radius: 8px;
            color: white;
            outline: none;
            font-size: 14px;
        }

        .form-textarea {
            height: 80px;
            resize: vertical;
        }

        .form-input::placeholder, .form-textarea::placeholder {
            color: #94a3b8;
        }

        .modal-actions {
            display: flex;
            justify-content: flex-end;
            gap: 12px;
            margin-top: 24px;
        }

        .status-bar {
            background: rgba(51, 65, 85, 0.2);
            border: 1px solid rgba(59, 130, 246, 0.1);
            border-radius: 8px;
            padding: 12px;
            text-align: center;
            font-size: 12px;
            color: #94a3b8;
            margin-top: 24px;
        }

        .status-highlight {
            color: #fbbf24;
            font-weight: 600;
        }

        .empty-state {
            text-align: center;
            padding: 48px 24px;
            color: #94a3b8;
        }

        .empty-state h3 {
            font-size: 18px;
            margin-bottom: 8px;
            color: #bfdbfe;
        }

        .hidden {
            display: none;
        }

        .message {
            background: rgba(51, 65, 85, 0.6);
            border: 1px solid rgba(251, 191, 36, 0.3);
            border-radius: 8px;
            padding: 12px;
            margin-bottom: 16px;
            text-align: center;
            color: #fbbf24;
            font-weight: 500;
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="header-content">
            <div class="logo-section">
                <div class="logo">R51</div>
                <div>
                    <h1 class="title">CRM Reims Volley 51</h1>
                    <p class="subtitle">Gestion des contacts du club</p>
                </div>
            </div>
            <div class="controls">
                <input type="text" class="search-box" placeholder="Rechercher..." id="searchInput">
                <button class="btn btn-secondary" onclick="saveManually()">💾</button>
                <button class="btn btn-secondary" onclick="exportToExcel()">📊</button>
                <button class="btn btn-primary" onclick="openModal()">+ Ajouter</button>
            </div>
        </div>
    </div>

    <div class="main-content">
        <!-- Message de statut -->
        <div id="statusMessage" class="message hidden"></div>

        <!-- Onglets -->
        <div class="tabs">
            <button class="tab active" onclick="switchTab('partenaires')">Partenaires (<span id="countPartenaires">2</span>)</button>
            <button class="tab" onclick="switchTab('benevoles')">Bénévoles (<span id="countBenevoles">1</span>)</button>
            <button class="tab" onclick="switchTab('entites')">Entités (<span id="countEntites">1</span>)</button>
        </div>

        <!-- Filtres -->
        <div class="filters">
            <h4>🔍 Filtres</h4>
            <div id="filtersContent">
                <!-- Filtres dynamiques selon l'onglet -->
            </div>
            <button class="btn btn-secondary" onclick="resetFilters()">🗑️ Réinitialiser les filtres</button>
        </div>

        <!-- Contenu -->
        <div id="content">
            <!-- Cartes dynamiques -->
        </div>

        <!-- Barre de statut -->
        <div class="status-bar">
            💾 Sauvegarde automatique activée | 📊 Export Excel disponible | 
            <span class="status-highlight">Total: <span id="totalCount">4</span> contacts</span>
        </div>
    </div>

    <!-- Modal -->
    <div id="modal" class="modal hidden">
        <div class="modal-content">
            <h3 class="modal-title" id="modalTitle">Ajouter un partenaire</h3>
            <div id="modalForm">
                <!-- Formulaire dynamique -->
            </div>
            <div class="modal-actions">
                <button class="btn btn-secondary" onclick="closeModal()">Annuler</button>
                <button class="btn btn-primary" onclick="saveItem()">Ajouter</button>
            </div>
        </div>
    </div>

    <script>
        // Données initiales
        let currentTab = 'partenaires';
        let editingItem = null;
        let filters = {
            partenaires: { statut: '', montantMin: '', montantMax: '' },
            benevoles: { fonction: '' },
            entites: { type: '' }
        };

        let data = {
            partenaires: [
                {
                    id: 1,
                    entreprise: "Boulangerie Martin",
                    representant: "Jean Martin",
                    telephone: "03 26 XX XX XX",
                    email: "contact@boulangeriemartin.fr",
                    descriptif: "Boulangerie locale intéressée par un partenariat alimentaire",
                    statut: "en-negociation",
                    montantHT: "1500",
                    dateCreation: new Date().toLocaleDateString()
                },
                {
                    id: 2,
                    entreprise: "Sport Plus",
                    representant: "Marie Dubois",
                    telephone: "03 26 YY YY YY",
                    email: "m.dubois@sportplus.fr",
                    descriptif: "Magasin de sport, partenaire équipement",
                    statut: "partenaire",
                    montantHT: "3000",
                    dateCreation: new Date().toLocaleDateString()
                }
            ],
            benevoles: [
                {
                    id: 1,
                    nom: "Pierre",
                    prenom: "Durand",
                    telephone: "06 XX XX XX XX",
                    email: "pierre.durand@email.fr",
                    fonction: "Entraineur",
                    disponibilite: "Lundi, Mercredi, Vendredi",
                    dateInscription: new Date().toLocaleDateString()
                }
            ],
            entites: [
                {
                    id: 1,
                    nom: "École Primaire Paul Bert",
                    contact: "Directrice Mme Lefebvre",
                    telephone: "03 26 ZZ ZZ ZZ",
                    email: "ecole.paulbert@ville.fr",
                    type: "École",
                    descriptif: "Partenariat pour initiation volley",
                    dateCreation: new Date().toLocaleDateString()
                }
            ]
        };

        const statutsPartenaires = [
            { value: 'prospect', label: 'Prospect' },
            { value: 'contacte', label: 'Contacté' },
            { value: 'rencontre', label: 'Rencontré' },
            { value: 'en-negociation', label: 'En négociation' },
            { value: 'partenaire', label: 'Partenaire' },
            { value: 'mecene', label: 'Mécène' },
            { value: 'refuse', label: 'Refusé' }
        ];

        const fonctionsBenevoles = [
            'Administratif', 'Entraineur', 'Buvette', 'Billetterie', 'Accueil public',
            'Salon VIP', 'Montage & démontage', 'Challenge vidéo', 'Animation de match'
        ];

        const typesEntites = ['École', 'Mairie', 'Association', 'Service social', 'Autre'];

        // Chargement automatique des données
        window.addEventListener('load', function() {
            loadData();
            renderContent();
            renderFilters();
            updateCounts();
        });

        // Sauvegarde automatique
        function saveData() {
            localStorage.setItem('reimsVolley51CRM', JSON.stringify({
                ...data,
                lastSaved: new Date().toLocaleString()
            }));
        }

        // Chargement des données
        function loadData() {
            const savedData = localStorage.getItem('reimsVolley51CRM');
            if (savedData) {
                try {
                    const parsedData = JSON.parse(savedData);
                    if (parsedData.partenaires) data.partenaires = parsedData.partenaires;
                    if (parsedData.benevoles) data.benevoles = parsedData.benevoles;
                    if (parsedData.entites) data.entites = parsedData.entites;
                    showMessage('✅ Données chargées automatiquement');
                } catch (error) {
                    console.error('Erreur chargement:', error);
                }
            }
        }

        // Affichage des messages
        function showMessage(message) {
            const messageEl = document.getElementById('statusMessage');
            messageEl.textContent = message;
            messageEl.classList.remove('hidden');
            setTimeout(() => messageEl.classList.add('hidden'), 3000);
        }

        // Changement d'onglet
        function switchTab(tab) {
            currentTab = tab;
            document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
            event.target.classList.add('active');
            renderContent();
            renderFilters();
        }

        // Rendu des filtres
        function renderFilters() {
            const filtersContent = document.getElementById('filtersContent');
            let html = '<div class="filter-grid">';

            if (currentTab === 'partenaires') {
                html += `
                    <select class="filter-select" onchange="updateFilter('statut', this.value)">
                        <option value="">📊 Tous les statuts</option>
                        ${statutsPartenaires.map(s => `<option value="${s.value}" ${filters.partenaires.statut === s.value ? 'selected' : ''}>${s.label}</option>`).join('')}
                    </select>
                    <input type="number" class="filter-input" placeholder="💰 Montant min (€)" value="${filters.partenaires.montantMin}" onchange="updateFilter('montantMin', this.value)">
                    <input type="number" class="filter-input" placeholder="💰 Montant max (€)" value="${filters.partenaires.montantMax}" onchange="updateFilter('montantMax', this.value)">
                `;
            } else if (currentTab === 'benevoles') {
                html += `
                    <select class="filter-select" onchange="updateFilter('fonction', this.value)">
                        <option value="">👥 Toutes les fonctions</option>
                        ${fonctionsBenevoles.map(f => `<option value="${f}" ${filters.benevoles.fonction === f ? 'selected' : ''}>${f}</option>`).join('')}
                    </select>
                `;
            } else if (currentTab === 'entites') {
                html += `
                    <select class="filter-select" onchange="updateFilter('type', this.value)">
                        <option value="">🏢 Tous les types</option>
                        ${typesEntites.map(t => `<option value="${t}" ${filters.entites.type === t ? 'selected' : ''}>${t}</option>`).join('')}
                    </select>
                `;
            }

            html += '</div>';
            filtersContent.innerHTML = html;
        }

        // Mise à jour des filtres
        function updateFilter(field, value) {
            filters[currentTab][field] = value;
            renderContent();
        }

        // Réinitialisation des filtres
        function resetFilters() {
            filters = {
                partenaires: { statut: '', montantMin: '', montantMax: '' },
                benevoles: { fonction: '' },
                entites: { type: '' }
            };
            renderFilters();
            renderContent();
        }

        // Filtrage des données
        function filterData(items) {
            const searchTerm = document.getElementById('searchInput').value.toLowerCase();
            
            return items.filter(item => {
                // Recherche textuelle
                const searchMatch = !searchTerm || Object.values(item).some(value => 
                    value && value.toString().toLowerCase().includes(searchTerm)
                );

                // Filtres spécifiques
                if (currentTab === 'partenaires') {
                    const { statut, montantMin, montantMax } = filters.partenaires;
                    const statutMatch = !statut || item.statut === statut;
                    const minMatch = !montantMin || (item.montantHT && parseFloat(item.montantHT) >= parseFloat(montantMin));
                    const maxMatch = !montantMax || (item.montantHT && parseFloat(item.montantHT) <= parseFloat(montantMax));
                    return searchMatch && statutMatch && minMatch && maxMatch;
                } else if (currentTab === 'benevoles') {
                    const { fonction } = filters.benevoles;
                    const fonctionMatch = !fonction || item.fonction === fonction;
                    return searchMatch && fonctionMatch;
                } else if (currentTab === 'entites') {
                    const { type } = filters.entites;
                    const typeMatch = !type || item.type === type;
                    return searchMatch && typeMatch;
                }

                return searchMatch;
            });
        }

        // Rendu du contenu
        function renderContent() {
            const content = document.getElementById('content');
            const items = filterData(data[currentTab]);

            if (items.length === 0) {
                content.innerHTML = `
                    <div class="empty-state">
                        <h3>Aucun élément trouvé</h3>
                        <p>Cliquez sur "Ajouter" pour créer votre premier ${currentTab.slice(0, -1)}</p>
                    </div>
                `;
                return;
            }

            let html = '';
            items.forEach(item => {
                if (currentTab === 'partenaires') {
                    html += renderPartenaire(item);
                } else if (currentTab === 'benevoles') {
                    html += renderBenevole(item);
                } else if (currentTab === 'entites') {
                    html += renderEntite(item);
                }
            });

            content.innerHTML = html;
        }

        // Rendu d'un partenaire
        function renderPartenaire(p) {
            const badgeClass = `badge-${p.statut.replace('-', '')}`;
            return `
                <div class="card">
                    <div class="card-header">
                        <div style="flex: 1;">
                            <div style="display: flex; align-items: center; margin-bottom: 12px;">
                                <h3 class="card-title">🏢 ${p.entreprise}</h3>
                                <span class="badge ${badgeClass}">${getStatutLabel(p.statut)}</span>
                                ${p.montantHT ? `<span class="badge badge-montant">${p.montantHT}€ HT</span>` : ''}
                            </div>
                            <div class="card-info">
                                <div class="info-row">👤 ${p.representant}</div>
                                ${p.telephone ? `<div class="info-row">📞 ${p.telephone}</div>` : ''}
                                ${p.email ? `<div class="info-row">📧 ${p.email}</div>` : ''}
                                ${p.descriptif ? `<div class="info-row">📄 ${p.descriptif}</div>` : ''}
                            </div>
                        </div>
                        <div class="card-actions">
                            <button class="btn-icon" onclick="editItem(${p.id})">✏️</button>
                            <button class="btn-icon btn-delete" onclick="deleteItem(${p.id})">🗑️</button>
                        </div>
                    </div>
                    <div style="font-size: 12px; color: #94a3b8; border-top: 1px solid rgba(59, 130, 246, 0.2); padding-top: 8px;">
                        Créé le ${p.dateCreation}
                    </div>
                </div>
            `;
        }

        // Rendu d'un bénévole
        function renderBenevole(b) {
            return `
                <div class="card">
                    <div class="card-header">
                        <div style="flex: 1;">
                            <div style="display: flex; align-items: center; margin-bottom: 12px;">
                                <h3 class="card-title">👤 ${b.prenom} ${b.nom}</h3>
                                ${b.fonction ? `<span class="badge" style="background: rgba(34, 197, 94, 0.2); color: #22c55e;">${b.fonction}</span>` : ''}
                            </div>
                            <div class="card-info">
                                ${b.telephone ? `<div class="info-row">📞 ${b.telephone}</div>` : ''}
                                ${b.email ? `<div class="info-row">📧 ${b.email}</div>` : ''}
                                ${b.disponibilite ? `<div class="info-row">🕐 Disponible: ${b.disponibilite}</div>` : ''}
                            </div>
                        </div>
                        <div class="card-actions">
                            <button class="btn-icon" onclick="editItem(${b.id})">✏️</button>
                            <button class="btn-icon btn-delete" onclick="deleteItem(${b.id})">🗑️</button>
                        </div>
                    </div>
                    <div style="font-size: 12px; color: #94a3b8; border-top: 1px solid rgba(59, 130, 246, 0.2); padding-top: 8px;">
                        Inscrit le ${b.dateInscription}
                    </div>
                </div>
            `;
        }

        // Rendu d'une entité
        function renderEntite(e) {
            return `
                <div class="card">
                    <div class="card-header">
                        <div style="flex: 1;">
                            <div style="display: flex; align-items: center; margin-bottom: 12px;">
                                <h3 class="card-title">🏢 ${e.nom}</h3>
                                ${e.type ? `<span class="badge" style="background: rgba(147, 51, 234, 0.2); color: #a855f7;">${e.type}</span>` : ''}
                            </div>
                            <div class="card-info">
                                ${e.contact ? `<div class="info-row">👤 ${e.contact}</div>` : ''}
                                ${e.telephone ? `<div class="info-row">📞 ${e.telephone}</div>` : ''}
                                ${e.email ? `<div class="info-row">📧 ${e.email}</div>` : ''}
                                ${e.descriptif ? `<div class="info-row">📄 ${e.descriptif}</div>` : ''}
                            </div>
                        </div>
                        <div class="card-actions">
                            <button class="btn-icon" onclick="editItem(${e.id})">✏️</button>
                            <button class="btn-icon btn-delete" onclick="deleteItem(${e.id})">🗑️</button>
                        </div>
                    </div>
                    <div style="font-size: 12px; color: #94a3b8; border-top: 1px solid rgba(59, 130, 246, 0.2); padding-top: 8px;">
                        Créé le ${e.dateCreation}
                    </div>
                </div>
            `;
        }

        // Obtenir le label du statut
        function getStatutLabel(statut) {
            const statutObj = statutsPartenaires.find(s => s.value === statut);
            return statutObj ? statutObj.label : statut;
        }

        // Ouverture du modal
        function openModal() {
            editingItem = null;
            renderModal();
            document.getElementById('modal').classList.remove('hidden');
        }

        // Édition d'un élément
        function editItem(id) {
            editingItem = data[currentTab].find(item => item.id === id);
            renderModal();
            document.getElementById('modal').classList.remove('hidden');
        }

        // Rendu du modal
        function renderModal() {
            const title = document.getElementById('modalTitle');
            const form = document.getElementById('modalForm');
            
            title.textContent = (editingItem ? 'Modifier' : 'Ajouter') + ' ' + 
                (currentTab === 'partenaires' ? 'un partenaire' : 
                 currentTab === 'benevoles' ? 'un bénévole' : 'une entité');

            let html = '';

            if (currentTab === 'partenaires') {
                html = `
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Nom de l'entreprise" id="entreprise" value="${editingItem?.entreprise || ''}" required>
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Nom du représentant" id="representant" value="${editingItem?.representant || ''}" required>
                    </div>
                    <div class="form-group">
                        <input type="tel" class="form-input" placeholder="Téléphone" id="telephone" value="${editingItem?.telephone || ''}">
                    </div>
                    <div class="form-group">
                        <input type="email" class="form-input" placeholder="Email" id="email" value="${editingItem?.email || ''}">
                    </div>
                    <div class="form-group">
                        <textarea class="form-textarea" placeholder="Descriptif" id="descriptif">${editingItem?.descriptif || ''}</textarea>
                    </div>
                    <div class="form-group">
                        <input type="number" class="form-input" placeholder="Montant HT (€)" id="montantHT" value="${editingItem?.montantHT || ''}">
                    </div>
                    <div class="form-group">
                        <select class="form-select" id="statut">
                            ${statutsPartenaires.map(s => `<option value="${s.value}" ${editingItem?.statut === s.value ? 'selected' : ''}>${s.label}</option>`).join('')}
                        </select>
                    </div>
                `;
            } else if (currentTab === 'benevoles') {
                html = `
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Nom" id="nom" value="${editingItem?.nom || ''}" required>
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Prénom" id="prenom" value="${editingItem?.prenom || ''}" required>
                    </div>
                    <div class="form-group">
                        <input type="tel" class="form-input" placeholder="Téléphone" id="telephone" value="${editingItem?.telephone || ''}">
                    </div>
                    <div class="form-group">
                        <input type="email" class="form-input" placeholder="Email" id="email" value="${editingItem?.email || ''}">
                    </div>
                    <div class="form-group">
                        <select class="form-select" id="fonction">
                            <option value="">Sélectionner une fonction</option>
                            ${fonctionsBenevoles.map(f => `<option value="${f}" ${editingItem?.fonction === f ? 'selected' : ''}>${f}</option>`).join('')}
                        </select>
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Disponibilités" id="disponibilite" value="${editingItem?.disponibilite || ''}">
                    </div>
                `;
            } else if (currentTab === 'entites') {
                html = `
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Nom de l'entité" id="nom" value="${editingItem?.nom || ''}" required>
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-input" placeholder="Personne de contact" id="contact" value="${editingItem?.contact || ''}">
                    </div>
                    <div class="form-group">
                        <input type="tel" class="form-input" placeholder="Téléphone" id="telephone" value="${editingItem?.telephone || ''}">
                    </div>
                    <div class="form-group">
                        <input type="email" class="form-input" placeholder="Email" id="email" value="${editingItem?.email || ''}">
                    </div>
                    <div class="form-group">
                        <select class="form-select" id="type">
                            <option value="">Type d'entité</option>
                            ${typesEntites.map(t => `<option value="${t}" ${editingItem?.type === t ? 'selected' : ''}>${t}</option>`).join('')}
                        </select>
                    </div>
                    <div class="form-group">
                        <textarea class="form-textarea" placeholder="Descriptif" id="descriptif">${editingItem?.descriptif || ''}</textarea>
                    </div>
                `;
            }

            form.innerHTML = html;
        }

        // Fermeture du modal
        function closeModal() {
            document.getElementById('modal').classList.add('hidden');
            editingItem = null;
        }

        // Sauvegarde d'un élément
        function saveItem() {
            const formData = {};
            
            // Récupération des données du formulaire
            document.querySelectorAll('#modalForm input, #modalForm select, #modalForm textarea').forEach(input => {
                formData[input.id] = input.value;
            });

            if (editingItem) {
                // Modification
                const index = data[currentTab].findIndex(item => item.id === editingItem.id);
                data[currentTab][index] = { ...formData, id: editingItem.id, [currentTab === 'benevoles' ? 'dateInscription' : 'dateCreation']: editingItem[currentTab === 'benevoles' ? 'dateInscription' : 'dateCreation'] };
            } else {
                // Ajout
                formData.id = Date.now();
                formData[currentTab === 'benevoles' ? 'dateInscription' : 'dateCreation'] = new Date().toLocaleDateString();
                data[currentTab].push(formData);
            }

            saveData();
            closeModal();
            renderContent();
            updateCounts();
            showMessage(editingItem ? '✅ Élément modifié' : '✅ Élément ajouté');
        }

        // Suppression d'un élément
        function deleteItem(id) {
            if (confirm('Êtes-vous sûr de vouloir supprimer cet élément ?')) {
                data[currentTab] = data[currentTab].filter(item => item.id !== id);
                saveData();
                renderContent();
                updateCounts();
                showMessage('🗑️ Élément supprimé');
            }
        }

        // Mise à jour des compteurs
        function updateCounts() {
            document.getElementById('countPartenaires').textContent = data.partenaires.length;
            document.getElementById('countBenevoles').textContent = data.benevoles.length;
            document.getElementById('countEntites').textContent = data.entites.length;
            document.getElementById('totalCount').textContent = data.partenaires.length + data.benevoles.length + data.entites.length;
        }

        // Sauvegarde manuelle
        function saveManually() {
            saveData();
            showMessage('💾 Sauvegarde manuelle effectuée !');
        }

        // Export Excel (fonction basique)
        function exportToExcel() {
            showMessage('📊 Fonction Excel non disponible dans cette version');
        }

        // Événement de recherche
        document.getElementById('searchInput').addEventListener('input', function() {
            renderContent();
        });
    </script>
</body>
</html>ml…]()
