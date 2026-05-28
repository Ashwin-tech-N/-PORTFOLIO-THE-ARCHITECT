# Vanguard | The Architect Portfolio

A premium, cinematic full-stack developer portfolio built by **Ashwin N**. Designed with a medieval-futuristic luxury aesthetic ("House Stark / Winter is Coding"), this portfolio features custom animations, high-end visual effects, and full responsive design.

<img width="1919" height="961" alt="Screenshot 2026-05-28 132051" src="https://github.com/user-attachments/assets/f9ed7f07-ff28-4e08-9191-4dc2c7215145" />

## 🌟 Key Features

*   **Cinematic Loader:** A custom SVG sword drawing animation followed by a shockwave ripple transition that slides open to reveal the main landing page.
*   **Dynamic Particle System:** Interactive HTML5 background embers/sparks that float upwards and drift organically.
*   **Parallax Scroll Waves:** Dynamic CSS-based background waves that shift horizontally at varying speeds relative to scroll depth.
*   **The Armory (Project Showcase):** A horizontal 3D-perspective slider displaying projects (ACODER, Puducherry Police Digital Portal, CareerFlow AI, and more) with hover scale effects, overlays, and descriptions.
*   **Credentials (Certificates):** A custom horizontal showcase demonstrating academic certificates and digital credentials.
*   **The Arsenal (Skills):** Interactive mastery indicators with hover-activated custom CSS gradient progress bars.
*   **Send A Raven (Contact Form):** A fully operational client-side form integrated with **EmailJS** for instant email alerts, with input validation.
*   **Cross-Device Optimization:** Complete responsive compatibility across mobile devices, tablets, and desktops (with custom gesture-based touch/drag support for horizontal carousels).

---

## 🛠️ Tech Stack & Integration

*   **Core:** Semantic HTML5, Vanilla CSS3 (Custom Variables, Keyframes, Perspective), Vanilla ES6+ JavaScript.
*   **Email Gateway:** [EmailJS SDK](https://www.emailjs.com/) for form submissions.
*   **Typography:** Google Fonts (Outfit / Inter / Serif families).
*   **Asset Management:** PDF resumes, optimized raster thumbnails, and vector inline SVGs.

---

## 📂 Project Structure

```bash
├── .vscode/               # Local VS Code settings (Live Server configuration)
├── certificate/           # Credential images/certificates
├── images/                # Project thumbnails and profile images
├── Ashwin_N_Resume.pdf    # Ashwin's professional resume (PDF)
├── index.html             # Core HTML template containing layout & structure
├── script.js              # Application logic, particle physics, and email triggers
├── style.css              # Custom styling, animations, responsive design tokens
└── README.md              # Project documentation
```

---

## 🚀 Setup & Local Development

### 1. Run Locally
This is a static front-end web application that can be run with any local development server. 

The project contains configuration settings for **VS Code Live Server**:
1. Open the root folder (`portfolio`) in **VS Code**.
2. Click **Go Live** in the status bar (uses port `5501` as configured in `.vscode/settings.json`).
3. The page will automatically open at `http://127.0.0.1:5501`.

### 2. Configure the Contact Form (EmailJS)
To receive emails from the **Send A Raven** contact form, connect it to your EmailJS account:

1. Sign up/Log in to your account at [EmailJS](https://www.emailjs.com/).
2. Create an **Email Service** (e.g., using Gmail) and note the `Service ID`.
3. Create an **Email Template** and note the `Template ID`. The template should contain variables matching the form inputs:
    *   `{{from_name}}`
    *   `{{from_email}}`
    *   `{{phone}}`
    *   `{{message}}`
4. Update the initialization code in [script.js](file:///a:/portfolio/script.js#L1-L27):
    *   Replace the User Public Key on line 2:
        ```javascript
        emailjs.init("YOUR_PUBLIC_KEY");
        ```
    *   Replace the Service ID and Template ID on lines 13-14:
        ```javascript
        emailjs.sendForm(
            "YOUR_SERVICE_ID",
            "YOUR_TEMPLATE_ID",
            "#ravenForm"
        )
        ```

---

## 📋 License

This project is open-source and available under the MIT License. Winter is Coding.
