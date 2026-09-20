# Online Ticket Booking & Encrypted Verification 🎫

An end-to-end event and transport ticketing web platform featuring interactive seat reservations, automated payment verification, and encrypted QR Code E-Ticket generation with real-time gate scanner validation.

---

## 🌟 Live Demo & Portfolio
- **Author:** Frans Kurniawan
- **Portfolio:** [https://franskur.github.io](https://franskur.github.io)
- **Role:** Full-Stack PHP Web Developer

---

## 🚀 Key Features

- **Interactive Seat Map & Live Allocation:**
  - Real-time visual seat map showing available, reserved, and locked seats.
  - Concurrency control with database row-level locking to eliminate double-booking race conditions.

- **Encrypted QR Code PDF E-Ticket Issuance:**
  - Automated generation of tamper-proof PDF tickets with embedded encrypted HMAC tokens.
  - Barcode and QR code generation for digital or printed passes.

- **Gate Check-In Validator Module:**
  - Web camera / mobile-friendly QR scanner integration for sub-second ticket admission.
  - Instant validation logic: Valid, Already Used (with exact entry timestamp), or Invalid/Expired ticket alerts.

- **Order & Payment Lifecycle Management:**
  - Automated booking countdown timer and seat release upon payment timeout.
  - Transaction history, revenue reporting, and attendee export tools.

---

## 🛠️ Tech Stack & Architecture

- **Backend:** PHP 8.x, Laravel Framework (Routing, Controllers, Eloquent ORM, Middleware)
- **Database:** MySQL (ACID Transactions for transactional booking integrity)
- **QR Engine & PDF:** Endroid QR Code, DomPDF / TCPDF
- **Frontend:** JavaScript (ES6+), Blade Templating, Bootstrap 5, HTML5/CSS3
- **Security:** CSRF Protection, Encrypted Payload Tokenization, Rate Limiting

---

## ⚡ Local Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/franskur/ticket-booking-qr-verification.git
   cd ticket-booking-qr-verification
   ```

2. **Install Composer Dependencies:**
   ```bash
   composer install
   ```

3. **Configure Environment:**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
   *Configure your MySQL credentials in the `.env` file.*

4. **Run Migrations & Seeders:**
   ```bash
   php artisan migrate --seed
   ```

5. **Start Application:**
   ```bash
   php artisan serve
   ```
   *Access the web application at `http://127.0.0.1:8000`.*

---

## 📄 License & Notes
Designed and developed by **Frans Kurniawan**. Open for portfolio showcase and enterprise deployment.
