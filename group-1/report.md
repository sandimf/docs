---
description: >-
  Report aktivitas klinik gunung mencakup setiap data pada pengguna, pengguna
  atau role tertuntu akan memiliki reportnya masing masing seperti report untuk
  screening ataupun payments untuk kasir.
---

# Report

## Route

Cashier

* Personal Report

```php
Route::get('/report', [CashierReportController::class, 'index'])
->name('cashier.report');
```

* Laporan atau aktivitas sebelumnya

```php
Route::get('/daily-report', [CashierReportController::class, 'dailyReport'])
->name('cashier.dailyReport');
```

## Paramedis
