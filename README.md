# Basket Builder - Optical Dispensing Calculator

A responsive web application designed for optical professionals to generate quick quotes, calculate NHS vouchers, and apply complex retail offers.

## 🛠 Pricing & Logic Details

The application uses specific "business rules" to ensure accurate dispensing quotes:

### 1. The 2-for-1 Offer Logic
* **Frames:** The cheapest frame of the two is discounted to £0.
* **Lenses:** * If Pair 2 uses "Standard" lenses, they are discounted to £0.
    * If Pair 2 uses "Super" lenses (e.g., SuperDigital), the cost is reduced to a flat £40.
* **Reglaze Special:** If a "Reglaze 2-for-1" is selected, the first frame is £40 and the second is £30.

### 2. Intelligent Conflict Handling
To prevent incorrect dispensing, the app automatically disables certain combinations:
* **Rimless:** Automatically triggers a validation warning if thinning (1.6 or higher) is not selected.
* **Aspheric (1.5):** Disabled if high-index thinning or tints are selected, as these are incompatible in the stock range.
* **UV/Tints:** Ensures only one type of UV protection or tint is applied (e.g., you cannot select Polarised and Reactions on the same lens).

### 3. Dynamic Upcharge Scaling
Thinning prices change based on the frame and lens selected:
* **Rimless Discount:** Thinning options are reduced by £60 if a Rimless frame is selected (assuming the base price includes a higher starting point).
* **Super Lens Discount:** Thinning options are reduced by £40 if "Super" category lenses are selected.
* **Tint Bundle:** "Tint & UV" is discounted to £15 if high-index thinning is already applied.

## 🚀 Deployment
This project is built with vanilla HTML/CSS/JS and can be hosted for free on **GitHub Pages**. Simply upload the files and enable "Pages" in the repository settings.
