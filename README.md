<!-- HEADER BANNER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Nigeria%20State%20%26%20LGA%20Dataset&fontSize=35&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=SQL%20·%20JSON%20·%20CSV%20·%20XLSX%20·%20TXT&descAlignY=55&descSize=18" />
</p>

<!-- TYPING EFFECT -->
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&pause=1000&color=00F7FF&center=true&vCenter=true&width=700&lines=36+States+%2B+FCT+(Abuja);774+Local+Government+Areas;Ready-to-Use+Database+Files;Interactive+Web+Explorer+Included" />
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=2" width="100%"/>

<br>

<p align="center">
A clean, structured, and complete dataset of all <strong>36 Nigerian States + FCT (Abuja)</strong> and their corresponding <strong>Local Government Areas (LGAs)</strong> — ready to plug into any project.
</p>

<br>

---

## 📦 What's Inside

<p align="center">

```
├── files/
│   ├── states.sql       # All 37 states (36 + FCT) INSERT statements
│   ├── lgas.sql         # All LGAs with state_id foreign keys
│   ├── StateSeeder.php  # Laravel seeder for states
│   └── LgaSeeder.php    # Laravel seeder for LGAs
├── index.html           # Interactive browser-based explorer & exporter
├── README.md
└── LICENSE
```

</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:24243e,50:302b63,100:0f0c29&height=2" width="100%"/>

---

## 🗄️ Database Schema

### 📋 `states` table
```sql
CREATE TABLE `states` (
  `id`   INT UNSIGNED NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`id`)
);
```

### 🏛️ `lgas` table
```sql
CREATE TABLE `lgas` (
  `id`       INT UNSIGNED NOT NULL AUTO_INCREMENT,
  `state_id` INT UNSIGNED NOT NULL,
  `name`     VARCHAR(150) NOT NULL,
  PRIMARY KEY (`id`),
  FOREIGN KEY (`state_id`) REFERENCES `states`(`id`) ON DELETE CASCADE
);
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=2" width="100%"/>

---

## 🚀 Usage Options

<table>
<tr>
<td width="33%" valign="top">

### 🔹 Option 1
**Direct SQL Import**

Fast and straightforward database seeding.

```bash
mysql -u root -p database_name < files/states.sql
mysql -u root -p database_name < files/lgas.sql
```

</td>
<td width="33%" valign="top">

### 🔹 Option 2
**Interactive Explorer**

No installation required — works in browser!

<p align="center">
  <a href="https://solutionexe.github.io/nigeria-state-lga-sql/">
    <img src="https://img.shields.io/badge/🌐_Live_Explorer-00c9ff?style=for-the-badge&logoColor=white" />
  </a>
</p>

✨ Browse, filter, and export data

</td>
<td width="33%" valign="top">

### 🔹 Option 3
**Laravel Seeders**

Clean and maintainable approach for Laravel projects.

```bash
php artisan db:seed
```

Recommended for production systems.

</td>
</tr>
</table>

---

### 🎯 Detailed Laravel Integration

<details>
<summary><strong>📂 Using Seeder Classes (Recommended)</strong></summary>

<br>

**Step 1:** Copy seeder files to your project

```
database/
└── seeders/
    ├── StateSeeder.php
    └── LgaSeeder.php
