<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Portfolio - Matthieu RATIANARIVO</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }

        body {
            background: linear-gradient(145deg, #e0f2fe 0%, #b4d6d6 100%);
            min-height: 100vh;
            color: #1e293b;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Header moderne */
        header {
            background: rgba(255,255,255,0.85);
            backdrop-filter: blur(20px) saturate(180%);
            -webkit-backdrop-filter: blur(20px) saturate(180%);
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.15);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(255,255,255,0.5);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.8rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.3rem;
            font-weight: 700;
            background: linear-gradient(135deg, #1e3c4f, #2c5e6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-decoration: none;
            letter-spacing: -0.5px;
            transition: 0.3s;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
        }

        .nav-links a {
            text-decoration: none;
            font-weight: 600;
            color: #1e3c4f;
            position: relative;
            padding-bottom: 4px;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 3px;
            background: #3b8f9e;
            border-radius: 2px;
            transition: 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Sections */
        section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 100px 0;
            position: relative;
        }

        #accueil {
            background: radial-gradient(circle at 80% 30%, rgba(146, 210, 230, 0.4), transparent 40%);
        }

        .hero h1 {
            font-size: clamp(2rem, 5vw, 3.5rem);
            margin-bottom: 1rem;
            background: linear-gradient(145deg, #1e3c4f, #205b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            color: #1e3c4f;
            font-weight: 400;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: linear-gradient(145deg, #317f8c, #235f6b);
            color: white;
            border-radius: 60px;
            text-decoration: none;
            font-weight: 600;
            box-shadow: 0 20px 30px -10px rgba(34, 98, 112, 0.4);
            transition: 0.3s;
            border: 1px solid rgba(255,255,255,0.3);
        }

        .btn:hover {
            transform: translateY(-6px);
            box-shadow: 0 30px 40px -10px #1e5a67;
        }

        /* À propos */
        #apropos {
            background: rgba(255,250,240,0.5);
            backdrop-filter: blur(8px);
        }

        .apropos-content {
            display: flex;
            gap: 4rem;
            align-items: center;
            flex-wrap: wrap;
        }

        .apropos-text {
            flex: 2;
            min-width: 300px;
        }

        .apropos-text h2 {
            font-size: 2.5rem;
            color: #1e3c4f;
            margin-bottom: 1.5rem;
            position: relative;
        }

        .apropos-text h2:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -10px;
            width: 80px;
            height: 4px;
            background: #317f8c;
            border-radius: 4px;
        }

        .apropos-text p {
            margin: 1.2rem 0;
            line-height: 1.7;
            color: #1e3c4f;
            font-weight: 450;
        }

        .skills {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin: 2rem 0;
        }

        .skill {
            background: white;
            padding: 0.7rem 1.8rem;
            border-radius: 40px;
            font-weight: 600;
            color: #1e4b59;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border: 1px solid #cbd5e1;
            transition: 0.2s;
            cursor: default;
        }

        .skill:hover {
            background: #317f8c;
            color: white;
            border-color: #317f8c;
            transform: scale(1.05);
        }

        .apropos-image {
            flex: 1;
            min-width: 250px;
            text-align: center;
        }

        .apropos-image img {
            width: 100%;
            max-width: 350px;
            border-radius: 30px 10px 30px 10px;
            box-shadow: 0 30px 40px -15px #1e3c4f;
            border: 4px solid white;
            transition: 0.4s;
        }

        .apropos-image img:hover {
            border-radius: 10px 30px 10px 30px;
            transform: rotate(2deg) scale(1.02);
        }

        /* Contact Cards */
        #contact {
            background: linear-gradient(145deg, #c3e0e5, #a7cfd5);
        }

        .contact-cards {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin: 3rem 0;
        }

        .contact-card {
            background: rgba(255,255,255,0.7);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.5);
            padding: 2rem 2rem;
            border-radius: 30px;
            flex: 1 1 250px;
            text-align: center;
            box-shadow: 0 20px 40px -15px #1e4b59;
            transition: 0.4s;
        }

        .contact-card:hover {
            transform: translateY(-15px);
            background: rgba(255,255,255,0.9);
        }

        .contact-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
        }

        .contact-card h3 {
            font-size: 1.6rem;
            margin-bottom: 0.5rem;
            color: #1d3f4a;
        }

        .contact-card p {
            font-weight: 600;
            margin-bottom: 1.5rem;
            word-break: break-word;
        }

        .contact-link {
            display: inline-block;
            padding: 0.8rem 2rem;
            background: #317f8c;
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
            border: 1px solid transparent;
        }

        .contact-link:hover {
            background: white;
            color: #1e4b59;
            border-color: #1e4b59;
        }

        /* --- NOUVEAU : BLOC EMAIL INTERACTIF --- */
        .live-message-section {
            background: white;
            border-radius: 40px 40px 20px 20px;
            padding: 2rem 2rem 3rem;
            margin-top: 3rem;
            box-shadow: 0 -5px 30px rgba(0,0,0,0.1);
            border: 1px solid #d1e6ed;
        }

        .live-message-section h3 {
            font-size: 2rem;
            color: #1e3c4f;
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 1rem;
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
            background: #e5f0f3;
            border-radius: 30px;
            padding: 2rem;
            border: 2px dashed #5f9ea0;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            font-weight: 600;
            color: #1d4c58;
            display: block;
            margin-bottom: 0.3rem;
        }

        .form-group input, 
        .form-group textarea {
            width: 100%;
            padding: 1rem 1.2rem;
            border: 2px solid #c7e0e7;
            border-radius: 60px;
            font-size: 1rem;
            transition: 0.2s;
            background: rgba(255,255,255,0.8);
        }

        .form-group textarea {
            border-radius: 30px;
            resize: vertical;
            min-height: 120px;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #2e7e8c;
            box-shadow: 0 0 0 4px rgba(56, 142, 160, 0.3);
        }

        .send-btn {
            background: linear-gradient(145deg, #267a88, #1b5c68);
            color: white;
            border: none;
            padding: 1rem 2.5rem;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            transition: 0.3s;
            border: 1px solid #a2d6df;
        }

        .send-btn:hover {
            background: #1b5c68;
            transform: scale(1.05);
            box-shadow: 0 15px 30px #1b5c6870;
        }

        .preview-card {
            background: white;
            border-radius: 25px;
            padding: 1.5rem;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .preview-card p {
            margin: 0.5rem 0;
            border-bottom: 1px solid #e2e8f0;
            padding-bottom: 0.5rem;
        }

        .preview-card strong {
            color: #1d4c58;
            min-width: 80px;
            display: inline-block;
        }

        .highlight {
            background: #b9e6ed;
            padding: 0.2rem 0.6rem;
            border-radius: 30px;
            font-size: 0.9rem;
            color: #0b3f4a;
        }

        .message-actions {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 1.5rem;
        }

        .small-btn {
            background: #d1e7ed;
            border: none;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            font-weight: 600;
            color: #1b4c58;
            cursor: pointer;
            transition: 0.2s;
            border: 1px solid #a0c4cf;
        }

        .small-btn:hover {
            background: #b1d4de;
        }

        /* Footer */
        footer {
            background: #1e3c4f;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* Responsive */
        @media (max-width: 700px) {
            .nav-links {
                gap: 1rem;
            }
            .message-grid {
                flex-direction: column;
            }
            .apropos-content {
                flex-direction: column-reverse;
                text-align: center;
            }
            .apropos-text h2:after {
                left: 50%;
                transform: translateX(-50%);
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a href="#accueil" class="logo">RATIANARIVO M. Matthieu</a>
            <div class="nav-links">
                <a href="#accueil">Accueil</a>
                <a href="#apropos">À propos</a>
                <a href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <section id="accueil">
        <div class="container hero">
            <h1>Bonjour, je suis RATIANARIVO Mirindra Matthieu</h1>
            <p>Développeur créatif passionné par la création d'expériences web uniques et mémorables</p>
            <a href="#apropos" class="btn">En savoir plus</a>
        </div>
    </section>

    <section id="apropos">
        <div class="container apropos-content">
            <div class="apropos-text">
                <h2>À propos de moi</h2>
                <p>Je suis un développeur passionné par le site web. J'aime transformer des idées créatives en solutions numériques fonctionnelles. J'ai acquis des bases en programmation (HTML, CSS, JavaScript).</p>
                <p>Motivé, sérieux et curieux d'apprendre, je cherche une opportunité pour développer mes compétences pratiques et mieux comprendre le fonctionnement web, notamment sur des sites simples, ce qui nourrit ma logique et ma créativité.</p>
                <p>Je reste à votre disposition pour un entretien et vous remercie de l'intention portée à ma candidature.</p>
                <p><em>"La technologie construit le système, l'expérience construit la relation."</em></p>
                <div class="skills">
                    <span class="skill">HTML</span>
                    <span class="skill">CSS</span>
                    <span class="skill">JavaScript</span>
                    <span class="skill">UI/Design</span>
                </div>
            </div>
            <div class="apropos-image">
                <img src="1772355979542.jpg" alt="Photo de profil Matthieu" onerror="this.src='https://via.placeholder.com/350x400?text=Photo+Matthieu'">
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container contact-content">
            <h2 style="font-size: 2.5rem; color: #1e3c4f;">Travaillons ensemble</h2>
            <p style="margin-bottom: 2rem; font-size: 1.2rem;">Vous avez un projet en tête ? Écrivez-moi directement !</p>

            <div class="contact-cards">
                <div class="contact-card">
                    <span class="contact-icon">📱</span>
                    <h3>WhatsApp</h3>
                    <p>+261 38 62 876 80</p>
                    <a href="https://wa.me/261386287680?text=Bonjour%20Matthieu" class="contact-link" target="_blank">Message</a>
                </div>
                <div class="contact-card">
                    <span class="contact-icon">📞</span>
                    <h3>Téléphone</h3>
                    <p>+261 38 62 876 80</p>
                    <a href="tel:+261386287680" class="contact-link">Appeler</a>
                </div>
                <div class="contact-card">
                    <span class="contact-icon">✉️</span>
                    <h3>Email</h3>
                    <p>mirindramatthieu@gmail.com</p>
                    <a href="mailto:mirindramatthieu@gmail.com" class="contact-link">Envoyer mail</a>
                </div>
            </div>

            <!-- ========== NOUVEAU BLOC MESSAGE EN BAS ========== -->
            <div class="live-message-section">
                <h3>📬 Me contacter par email</h3>
                <div class="message-grid">
                    <!-- Partie formulaire -->
                    <div class="message-form">
                        <div class="form-group">
                            <label>Votre nom</label>
                            <input type="text" id="nameInput" placeholder="ex: Jean Dupont" value="Faniry">
                        </div>
                        <div class="form-group">
                            <label>Votre email</label>
                            <input type="email" id="emailInput" placeholder="ex: jean@exemple.fr" value="faniry@test.com">
                        </div>
                        <div class="form-group">
                            <label>Message</label>
                            <textarea id="msgInput" placeholder="Bonjour Matthieu, j'ai un projet web...">Bonjour, j'aimerais discuter de vos services !</textarea>
                        </div>
                        <button class="send-btn" id="sendMessageBtn">
                            <span>✈️</span> Envoyer le message
                        </button>
                        <div style="margin-top: 1rem; font-size: 0.95rem; color: #23606e;" id="liveFeedback"></div>
                    </div>
                    
                    <!-- Partie prévisualisation + actions -->
                    <div class="message-preview">
                        <h4 style="color: #1e3c4f; margin-bottom: 1rem;">🔍 Aperçu</h4>
                        <div class="preview-card" id="previewBox">
                            <p><strong>Nom :</strong> <span id="previewName">Faniry</span></p>
                            <p><strong>Email :</strong> <span id="previewEmail">faniry@test.com</span></p>
                            <p><strong>Message :</strong><br> <span id="previewMsg">Bonjour, j'aimerais discuter de vos services !</span></p>
                        </div>
                        <div class="message-actions">
                            <button class="small-btn" id="copyPreviewBtn">📋 Copier le message</button>
                            <button class="small-btn" id="resetDemoBtn">🔄 Réinitialiser</button>
                        </div>
                        <p style="margin-top: 1rem; font-size: 0.9rem; background: #fff2d8; padding: 0.6rem; border-radius: 20px;">
                            ⚡ Le bouton "Envoyer" ouvre votre logiciel de messagerie avec les informations ci-dessus.
                        </p>
                    </div>
                </div>
            </div>
            <!-- ========== FIN BLOC ========== -->

            <div style="margin-top: 2rem; display: flex; gap: 1rem; justify-content: center;">
                <a href="#" class="contact-link" style="background: #0077b5;">LinkedIn</a>
                <a href="#" class="contact-link" style="background: #24292e;">GitHub</a>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2026 RATIANARIVO Mirindra Matthieu — Créativité & développement</p>
        </div>
    </footer>

    <script>
        (function() {
            // Smooth scroll
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const id = this.getAttribute('href');
                    document.querySelector(id)?.scrollIntoView({ behavior: 'smooth' });
                });
            });

            // ===== GESTION DU FORMULAIRE DE MESSAGE =====
            const nameInput = document.getElementById('nameInput');
            const emailInput = document.getElementById('emailInput');
            const msgInput = document.getElementById('msgInput');
            const previewName = document.getElementById('previewName');
            const previewEmail = document.getElementById('previewEmail');
            const previewMsg = document.getElementById('previewMsg');
            const liveFeedback = document.getElementById('liveFeedback');
            const sendBtn = document.getElementById('sendMessageBtn');

            // Fonction de mise à jour de l'aperçu
            function updatePreview() {
                previewName.innerText = nameInput.value.trim() || '(non renseigné)';
                previewEmail.innerText = emailInput.value.trim() || '(non renseigné)';
                previewMsg.innerText = msgInput.value.trim() || '(vide)';
            }

            // Écouter les changements
            nameInput.addEventListener('input', updatePreview);
            emailInput.addEventListener('input', updatePreview);
            msgInput.addEventListener('input', updatePreview);

            // Bouton envoyer : prépare le mail
            sendBtn.addEventListener('click', function() {
                const nom = encodeURIComponent(nameInput.value.trim());
                const email = encodeURIComponent(emailInput.value.trim());
                const message = encodeURIComponent(msgInput.value.trim());
                
                if (!nom || !email || !message) {
                    liveFeedback.innerText = '❌ Veuillez remplir tous les champs.';
                    liveFeedback.style.color = '#b91c1c';
                    return;
                }

                // Construction du mailto: avec corps et sujet
                const sujet = encodeURIComponent('Contact depuis votre portfolio');
                const corps = encodeURIComponent(
`Nom : ${nameInput.value.trim()}
Email : ${emailInput.value.trim()}

Message :
${msgInput.value.trim()}`
                );
                
                const mailtoLink = `mailto:mirindramatthieu@gmail.com?subject=${sujet}&body=${corps}`;
                
                // Petit retour avant ouverture
                liveFeedback.innerText = '✅ Ouverture de votre application mail...';
                liveFeedback.style.color = '#1f7a4b';
                
                // Ouvre le client mail
                window.location.href = mailtoLink;

                // Option : ouverture en arrière plan (certains navigateurs)
                setTimeout(() => {
                    liveFeedback.innerText = '📨 N\'oubliez pas d\'envoyer !';
                }, 2000);
            });

            // Copier le message dans le presse-papier
            document.getElementById('copyPreviewBtn').addEventListener('click', function() {
                const textToCopy = `Nom: ${previewName.innerText}\nEmail: ${previewEmail.innerText}\nMessage: ${previewMsg.innerText}`;
                navigator.clipboard.writeText(textToCopy).then(() => {
                    liveFeedback.innerText = '📋 Message copié dans le presse-papier !';
                    liveFeedback.style.color = '#2b6e7d';
                }).catch(() => {
                    liveFeedback.innerText = '❌ Erreur de copie';
                });
            });

            // Réinitialiser les champs (exemple)
            document.getElementById('resetDemoBtn').addEventListener('click', function() {
                nameInput.value = 'Jean Test';
                emailInput.value = 'jean@demo.fr';
                msgInput.value = 'Bonjour, je souhaite en savoir plus.';
                updatePreview();
                liveFeedback.innerText = '🔄 Champs réinitialisés (exemple)';
                liveFeedback.style.color = '#1e3c4f';
            });

            // confirmation appel téléphonique
            document.querySelectorAll('a[href^="tel:"]').forEach(link => {
                link.addEventListener('click', (e) => {
                    if (!confirm('Appeler ce numéro ?')) e.preventDefault();
                });
            });

            // Observer pour animations douces
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, { threshold: 0.2 });
            
            document.querySelectorAll('section, .contact-card').forEach(el => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                el.style.transition = '0.6s';
                observer.observe(el);
            });

            // Initial preview
            updatePreview();
        })();
    </script>
</body>
</html>
