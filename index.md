<style>
  /* 1. Oculta el encabezado del tema y ajusta espacio superior */
  header { display: none !important; }
  .wrapper { margin-top: 0px !important; padding-top: 60px !important; }

  /* 2. BLOQUEO AGRESIVO DE LA BARRA DE GOOGLE */
  /* Forzamos que el HTML y el Body no se desplacen hacia abajo */
  html { top: 0px !important; }
  body { top: 0px !important; position: static !important; }

  /* Ocultamos el iframe de la barra superior */
  .goog-te-banner-frame, 
  .goog-te-banner-frame.skiptranslate,
  iframe.goog-te-banner-frame {
    display: none !important;
    visibility: hidden !important;
  }

  /* 3. OCULTAR WIDGETS RESIDUALES */
  #google_translate_element, 
  .goog-te-gadget, 
  .goog-te-gadget-simple,
  .skiptranslate > iframe {
    display: none !important;
  }

  /* 4. EVITAR EL "SUBRAYADO" Y GLOBOS DE TEXTO AL TRADUCIR */
  #goog-gt-tt, .goog-te-balloon-frame, .goog-tooltip, .goog-tooltip:hover {
    display: none !important;
    visibility: hidden !important;
  }
  .goog-text-highlight {
    background-color: transparent !important;
    box-shadow: none !important;
  }
</style>

<div align="right" style="padding-right: 20px;">
  <a href="#" onclick="doGTranslate('pt|pt');return false;" title="Português" style="text-decoration:none; font-size:28px;">🇧🇷</a> 
  <a href="#" onclick="doGTranslate('pt|es');return false;" title="Español" style="text-decoration:none; font-size:28px;">&nbsp;🇦🇷</a> 
  <a href="#" onclick="doGTranslate('pt|en');return false;" title="English" style="text-decoration:none; font-size:28px;">&nbsp;🇺🇸</a>
</div>

<div id="google_translate_element" style="display:none"></div>
<script type="text/javascript">
function googleTranslateElementInit() {
  new google.translate.TranslateElement({pageLanguage: 'pt', autoDisplay: false}, 'google_translate_element');
}
function doGTranslate(lang_pair) {
  if(lang_pair.value) lang_pair=lang_pair.value;
  if(lang_pair=='') return;
  var lang=lang_pair.split('|')[1];
  var teCombo = document.querySelector('.goog-te-combo');
  if(teCombo == null || teCombo.value == null) {
    setTimeout(function(){doGTranslate(lang_pair)}, 500);
  } else {
    teCombo.value = lang;
    const event = new Event('change', { bubbles: true });
    teCombo.dispatchEvent(event);
  }
}
  // Función para eliminar rastro de la barra de Google cada vez que se traduce
function removeGoogleBar() {
  var barra = document.querySelector('.goog-te-banner-frame');
  if (barra) {
    barra.style.display = 'none';
  }
  document.body.style.top = "0px";
}

// Ejecutar la limpieza periódicamente mientras se usa la página
setInterval(removeGoogleBar, 500);
</script>
<script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>

<hr style="border: 0.5px solid #333; margin-top: 10px;">

# 🛡️ Miguel Ángel Lofredo | Cybersecurity Researcher

Bem-vindo ao meu espaço de documentação e segurança ofensiva. Sou um apaixonado por cibersegurança com foco especializado em **Infraestrutura (AD)**,**Web** e **Cloud** 

Ao longo de mais de 4 anos de formação autodidata e certificada, consolidei um perfil técnico orientado à resolução de problemas e à exploração ética em ciberseguranca.

---

### 🚀 Sobre mim
Atualmente, dedico-me à investigação de ameaças e à construção de ambientes controlados. Meu foco não se limita a "quebrar" sistemas, meu objetivo é compreender a arquitetura subjacente para propor mitigações eficazes.

* **Foco Atual:** Expandindo minha visão para o **Blue Team (SOC)** através do HackTheBox para desenvolver uma mentalidade defensiva que complemente minhas habilidades ofensivas.
* **Projeto atual:** [Red / Blue Active Directory homelab](https://github.com/miguellofredo85/Lab-AD-Red-Blue) Laboratório de ataque e defesa que inclui a criação de um diretório ativo (DC mais quatro Windows 10), monitorado pelo Wazuh SIEMS integrado com VirusTotal, Sysmon e Suricata - um potente sistema de detecção de intrusão de rede (IDS), sistema de prevenção de intrusão (IPS) e monitoramento de segurança de rede (NSM). Este repositório contém instruções passo a passo para que você mesmo possa montá-lo, com detalhes de cada ataque, desde a configuração no AD para que ele seja realizado, até as etapas passo a passo para atacar, prevenir e detectar (com regras para cada caso). Em constante desenvolvimento.

---

### 🎓 Certificações em Destaque
Possuo certificações que validam meus conhecimentos em operações de Red Team, Pentesting infra e web:


<img width="300" height="300" alt="e3abd5d7-15b6-4319-bdff-d97390af58ed" src="https://github.com/user-attachments/assets/5ca91d24-1fb8-48fc-8e2c-c73b8a0a3243" />
<img width="300" height="300" alt="hack-the-box-certified-penetration-testing-specialist-htb-cpts" src="https://github.com/user-attachments/assets/2fdabda9-b448-440a-91ab-ed826c8aecb2" />
<img width="300" height="300" alt="hack-the-box-certified-web-exploitation-specialist-" src="https://github.com/user-attachments/assets/9b0984cd-8a79-4b25-ba15-90416290eb75" />

<div align="center">
<br>
<img src="https://github.com/user-attachments/assets/2634aa32-43d8-4375-8629-f51991dc7e90" width="160" alt="CRTO" style="margin: 10px;">
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://github.com/user-attachments/assets/b7bb2680-cc74-46e9-9b9b-feae726256a0" width="160" alt="CPTS" style="margin: 10px;">
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://github.com/user-attachments/assets/543a828f-8f9c-4b94-b505-939a8c256234" width="110" alt="CWES" style="margin: 10px;">
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://github.com/user-attachments/assets/b6a8b63e-d2dd-4e2a-bfad-fb3f580d781c" width="110" alt="Google" style="margin: 10px;">
<br>
</div>

---

### 🛠️ Labs & Formação Contínua
Minha metodologia de aprendizado baseia-se na prática constante nas plataformas mais exigentes do setor:

* **Infraestrutura:** Criação de laboratórios próprios de AD para simular ataques, escalada de privilégios, movimentação lateral.
* **Plataformas que acompanham meus estudos:** *
    * **[HackTheBox](https://www.hackthebox.com/)**
    * **[TryHackMe](tryhackme.com)**
    * **[PortSwigger Academy](https://portswigger.net/web-security/learning-paths))**
    * **[TCM Security](https://academy.tcm-sec.com/)**
    * **[INE](https://ine.com/)** 
    * **[Pwn College](https://pwn.college/)**
    * **[Pwnedlabs](https://pwnedlabs.io/)**
      
---

### 📈 Objetivos
Minha meta é realizar a transição para o setor profissional, aportando uma mentalidade analítica e técnica. Estou convencido de que entender como o atacante pensa é a melhor forma de construir defesas.

---
📫 **Quer entrar em contato comigo?** Você pode me encontrar no [LinkedIn](https://www.linkedin.com/in/miguelangellofredo/).