```

**Step 2:** Register in `database/seeders/DatabaseSeeder.php`

```php
public function run(): void
{
    $this->call([
        StateSeeder::class,
        LgaSeeder::class,
    ]);
}
```

**Step 3:** Run the seeder

```bash
php artisan db:seed
```

</details>

<details>
<summary><strong>⚡ Alternative: Direct SQL Import</strong></summary>

<br>

```php
DB::unprepared(file_get_contents(database_path('files/states.sql')));
DB::unprepared(file_get_contents(database_path('files/lgas.sql')));
```

</details>

<br>

> **📌 Best Practice:**  
> **Direct SQL** (`.sql` files) → Fast, raw database insert  
> **Seeder Classes** → Laravel-friendly, recommended for maintainability and version control

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:24243e,50:302b63,100:0f0c29&height=2" width="100%"/>

---

## 📊 Dataset Overview

<p align="center">

| 🏛️ Entity | 📈 Count |
|-----------|----------|
| **States** | 37 (36 + FCT) |
| **LGAs** | 774 |

</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=2" width="100%"/>

---

## 🌍 Use Cases

<p align="center">

<img src="https://skillicons.dev/icons?i=laravel,django,nodejs,react,vue" />

</p>

<table>
<tr>
<td width="50%">

### 🛒 E-Commerce
- Shipping zone management
- Delivery fee calculation
- Regional product availability
- Store locator systems

</td>
<td width="50%">

### 📱 Web & Mobile Apps
- Registration forms
- Address autocomplete
- Location-based services
- User profile management

</td>
</tr>
<tr>
<td width="50%">

### 🏛️ Government & Civic Tech
- Electoral systems
- Census platforms
- Public service portals
- Administrative dashboards

</td>
<td width="50%">

### 📊 Research & Analytics
- Demographic studies
- Geographic analysis
- Data visualization
- Academic projects

</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:24243e,50:302b63,100:0f0c29&height=2" width="100%"/>

---

## 🎨 Interactive Web Explorer Features

<p align="center">
  <a href="https://solutionexe.github.io/nigeria-state-lga-sql/">
    <img src="https://img.shields.io/badge/🚀_Launch_Explorer-00c9ff?style=for-the-badge&logoColor=white" />
  </a>
</p>

<table>
<tr>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/📋_Browse-4CAF50?style=for-the-badge"/>
<br><br>
View all states and LGAs in an organized interface
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/🔍_Filter-2196F3?style=for-the-badge"/>
<br><br>
Search and filter states by name instantly
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/📥_Export-FF9800?style=for-the-badge"/>
<br><br>
Download as XLSX, CSV, JSON, or TXT
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/⚡_Zero_Install-9C27B0?style=for-the-badge"/>
<br><br>
Works directly in your browser
</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=2" width="100%"/>

---

## 🛠️ Built With

<p align="center">

| Technology | Purpose |
|------------|---------|
| **Raw SQL** | No ORM dependency — universal compatibility |
| **Vanilla HTML/CSS/JS** | Zero dependencies for the explorer |
| **SheetJS (CDN)** | Excel export functionality (optional) |

</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:24243e,50:302b63,100:0f0c29&height=2" width="100%"/>

---

## 🤝 Contributing

Found an LGA spelling issue or missing entry? **PRs are welcome!**

```bash
# 1. Fork the repo
# 2. Create your branch
git checkout -b fix/lga-name

# 3. Commit your changes
git commit -m 'fix: correct LGA name in Rivers State'

# 4. Push to your fork
git push origin fix/lga-name

# 5. Open a Pull Request
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=2" width="100%"/>

---

## 👤 Author

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&pause=1000&color=00F7FF&center=true&vCenter=true&width=500&lines=Crafted+by+Fasanya+Ayomide+Joshua;aka+Solution+%F0%9F%9A%80" />
</p>

<p align="center">
  <a href="https://github.com/SoLuTiOnExE">
    <img src="https://img.shields.io/badge/GitHub-@SoLuTiOnExE-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="mailto:fasanyaayomide2019@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:24243e,50:302b63,100:0f0c29&height=2" width="100%"/>

---

## 📄 License

<p align="center">
This project is licensed under the <strong>MIT License</strong> — see the <a href="./LICENSE">LICENSE</a> file for details.
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=2" width="100%"/>

---

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=18&pause=1000&color=00F7FF&center=true&vCenter=true&width=600&lines=If+this+helped+your+project...;a+%E2%AD%90+on+GitHub+goes+a+long+way!" />
</p>

<p align="center">
  <a href="https://github.com/SoLuTiOnExE/nigeria-state-lga-sql">
    <img src="https://img.shields.io/github/stars/SoLuTiOnExE/nigeria-state-lga-sql?style=social" />
  </a>
</p>

<!-- FOOTER BANNER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=120&section=footer"/>
</p>
