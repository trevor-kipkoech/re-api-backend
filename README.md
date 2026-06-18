<p align="center">
    <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Modern Real Estate Architecture" width="100%" style="border-radius: 12px;">
</p>

# 🏢 Real Estate App — Backend API

[![PHP Version](https://img.shields.io/badge/PHP-8.3-777BB4?style=flat&logo=php&logoColor=white)](https://php.net)
[![Laravel Version](https://img.shields.io/badge/Laravel-12-FF2D20?style=flat&logo=laravel&logoColor=white)](https://laravel.com)
[![Database](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat&logo=mysql&logoColor=white)](https://mysql.com)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=flat)](LICENSE)

> **Multi-tenant SaaS platform** for real estate agencies. Built with Laravel to handle property listings, CRM pipelines, secure document vaulting (KYC/Title Deeds), and escrow tracking.

---

## 📦 Stack

- **Runtime:** PHP 8.3
- **Framework:** Laravel 12
- **Database:** MySQL
- **Auth:** Laravel Sanctum (token-based, CSRF-protected)
- **Storage:** Supabase S3 (private bucket for KYC and title deeds)
- **Queue:** Laravel Jobs (notifications, matching algorithm)
- **Scheduler:** Laravel Cron (auto-expire listings)

---

## 🏛️ Architecture

Multi-tenancy is handled via **Logical Tenant Separation** — every model scoped to `agency_id` through a Laravel Global Scope. No agency can query another's data at the database level.
