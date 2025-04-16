<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Gestione Fascicoli - Wizard Overlay</title>
  
  <!-- Bootstrap CSS (CDN) -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <!-- Font Awesome (per icone) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
  <!-- FilePond CSS -->
  <link href="https://unpkg.com/filepond/dist/filepond.css" rel="stylesheet">
  
  <style>
    /* Layout Generale */
    body {
      margin: 0;
      padding: 0;
      background-color: #fff;
      color: #000;
      font-family: sans-serif;
    }
    /* Sidebar principale nera */
    .sidebar-main {
      background-color: #000;
      color: #fff;
      width: 220px;
      min-height: 100vh;
      flex-shrink: 0;
      padding: 20px;
    }
    .sidebar-main .logo {
      font-size: 1.2rem;
      font-weight: bold;
      margin-bottom: 40px;
    }
    .sidebar-main .nav-link {
      color: #fff;
      display: block;
      margin-bottom: 10px;
      padding: 8px;
      border-radius: 8px;
      transition: all 0.3s ease;
      text-decoration: none;
    }
    .sidebar-main .nav-link:hover,
    .sidebar-main .nav-link.active {
      background-color: #cc9900;
      color: #000;
    }
    .sidebar-main .nav-link i {
      margin-right: 8px;
    }
    
    /* Header principale */
    .header {
      background-color: #f8f9fa;
      border-bottom: 1px solid #ccc;
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    /* Contenuto principale (a destra della sidebar) */
    .main-content {
      flex-grow: 1;
      padding: 20px;
      position: relative;
    }
    
    /* La datatable (esempio statico) */
    .table-responsive {
      background-color: #fff;
      padding: 10px;
      border: 1px solid #ddd;
      border-radius: 5px;
    }
    
    /* Wizard Overlay: copre il contenuto principale, mostra una pagina a tutto schermo */
    #wizard-overlay {
      position: fixed;
      top: 0;
      left: 220px; /* inizio subito dopo la sidebar principale */
      right: 0;
      bottom: 0;
      background-color: #fff;
      z-index: 9999;
      display: none; /* inizialmente nascosto */
      overflow-y: auto;
      padding: 20px;
    }
    /* Bottone per chiudere il wizard */
    #wizard-close {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 1.5rem;
      cursor: pointer;
      color: #cc9900;
    }
    
    /* Sidebar del wizard (all'interno dell'overlay) */
    .wizard-sidebar {
      background-color: #000;
      color: #fff;
      padding: 15px;
      width: 200px;
      min-height: 100%;
      float: left;
      margin-right: 20px;
      border-right: 2px solid #cc9900;
    }
    .wizard-sidebar .menu-item {
      display: block;
      color: #fff;
      padding: 8px;
      margin-bottom: 10px;
      border-radius: 8px;
      text-decoration: none;
      transition: all 0.3s ease;
    }
    .wizard-sidebar .menu-item:hover,
    .wizard-sidebar .menu-item.active {
      background-color: #cc9900;
      color: #000;
    }
    
    /* Area del wizard (contenuto dei vari step) */
    .wizard-content {
      overflow: hidden;
    }
    .wizard-step {
      display: none;
      animation: fadeIn 0.5s ease-in-out;
    }
    .wizard-step.active {
      display: block;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    
    /* Stile "fascicolo impaginato": container interno per ogni form */
    .dossier-form {
      background-color: #fff;
      padding: 30px;
      border: 2px solid #cc9900;
      border-radius: 10px;
      margin: 20px 0;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .dossier-form label {
      font-weight: bold;
    }
    
    /* Bottoni rotondati */
    .btn-rounded {
      border-radius: 20px;
      transition: background-color 0.3s ease;
      border: none;
    }
  </style>
</head>
<body>

  <!-- Layout principale: Sidebar principale + contenuto -->
  <div class="d-flex">
    <!-- Sidebar principale nera -->
    <div class="sidebar-main">
      <div class="logo">
        <i class="fas fa-tools"></i> Tuo Logo
      </div>
      <a href="#" class="nav-link"><i class="fas fa-home"></i> Dashboard</a>
      <a href="#" class="nav-link"><i class="fas fa-cogs"></i> Gestioni</a>
      <a href="#" class="nav-link active"><i class="fas fa-folder-open"></i> Fascicoli Tecnici</a>
      <a href="#" class="nav-link"><i class="fas fa-user-shield"></i> Sistema</a>
    </div>
    
    <!-- Area di destra: header + contenuto -->
    <div class="main-content">
      <!-- Header -->
      <div class="header">
        <div>Bentornato, <strong>massimo.pisano</strong></div>
        <button class="btn btn-sm btn-outline-secondary">Log out</button>
      </div>
      
      <!-- Contenuto della datatable (esempio statico) -->
      <div class="mt-3">
        <div class="d-flex justify-content-between align-items-center mb-3">
          <h4>Fascicoli Tecnici</h4>
          <div>
            <button id="btnDelete" class="btn btn-danger btn-rounded">Cancella selezionati</button>
            <button id="btnNew" class="btn btn-primary btn-rounded">Nuovo</button>
          </div>
        </div>
        <div class="table-responsive">
          <table class="table table-striped table-hover">
            <thead>
              <tr>
                <th><input type="checkbox"></th>
                <th>#</th>
                <th>Codice Progetto</th>
                <th>Numero Fascicolo</th>
                <th>Cliente</th>
                <th>Tipo Macchinario</th>
                <th>Modello</th>
                <th>Anno</th>
                <th>Azione</th>
              </tr>
            </thead>
            <tbody>
              <!-- Riga di esempio 1 -->
              <tr>
                <td><input type="checkbox"></td>
                <td>1</td>
                <td>1234XYZ</td>
                <td>FASC-001</td>
                <td>Maxim SRL</td>
                <td>Pressa</td>
                <td>XP-100</td>
                <td>2022</td>
                <td>
                  <button class="btn btn-sm btn-outline-info btnSelectFascicolo" data-fascicolo="1">Dettagli</button>
                </td>
              </tr>
              <!-- Riga di esempio 2 -->
              <tr>
                <td><input type="checkbox"></td>
                <td>2</td>
                <td>5678ABC</td>
                <td>FASC-002</td>
                <td>ACME SpA</td>
                <td>Robot</td>
                <td>Robo-X</td>
                <td>2023</td>
                <td>
                  <button class="btn btn-sm btn-outline-info btnSelectFascicolo" data-fascicolo="2">Dettagli</button>
                </td>
              </tr>
              <!-- Altre righe -->
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
  
  <!-- Wizard Overlay: copre la parte destra (main-content) sopra la datatable -->
  <div id="wizard-overlay">
    <!-- Bottone per chiudere il wizard -->
    <div id="wizard-close"><i class="fas fa-times"></i></div>
    
    <!-- Titolo e indicazione del fascicolo selezionato -->
    <h5>Fascicolo: <span id="fascicoloSelezionato">N/D</span></h5>
    
    <div class="d-flex">
      <!-- Sidebar interna per il wizard -->
      <div class="wizard-sidebar">
        <a href="#" class="menu-item active" data-target="w-step1"><i class="fas fa-folder-open"></i> Informazioni Fascicolo</a>
        <a href="#" class="menu-item" data-target="w-step2"><i class="fas fa-cogs"></i> Macchinario</a>
        <a href="#" class="menu-item" data-target="w-step3"><i class="fas fa-book-open"></i> Capitolo 1</a>
        <a href="#" class="menu-item" data-target="w-step4"><i class="fas fa-book"></i> Capitolo 2</a>
        <a href="#" class="menu-item" data-target="w-step5"><i class="fas fa-book"></i> Capitolo 3</a>
      </div>
      
      <!-- Contenuto del wizard (ampio, stile fascicolo impaginato) -->
      <div class="wizard-content" style="flex-grow: 1;">
        <!-- Step 1: Informazioni Fascicolo -->
        <div id="w-step1" class="wizard-step active">
          <h2>Informazioni Fascicolo</h2>
          <div class="dossier-form">
            <form action="process.php" method="post">
              <div class="form-group">
                <label for="numeroFascicolo">Numero Fascicolo</label>
                <input type="text" class="form-control" id="numeroFascicolo" name="numeroFascicolo" placeholder="Inserisci il numero">
              </div>
              <div class="form-group">
                <label for="dataApertura">Data Apertura</label>
                <input type="date" class="form-control" id="dataApertura" name="dataApertura">
              </div>
              <div class="form-group">
                <label for="descrizioneFascicolo">Descrizione Fascicolo</label>
                <input type="text" class="form-control" id="descrizioneFascicolo" name="descrizioneFascicolo" placeholder="Inserisci una breve descrizione">
              </div>
              <div class="form-group">
                <label for="statoFascicolo">Stato Fascicolo</label>
                <select class="form-control" id="statoFascicolo" name="statoFascicolo">
                  <option value="aperto">Aperto</option>
                  <option value="chiuso">Chiuso</option>
                </select>
              </div>
              <button type="button" class="btn btn-primary btn-rounded next-step">Successivo</button>
            </form>
          </div>
        </div>
        
        <!-- Step 2: Macchinario -->
        <div id="w-step2" class="wizard-step">
          <h2>Macchinario</h2>
          <div class="dossier-form">
            <form action="process.php" method="post">
              <div class="form-group">
                <label for="modello">Modello</label>
                <input type="text" class="form-control" id="modello" name="modello" placeholder="Inserisci il modello">
              </div>
              <div class="form-group">
                <label for="seriale">Seriale</label>
                <input type="text" class="form-control" id="seriale" name="seriale" placeholder="Inserisci il seriale">
              </div>
              <div class="form-group">
                <label for="dataManutenzione">Data Manutenzione</label>
                <input type="date" class="form-control" id="dataManutenzione" name="dataManutenzione">
              </div>
              <div class="form-group">
                <label for="statoMacchinario">Stato</label>
                <select class="form-control" id="statoMacchinario" name="statoMacchinario">
                  <option value="funzionante">Funzionante</option>
                  <option value="daManutenzione">Da manutenzione</option>
                </select>
              </div>
              <!-- Caricamento immagine con FilePond -->
              <div class="form-group">
                <label for="foto">Foto</label>
                <input type="file" class="filepond" id="foto" name="foto" accept="image/*">
              </div>
              <button type="button" class="btn btn-secondary btn-rounded prev-step">Precedente</button>
              <button type="button" class="btn btn-primary btn-rounded next-step">Successivo</button>
            </form>
          </div>
        </div>
        
        <!-- Step 3: Capitolo 1 -->
        <div id="w-step3" class="wizard-step">
          <h2>Capitolo 1</h2>
          <div class="dossier-form">
            <form action="process.php" method="post">
              <div class="form-group">
                <label for="titoloCap1">Titolo Capitolo 1</label>
                <input type="text" class="form-control" id="titoloCap1" name="titoloCap1" placeholder="Inserisci il titolo">
              </div>
              <div class="form-group">
                <label for="contenutoCap1">Contenuto</label>
                <textarea class="form-control" id="contenutoCap1" name="contenutoCap1" rows="6" placeholder="Inserisci il contenuto"></textarea>
              </div>
              <button type="button" class="btn btn-secondary btn-rounded prev-step">Precedente</button>
              <button type="button" class="btn btn-primary btn-rounded next-step">Successivo</button>
            </form>
          </div>
        </div>
        
        <!-- Step 4: Capitolo 2 -->
        <div id="w-step4" class="wizard-step">
          <h2>Capitolo 2</h2>
          <div class="dossier-form">
            <form action="process.php" method="post">
              <div class="form-group">
                <label for="titoloCap2">Titolo Capitolo 2</label>
                <input type="text" class="form-control" id="titoloCap2" name="titoloCap2" placeholder="Inserisci il titolo">
              </div>
              <div class="form-group">
                <label for="contenutoCap2">Contenuto</label>
                <textarea class="form-control" id="contenutoCap2" name="contenutoCap2" rows="6" placeholder="Inserisci il contenuto"></textarea>
              </div>
              <button type="button" class="btn btn-secondary btn-rounded prev-step">Precedente</button>
              <button type="button" class="btn btn-primary btn-rounded next-step">Successivo</button>
            </form>
          </div>
        </div>
        
        <!-- Step 5: Capitolo 3 -->
        <div id="w-step5" class="wizard-step">
          <h2>Capitolo 3</h2>
          <div class="dossier-form">
            <form action="process.php" method="post">
              <div class="form-group">
                <label for="titoloCap3">Titolo Capitolo 3</label>
                <input type="text" class="form-control" id="titoloCap3" name="titoloCap3" placeholder="Inserisci il titolo">
              </div>
              <div class="form-group">
                <label for="contenutoCap3">Contenuto</label>
                <textarea class="form-control" id="contenutoCap3" name="contenutoCap3" rows="6" placeholder="Inserisci il contenuto"></textarea>
              </div>
              <button type="button" class="btn btn-secondary btn-rounded prev-step">Precedente</button>
              <button type="submit" class="btn btn-success btn-rounded">Invia</button>
            </form>
          </div>
        </div>
        <!-- Fine Wizard Steps -->
        
      </div><!-- Fine wizard-content -->
    </div><!-- Fine area flessibile interna -->
    
  </div><!-- Fine wizard-overlay -->
  
  <!-- Caricamento JS: jQuery, Bootstrap, FilePond -->
  <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.bundle.min.js"></script>
  <script src="https://unpkg.com/filepond/dist/filepond.js"></script>
  
  <script>
    $(function(){
      // Inizializzazione dei wizard-step all'interno dell'overlay:
      $('.wizard-step').hide();
      $('#w-step1').show().addClass('active');
      
      // Navigazione tramite il menu interno del wizard
      $('.wizard-sidebar .menu-item').on('click', function(e){
        e.preventDefault();
        var target = $(this).data('target');
        // evidenzia il menu corrente
        $('.wizard-sidebar .menu-item').removeClass('active');
        $(this).addClass('active');
        // cambia il passo del wizard
        $('.wizard-step').removeClass('active').hide();
        $('#' + target).fadeIn(300).addClass('active');
      });
      
      // Next e Prev generici per i form del wizard
      $('.next-step').on('click', function(){
        var currentStep = $(this).closest('.wizard-step');
        var nextStep = currentStep.next('.wizard-step');
        if(nextStep.length){
          currentStep.removeClass('active').hide();
          nextStep.fadeIn(300).addClass('active');
          // Aggiorna la selezione nel menu del wizard
          $('.wizard-sidebar .menu-item').removeClass('active');
          $('.wizard-sidebar .menu-item[data-target="'+ nextStep.attr('id') +'"]').addClass('active');
        }
      });
      
      $('.prev-step').on('click', function(){
        var currentStep = $(this).closest('.wizard-step');
        var prevStep = currentStep.prev('.wizard-step');
        if(prevStep.length){
          currentStep.removeClass('active').hide();
          prevStep.fadeIn(300).addClass('active');
          $('.wizard-sidebar .menu-item').removeClass('active');
          $('.wizard-sidebar .menu-item[data-target="'+ prevStep.attr('id') +'"]').addClass('active');
        }
      });
      
      // Mostra il wizard-overlay alla selezione del fascicolo o click su "Nuovo"
      $('.btnSelectFascicolo, #btnNew').on('click', function(){
        var fascicoloId = $(this).data('fascicolo');
        if(fascicoloId){
          $('#fascicoloSelezionato').text('FASC-' + fascicoloId);
        } else {
          $('#fascicoloSelezionato').text('Nuovo Fascicolo');
        }
        $('#wizard-overlay').slideDown(300);
        // Reset al primo step interno del wizard
        $('.wizard-step').removeClass('active').hide();
        $('#w-step1').fadeIn(300).addClass('active');
        $('.wizard-sidebar .menu-item').removeClass('active');
        $('.wizard-sidebar .menu-item[data-target="w-step1"]').addClass('active');
      });
      
      // Pulsante per chiudere il wizard overlay
      $('#wizard-close').on('click', function(){
        $('#wizard-overlay').slideUp(300);
      });
      
      // Inizializza FilePond (es. nel form Macchinario)
      const inputElement = document.querySelector('input.filepond');
      if(inputElement) {
        FilePond.create(inputElement);
      }
    });
  </script>
  
</body>
</html>
