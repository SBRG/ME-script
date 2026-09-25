# ME-script
Custom code for constraining and solving COBRAme models

## Notebooks

- `run_simulations.ipynb`: constrains a COBRAme model with measured growth and exchange rates, applies gene knockouts, and adds proteome sector constraints from RNA-seq. Each sector's transcript mass fraction, relative to ribosomal proteins, sets a lower bound on the protein the model allocates to that sector.
- `run_simulations_w_cap.ipynb`: the same, plus an oxygen uptake band (mean ± SD) and `set_expression_cap`, an upper bound on a sector's protein allocation at a multiple of its transcript-implied ratio. The floor only says "at least this much", so the cap is what stops the model from over-allocating a sector. The example caps the D-lactate dehydrogenases (ldhA, dld).

Both need `cobrame`, `ecolime` and `qminospy`.
