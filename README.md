# Semapore Örneği
Bu örnek uygulama, Texas Instruments Tiva4c mikrodenetleyici kartı üzerinde çalışan bir senkronizasyon örneğidir. Bu örnekte, iki farklı görev (task) arasında bir senkronizasyon sağlamak için semaforlar kullanılmıştır.

## Kod Açıklaması

Bu kod bloğu aşağıdaki işlevleri gerçekleştirir:

- İki farklı görev (task) oluşturur: `task1` ve `task2`.
- Her iki görev de bir döngü içinde çalışır ve belirli işlemleri gerçekleştirir.
- `task1`, bir semaforu gönderir (`Semaphore_post`) ve diğer semaforu bekler (`Semaphore_pend`).
- `task2`, diğer semaforu gönderir ve ilk semaforu bekler.
- Her iki görev de birbirlerine bağımlı bir şekilde çalışır, böylece senkronize olurlar.
- `task2`, belirli bir sayıda döngüden sonra BIOS'u sonlandırır, böylece logları konsola yazdırır.

## Kullanılan Donanım ve Kütüphaneler

- Texas Instruments Tiva C Series TM4C1294XL mikrodenetleyici kartı
- TI-RTOS (TI Gerçek Zamanlı İşletim Sistemi)
- TI-DRIVERS Kütüphanesi
- TI-SYSBIOS Kütüphanesi
