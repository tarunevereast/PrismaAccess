# PrismaAccess
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Post-Quantum Cryptography Overview</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap');
    body {
      margin: 0;
      background-color: #121213;
      font-family: 'Orbitron', Arial, sans-serif;
      color: #e0e0e0;
      overflow-x: hidden;
      position: relative;
      min-height: 100vh;
      padding: 20px 24px 40px 24px;
    }

    /* Watermark */
    .watermark {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-45deg);
      font-size: 5.2em;
      font-weight: 900;
      color: rgba(255, 0, 0, 0.3);
      letter-spacing: 10px;
      user-select: none;
      pointer-events: none;
      white-space: nowrap;
      z-index: 1000;
      text-shadow: 0 0 15px rgba(255, 0, 0, 0.5);
    }

    h1 {
      text-align: center;
      font-size: 2.8em;
      margin-bottom: 48px;
      color: #ff3a3a;
      text-shadow: 0 0 10px #ff1a1a;
    }

    /* Container for clickable cards */
    .container {
      max-width: 1080px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      gap: 28px;
      justify-content: center;
    }

    /* Card style */
    .card {
      background: rgba(25, 25, 25, 0.98);
      border-radius: 14px;
      box-shadow: 0 0 22px #ff2f2faa;
      width: 260px;
      padding: 20px;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      user-select: none;
    }
    .card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 30px #ff4a4aee;
    }

    .card img {
      max-width: 100%;
      height: 140px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 14px;
      box-shadow: 0 0 15px #ff3d3dbb;
    }

    .card h2 {
      font-size: 1.25rem;
      margin-bottom: 10px;
      color: #ff5050;
      text-shadow: 0 0 7px #ff1616;
    }

    /* Section content area */
    #content {
      max-width: 900px;
      margin: 40px auto 60px auto;
      background: rgba(25, 25, 25, 0.98);
      border-radius: 14px;
      box-shadow: 0 0 25px #ff2f2faa;
      padding: 30px 40px;
      color: #ddd;
      line-height: 1.65;
    }

    #content h2 {
      color: #ff3a3a;
      margin-bottom: 18px;
      text-shadow: 0 0 10px #ff1a1a;
      font-size: 2rem;
    }

    #content img {
      max-width: 100%;
      height: auto;
      border-radius: 12px;
      margin: 18px 0 22px 0;
      box-shadow: 0 0 18px #ff3d3dbb;
      display: block;
      margin-left: auto;
      margin-right: auto;
    }

    /* OEM logos inside content */
    .oem-logos {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 30px;
      margin-top: 25px;
    }
    .oem-logo {
      filter: brightness(0) invert(1);
      width: 140px;
      height: auto;
      cursor: default;
      transition: transform 0.3s ease;
    }
    .oem-logo:hover {
      filter: brightness(1) invert(0);
      transform: scale(1.1);
    }

    @media (max-width: 720px) {
      .card {
        width: 100%;
        max-width: 320px;
      }
      #content {
        padding: 25px 20px;
      }
      .oem-logo {
        width: 110px;
      }
    }
  </style>
