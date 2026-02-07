# Filament Laravel: “POST method is not supported for route admin/login” problemi və həlli

Laravel/Filament layihənizi serverə yüklədikdən sonra belə bir xəta ilə qarşılaşa bilərsiniz:

The POST method is not supported for route admin/login. Supported methods: GET, HEAD.


Bu xəta adətən **Livewire assets-lərinin düzgün serverə yüklənməməsi** və ya **cache-in köhnə qalması** səbəbindən baş verir.

---

## Problem

- Filament admin paneli Livewire üzərində işləyir və login formu POST metodu ilə məlumat göndərir.  
- Serverdə Livewire asset-ləri düzgün yayımlanmayıbsa, form POST metodu işləməyəcək və yuxarıdakı xəta yaranacaq.  

---

## Həll

Terminalda layihənin kök qovluğunda aşağıdakı əmri işə salın:

```bash
php artisan vendor:publish --force --tag=livewire:assets
