# Muhammad Amin — Portfolio WordPress Theme

A custom WordPress theme built for **muhammadamin.com** — a personal portfolio showcasing work, credentials, and contact information.

---

## 🚀 Getting Started (Local Setup)

Follow these steps to run this project on your local machine.

### ✅ Prerequisites

Make sure you have the following installed:

| Tool | Purpose | Download |
|------|---------|----------|
| [XAMPP](https://www.apachefriends.org/) | Local PHP + MySQL server | [Download](https://www.apachefriends.org/download.html) |
| [Git](https://git-scm.com/) | Version control | [Download](https://git-scm.com/downloads) |
| A code editor | e.g. VS Code | [Download](https://code.visualstudio.com/) |

---

### 📥 Step 1 — Clone the Repository

```bash
git clone https://github.com/obaidjaved/Portfolio-wordpress-theme.git
cd Portfolio-wordpress-theme
```

Place the cloned folder inside XAMPP's web root:

- **Windows:** `C:\xampp\htdocs\`
- **Mac/Linux:** `/opt/lampp/htdocs/`

So the final path should look like:
```
C:\xampp\htdocs\Portfolio-wordpress-theme\
```

---

### 🗄️ Step 2 — Create the Database

1. Start **Apache** and **MySQL** in the XAMPP Control Panel
2. Open your browser and go to: `http://localhost/phpmyadmin`
3. Click **"New"** in the left sidebar
4. Create a database — name it anything (e.g., `muhammad_amin_db`)

---

### ⚙️ Step 3 — Configure `wp-config.php`

The `wp-config.php` file is **intentionally excluded** from the repo (for security). You need to create your own:

1. Copy the sample file:
```bash
cp wp-config-sample.php wp-config.php
```

2. Open `wp-config.php` in your editor and update these lines:

```php
define( 'DB_NAME',     'muhammad_amin_db' );   // Your database name
define( 'DB_USER',     'root' );               // XAMPP default user
define( 'DB_PASSWORD', '' );                   // XAMPP default (empty)
define( 'DB_HOST',     'localhost' );
```

3. Update the secret keys by visiting:
   👉 https://api.wordpress.org/secret-key/1.1/salt/
   
   Copy and paste the generated keys into `wp-config.php`.

---

### 🔧 Step 4 — Run the WordPress Installer

Open your browser and go to:

```
http://localhost/Portfolio-wordpress-theme/
```

Follow the on-screen WordPress installation steps:
- Set a site title
- Create an admin username & password
- Enter your email

---

### 🎨 Step 5 — Activate the Custom Theme

1. Log in to WordPress Admin: `http://localhost/Portfolio-wordpress-theme/wp-admin`
2. Go to **Appearance → Themes**
3. Find **"Muhammad Amin"** theme and click **Activate**

Your local site is now running! 🎉

---

## 📁 Theme File Structure

```
wp-content/themes/muhammad-amin/
├── assets/
│   ├── img/              # Theme images
│   ├── styles.css        # Main stylesheet
│   └── script.js         # Theme JavaScript
├── front-page.php        # Homepage template
├── header.php            # Site header
├── footer.php            # Site footer
├── functions.php         # Theme functions & hooks
├── index.php             # Default template
├── page-about.php        # About page template
├── page-contact.php      # Contact page template
├── page-credentials.php  # Credentials/Resume page
├── page-work.php         # Portfolio/Work page
└── style.css             # Theme metadata (required by WordPress)
```

---

## 🛠️ Making Changes

All theme customizations live in:
```
wp-content/themes/muhammad-amin/
```

After making your changes:

```bash
git add .
git commit -m "describe your change here"
git push origin main
```

---

## 🌐 Setting Up WordPress Pages

After installing, create these Pages in **WordPress Admin → Pages → Add New**:

| Page Title | Template to Select |
|---|---|
| Home | Front Page |
| About | Page — About |
| Work | Page — Work |
| Credentials | Page — Credentials |
| Contact | Page — Contact |

Then go to **Settings → Reading** and set:
- **Your homepage displays:** A static page
- **Homepage:** Home

---

## 🔒 Security Notes

- `wp-config.php` is in `.gitignore` — **never commit it**
- Never push your database passwords to GitHub
- Use environment-specific `wp-config.php` files for local vs. production

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes
4. Push and open a Pull Request

---

## 📄 License

This theme is custom-built for Muhammad Amin's personal portfolio.  
All rights reserved © Muhammad Amin.

---

## 📬 Contact

**Live Site:** [muhammadamin.com](https://muhammadamin.com)  
**GitHub:** [@obaidjaved](https://github.com/obaidjaved)
