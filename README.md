# mastocalc
MastoCalc is a Multi-factor, weighted & interaction-aware breast cancer risk model with experimental biomarker layers.
⚠️ **For experimental and educational purposes only.** MastoCalc is NOT a medical device and must NOT be used for diagnosis, screening, treatment or any medical decision. Its coefficients are approximate and have not been validated. If you have a health concern, talk to a healthcare professional.

Built for the 2026 Congressional App Challenge by Viraj Srivastava, STISD Science Academy, Congressional District 34.

**Live app:** https://mastocalc.netlify.app
**Demo video:** [your YouTube link]

## What it does

MastoCalc estimates relative and absolute breast cancer risk from many factors at once. Instead of a simple points tally, it uses a weighted model where each factor has its own influence and factors interact with each other.

- **13 input sections:** demographics (with ancestry and subgroup detail), reproductive and hormonal history, body size and metabolism, lifestyle, prior breast disease, mammographic density, radiation exposure, family history (relative by relative), germline gene variants, and polygenic risk.
- **3 experimental research layers:** circulating proteomics, cfDNA and epigenetics, and metabolomics. These are labeled research-only, capped, and kept separate from established factors so they never silently change the core result.
- **Results:** 5-year, 10-year and to-age-90 absolute risk compared with an average person, an uncertainty range, a risk gauge, a breakdown by factor, and data-quality checks.
- **Your Factors tab:** an interactive chart showing how each factor shifts risk, with your own values marked.
- **Learn tab:** plain-language information on breast cancer, screening guidelines, prevention and warning signs.
- **Built-in explanations:** a ? button beside every field explains it in simple terms.
- **Extras:** autosave, import and export of your data, a printable report, and light and dark mode.

## How to run it

It is a single file with no installation or server needed. Open `index.html` in any modern browser, or visit the live link above. All calculations run locally in your browser. Nothing is uploaded.

## How the model works

- Each factor adds a weighted value to a total log relative risk, so effects multiply.
- Weights follow rough importance: germline variants and strong radiation exposure count most, then family history, density and polygenic risk, then hormonal factors, body size and alcohol, then lifestyle, with race and ancestry weighted least.
- Interactions include BMI and menopausal status (the effect flips direction), HRT and BMI, density and BMI, and age-dependent gene and family-history effects.
- Overlapping factors are compressed so they do not double-count, and the total relative risk saturates at very high levels.
- Absolute risk applies the relative risk to age-specific population incidence and accounts for the chance of dying of other causes.

**Limitations:** the weights are hand-chosen approximations based on published trends, not fitted to patient data. The model is not validated against clinical datasets and is not equivalent to clinical tools such as the Gail model, IBIS or CanRisk.

## Built with

HTML, CSS and JavaScript (no frameworks or libraries). One self-contained file.

## AI assistance disclosure

I designed the concept, chose the factors and features, and directed the project. I used **Claude (by Anthropic)** as an AI coding assistant to help write and refine parts of the code. 

## What I learned

Building MastoCalc taught me many different things such as: complex multi-factor risk modeling, non-linear weighting, risk saturation caps, and overall website building and mechanics. Working on this project also strengthened my ability to truly understand more about what is happening in the world around us, and it gave me a new perspective on disease and how it impacts society. This was truly a unique experience and I am very glad I was able to participate in the Congressional App Challenge, and there is no doubt in my mind that this challenge helped me develop in more ways than one.
