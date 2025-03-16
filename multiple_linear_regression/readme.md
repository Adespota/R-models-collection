# Modello di Regressione Lineare Multipla 📊

Il modello di regressione lineare multipla che hai creato ti dirà come le variabili predittive (`cyl`, `disp`, `hp`, `wt`) influenzano il consumo di carburante (`mpg`).

## 📌 Interpretazione del Modello

### 🔹 Effetto di ciascuna variabile su `mpg`
- I **coefficienti** del modello indicano quanto cambia `mpg` per un'unità di aumento di ogni variabile predittiva, mantenendo le altre costanti.
- Se il coefficiente di `wt` (peso) è **negativo**, significa che all'aumentare del peso dell'auto, il consumo (`mpg`) diminuisce (quindi l'auto consuma più carburante).

### 🔹 Significatività delle variabili
- Il **p-value** per ogni variabile indica se il suo effetto su `mpg` è **statisticamente significativo**.
- Se **p < 0.05**, la variabile è considerata rilevante nel modello.

### 🔹 Qualità del modello
- L'**R²** (coefficiente di determinazione) indica quanto il modello spiega la variabilità di `mpg`.
  - Se **R² = 0.80**, significa che l'80% della variazione di `mpg` è spiegata dalle variabili nel modello.
  - Se **R² è basso (< 0.50)**, il modello potrebbe non essere molto efficace nel prevedere `mpg`.

### 🔹 Intercetta (`Intercept`)
- Indica il valore di `mpg` quando **tutte le variabili predittive sono pari a zero**.
- Spesso non ha un significato pratico, ma è utile nel calcolo.

---

📌 **Vuoi testare il modello?**  
Esegui il seguente codice in R:
```r
# Caricare il dataset mtcars
data("mtcars")

# Creare il modello di regressione lineare multipla
modello <- lm(mpg ~ cyl + disp + hp + wt, data = mtcars)

# Riepilogo del modello
summary(modello)
