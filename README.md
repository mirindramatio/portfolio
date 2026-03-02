<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - RATIANARIVO Mirindra Matthieu</title>
    <style>
        body {
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
            background-color: #f8fafc;
            color: #1e293b;
            line-height: 1.6;
        }
    
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 2rem;
        }
    
        /* HEADER CLASSIQUE */
        header {
            background: #ffffff;
            border-bottom: 2px solid #e2e8f0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
    
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }
    
        .logo {
            font-size: 1.5rem;
            font-weight: 600;
            color: #0f3b4c;
            text-decoration: none;
            letter-spacing: -0.5px;
        }
    
        .nav-links {
            display: flex;
            gap: 2rem;
        }
    
        .nav-links a {
            text-decoration: none;
            color: #2c3e50;
            font-weight: 500;
            padding: 0.5rem 0;
            border-bottom: 2px solid transparent;
            transition: 0.2s;
        }
    
        .nav-links a:hover {
            border-bottom-color: #2c7a8c;
            color: #0f3b4c;
        }
    
        /* SECTIONS */
        section {
            padding: 100px 0 80px;
            min-height: auto;
            border-bottom: 1px solid #e9ecef;
        }
    
        #accueil {
            background-color: #ffffff;
            padding-top: 120px;
        }
    
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #0c2f3a;
            font-weight: 600;
        }
    
        .hero p {
            font-size: 1.2rem;
            color: #334e5c;
            max-width: 600px;
            margin-bottom: 2rem;
        }
    
        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            background-color: #2c7a8c;
            color: white;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 500;
            border: 1px solid #1f5c6b;
            transition: 0.2s;
        }
    
        .btn:hover {
            background-color: #1f5c6b;
            border-color: #15424e;
        }
    
        /* À PROPOS */
        #apropos {
            background-color: #f9f9f9;
        }
    
        .apropos-content {
            display: flex;
            gap: 3rem;
            align-items: center;
            flex-wrap: wrap;
        }
    
        .apropos-text {
            flex: 2;
            min-width: 300px;
        }
    
        .apropos-text h2 {
            font-size: 2.2rem;
            color: #0c2f3a;
            margin-bottom: 1.5rem;
            border-left: 5px solid #2c7a8c;
            padding-left: 1rem;
        }
    
        .apropos-text p {
            margin: 1.2rem 0;
            color: #2c3e50;
        }
    
        .skills {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
            margin: 2rem 0;
        }
    
        .skill {
            background: #e9f0f3;
            padding: 0.5rem 1.5rem;
            border-radius: 4px;
            font-weight: 500;
            color: #1f5c6b;
            border: 1px solid #cbd5e1;
            font-size: 0.95rem;
        }
    
        .apropos-image {
            flex: 1;
            min-width: 250px;
            text-align: center;
        }
    
        .apropos-image img {
            width: 100%;
            max-width: 300px;
            border-radius: 8px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            border: 3px solid white;
        }
    
        /* CONTACT CARDS (version classique) */
        #contact {
            background-color: #ffffff;
        }
    
        .contact-cards {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin: 3rem 0;
        }
    
        .contact-card {
            background: #f8fbfc;
            border: 1px solid #dde7eb;
            padding: 2rem 1.5rem;
            border-radius: 8px;
            flex: 1 1 220px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
            transition: 0.2s;
        }
    
        .contact-card:hover {
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            border-color: #2c7a8c;
        }
    
        .contact-icon {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            display: block;
        }
    
        .contact-card h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #1d3f4a;
        }
    
        .contact-card p {
            margin-bottom: 1.2rem;
            color: #3a5a66;
        }
    
        .contact-link {
            display: inline-block;
            padding: 0.5rem 1.5rem;
            background: #2c7a8c;
            color: white;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 500;
            border: 1px solid #1f5c6b;
        }
    
        .contact-link:hover {
            background: #1f5c6b;
        }
    
        /* BLOC EMAIL (version classique épurée) */
        .live-message-section {
            background: #f9f9f9;
            border: 1px solid #dce5e9;
            border-radius: 8px;
            padding: 2.5rem;
            margin-top: 3rem;
        }
    
        .live-message-section h3 {
            font-size: 1.8rem;
            color: #0c2f3a;
            margin-bottom: 1.5rem;
            font-weight: 600;
        }
    
        .message-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
        }
    
        .message-form {
            flex: 2;
            min-width: 280px;
        }
    
        .message-preview {
            flex: 1.5;
            background: #ffffff;
            border: 1px solid #d4e1e7;
            border-radius: 8px;
            padding: 2rem;
        }
    
        .form-group {
            margin-bottom: 1.5rem;
        }
    
        .form-group label {
            font-weight: 600;
            color: #1d4a57;
            display: block;
            margin-bottom: 0.4rem;
            font-size: 0.95rem;
        }
    
        .form-group input, 
        .form-group textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #cbd5e1;
            border-radius: 4px;
            font-size: 1rem;
            background: white;
            transition: 0.15s;
        }
    
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #2c7a8c;
            box-shadow: 0 0 0 2px rgba(44,122,140,0.2);
        }
    
        .send-btn {
            background: #2c7a8c;
            color: white;
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            border: 1px solid #1f5c6b;
            transition: 0.2s;
        }
    
        .send-btn:hover {
            background: #1f5c6b;
        }
    
        .preview-card {
            background: #f8fbfc;
            padding: 1.5rem;
            border-radius: 6px;
            border-left: 4px solid #2c7a8c;
        }
    
        .preview-card p {
            margin: 0.7rem 0;
            border-bottom: 1px dashed #ced9df;
            padding-bottom: 0.5rem;
        }
    
        .preview-card strong {
            color: #1a4a57;
            min-width: 90px;
            display: inline-block;
        }
    
        .message-actions {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
    
        .small-btn {
            background: #e2eef2;
            border: 1px solid #b9cfd8;
            padding: 0.5rem 1.2rem;
            border-radius: 4px;
            font-weight: 500;
            color: #1b4a57;
            cursor: pointer;
        }
    
        .small-btn:hover {
            background: #cddee5;
        }
    
        /* FOOTER */
        footer {
            background: #1e3c4f;
            color: #e0edf2;
            text-align: center;
            padding: 2rem;
            border-top: 3px solid #154653;
        }
    
        /* RESPONSIVE */
        @media (max-width: 700px) {
            .nav-links { gap: 1rem; }
            .hero h1 { font-size: 2.2rem; }
            .apropos-content { flex-direction: column-reverse; text-align: center; }
            .apropos-text h2 { border-left: none; text-align: center; }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a href="#" class="logo">Portfolio</a>
            <div class="nav-links">
                <a href="#accueil">Accueil</a>
                <a href="#apropos">À propos</a>
                <a href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <main>
        <!-- ACCUEIL -->
        <section id="accueil">
            <div class="container hero">
                <h1>RATIANARIVO Mirindra Matthieu</h1>
                <p>Développeur web & intégrateur passionné par les interfaces propres et fonctionnelles.</p>
                <a href="#contact" class="btn">Me contacter</a>
            </div>
        </section>

        <!-- À PROPOS -->
        <section id="apropos">
            <div class="container">
                <div class="apropos-content">
                    <div class="apropos-text">
                        <h2>À propos</h2>
                        <p>Fort de 5 ans d'expérience dans la création de sites web et d'applications, j'allie rigueur technique et souci du détail pour offrir des expériences utilisateur réussies.</p>
                        <p>Passionné par le développement front-end et le design responsive, je travaille avec des technologies modernes tout en gardant une approche pragmatique.</p>
                        <div class="skills">
                            <span class="skill">HTML5/CSS3</span>
                            <span class="skill">JavaScript</span>
                            <span class="skill">React</span>
                            <span class="skill">Node.js</span>
                            <span class="skill">UI/Design</span>
                        </div>
                    </div>
                    <div class="apropos-image">
                        <img src="https://picsum.photos/id/1005/400/400" alt="Photo de profil">
                    </div>
                </div>
            </div>
        </section>

        <!-- CONTACT + MESSAGE -->
        <section id="contact">
            <div class="container">
                <h2 style="font-size: 2.2rem; color: #0c2f3a; border-left: 5px solid #2c7a8c; padding-left: 1rem;">Contact</h2>
                
                <div class="contact-cards">
                    <div class="contact-card">
                        <span class="contact-icon">📧</span>
                        <h3>Email</h3>
                        <p>matthieu.ratianarivo@email.com</p>
                        <a href="#" class="contact-link">Envoyer</a>
                    </div>
                    <div class="contact-card">
                        <span class="contact-icon">📱</span>
                        <h3>Téléphone</h3>
                        <p>+33 6 12 34 56 78</p>
                        <a href="#" class="contact-link">Appeler</a>
                    </div>
                    <div class="contact-card">
                        <span class="contact-icon">💼</span>
                        <h3>LinkedIn</h3>
                        <p>/in/matthieuratianarivo</p>
                        <a href="#" class="contact-link">Profil</a>
                    </div>
                </div>

                <!-- BLOC EMAIL INTERACTIF (classique) -->
                <div class="live-message-section">
                    <h3>✉️ Message direct</h3>
                    <div class="message-grid">
                        <div class="message-form">
                            <div class="form-group">
                                <label>Nom</label>
                                <input type="text" id="nameInput" placeholder="Votre nom">
                            </div>
                            <div class="form-group">
                                <label>Email</label>
                                <input type="email" id="emailInput" placeholder="adresse@email.com">
                            </div>
                            <div class="form-group">
                                <label>Message</label>
                                <textarea id="msgInput" placeholder="Votre message..."></textarea>
                            </div>
                            <button class="send-btn" id="sendMsg">Envoyer le message</button>
                        </div>
                        <div class="message-preview">
                            <div class="preview-card" id="previewBlock">
                                <p><strong>Nom :</strong> <span id="previewName">—</span></p>
                                <p><strong>Email :</strong> <span id="previewEmail">—</span></p>
                                <p><strong>Message :</strong><br> <span id="previewMsg">Aperçu en direct</span></p>
                            </div>
                            <div class="message-actions">
                                <button class="small-btn" id="resetPreview">Réinitialiser</button>
                                <span class="highlight" id="charCount">0 caractères</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>© 2025 RATIANARIVO Mirindra Matthieu - Tous droits réservés</p>
    </footer>

    <script>
        // JavaScript pour l'aperçu en direct (optionnel mais fonctionnel)
        const nameInput = document.getElementById('nameInput');
        const emailInput = document.getElementById('emailInput');
        const msgInput = document.getElementById('msgInput');
        const previewName = document.getElementById('previewName');
        const previewEmail = document.getElementById('previewEmail');
        const previewMsg = document.getElementById('previewMsg');
        const charCount = document.getElementById('charCount');
        const resetBtn = document.getElementById('resetPreview');
        const sendBtn = document.getElementById('sendMsg');

        function updatePreview() {
            previewName.textContent = nameInput.value.trim() || '—';
            previewEmail.textContent = emailInput.value.trim() || '—';
            previewMsg.textContent = msgInput.value.trim() || 'Aperçu en direct';
            charCount.textContent = msgInput.value.length + ' caractères';
        }

        function resetForm() {
            nameInput.value = '';
            emailInput.value = '';
            msgInput.value = '';
            updatePreview();
        }

        nameInput.addEventListener('input', updatePreview);
        emailInput.addEventListener('input', updatePreview);
        msgInput.addEventListener('input', updatePreview);
        resetBtn.addEventListener('click', resetForm);

        sendBtn.addEventListener('click', function() {
            alert('Message envoyé (simulation)\nNom: ' + (nameInput.value || 'vide') + '\nEmail: ' + (emailInput.value || 'vide') + '\nMessage: ' + (msgInput.value || 'vide'));
        });

        // Initialisation
        updatePreview();
    </script>
</body>
</html>
