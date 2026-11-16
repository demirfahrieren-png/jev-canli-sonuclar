# Duygu filtresi geçmiş testi

Veri: Binance günlük kapanış BTCUSDT+ETHUSDT, Korku/Açgözlülük (alternative.me), Binance fonlama (başlangıç: {'BTCUSDT': '2019-09-10', 'ETHUSDT': '2019-11-27'}). Eğitim 2018-02-01 → 2023-12-31, test 2024-01-01 → 2026-11-15. Masraf her ağırlık değişiminde %0.15; karar kapanışta, uygulama ertesi gün.

**Eğitimde seçilen filtre:** korku≤20→en az %50 (eğitim Sharpe 1.11, filtresiz trend 1.10).

**Sonuç:** Duygu filtresi test döneminde trendi **anlamlı biçimde iyileştirmedi** (Sharpe 1.01 → 1.00). Izgaradaki 19 filtrenin 10'i test döneminde filtresiz trendi Sharpe'ta geçti; bu sayı düşükse seçilen filtrenin başarısı tesadüf olabilir.

## Test dönemi (eğitimde hiç kullanılmadı)

| Strateji | Toplam | Yıllık | En büyük düşüş | Sharpe | Masraf | Ort. yatırım |
|---|---|---|---|---|---|---|
| Al-tut (BTC+ETH eşit) | +17.5% | +5.8% | -59.9% | 0.37 | %0.1 | %100 |
| Trend topluluğu | +122.5% | +32.1% | -31.6% | 1.01 | %4.3 | %53 |
| Trend + korku≤20→en az %50 | +129.3% | +33.4% | -33.3% | 1.00 | %6.7 | %58 |

## Tüm dönem (bilgi amaçlı; ayar seçimi eğitimde yapıldı)

| Strateji | Toplam | Yıllık | En büyük düşüş | Sharpe | Masraf | Ort. yatırım |
|---|---|---|---|---|---|---|
| Al-tut (BTC+ETH eşit) | +308.4% | +17.4% | -84.3% | 0.59 | %0.1 | %100 |
| Trend topluluğu | +2392.9% | +44.2% | -49.1% | 1.07 | %12.5 | %52 |
| Trend + korku≤20→en az %50 | +2803.4% | +46.7% | -54.4% | 1.07 | %24.0 | %57 |

## Izgara — eğitim ve test Sharpe

| Filtre | Eğitim | Test |
|---|---|---|
| filtresiz | 1.10 | 1.01 |
| açgözlülük≥70→yarım | 0.81 | 1.02 |
| açgözlülük≥75→yarım | 0.96 | 1.04 |
| açgözlülük≥80→yarım | 0.97 | 1.01 |
| açgözlülük≥85→yarım | 0.96 | 1.01 |
| korku≤10→en az %50 | 1.04 | 0.98 |
| korku≤15→en az %50 | 1.07 | 0.99 |
| korku≤20→en az %50 | 1.11 | 1.00 |
| korku≤25→en az %50 | 1.07 | 0.98 |
| fonlama>%20/yıl→yarım | 1.10 | 0.98 |
| fonlama>%30/yıl→yarım | 1.07 | 1.04 |
| fonlama>%50/yıl→yarım | 1.08 | 0.99 |
| açgözlülük≥75→yarım, korku≤15→en az %50 | 0.92 | 1.01 |
| açgözlülük≥75→yarım, korku≤15→en az %50, fonlama>%30/yıl→yarım | 0.85 | 1.01 |
| açgözlülük≥75→yarım, korku≤20→en az %50 | 0.97 | 1.02 |
| açgözlülük≥75→yarım, korku≤20→en az %50, fonlama>%30/yıl→yarım | 0.90 | 1.03 |
| açgözlülük≥80→yarım, korku≤15→en az %50 | 0.93 | 0.99 |
| açgözlülük≥80→yarım, korku≤15→en az %50, fonlama>%30/yıl→yarım | 0.91 | 1.02 |
| açgözlülük≥80→yarım, korku≤20→en az %50 | 0.98 | 1.00 |
| açgözlülük≥80→yarım, korku≤20→en az %50, fonlama>%30/yıl→yarım | 0.95 | 1.03 |

Veri: alternative.me Korku ve Açgözlülük Endeksi; Binance. Geçmiş sonuç gelecekteki getiriyi göstermez.