</head>
<body>
  <div class="watermark">DEMO_WEB_APP</div>

  <h1>Post-Quantum Cryptography Overview</h1>

  <div class="container">
    <div class="card" data-section="origin">
      <img src="https://images.unsplash.com/photo-1602524815433-d3fca9d1a7d6?auto=format&fit=crop&w=600&q=80" alt="Mathematics and Quantum Physics" />
      <h2>Origin of PQC</h2>
      <p>Discover how PQC emerged to protect against quantum threats.</p>
    </div>
    <div class="card" data-section="relevance">
      <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80" alt="Data Protection" />
      <h2>Why PQC is Relevant Today</h2>
      <p>Understand challenges PQC defends against in today’s world.</p>
    </div>
    <div class="card" data-section="adoption">
      <img src="https://images.unsplash.com/photo-1463438690606-f6778b8c1d10?auto=format&fit=crop&w=600&q=80" alt="Industry Collaboration" />
      <h2>Industry Adoption Plans</h2>
      <p>See how organizations plan to implement PQC strategies.</p>
    </div>
    <div class="card" data-section="oem">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Palo_Alto_Networks_Logo.svg/2560px-Palo_Alto_Networks_Logo.svg.png" alt="OEM Logos" />
      <h2>OEM Solutions & Logos</h2>
      <p>Explore major security vendors offering PQC solutions.</p>
    </div>
  </div>

  <div id="content">
    <!-- Dynamic content will be loaded here -->
  </div>

  <script>
    const content = document.getElementById('content');

    const sections = {
      origin: `
        <h2>Origin of Post-Quantum Cryptography</h2>
        <img src="https://images.unsplash.com/photo-1602524815433-d3fca9d1a7d6?auto=format&fit=crop&w=900&q=80" alt="Mathematics and Quantum Physics" />
        <p>
          Post-Quantum Cryptography (PQC) emerged to counter the growing threat of quantum computers which can break classical encryption methods like RSA and ECC.
          After Shor’s algorithm demonstrated the ability to efficiently factor large numbers on quantum systems in the 1990s, researchers began developing quantum-resistant algorithms.
        </p>
        <p>
          PQC algorithms rely on mathematical problems believed to be resistant against both classical and quantum computing attacks,
          including lattice-based, code-based, hash-based, and multivariate polynomial cryptographic schemes.
        </p>
      `,
      relevance: `
        <h2>Why PQC is Relevant & Challenges it Solves</h2>
        <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=900&q=80" alt="Data Protection" />
        <p>
          Data today often needs to stay confidential for decades, encompassing sensitive government, health, and financial information.
          Quantum computers threaten these data security guarantees by potentially breaking classical encryption algorithms.
        </p>
        <p>
          The "store now, harvest later" attack is a major concern where adversaries collect encrypted data now and decrypt it once quantum capabilities mature.
          PQC provides the crucial protection necessary to defend against these challenges.
        </p>
      `,
      adoption: `
        <h2>How Organizations Are Planning to Adopt PQC</h2>
        <img src="https://images.unsplash.com/photo-1463438690606-f6778b8c1d10?auto=format&fit=crop&w=900&q=80" alt="Industry Collaboration" />
        <p>
          Leading organizations, led by NIST, are testing and standardizing PQC algorithms.
          Industry experts emphasize adopting crypto agility, allowing seamless algorithm updates as PQC matures.
        </p>
        <p>
          Adoption strategies include hybrid cryptography (mixing classical and PQC algorithms) as well as advances in quantum key distribution (QKD).
          Early adoption reduces future security risks posed by quantum computers.
        </p>
      `,
      oem: `
        <h2>Security Product OEMs Offering PQC Solutions</h2>
        <p>Several major security vendors incorporate PQC in their technologies or have active PQC initiatives:</p>
        <ul style="max-width:600px; margin: 20px auto; font-size:1.1rem; color:#fc6b6b; padding-left:18px;">
          <li><strong>Palo Alto Networks:</strong> Hybrid PQC-enabled firewalls and VPNs.</li>
          <li><strong>IBM Security:</strong> PQC in cloud and enterprise encryption services.</li>
          <li><strong>Microsoft Azure:</strong> Quantum-safe key management platforms.</li>
          <li><strong>Oracle:</strong> Embedding PQC in database & cloud security.</li>
          <li><strong>Entrust:</strong> PQC in PKI & identity management solutions.</li>
          <li><strong>Thales:</strong> PQC integrated in HSMs and network security products.</li>
        </ul>
        <div class="oem-logos" aria-label="PQC OEM Logos">
          <img class="oem-logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Palo_Alto_Networks_Logo.svg/2560px-Palo_Alto_Networks_Logo.svg.png" alt="Palo Alto Networks Logo" />
          <img class="oem-logo" src="https://upload.wikimedia.org/wikipedia/commons/5/51/IBM_logo.svg" alt="IBM Logo" />
          <img class="oem-logo" src="https://upload.wikimedia.org/wikipedia/commons/4/44/Microsoft_logo.svg" alt="Microsoft Logo" />
          <img class="oem-logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Oracle_logo.svg/2560px-Oracle_logo.svg.png" alt="Oracle Logo" />
          <img class="oem-logo" src="https://upload.wikimedia.org/wikipedia/commons/5/5f/Entrust_Logo.png" alt="Entrust Logo" />
          <img class="oem-logo" src="https://upload.wikimedia.org/wikipedia/commons/e/e9/Thales_Logo_2018.svg" alt="Thales Logo" />
        </div>
      `
    };

    // Default content
    content.innerHTML = sections.origin;

    // Card click event to switch content
    document.querySelectorAll('.card').forEach(card => {
      card.addEventListener('click', () => {
        const sectionKey = card.getAttribute('data-section');
        content.innerHTML = sections[sectionKey] || '';
        window.scrollTo({ top: 0, behavior: 'smooth' });
      });
    });
  </script>
</body>
</html>
