# Beijing Airport Transfer Brief: Capital (PEK) vs Daxing (PKX)

**Purpose:** Decide which Beijing airport a colleague should book into, based on the taxi drive from central Beijing.

**Source of figures:** Live driving distance/duration from the mapping service (Google Maps). All fare, difference, and conversion arithmetic was computed in Python from those exact returned values.

---

## 1. Start reference (for the driver dispatch app)

Lookup: `Beijing`

| Field | Value |
|---|---|
| Coordinates | **39.904211, 116.407395** |
| Place identifier | **ChIJuSwU55ZS8DURiqkPryBWYrk** |
| Formatted address | Beijing, China |

## 2. Live driving figures (driving mode, from 39.904211, 116.407395)

| Airport | Driving distance | Driving time |
|---|---|---|
| Beijing Capital International Airport (PEK) | **28.8 km** (28,776 m) | **32 mins** (1,925 s) |
| Beijing Daxing International Airport (PKX) | **55.1 km** (55,054 m) | **1 hour 5 mins** (3,929 s) |

## 3. Taxi fare estimate (13 yuan flag-down + 2.3 yuan/km, applied to driving distance)

| Airport | Fare calculation | Estimated fare |
|---|---|---|
| Beijing Capital (PEK) | 13 + 2.3 x 28.776 | **79.18 yuan** |
| Beijing Daxing (PKX) | 13 + 2.3 x 55.054 | **139.62 yuan** |

## 4. Distance in miles (0.621371 miles per km)

| Airport | Conversion | Miles |
|---|---|---|
| Beijing Capital (PEK) | 28.776 x 0.621371 | **17.881 miles** |
| Beijing Daxing (PKX) | 55.054 x 0.621371 | **34.209 miles** |

## 5. Verdict: which is the shorter drive

**Book Beijing Capital International Airport (PEK).**

| Metric | Capital (PEK) | Daxing (PKX) | Difference (Daxing - Capital) |
|---|---|---|---|
| Driving distance | 28.776 km | 55.054 km | **26.278 km shorter to PEK** |
| Driving time | 32.0833 min | 65.4833 min | **33.4 min shorter to PEK** |
| Estimated fare | 79.18 yuan | 139.62 yuan | **60.44 yuan cheaper to PEK** |
| Distance in miles | 17.881 mi | 34.209 mi | **16.328 mi shorter to PEK** |

**Bottom line:** Capital (PEK) is the shorter drive by **26.278 km (26.3 km)** and **33.4 minutes**, and costs roughly **60.44 yuan** less on the fare model used. Recommend the colleague books into **Beijing Capital International Airport (PEK)** if the flight options are otherwise equal.

> Note: Figures are from the mapping service at time of lookup and reflect typical driving conditions; actual drive time varies with Beijing traffic. The fare model (13 yuan flag-down + 2.3 yuan/km) is an approximation and excludes fuel surcharges, tolls, night-time surcharges, and low-speed/traffic waiting charges.

## 6. Arithmetic reference (Python output)

```
Beijing Capital International Airport (PEK)
  distance  : 28.776 km  (28.8 km)
  duration  : 32.0833 minutes  (32.1 min)
  fare      : 2.30 x 28.776 + 13 = 79.18 yuan
  miles     : 28.776 x 0.621371 = 17.881 miles

Beijing Daxing International Airport (PKX)
  distance  : 55.054 km  (55.1 km)
  duration  : 65.4833 minutes  (65.5 min)
  fare      : 2.30 x 55.054 + 13 = 139.62 yuan
  miles     : 55.054 x 0.621371 = 34.209 miles

=== Comparison (Daxing minus Capital) ===
distance difference : 26.278 km  (26.3 km)
time difference     : 33.4000 minutes  (33.4 min)
fare difference     : 60.44 yuan
miles difference    : 16.328 miles
```
